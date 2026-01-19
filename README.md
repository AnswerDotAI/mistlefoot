# mistlefoot

Extended markdown features for mistletoe, including subscript, superscript, highlighting, emojis, footnotes, task lists, and more.

## Installation

```bash
pip install mistlefoot
```

## Features

- **Subscript & Superscript**: H~2~O and E=mc^2^
- **Highlighting**: ==marked text==
- **Strikethrough**: ~~deleted text~~
- **Emojis**: :smile: :rocket: :heart: (50+ supported)
- **Auto-linking**: URLs automatically become clickable links
- **Footnotes**: Reference[^1] with definitions
- **Task lists**: GitHub-style checkboxes
- **Heading attributes**: Add IDs, classes, and custom attributes to headings

## Usage

```python
from mistletoe import Document
from mistletoe_extended import ExtendedHtmlRenderer

markdown_text = """
# My Document {#intro .important}

This is **H~2~O** and ==highlighted text==.

Check out https://fast.ai :rocket:

- [x] Done
- [ ] Todo
"""

with ExtendedHtmlRenderer() as renderer:
    html = renderer.render(Document(markdown_text))
    print(html)
```

## Examples

**Scientific notation:**
```markdown
H~2~O and E=mc^2^
```

**Emojis:**
```markdown
Great work! :tada: :100:
```

**Footnotes:**
```markdown
Here's a claim[^1].

[^1]: This is the supporting reference.
```

**Heading attributes:**
```markdown
# Section {#my-id .highlight data-level="1"}
```

## Contributing

By Jeremy Howard. Contributions welcome.

