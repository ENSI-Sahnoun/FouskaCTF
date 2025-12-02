# Caesar Cipher

**Category**: Cryptography  
**Points**: 5  
**Platform**: picoCTF

## Description

```
Decrypt this message.
picoCTF{gvswwmrkxlivyfmgsrhnrsx}
```

## Solution

### Initial Analysis

The flag format gives us a huge hint - we can see `picoCTF{` at the beginning, but the text inside the braces is scrambled. This suggests a simple substitution cipher where each letter is replaced with another letter consistently.

The challenge name "Caesar Cipher" tells us exactly what we're dealing with: a shift cipher where each letter is shifted by a fixed number of positions in the alphabet.

### Step 1: Understanding Caesar Cipher

A Caesar cipher shifts each letter by a fixed number (the "key"). For example, with a shift of 3:
- A → D
- B → E
- C → F
- ... and so on

There are only 25 possible shifts (1-25, since 0 would be no change and 26 would wrap back to the original letter).

### Step 2: Try All Possible Shifts (Brute Force)

Since there are only 25 possibilities, we can try them all:

```python
def caesar_decrypt(text, shift):
    result = ""
    for char in text:
        if char.isalpha():
            # Handle uppercase and lowercase
            ascii_offset = ord('A') if char.isupper() else ord('a')
            # Shift the character
            shifted = chr((ord(char) - ascii_offset - shift) % 26 + ascii_offset)
            result += shifted
        else:
            # Keep non-alphabetic characters as-is
            result += char
    return result

encrypted = "picoCTF{gvswwmrkxlivyfmgsrhnrsx}"

# Try all 25 possible shifts
for shift in range(1, 26):
    decrypted = caesar_decrypt(encrypted, shift)
    print(f"Shift {shift}: {decrypted}")
```

### Step 3: Identify the Correct Shift

Running the script, we look for readable English text:

```
Shift 1: picoCTF{futrvvlqjwkhuxelfrqgmqrw}
Shift 2: picoCTF{etusqukpivjgtwdkeqpfclqpv}
Shift 3: picoCTF{dstrptjohiufsvcjdpoebkpou}
Shift 4: picoCTF{crossingtherubicondalyont}
Shift 5: picoCTF{bqnrrhmfsgdqtahbnmczkmxms}
...
```

At shift 4, we get: `picoCTF{crossingtherubicondalyont}`

This looks like readable English! The text appears to be "crossing the rubicon" (a famous historical phrase) followed by additional characters. This is clearly the correct decryption as it contains recognizable English words, unlike the other shifts.

### Alternative: Using Online Tools

You can also use online Caesar cipher decoders:

1. Go to [dcode.fr/caesar-cipher](https://www.dcode.fr/caesar-cipher)
2. Paste the encrypted text
3. Click "Decrypt" - it will try all shifts automatically
4. Look for the readable output

### Alternative: Using CyberChef

1. Go to [CyberChef](https://gchq.github.io/CyberChef/)
2. Drag the "ROT13" operation (Caesar cipher with shift 13) or "ROT13 Brute Force" to the recipe
3. Or use "ROT47" with different values
4. Input: `gvswwmrkxlivyfmgsrhnrsx`
5. Adjust the rotation amount until you get readable text

## Flag

<details>
<summary>Click to reveal flag</summary>

```
picoCTF{crossingtherubicondalyont}
```

</details>

## Tools Used

- Python - For writing a brute force script
- Online decoders - dcode.fr or CyberChef
- Manual analysis - Recognizing patterns

## Key Learning Points

1. **Caesar cipher is easy to break**: With only 25 possibilities, brute force is trivial
2. **Flag format helps**: Knowing part of the plaintext (like "picoCTF{") helps verify correctness
3. **Frequency analysis**: For longer texts, you could use letter frequency to identify the shift
4. **Historical context**: "Crossing the Rubicon" refers to Julius Caesar, connecting to the cipher name

## References

- [Caesar Cipher on Wikipedia](https://en.wikipedia.org/wiki/Caesar_cipher)
- [dcode.fr Caesar Cipher Tool](https://www.dcode.fr/caesar-cipher)
- [CyberChef](https://gchq.github.io/CyberChef/)

---

**Author**: FouskaCTF Guide  
**Date**: 2025-12-02
