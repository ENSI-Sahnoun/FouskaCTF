# Forensics Challenges 🔍

Forensics in CTF involves analyzing files, memory dumps, network traffic, and other digital artifacts to find hidden information or flags.

## Common Techniques

### File Analysis
- **File type identification**: Use `file` command to determine actual file type
- **Metadata extraction**: Use `exiftool` to extract metadata from files
- **Strings search**: Use `strings` to find human-readable text in binary files
- **Hex editing**: Analyze and modify files at the byte level

### Steganography
- **Image steganography**: Hidden data in images (LSB, EXIF data, etc.)
- **Audio steganography**: Hidden data in audio files
- **Tools**: steghide, stegsolve, zsteg, binwalk

### Network Analysis
- **Packet capture analysis**: Use Wireshark to analyze .pcap files
- **Protocol analysis**: Understanding HTTP, TCP, UDP, DNS traffic
- **Data extraction**: Exporting objects and files from packet captures

### Memory Forensics
- **Memory dumps**: Analyzing RAM dumps using Volatility
- **Process analysis**: Identifying running processes and artifacts
- **Registry analysis**: Examining Windows registry data

## Challenges

*Challenges will be added here as they are solved*

## Useful Tools

- `file` - Determine file type
- `exiftool` - Extract metadata
- `strings` - Extract readable strings
- `binwalk` - Firmware analysis and extraction
- `foremost` - File carving
- `steghide` - Steganography tool
- `stegsolve` - Image analysis
- `wireshark` - Network protocol analyzer
- `volatility` - Memory forensics framework

## Tips

1. Always start with `file` to verify the file type
2. Look for hidden data in image metadata
3. Check for embedded files with `binwalk`
4. Search for patterns with `strings` and `grep`
5. Don't assume the file extension is correct
