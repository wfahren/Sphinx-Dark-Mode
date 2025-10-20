# Sphinx RTD-Theme Dark Mode CSS

A comprehensive dark mode implementation for the Sphinx Read the Docs theme that provides an elegant dark interface while maintaining excellent readability and accessibility.

## Features

### 🌙 **Dark Mode Styling**

- **Complete Dark Theme**: Professional dark color scheme for all elements
- **High Contrast**: Optimized text contrast for excellent readability
- **Eye-Friendly**: Reduces eye strain during extended reading sessions
- **Consistent Design**: Maintains RTD theme's clean, professional appearance

### 🎨 **Enhanced Visual Elements**

- **Smooth Transitions**: Animated hover effects and state changes
- **Custom Scrollbars**: Dark-themed scrollbars that match the overall design
- **Improved Navigation**: Enhanced sidebar and navigation styling
- **Code Block Optimization**: Dark syntax highlighting for better code readability

### 🔧 **Responsive Design**

- **Mobile Friendly**: Optimized for all screen sizes
- **Print Compatibility**: Maintains readability when printed
- **Accessibility**: WCAG compliant color contrasts
- **Cross-Browser**: Works across all modern browsers

## Installation

### Requirements

- Sphinx documentation generator
- Read the Docs theme (`sphinx_rtd_theme`)
- Basic CSS customization support

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
   make html
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

### Primary Colors

| Element | Light Mode | Dark Mode | Usage |
|---------|------------|-----------|-------|
| Background | `#ffffff` | `#1e1e1e` | Main page background |
| Text | `#404040` | `#e0e0e0` | Primary text content |
| Sidebar | `#f8f8f8` | `#2d2d2d` | Navigation background |
| Code Blocks | `#f8f8f8` | `#2d2d2d` | Code background |
| Links | `#2980b9` | `#4da6e0` | Hyperlinks |
| Borders | `#e1e4e5` | `#404040` | Dividers and borders |

### Accent Colors

- **Success**: `#27ae60` → `#2ecc71` (Green)
- **Warning**: `#f39c12` → `#f1c40f` (Orange/Yellow)
- **Error**: `#e74c3c` → `#e67e22` (Red/Orange)
- **Info**: `#3498db` → `#74b9ff` (Blue)

## Customization

### Adjusting Colors

To modify the color scheme, edit the CSS variables at the top of the file:

```css
:root {
  --bg-color: #1e1e1e;           /* Main background */
  --text-color: #e0e0e0;         /* Primary text */
  --sidebar-bg: #2d2d2d;         /* Sidebar background */
  --accent-color: #4da6e0;       /* Links and accents */
  --border-color: #404040;       /* Borders and dividers */
}
```

### Theme Variants

Create different dark mode variants by adjusting the color variables:

#### Midnight Blue Theme

```css
--bg-color: #0f1419;
--sidebar-bg: #1a1f2e;
--accent-color: #39d7ff;
```

#### Warm Dark Theme

```css
--bg-color: #1a1611;
--sidebar-bg: #2a251f;
--accent-color: #ff9500;
```

### Typography Adjustments

Modify font settings for better readability:

```css
body {
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 16px;
  line-height: 1.6;
}

.rst-content h1, .rst-content h2, .rst-content h3 {
  font-weight: 600;
  color: var(--text-color);
}
```

## Browser Support

- **Chrome/Chromium**: Full support
- **Firefox**: Full support
- **Safari**: Full support
- **Edge**: Full support
- **Mobile Browsers**: Responsive design supported

## Accessibility

### WCAG Compliance

- **AA Color Contrast**: All text meets WCAG AA standards
- **Focus Indicators**: Clear keyboard navigation
- **Screen Reader**: Compatible with assistive technologies
- **High Contrast**: Optional high contrast mode available

### Color Blind Friendly

The color scheme is designed to be accessible for users with:

- Protanopia (red-blind)
- Deuteranopia (green-blind)
- Tritanopia (blue-blind)

## Development

### Building and Testing

1. **Make changes** to `source/_static/css/custom.css`
2. **Rebuild documentation**:

   ```bash
   make clean
   make html
   ```

3. **Clear browser cache** (critical step):
   - **Hard refresh**: `Ctrl+F5` (Windows/Linux) or `Cmd+Shift+R` (Mac)
   - **Force reload**: `Ctrl+Shift+R` in most browsers
   - **Developer tools**: F12 → Network tab → "Disable cache" checkbox
   - **Incognito mode**: Test in private browsing to bypass cache entirely

4. **Test across devices** and browsers
5. **Validate accessibility** using browser dev tools

> **Important**: CSS changes often require a hard refresh or cache clear to be visible. If you don't see your changes immediately, try a hard refresh before assuming the CSS isn't working.

### CSS Organization

The CSS follows these principles:

- **Mobile-first**: Base styles for mobile, enhanced for desktop
- **Progressive Enhancement**: Graceful degradation for older browsers
- **Maintainable**: Clear organization and commenting
- **Performance**: Optimized selectors and minimal redundancy

### Debugging

Use browser developer tools to:

- Inspect color contrast ratios
- Test responsive breakpoints
- Validate CSS performance
- Check accessibility compliance

## Integration with Search Enhancement

This dark mode CSS works seamlessly with the Enhanced Sphinx Search:

```css
/* Search result highlighting in dark mode */
.highlighted {
  background-color: #3a3a00;
  color: #ffff99;
  padding: 2px 4px;
  border-radius: 2px;
}
```

## Performance

### Optimization Features

- **CSS Variables**: Efficient color management
- **Minimal Overrides**: Only necessary style changes
- **Compressed**: Minified for production use
- **Cache-Friendly**: Structured for optimal browser caching

### Loading Speed

- **Small File Size**: ~15KB compressed
- **No External Dependencies**: Self-contained CSS
- **Efficient Selectors**: Optimized for browser performance

## Troubleshooting

### Common Issues

**Q: Dark mode not applying**
A: Ensure `custom.css` is in the correct path and listed in `html_css_files`

**Q: CSS changes not visible**
A: **Hard refresh your browser** (`Ctrl+F5` or `Cmd+Shift+R`) or clear browser cache. This is the most common issue when developing CSS.

**Q: Navigation hover effects not working**
A: Try a hard refresh first. If still not working, check browser developer tools to see if CSS is loading properly.

**Q: Some elements still show light colors**
A: Check for theme-specific CSS that may override the dark styles

**Q: Text is hard to read**
A: Adjust contrast ratios in the color variables section

**Q: Mobile layout issues**
A: Verify responsive breakpoints are working correctly

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

## Contributing

When contributing improvements:

1. **Test thoroughly** across browsers and devices
2. **Maintain accessibility** standards
3. **Document changes** in CSS comments
4. **Follow naming conventions** for consistency
5. **Validate CSS** using standard tools

## License

This CSS customization maintains the same license as your documentation project.

## Changelog

### v1.0.0

- Initial dark mode implementation
- Complete RTD theme coverage
- Responsive design optimization
- Accessibility compliance
- Search integration support

### Future Enhancements

- [ ] Auto dark/light mode detection
- [ ] Theme switcher widget
- [ ] Additional color scheme variants
- [ ] Enhanced print styles
- [ ] Animation preferences support

---

*This dark mode CSS was developed to provide a professional, accessible, and visually appealing dark theme for Sphinx documentation while maintaining the excellent usability of the Read the Docs theme.*
