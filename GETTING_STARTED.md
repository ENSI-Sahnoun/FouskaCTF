# Getting Started with CTFs 🚀

Welcome to the world of Capture The Flag competitions! This guide will help you get started on your CTF journey.

## What is a CTF?

A Capture The Flag (CTF) competition is a cybersecurity competition where participants solve security-related challenges to find "flags" - strings that prove you've successfully completed the challenge. Flags typically follow a format like `picoCTF{this_is_a_flag}` or `flag{example_flag_here}`.

## Types of CTF Competitions

### 1. Jeopardy-Style CTFs
- Challenges organized by category
- Each challenge has a point value
- Solve challenges independently
- Most common format (including picoCTF)

### 2. Attack-Defense CTFs
- Teams defend their own servers while attacking others
- Real-time competition
- More advanced format

### 3. King of the Hill
- Compete for control of vulnerable systems
- Maintain access while blocking others

## Challenge Categories

CTF challenges typically fall into these categories:

- **Forensics**: Analyzing files, network traffic, memory dumps
- **Cryptography**: Breaking encryption and ciphers
- **Web Exploitation**: Finding vulnerabilities in web applications
- **Binary Exploitation**: Exploiting compiled programs
- **Reverse Engineering**: Understanding how programs work
- **General/Misc**: Everything else (OSINT, puzzles, trivia)

## Setting Up Your Environment

### Essential Software

#### 1. Operating System
- **Linux** (Ubuntu, Kali Linux, or ParrotOS recommended)
- Can use Windows with WSL2 or a virtual machine
- macOS works but may need additional setup

#### 2. Programming Languages
```bash
# Python 3 (essential!)
sudo apt install python3 python3-pip

# Install common Python libraries
pip3 install pwntools requests pycryptodome
```

#### 3. Basic Tools
```bash
# Update package list
sudo apt update

# Essential command-line tools
sudo apt install git curl wget netcat
sudo apt install binutils gcc gdb
sudo apt install file binwalk exiftool
sudo apt install wireshark nmap
```

### Recommended Tools by Category

#### Forensics
```bash
sudo apt install binwalk foremost steghide
sudo apt install exiftool wireshark
pip3 install stegcracker
```

#### Cryptography
- CyberChef (web-based, no install)
- Python cryptography libraries
```bash
pip3 install pycryptodome cryptography
```

#### Web Exploitation
- Burp Suite Community Edition
- Browser Developer Tools (built-in)
```bash
sudo apt install curl sqlmap
```

#### Binary Exploitation & Reverse Engineering
```bash
# GDB with enhancements
sudo apt install gdb
pip3 install pwntools

# Ghidra (download from NSA's GitHub)
# Radare2
sudo apt install radare2
```

## Your First Challenge

### Step 1: Choose a Platform

**For Beginners:**
- **picoCTF**: Perfect for learning, permanent practice challenges
- **OverTheWire**: Wargames for learning specific skills
- **TryHackMe**: Guided learning paths

**For Intermediate:**
- **HackTheBox**: Active machines and challenges
- **CTFtime**: Find live competitions
- **CryptoHack**: Specialized in cryptography

### Step 2: Start Simple

Begin with challenges marked as "Easy" or worth fewer points:

1. **General/Sanity Checks**: Usually very simple, good confidence boosters
2. **Forensics - Basic**: File analysis, strings, metadata
3. **Cryptography - Classical**: Caesar cipher, Base64
4. **Web - Basic**: View source, inspect elements

### Step 3: Develop a Methodology

For every challenge:

1. **Read carefully**: Understand what you're being asked
2. **Gather information**: What files/URLs are provided?
3. **Identify the category**: What type of challenge is this?
4. **Try basic techniques first**: 
   - `file` command for file type
   - `strings` for readable text
   - `exiftool` for metadata
   - View page source for web challenges
5. **Research**: Google unfamiliar concepts
6. **Document your process**: Take notes as you go

## Common Beginner Mistakes

### ❌ Don't Do This:
1. Skipping the challenge description
2. Assuming file extensions are correct
3. Giving up too quickly
4. Not documenting what you tried
5. Working alone when stuck

### ✅ Do This Instead:
1. Read descriptions multiple times
2. Always verify file types with `file` command
3. Take breaks and come back with fresh eyes
4. Keep notes of attempted solutions
5. Ask for hints or collaborate (when allowed)

## Essential Skills to Learn

### 1. Command Line Basics
```bash
# Navigation
cd, ls, pwd

# File operations
cat, less, head, tail, grep

# File inspection
file, strings, xxd, hexdump

# Text processing
grep, sed, awk, cut, sort
```

### 2. Basic Python
```python
# Reading files
with open('file.txt', 'r') as f:
    content = f.read()

# Working with bytes
data = bytes.fromhex('48656c6c6f')
print(data.decode())

# HTTP requests
import requests
response = requests.get('http://example.com')
```

### 3. Using Google Effectively
- Search for error messages in quotes
- Use site:stackoverflow.com for specific sites
- Add "CTF" or "writeup" to find similar solutions
- Search for "how to decode [encoding_type]"

## Practice Strategy

### Week 1-2: Foundations
- Solve 5-10 easy challenges across different categories
- Focus on understanding basic tools
- Read writeups of challenges you can't solve

### Week 3-4: Building Skills
- Attempt medium difficulty challenges
- Deep dive into 1-2 categories you enjoy
- Join a CTF community or team

### Month 2+: Competition Ready
- Participate in live CTFs (check CTFtime.org)
- Challenge yourself with harder problems
- Write your own writeups to reinforce learning

## Resources

### Learning Platforms
- [picoCTF](https://picoctf.org/) - Beginner-friendly
- [OverTheWire](https://overthewire.org/) - Linux basics
- [CryptoHack](https://cryptohack.org/) - Learn cryptography
- [TryHackMe](https://tryhackme.com/) - Guided rooms

### Practice Platforms
- [HackTheBox](https://www.hackthebox.eu/)
- [CTFtime](https://ctftime.org/) - Find live CTFs
- [Root-Me](https://www.root-me.org/)

### Learning Resources
- [CTF101](https://ctf101.org/) - Introduction to CTF concepts
- [LiveOverflow YouTube](https://www.youtube.com/c/LiveOverflow) - Binary exploitation
- [IppSec YouTube](https://www.youtube.com/c/ippsec) - HackTheBox walkthroughs
- [Trail of Bits CTF Guide](https://trailofbits.github.io/ctf/)

### Communities
- Reddit: r/securityCTF, r/netsec
- Discord: Join CTF team servers
- Twitter: Follow #CTF hashtag

## Tips for Success

1. **Start Early**: In timed CTFs, start as soon as possible
2. **Go for Quick Wins**: Do easy challenges first for points
3. **Read Hints Carefully**: They often contain crucial information
4. **Take Breaks**: Fresh eyes solve problems faster
5. **Learn from Failures**: Read writeups after the CTF ends
6. **Build a Toolkit**: Create scripts for common tasks
7. **Network**: Join a team or community
8. **Stay Curious**: Every challenge teaches something new

## Next Steps

1. ✅ Read this guide
2. ✅ Set up your basic environment
3. ✅ Create an account on picoCTF or another platform
4. ✅ Solve your first challenge
5. ✅ Document your solution
6. ✅ Share your success!

---

**Remember**: Everyone was a beginner once. The key is persistence and continuous learning. Don't be discouraged by challenges you can't solve immediately - they're opportunities to learn something new!

Good luck, and happy hacking! 🎉
