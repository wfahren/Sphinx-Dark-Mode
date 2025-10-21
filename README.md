# Sphinx RTD-Theme Dark Mode CSS

A comprehensive dark mode implementation for the Sphinx Read the Docs theme that provides an elegant dark interface while maintaining excellent readability and accessibility.

## Installation

### Requirements

- Sphinx documentation generator
- Read the Docs theme (`sphinx_rtd_theme`)

### Setup

1. **Copy the CSS file** to your Sphinx project:

   ```text
   source/_static/css/custom.css
   ```

2. **Update your `conf.py`** to include the CSS:

   ```python
   # Ensure static path is configured
   html_static_path = ['_static']
   
   # Add your custom CSS
   html_css_files = [
       'css/custom.css',
       # ... your other CSS files
   ]
   ```

3. **Build your documentation**:

   ```bash
   make clean && make html
   ```

4. **Clear browser cache** (important for seeing changes):
   - **Hard refresh**: `Ctrl+F5` (Windows/Linux) or `Cmd+Shift+R` (Mac)
   - **Clear cache**: Use browser developer tools to clear site data
   - **Incognito/Private mode**: Test in a fresh browser session

## CSS File Structure

The dark mode CSS is organized into logical sections:

```text
custom.css
├── Color Variables          # Global color definitions
├── Body & Background        # Main page styling
├── Navigation & Sidebar     # Left sidebar styling
├── Content Area            # Main content styling
├── Code Blocks             # Syntax highlighting
├── Tables & Lists          # Data presentation
├── Search & Forms          # Interactive elements
├── Responsive Design       # Mobile adaptations
└── Print Styles           # Print-friendly overrides
```

## Color Scheme

The dark mode CSS uses a comprehensive set of CSS variables for easy customization and maintenance. All colors are defined in the `:root` section for global access.

### 🎨 **CSS Variables Reference**

#### **Background Colors**

| Variable | Default Value | Usage |
|----------|---------------|-------|
| `--dark-bg` | `#1c1c1c` | Primary dark background |
| `--dark-bg-alt` | `#282828` | Secondary background for contrast |
| `--dark-bg-hover` | `#333333` | Hover state background |

#### **Text Colors**

| Variable | Default Value | Usage |
|----------|---------------|-------|
| `--light-text` | `#e0e0e0` | Primary light text color |
| `--light-text-alt` | `#c0c0c0` | Secondary light text (dimmer) |
| `--dark-text` | `#1f1f1f` | Dark text for light backgrounds |
| `--white-text` | `#ffffff` | Pure white text for contrast |
| `--search-highlight-text` | `#333333` | Dark text on highlighted backgrounds |

#### **Accent and Interactive Colors**

| Variable | Default Value | Usage |
|----------|---------------|-------|
| `--accent-blue` | `#40B4E8` | Primary blue accent for links |
| `--highlight-yellow` | `#f1c40f` | Search term highlighting |
| `--hover-gray` | `#404040` | Navigation hover background |

#### **Heading Colors**

| Variable | Default Value | Usage |
|----------|---------------|-------|
| `--heading-h1` | `#0000ff` | Blue for main headings |
| `--heading-h2` | `#008000` | Green for subheadings |
| `--emphasis-gold` | `#daa520` | Goldenrod for emphasized text |
| `--code-teal` | `#20b2aa` | Light sea green for inline code |

#### **Navigation Hierarchy Colors**

| Variable | Default Value | Usage |
|----------|---------------|-------|
| `--nav-current-light` | `#e3e3e3` | Light background for current items |
| `--nav-current-l1` | `#4e4e4e` | Level 1 current page background |
| `--nav-current-active` | `#8a8a8a` | Active current page link background |
| `--nav-current-l2` | `#8f8f8f` | Level 2 current page background |
| `--nav-current-l3` | `#bdbdbd` | Level 3 current page background |
| `--nav-current-text` | `#008000` | Green text for current page links |

#### **Interface Elements**

| Variable | Default Value | Usage |
|----------|---------------|-------|
| `--border-dark` | `#555555` | Dark borders and dividers |
| `--expand-button` | `#c2c2c2` | Tree expand button color |

#### **Table Colors**

| Variable | Default Value | Usage |
|----------|---------------|-------|
| `--table-odd` | `#2e2e2e` | Odd table row background |
| `--table-even` | `#262626` | Even table row background |

#### **Admonition Colors**

