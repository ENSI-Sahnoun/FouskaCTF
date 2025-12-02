# Information

**Category**: Forensics  
**Points**: 10  
**Platform**: picoCTF

## Description

```
Files can always be changed in a secret way. Can you find the flag?
cat.jpg
```

## Files Provided

- `cat.jpg` - An image file of a cat

## Solution

### Initial Analysis

When we encounter a forensics challenge involving an image file, the first thing to check is the file metadata. Image files often contain EXIF (Exchangeable Image File Format) data that can store additional information like camera settings, GPS coordinates, and sometimes hidden messages.

### Step 1: Verify the File Type

Always start by confirming the file type:

```bash
$ file cat.jpg
cat.jpg: JPEG image data, JFIF standard 1.01
```

Good! It's actually a JPEG file as the extension suggests.

### Step 2: Extract Metadata with exiftool

`exiftool` is the go-to tool for extracting metadata from image files:

```bash
$ exiftool cat.jpg
ExifTool Version Number         : 12.40
File Name                       : cat.jpg
Directory                       : .
File Size                       : 858 KiB
File Modification Date/Time     : 2019:03:09 22:24:32-05:00
File Access Date/Time           : 2019:03:09 22:24:32-05:00
File Inode Change Date/Time     : 2019:03:09 22:24:32-05:00
File Permissions                : rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Progressive DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
```

### Step 3: Identify the Suspicious Data

Looking at the output, most fields contain normal image metadata. However, the `License` field looks suspicious:

```
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
```

This doesn't look like a normal license string. The format with random-looking characters and the fact that it ends with `}` suggests this might be encoded data - possibly Base64.

### Step 4: Decode the Base64 String

Base64 is a common encoding scheme used in CTFs. Let's decode it:

```bash
$ echo "cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9" | base64 -d
picoCTF{the_m3tadata_1s_modified}
```

Perfect! The decoded string is our flag.

## Flag

<details>
<summary>Click to reveal flag</summary>

```
picoCTF{the_m3tadata_1s_modified}
```

</details>

## Tools Used

- `file` - Verify file type
- `exiftool` - Extract image metadata
- `base64` - Decode Base64 encoded data

## Key Learning Points

1. **Always check metadata**: Image files often hide information in EXIF data
2. **Recognize Base64**: Base64 encoded strings typically contain alphanumeric characters, plus (+), slash (/), and equals (=) for padding
3. **Verify file types**: Don't trust file extensions - always use the `file` command
4. **exiftool is essential**: For any image-based forensics challenge, exiftool should be one of your first tools

## Alternative Solutions

You could also use other tools to extract metadata:

### Using `strings` command
```bash
$ strings cat.jpg | grep pico
```
This might reveal the Base64 string, which you'd still need to decode.

### Using online tools
- Online EXIF viewers
- CyberChef with "From Base64" recipe

## References

- [ExifTool Documentation](https://exiftool.org/)
- [Base64 Encoding on Wikipedia](https://en.wikipedia.org/wiki/Base64)
- [EXIF Standard](https://en.wikipedia.org/wiki/Exif)

---

**Author**: FouskaCTF Guide  
**Date**: 2025-12-02
