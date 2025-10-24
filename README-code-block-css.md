# Code Block CSS - Syntax Highlighting Reference

A comprehensive syntax highlighting theme for Sphinx code blocks that provides enhanced readability and visual distinction for different code elements.

## Overview

This CSS file (`code-block.css`) defines custom syntax highlighting colors for code blocks in Sphinx documentation. It uses Pygments token classes to style different elements of code syntax with carefully chosen colors for optimal readability.

## Color Scheme

The theme uses a balanced color palette designed for:
- **High contrast** for better readability
- **Semantic color coding** where similar elements share similar colors
- **Visual hierarchy** with bold fonts for important elements like keywords
- **Accessibility** with colors that work for most color vision types

## CSS Class Reference

### 🎨 **Base Elements**

| Class Name | Color | Weight/Style | Description |
|------------|-------|--------------|-------------|
| `#codecell3` | `#c9c9c9` | normal | General code block text color |
| `.highlight .hll` | `#ffffcc` (bg) | normal | Highlighted line background |
| `.highlight` | `#eeffcc` (bg) | normal | Main code block background |

### 💬 **Comments**

| Class Name | Color | Weight/Style | Description |
|------------|-------|--------------|-------------|
| `.highlight .c` | `#408090` | italic | General comments |
| `.highlight .ch` | `#408090` | italic | Hashbang comments (#!/bin/bash) |
| `.highlight .cm` | `#408090` | italic | Multi-line comments (/* ... */) |
| `.highlight .cp` | `#007020` | normal | Preprocessor comments (#include) |
| `.highlight .cpf` | `#408090` | italic | Preprocessor file comments |
| `.highlight .c1` | `#408090` | italic | Single-line comments (//, #) |
| `.highlight .cs` | `#408090` | italic | Special comments with background |

### 🔑 **Keywords & Operators**

| Class Name | Color | Weight/Style | Description |
|------------|-------|--------------|-------------|
| `.highlight .k` | `#007020` | **bold** | General keywords (if, for, while) |
| `.highlight .kc` | `#007020` | **bold** | Keyword constants (True, False, None) |
| `.highlight .kd` | `#007020` | **bold** | Keyword declarations (def, class, var) |
| `.highlight .kn` | `#007020` | **bold** | Keyword namespace (import, from) |
| `.highlight .kp` | `#007020` | normal | Pseudo keywords |
| `.highlight .kr` | `#007020` | **bold** | Reserved keywords |
| `.highlight .kt` | `#902000` | normal | Keyword types (int, string, bool) |
| `.highlight .o` | `#666` | normal | Operators (+, -, *, =) |
| `.highlight .ow` | `#007020` | **bold** | Operator words (and, or, not, in) |

### 🔢 **Numbers & Literals**

| Class Name | Color | Weight/Style | Description |
|------------|-------|--------------|-------------|
| `.highlight .m` | `#208050` | normal | General numbers |
| `.highlight .mb` | `#208050` | normal | Binary numbers (0b1010) |
| `.highlight .mf` | `#208050` | normal | Float numbers (3.14) |
| `.highlight .mh` | `#208050` | normal | Hexadecimal numbers (0xFF) |
| `.highlight .mi` | `#208050` | normal | Integer numbers (42) |
| `.highlight .mo` | `#208050` | normal | Octal numbers (0o755) |
| `.highlight .il` | `#208050` | normal | Long integer numbers |

### 📝 **Strings**

| Class Name | Color | Weight/Style | Description |
|------------|-------|--------------|-------------|
| `.highlight .s` | `#4070A0` | normal | General strings |
| `.highlight .sa` | `#4070A0` | normal | String affixes (f"", r"") |
| `.highlight .sb` | `#4070A0` | normal | Backtick strings |
| `.highlight .sc` | `#4070A0` | normal | Character strings ('a') |
| `.highlight .dl` | `#4070A0` | normal | String delimiters |
| `.highlight .sd` | `#4070A0` | italic | Documentation strings (docstrings) |
| `.highlight .s2` | `#4070A0` | normal | Double-quoted strings ("text") |
| `.highlight .se` | `#4070A0` | **bold** | Escape sequences (\n, \t) |
| `.highlight .sh` | `#4070A0` | normal | Heredoc strings |
| `.highlight .si` | `#70A0D0` | italic | String interpolation (${var}) |
| `.highlight .sx` | `#C65D09` | normal | Other string types |
| `.highlight .sr` | `#235388` | normal | Regular expressions |
| `.highlight .s1` | `#4070A0` | normal | Single-quoted strings ('text') |
| `.highlight .ss` | `#517918` | normal | String symbols (:symbol) |

### 🏷️ **Names & Identifiers**

| Class Name | Color | Weight/Style | Description |
|------------|-------|--------------|-------------|
| `.highlight .na` | `#4070A0` | normal | Attribute names (obj.attr) |
| `.highlight .nb` | `#007020` | normal | Built-in names (print, len, max) |
| `.highlight .nc` | `#0E84B5` | **bold** | Class names |
| `.highlight .no` | `#60ADD5` | normal | Constant names (CONSTANT) |
| `.highlight .nd` | `#fff` | **bold** | Decorators (@property) |
| `.highlight .ni` | `#D55537` | **bold** | Named entities (&amp;, &lt;) |
| `.highlight .ne` | `#007020` | normal | Exception names |
| `.highlight .nf` | `#06287E` | normal | Function names |
| `.highlight .nl` | `#002070` | **bold** | Labels |
| `.highlight .nn` | `#0E84B5` | **bold** | Namespace names |
| `.highlight .nt` | `#0c4dc7` | **bold** | Tag names (HTML/XML) |
| `.highlight .nv` | `#BB60D5` | normal | Variable names |

### 🔧 **Variables (Specific Types)**

| Class Name | Color | Weight/Style | Description |
|------------|-------|--------------|-------------|
| `.highlight .bp` | `#007020` | normal | Built-in pseudo variables |
| `.highlight .fm` | `#06287E` | normal | Magic function names (__init__) |
| `.highlight .vc` | `#BB60D5` | normal | Class variables |
| `.highlight .vg` | `#BB60D5` | normal | Global variables |
| `.highlight .vi` | `#BB60D5` | normal | Instance variables |
| `.highlight .vm` | `#BB60D5` | normal | Magic variables (__name__) |

### 🚨 **Error & Generic Elements**

| Class Name | Color | Weight/Style | Description |
|------------|-------|--------------|-------------|
| `.highlight .err` | red border | normal | Syntax errors |
| `.highlight .gd` | `#A00000` | normal | Generic deleted text (diff -) |
| `.highlight .ge` | normal | italic | Generic emphasized text |
| `.highlight .ges` | normal | **bold italic** | Generic emphasized strong text |
| `.highlight .gr` | `#F00` | normal | Generic error text |
| `.highlight .gh` | `#000080` | **bold** | Generic heading |
| `.highlight .gi` | `#00A000` | normal | Generic inserted text (diff +) |
| `.highlight .go` | `#333` | normal | Generic output text |
| `.highlight .gp` | `#C65D09` | **bold** | Generic prompt (>>> in Python) |
| `.highlight .gs` | normal | **bold** | Generic strong text |
| `.highlight .gu` | `#800080` | **bold** | Generic subheading |
| `.highlight .gt` | `#04D` | normal | Generic traceback |
| `.highlight .w` | `#BBB` | normal | Whitespace |

## Usage

### Installation

1. **Add the CSS file** to your Sphinx project:
   ```
   source/_static/css/code-block.css
   ```

2. **Update your `conf.py`** to include the CSS:
   ```python
   html_css_files = [
       'css/custom.css',        # Your main dark mode CSS
       'css/code-block.css',    # Syntax highlighting CSS
   ]
   ```

3. **Build your documentation**:
   ```bash
   make html
   ```

### Code Block Examples

The syntax highlighting will automatically apply to code blocks:

````markdown
```python
def hello_world():
    """This is a docstring."""
    print("Hello, World!")  # This is a comment
    return True
```
````

````markdown
```bash
#!/bin/bash
# This is a shell script comment
echo "Setting up environment..."
export PATH=/usr/local/bin:$PATH
```
````

## Customization

To customize colors, modify the CSS variables or specific class colors:

```css
/* Example: Change keyword color to purple */
.highlight .k { color: #8A2BE2; font-weight: bold; }

/* Example: Change string color to orange */
.highlight .s { color: #FF8C00; }
```

This syntax highlighting works with any language supported by Pygments, including:

- **Python** (.py files)
- **JavaScript** (.js files)  
- **Bash/Shell** (.sh files)
- **CSS** (.css files)
- **HTML** (.html files)
- **JSON** (.json files)
- **YAML** (.yml files)
- **SQL** (.sql files)
- **And many more...**

---

*This syntax highlighting theme was designed to complement the enhanced dark mode CSS and provide optimal code readability in Sphinx documentation.*