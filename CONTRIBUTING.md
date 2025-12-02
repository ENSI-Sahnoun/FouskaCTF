# Contributing to FouskaCTF 🤝

Thank you for your interest in contributing to FouskaCTF! This guide will help you add your own CTF writeups and improve the repository.

## How to Contribute

### Adding a Challenge Writeup

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/FouskaCTF.git
   cd FouskaCTF
   ```

3. **Create a new branch** for your writeup:
   ```bash
   git checkout -b add-challenge-name
   ```

4. **Choose the correct category** for your challenge:
   - Forensics
   - Cryptography
   - Web-Exploitation
   - Binary-Exploitation
   - Reverse-Engineering
   - General

5. **Use the template**: Copy `CHALLENGE_TEMPLATE.md` as a starting point:
   ```bash
   cp CHALLENGE_TEMPLATE.md Forensics/your-challenge-name.md
   ```

6. **Write your writeup** following the template structure:
   - Be detailed but concise
   - Include all necessary commands and code
   - Explain your thought process
   - Add screenshots if helpful
   - Hide the flag in a spoiler/details tag

7. **Update the category README**: Add a link to your challenge in the appropriate category's README.md

8. **Commit your changes**:
   ```bash
   git add .
   git commit -m "Add writeup for [Challenge Name]"
   ```

9. **Push to your fork**:
   ```bash
   git push origin add-challenge-name
   ```

10. **Create a Pull Request** on GitHub

## Writeup Guidelines

### Do's ✅

- **Be thorough**: Explain each step clearly
- **Show your work**: Include commands, code, and output
- **Explain why**: Don't just show what to do, explain why
- **Credit sources**: If you used external resources, link to them
- **Test your writeup**: Make sure someone else could follow it
- **Use proper markdown**: Format your writeup nicely
- **Include learning points**: What should readers take away?

### Don'ts ❌

- **Don't plagiarize**: Write in your own words
- **Don't skip steps**: Assume the reader is a beginner
- **Don't share during active CTFs**: Wait until the competition ends
- **Don't include personal information**: Remove tokens, keys, etc.
- **Don't be discouraging**: Keep the tone helpful and positive

## Markdown Guidelines

### Code Blocks

Use triple backticks with language specification:

````markdown
```bash
$ ls -la
```

```python
def solve():
    return flag
```
````

### File Structure

```
FouskaCTF/
├── README.md
├── GETTING_STARTED.md
├── CHALLENGE_TEMPLATE.md
├── CONTRIBUTING.md
├── Forensics/
│   ├── README.md
│   └── challenge-name.md
├── Cryptography/
│   ├── README.md
│   └── challenge-name.md
└── ...
```

### Naming Conventions

- **Files**: Use lowercase with hyphens: `challenge-name.md`
- **Titles**: Use the exact challenge name from the CTF
- **Images**: Store in an `images/` folder within the category

## Quality Standards

### Minimum Requirements

Your writeup should include:
- [ ] Challenge description
- [ ] Step-by-step solution
- [ ] Commands/code used
- [ ] Flag (in spoiler tags)
- [ ] Tools used
- [ ] Learning points

### Preferred Additions

- Screenshots or diagrams
- Alternative solutions
- Common pitfalls to avoid
- Related challenges or concepts
- References and resources

## Adding Examples and Resources

### Updating Getting Started Guide

If you have tips for beginners:
1. Edit `GETTING_STARTED.md`
2. Add your tips in the appropriate section
3. Keep the tone beginner-friendly

### Adding Tools or Resources

To add a new tool or resource:
1. Edit the relevant category README
2. Add the tool with a brief description
3. Maintain alphabetical ordering

## Code of Conduct

### Be Respectful

- Welcome newcomers
- Provide constructive feedback
- Be patient with questions
- Respect different skill levels

### Be Ethical

- Don't share solutions during active competitions
- Respect CTF rules and guidelines
- Give credit where credit is due
- Don't use this for malicious purposes

### Be Helpful

- Answer questions in issues
- Review pull requests
- Share knowledge generously
- Help improve existing writeups

## Reporting Issues

If you find any issues:

1. **Check existing issues** first
2. **Create a new issue** with:
   - Clear title
   - Detailed description
   - Steps to reproduce (if applicable)
   - Suggested fix (if you have one)

### Issue Types

- **Bug**: Something is broken or incorrect
- **Enhancement**: Suggestion for improvement
- **Question**: Need help or clarification
- **Documentation**: Needs better documentation

## Review Process

### What We Look For

1. **Accuracy**: Is the solution correct?
2. **Clarity**: Is it easy to follow?
3. **Completeness**: Does it cover all important points?
4. **Style**: Does it follow the guidelines?

### Timeline

- Initial review: Within 1 week
- Feedback provided: Within 2 weeks
- Merge: After all feedback addressed

## Getting Help

Need help with your contribution?

- **Open an issue**: Ask questions in GitHub issues
- **Check examples**: Look at existing writeups
- **Read the template**: Follow `CHALLENGE_TEMPLATE.md`

## Recognition

Contributors will be:
- Listed in the challenge writeup (Author field)
- Mentioned in pull request acknowledgments
- Part of the FouskaCTF community

## Thank You!

Every contribution makes this resource better for the entire CTF community. Whether you're adding one writeup or dozens, your effort is appreciated!

Happy contributing! 🎉

---

**Questions?** Open an issue or reach out to the maintainers.
