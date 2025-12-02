# Obedient Cat

**Category**: General  
**Points**: 5  
**Platform**: picoCTF

## Description

```
This file has a flag in plain sight (aka "in-the-clear").
Download flag
```

## Files Provided

- `flag` - A text file

## Solution

### Initial Analysis

This is one of the simplest CTF challenges, often used as a "sanity check" to ensure participants can submit flags correctly. The description tells us the flag is in plain sight, meaning it's not hidden or encoded.

The challenge name "Obedient Cat" is a hint - in Unix/Linux, the `cat` command is used to display file contents. An "obedient cat" would simply show you what's in the file!

### Step 1: Download the File

First, download the provided file named `flag`.

### Step 2: Display the Contents

Use the `cat` command to display the file contents:

```bash
$ cat flag
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}
```

That's it! The flag is right there in plain text.

### Alternative Methods

Since the file is plain text, there are many ways to view it:

#### Using `less` or `more`
```bash
$ less flag
```

#### Using `head` or `tail`
```bash
$ head flag
```

#### Opening in a text editor
```bash
$ nano flag
# or
$ vim flag
# or
$ gedit flag
```

#### On Windows
```cmd
type flag
```

#### Using Python
```python
with open('flag', 'r') as f:
    print(f.read())
```

### Step 3: Verify File Type (Good Practice)

Even though this challenge is straightforward, it's good practice to verify the file type:

```bash
$ file flag
flag: ASCII text
```

This confirms it's a plain text file, so `cat` is the right tool.

## Flag

<details>
<summary>Click to reveal flag</summary>

```
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}
```

</details>

## Tools Used

- `cat` - Display file contents
- `file` - Identify file type (optional)
- Text editor - Any text editor works

## Key Learning Points

1. **Start simple**: Not every challenge requires complex tools or techniques
2. **Read the description**: The challenge tells you the flag is "in plain sight"
3. **Know your tools**: `cat` is one of the most basic and essential Unix commands
4. **Sanity checks matter**: These easy challenges help verify your setup and submission process
5. **File type verification**: Even for simple challenges, using `file` is good practice

## Why This Challenge Exists

"Sanity check" challenges like this serve several purposes:

1. **Verify setup**: Ensure you can download files and submit flags
2. **Build confidence**: Everyone can get points and feel accomplished
3. **Learn the platform**: Understand how flag submission works
4. **Warm up**: Get into the CTF mindset before tackling harder challenges

## Command Reference

### The `cat` command

`cat` stands for "concatenate" and is used to:
- Display file contents: `cat filename`
- Concatenate files: `cat file1 file2`
- Create files: `cat > newfile`
- Number lines: `cat -n filename`

### Examples
```bash
# Display a file
cat flag

# Display multiple files
cat file1.txt file2.txt

# Display with line numbers
cat -n flag

# Display non-printing characters
cat -v flag
```

## References

- [cat command documentation](https://man7.org/linux/man-pages/man1/cat.1.html)
- [Linux Command Line Basics](https://linuxcommand.org/)

---

**Author**: FouskaCTF Guide  
**Date**: 2025-12-02
