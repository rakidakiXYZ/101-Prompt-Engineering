# Markdown Tutorial - Complete Guide

This file demonstrates all major Markdown features for GitHub repositories.

## Table of Contents
- [Headers](#headers)
- [Text Formatting](#text-formatting)
- [Lists](#lists)
- [Links](#links)
- [Images](#images)
- [Code](#code)
- [Tables](#tables)
- [Blockquotes](#blockquotes)
- [Horizontal Rules](#horizontal-rules)
- [Task Lists](#task-lists)
- [GitHub Specific Features](#github-specific-features)

---

## Headers

```markdown
# H1 - Largest Header
## H2 - Second Level
### H3 - Third Level
#### H4 - Fourth Level
##### H5 - Fifth Level
###### H6 - Smallest Header
```

# H1 - Largest Header
## H2 - Second Level
### H3 - Third Level
#### H4 - Fourth Level
##### H5 - Fifth Level
###### H6 - Smallest Header

---

## Text Formatting

```markdown
**Bold text** or __Bold text__
*Italic text* or _Italic text_
***Bold and italic*** or ___Bold and italic___
~~Strikethrough text~~
```

**Bold text** or __Bold text__  
*Italic text* or _Italic text_  
***Bold and italic*** or ___Bold and italic___  
~~Strikethrough text~~

---

## Lists

### Unordered Lists
```markdown
- First item
- Second item
  - Nested item
  - Another nested item
    - Deep nested item
* Can also use asterisks
+ Or plus signs
```

- First item
- Second item
  - Nested item
  - Another nested item
    - Deep nested item
* Can also use asterisks
+ Or plus signs

### Ordered Lists
```markdown
1. First item
2. Second item
   1. Nested item
   2. Another nested item
3. Third item
```

1. First item
2. Second item
   1. Nested item
   2. Another nested item
3. Third item

---

## Links

```markdown
[Inline link to Google](https://www.google.com)
[Link with title](https://www.google.com "Google's Homepage")
[Reference-style link][reference]
[Relative link to README](../README.md)
https://www.automatic-link.com

[reference]: https://www.github.com "GitHub"
```

[Inline link to Google](https://www.google.com)  
[Link with title](https://www.google.com "Google's Homepage")  
[Reference-style link][reference]  
[Relative link to README](../README.md)  
https://www.automatic-link.com

[reference]: https://www.github.com "GitHub"

---

## Images

```markdown
![Alt text for image](https://via.placeholder.com/150 "Optional title")
![Local image](./images/screenshot.png)

<!-- Image with link -->
[![Clickable image](https://via.placeholder.com/150)](https://github.com)
```

![Alt text for image](https://via.placeholder.com/150 "Optional title")

---

## Code

### Inline Code
```markdown
Use `git status` to check your changes.
```

Use `git status` to check your changes.

### Code Blocks
````markdown
```python
def hello_world():
    print("Hello, World!")
    return True
```

```javascript
const greeting = (name) => {
    console.log(`Hello, ${name}!`);
};
```

```bash
# Terminal commands
git add .
git commit -m "Update README"
git push origin main
```
````

```python
def hello_world():
    print("Hello, World!")
    return True
```

```javascript
const greeting = (name) => {
    console.log(`Hello, ${name}!`);
};
```

```bash
# Terminal commands
git add .
git commit -m "Update README"
git push origin main
```

---

## Tables

```markdown
| Header 1 | Header 2 | Header 3 |
|----------|:--------:|---------:|
| Left     | Center   | Right    |
| Data 1   | Data 2   | Data 3   |
| Row 3    | Row 3    | Row 3    |
```

| Header 1 | Header 2 | Header 3 |
|----------|:--------:|---------:|
| Left     | Center   | Right    |
| Data 1   | Data 2   | Data 3   |
| Row 3    | Row 3    | Row 3    |

---

## Blockquotes

```markdown
> This is a blockquote
> 
> > Nested blockquote
> > > Even more nested
> 
> Back to first level
```

> This is a blockquote
> 
> > Nested blockquote
> > > Even more nested
> 
> Back to first level

---

## Horizontal Rules

```markdown
Three or more hyphens
---
Three or more asterisks
***
Three or more underscores
___
```

Three or more hyphens
---
Three or more asterisks
***
Three or more underscores
___

---

## Task Lists

```markdown
- [x] Completed task
- [ ] Incomplete task
- [ ] Another task to do
  - [x] Completed subtask
  - [ ] Incomplete subtask
```

- [x] Completed task
- [ ] Incomplete task
- [ ] Another task to do
  - [x] Completed subtask
  - [ ] Incomplete subtask

---

## GitHub Specific Features

### Mentioning Users and Teams
```markdown
@username will notify the user
@organization/team mentions a team
```

### Issue and PR References
```markdown
#123 - Links to issue or PR #123
GH-123 - Also links to issue #123
username/repo#123 - Links to issue in another repo
```

### Emoji
```markdown
:smile: :heart: :thumbsup: :rocket:
```
:smile: :heart: :thumbsup: :rocket:

### Collapsible Sections
```markdown
<details>
<summary>Click to expand!</summary>

This content is hidden by default!

- You can put any markdown here
- Including lists
- And code blocks

```python
print("Hidden code!")
```

</details>
```

<details>
<summary>Click to expand!</summary>

This content is hidden by default!

- You can put any markdown here
- Including lists
- And code blocks

```python
print("Hidden code!")
```

</details>

### Alerts (GitHub Flavored)
```markdown
> [!NOTE]
> Useful information that users should know.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know.

> [!WARNING]
> Urgent info that needs immediate attention.

> [!CAUTION]
> Advises about risks or negative outcomes.
```

> [!NOTE]
> Useful information that users should know.

> [!TIP]
> Helpful advice for doing things better or more easily.

---

## Advanced Tips

1. **Line Breaks**: End a line with two spaces  
   to create a line break without paragraph spacing.

2. **Escaping**: Use backslash \ to escape special characters: \*not italic\*

3. **HTML**: You can use HTML tags when Markdown isn't enough:
   <kbd>Ctrl</kbd> + <kbd>C</kbd> for copy

4. **Comments**: <!-- This is a comment and won't be displayed -->

5. **Math** (GitHub supports LaTeX):
   ```markdown
   $x = {-b \pm \sqrt{b^2-4ac} \over 2a}$
   
   $$
   \sum_{i=1}^{n} x_i = x_1 + x_2 + \ldots + x_n
   $$
   ```

---

## Best Practices for GitHub READMEs

1. **Start with a clear title and description**
2. **Include badges** (build status, version, license)
3. **Add a table of contents** for long documents
4. **Include installation instructions**
5. **Provide usage examples**
6. **List prerequisites and dependencies**
7. **Add contribution guidelines**
8. **Include license information**
9. **Add contact information**
10. **Use meaningful commit messages** when updating

---

## Example README Structure

```markdown
# Project Name

Brief description of what this project does.

## Features

- Feature 1
- Feature 2
- Feature 3

## Installation

```bash
git clone https://github.com/username/project.git
cd project
npm install
```

## Usage

```javascript
const project = require('project');
project.doSomething();
```

## Contributing

Please read CONTRIBUTING.md for details.

## License

This project is licensed under the MIT License.
```

---

Created with ❤️ for learning Markdown on GitHub