| Variable | Default Value | Usage |
|----------|---------------|-------|
| `--warning-orange` | `#f39c12` | Orange for warning admonitions |
| `--danger-red` | `#e74c3c` | Red for danger/error admonitions |

#### **Print Mode Colors**

| Variable | Default Value | Usage |
|----------|---------------|-------|
| `--print-bg` | `#ffffff` | White background for printing |
| `--print-text` | `#000000` | Black text for printing |

## 🎨 **Customization Guide**

### **Quick Color Adjustments**

The easiest way to customize the theme is by modifying the CSS variables in the `:root` section. All 37 variables are clearly documented and can be changed to match your brand or preferences.

**Basic customization example:**

```css
:root {
  /* Change the main background to a warmer dark tone */
  --dark-bg: #1a1611;
  
  /* Adjust the accent color to match your brand */
  --accent-blue: #ff6b6b;
  
  /* Modify heading colors for better hierarchy */
  --heading-h1: #4ecdc4;
  --heading-h2: #45b7d1;
  
  /* Customize search highlighting */
  --highlight-yellow: #feca57;
}
```

## Troubleshooting

### **Common Issues and Solutions**

**Q: Dark mode not applying**  
A: Ensure `custom.css` is in the correct path (`source/_static/css/custom.css`) and listed in `html_css_files` in your `conf.py`

**Q: CSS changes not visible**  
A: **Hard refresh your browser** (`Ctrl+F5` or `Cmd+Shift+R`) or clear browser cache. This is the most common issue when developing CSS.

**Q: Navigation hover effects not working**  
A: Try a hard refresh first. If still not working, check browser developer tools to see if CSS is loading properly.

**Q: Some elements still show light colors**  
A: Check for theme-specific CSS that may override the dark styles. Use `!important` or increase CSS specificity if needed.

**Q: Text is hard to read**  
A: Adjust contrast ratios using the CSS variables:

```css
:root {
  --light-text: #f0f0f0;        /* Brighter text */
  --dark-bg: #0a0a0a;           /* Darker background */
}
```

**Q: Custom variable changes not working**  
A: Ensure you're modifying the `:root` section and that your custom CSS loads after the base styles.

**Q: Search highlighting not visible**  
A: Adjust the highlighting variables:

```css
:root {
  --highlight-yellow: #your-preferred-color;
  --search-highlight-text: #contrasting-text-color;
}
```

**Q: Mobile layout issues**  
A: The CSS includes responsive breakpoints. Check if custom modifications are interfering:

```css
@media (max-width: 768px) {
  .wy-nav-content {
    padding: 1.618em 1em;
  }
}
```

**Q: Variables not recognized**  
A: Ensure your browser supports CSS custom properties (all modern browsers do). For older browser support, consider fallback values:

```css
color: #e0e0e0; /* fallback */
color: var(--light-text, #e0e0e0); /* with fallback */
```

### Browser-Specific Fixes

```css
/* Firefox scrollbar styling */
@-moz-document url-prefix() {
  .wy-side-scroll {
    scrollbar-width: thin;
    scrollbar-color: #666 #2d2d2d;
  }
}

/* Safari-specific adjustments */
@supports (-webkit-appearance: none) {
  .wy-nav-content {
    -webkit-font-smoothing: antialiased;
  }
}
```

## Changelog

### **v1.0.0 - Initial Release**

- Initial dark mode implementation
- Complete RTD theme coverage
- Responsive design optimization
- Accessibility compliance
- Search integration support

### **v2.0.0 - Variable-Based Architecture**

- **37 CSS variables** for comprehensive customization
- **Detailed documentation** with usage examples
- **Pre-built theme variants** (Midnight Blue, Warm Dark, Matrix, Soft Purple)
- **Component-specific customization** sections
- **Enhanced search integration** with dedicated variables
- **Improved navigation hierarchy** styling
- **Better organization** and maintainability

### **Future Enhancements**

- [ ] Auto dark/light mode detection based on system preferences
- [ ] JavaScript theme switcher widget
- [ ] Additional pre-built color scheme variants
- [ ] Enhanced print styles with better formatting
- [ ] Animation preferences support (`prefers-reduced-motion`)
- [ ] High contrast mode for accessibility
- [ ] Custom font loading and typography options

---

*This dark mode CSS was developed to provide a professional, accessible, and visually appealing dark theme for Sphinx documentation while maintaining the excellent usability of the Read the Docs theme.*
