# Contributing to Email Newsletter using Thunderbird

Thank you for your interest in contributing! This document provides guidelines for contributing to this project.

## Ways to Contribute

### 1. Report Bugs
- Check if the issue already exists
- Provide detailed description
- Include steps to reproduce
- Specify your environment (OS, Thunderbird version, etc.)

### 2. Suggest Enhancements
- Describe the feature clearly
- Explain the use case
- Consider backward compatibility

### 3. Submit Templates
New email templates are always welcome!

**Template Requirements:**
- Mobile-responsive design
- Compatible with major email clients
- Uses inline CSS
- Includes clear documentation of merge fields
- Professional design
- Includes sample CSV file

**Template Submission:**
1. Create HTML template file
2. Create matching CSV sample file
3. Document all merge fields used
4. Test in multiple email clients
5. Submit via pull request

### 4. Improve Documentation
- Fix typos and errors
- Add clarifications
- Include examples
- Update screenshots
- Translate to other languages

### 5. Share Best Practices
- Email marketing strategies
- Design tips
- Deliverability improvements
- Case studies

## Development Guidelines

### Template Development

**HTML Standards:**
- Valid HTML5
- Inline CSS (no external stylesheets)
- Table-based layouts for compatibility
- Alt text for all images
- Responsive design considerations

**Testing Requirements:**
- Test in Gmail (web and mobile)
- Test in Outlook (desktop and web)
- Test in Apple Mail
- Test in Yahoo Mail
- Validate HTML

**Merge Field Naming:**
- Use PascalCase: `{{FirstName}}`, not `{{firstname}}`
- Be descriptive: `{{EventDate}}`, not `{{Date}}`
- Match common CSV headers

### Documentation Standards

**Writing Style:**
- Clear and concise
- Step-by-step when applicable
- Include examples
- Use proper markdown formatting

**Structure:**
- Use headers for sections
- Include table of contents for long documents
- Cross-reference related documents
- Keep consistent formatting

## Pull Request Process

1. **Fork the Repository**
   ```bash
   git clone https://github.com/mool3s/Email-Newsletter-using-Thunderbird.git
   ```

2. **Create a Branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make Your Changes**
   - Follow the style guidelines
   - Test thoroughly
   - Update documentation

4. **Commit Your Changes**
   ```bash
   git add .
   git commit -m "Add: Brief description of changes"
   ```

5. **Push to GitHub**
   ```bash
   git push origin feature/your-feature-name
   ```

6. **Create Pull Request**
   - Provide clear description
   - Reference any related issues
   - Include screenshots if applicable

## Commit Message Guidelines

Use clear, descriptive commit messages:

- `Add: New promotional template`
- `Fix: Variable replacement in event template`
- `Update: Setup guide with new screenshots`
- `Improve: Mobile responsiveness in basic template`
- `Docs: Add troubleshooting section to FAQ`

## Code of Conduct

### Our Standards

**Positive Behavior:**
- Be respectful and inclusive
- Welcome newcomers
- Accept constructive criticism
- Focus on what's best for the community
- Show empathy

**Unacceptable Behavior:**
- Harassment or discrimination
- Trolling or insulting comments
- Personal or political attacks
- Publishing others' private information
- Unprofessional conduct

## Questions?

If you have questions about contributing:
- Open an issue for discussion
- Check existing documentation
- Reach out to maintainers

## Recognition

Contributors will be:
- Listed in project documentation
- Credited in release notes
- Acknowledged in README (for significant contributions)

## Testing Checklist

Before submitting templates:

- [ ] HTML is valid
- [ ] CSS is inline
- [ ] Tested in Gmail
- [ ] Tested in Outlook
- [ ] Tested in Apple Mail
- [ ] Mobile responsive
- [ ] All links work
- [ ] Images load correctly
- [ ] Alt text included
- [ ] Merge fields documented
- [ ] Sample CSV provided
- [ ] README updated

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

## Thank You!

Your contributions help make this project better for everyone. We appreciate your time and effort!
