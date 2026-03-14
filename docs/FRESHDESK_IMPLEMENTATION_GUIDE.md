# Freshdesk Theme Implementation Guide

## Overview

This guide provides step-by-step instructions to apply the Beyond Intelligence design system theme to a Freshdesk support portal, ensuring visual consistency between the main website (beyondintelligence.ai) and the help center.

---

## Table of Contents

1. [Quick Start](#quick-start)
2. [Installation Steps](#installation-steps)
3. [Configuration Guide](#configuration-guide)
4. [Theme Customization](#theme-customization)
5. [Testing & Validation](#testing--validation)
6. [Troubleshooting](#troubleshooting)
7. [File References](#file-references)

---

## Quick Start

**Time Required**: 15-20 minutes  
**Difficulty**: Intermediate  
**Prerequisites**: Freshdesk admin access

### Three Files Needed:
1. **theme.css** — General design system styles
2. **freshdesk-theme.css** — Freshdesk portal-specific styles
3. **theme.json** — Reference for colors and tokens

---

## Installation Steps

### Step 1: Access Freshdesk Portal Settings

1. Log in to your Freshdesk account
2. Navigate to **Admin** (gear icon)
3. Go to **Portal Settings** → **Portal Customization**
4. Click on the **Custom CSS** tab

### Step 2: Apply Base Theme CSS

1. Copy the entire content from [theme.css](theme.css)
2. Paste it into the **Custom CSS** section
3. Click **Save**

### Step 3: Apply Freshdesk-Specific Styles

1. At the end of the existing CSS, paste the content from [freshdesk-theme.css](freshdesk-theme.css)
2. Click **Save & Publish**

### Step 4: Verify Installation

1. Clear your browser cache (Cmd+Shift+R on Mac, Ctrl+Shift+R on Windows)
2. Open your Freshdesk support portal: `https://yourcompany.freshdesk.com/support`
3. Verify that:
   - Background colors match Beyond Intelligence theme
   - Primary action buttons are indigo (#6366F1)
   - Typography and spacing match the design system
   - Navigation bar has proper styling

---

## Configuration Guide

### Primary Color Customization

If you need to change the primary color from indigo to another color, update the CSS variable:

**In Custom CSS:**
```css
:root {
  --freshdesk-primary: #YOUR_HEX_COLOR;
  --freshdesk-primary-hover: #DARKER_VERSION;
  --freshdesk-primary-light: #LIGHTER_VERSION;
}
```

**Color Values Used:**
- Primary: `#6366F1` (Indigo)
- Hover: `#4F46E5` (Darker Indigo)
- Light: `#EEF2FF` (Light Indigo background)
- Dark BG: `#0B0C26` (Footer background)

### Font Customization

The design system uses **Inter** from Google Fonts. To use a different font:

```css
:root {
  --freshdesk-font: 'Your Font Name', system-ui, sans-serif;
}
```

**Recommended Fonts:**
- Sans-serif: Inter, Segoe UI, -apple-system, BlinkMacSystemFont
- Serif: Playfair Display, Lora, Georgia

### Dark Mode Implementation

If Freshdesk supports dark mode, the CSS already includes dark color overrides. To enable:

```css
.dark {
  --freshdesk-background: #0B0C26;
  --freshdesk-text: #FFFFFF;
  /* ... other dark mode variables */
}
```

---

## Theme Customization

### Spacing & Layout

Adjust container max-width and padding:

```css
.portal-container,
.container {
  max-width: 1350px; /* Change if needed */
  margin: 0 auto;
  padding: 0 24px; /* Adjust padding */
}
```

### Button Styling

To customize button appearance:

```css
.btn-primary {
  background-color: var(--freshdesk-primary);
  color: #FFFFFF;
  padding: 8px 16px; /* Adjust padding */
  border-radius: 8px; /* Adjust radius */
  font-size: 14px; /* Adjust font size */
}
```

### Border Radius

To adjust roundness globally:

```css
:root {
  --freshdesk-radius: 8px; /* Change this value */
}
```

### Shadows

To adjust shadow intensity:

```css
:root {
  --freshdesk-shadow: 0 1px 2px 0 rgba(16, 24, 40, 0.08);
  /* Adjust rgba values (last number = strength) */
}
```

---

## Testing & Validation

### Checklist

- [ ] Header displays with correct logo and navigation
- [ ] Search box has proper styling and focus state
- [ ] All buttons are indigo with proper hover states
- [ ] Form inputs have focus rings and error states
- [ ] Articles/categories display in card layout
- [ ] Footer appears with dark background
- [ ] Mobile responsive layout works correctly
- [ ] Color contrast meets WCAG AA standards
- [ ] Links are underlined and have proper hover states
- [ ] Badges and labels display correctly

### Cross-Browser Testing

Test on:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile Safari (iOS)
- Chrome Mobile (Android)

### Device Testing

Test on:
- Desktop (1920px+)
- Tablet (768px - 1024px)
- Mobile (320px - 480px)

---

## Troubleshooting

### Styles Not Applying

**Problem**: CSS changes don't appear on the portal.

**Solutions**:
1. Clear browser cache (Cmd+Shift+R or Ctrl+Shift+R)
2. In Freshdesk admin, click "Save & Publish" (not just Save)
3. Wait 1-2 minutes for changes to propagate
4. Check browser console for CSS errors (F12)
5. Verify CSS syntax using a validator: [csslint.net](https://csslint.net)

### Incorrect Colors

**Problem**: Colors don't match the design system.

**Solution**:
1. Verify hex color codes in `theme.json`
2. Check if Freshdesk has color overrides in other settings
3. Look for inline styles that might override CSS variables
4. Use browser DevTools (F12) to inspect elements and see applied styles

### Mobile Layout Broken

**Problem**: Layout looks incorrect on mobile devices.

**Solution**:
1. Check media queries in `freshdesk-theme.css`
2. Verify viewport meta tag is set: `<meta name="viewport" content="width=device-width, initial-scale=1">`
3. Test in responsive mode in browser DevTools
4. Reduce font sizes or padding if content overflows

### Fonts Not Loading

**Problem**: Custom font doesn't appear.

**Solution**:
1. Ensure you're using system fonts or Google Fonts
2. In Custom CSS, add font import:
   ```css
   @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');
   ```
3. Clear cache and reload portal

### Button Styles Override by Freshdesk

**Problem**: Default portal buttons still show old styling.

**Solution**:
1. Use `!important` flag in CSS (last resort):
   ```css
   .btn-primary {
     background-color: var(--freshdesk-primary) !important;
   }
   ```
2. Check Freshdesk portal settings for conflicting button colors
3. Look for Freshdesk-generated class names (e.g., `.fr-btn-primary`)

---

## File References

### 1. theme.json
**Purpose**: Design token reference  
**Use**: Look up colors, spacing, font sizes, shadows  
**Key Sections**:
- `colors` — All color values
- `typography` — Font sizes and weights
- `spacing` — Spacing scale
- `radius` — Border radius values
- `shadows` — Shadow definitions
- `components` — Component-specific styles

### 2. theme.css
**Purpose**: Generic CSS variables and styles  
**Use**: Import into projects, base styling  
**Key Sections**:
- CSS custom properties at `:root`
- Typography styles (h1-h6, p)
- Button component classes
- Input/form element styles
- Card component styles
- Utility classes

### 3. freshdesk-theme.css
**Purpose**: Freshdesk portal-specific customizations  
**Use**: Paste directly into Freshdesk Custom CSS  
**Key Sections**:
- Freshdesk theme variables
- Portal header/footer styles
- Navigation menu styles
- Article list and search result styles
- Category grid customization
- Badge, breadcrumb, pagination styles
- Responsive media queries
- Accessibility features

### 4. THEME_EXPORT.md
**Purpose**: Comprehensive design system documentation  
**Use**: Reference for designers and developers  
**Key Sections**:
- Color palette with hex values
- Typography scale with responsive sizes
- Spacing system and container sizes
- Border radius tokens
- Shadow and elevation system
- Breakpoints and responsive design
- Component specifications
- Animation and transition timings
- Accessibility guidelines

---

## Advanced Customization

### Custom Font Integration

To add the Inter font to Freshdesk:

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

:root {
  --freshdesk-font: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', sans-serif;
}
```

### Custom Gradient Backgrounds

To use the CTA gradient:

```css
.cta-section {
  background: linear-gradient(0deg, #07081D 0%, #07081D 100%), #6366F1;
}
```

### Animation & Transitions

To add the float animation to elements:

```css
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

.float-element {
  animation: float 6s ease-in-out infinite;
}
```

### Dark Mode Toggle

If Freshdesk supports theme toggles:

```css
/* Light Mode */
:root {
  --freshdesk-background: #FFFFFF;
  --freshdesk-text: #1d1d1d;
}

/* Dark Mode */
html.dark,
[data-theme="dark"] {
  --freshdesk-background: #0B0C26;
  --freshdesk-text: #FFFFFF;
}
```

---

## Performance Optimization

### CSS File Size
- **theme.css**: ~15 KB
- **freshdesk-theme.css**: ~35 KB
- **Combined**: ~50 KB (minified: ~35 KB)

### Optimization Tips

1. **Remove Unused Styles**: Delete component styles you don't use
2. **Use CSS Variables**: Reduces file size and enables easy customization
3. **Minify CSS**: Use online minifier for production
4. **Load Fonts Efficiently**:
   ```css
   @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');
   ```
5. **Lazy Load Images**: Use `loading="lazy"` on images

---

## Support & Maintenance

### Regular Updates

1. **Check for Freshdesk updates** that might affect custom CSS
2. **Test quarterly** to ensure theme still matches main site
3. **Update colors** if brand guidelines change
4. **Add new components** as site evolves

### Version Control

Keep track of changes:

```
v1.0.0 - Initial Freshdesk theme setup
v1.0.1 - Fixed mobile navigation layout
v1.1.0 - Added dark mode support
```

### Backup CSS

Always save your CSS modifications:

```
Theme Library/
├── freshdesk-theme-v1.0.0.css (backup)
├── freshdesk-theme-current.css (active)
└── theme.json (reference)
```

---

## FAQ

**Q: Can I use this theme on other platforms?**  
A: Yes! The `theme.css` is platform-agnostic. The `freshdesk-theme.css` is Freshdesk-specific but can be adapted for other platforms.

**Q: How do I match the dark mode?**  
A: Use the `.dark` class overrides in `theme.css` and apply `[data-theme="dark"]` selector.

**Q: Can I add custom branding?**  
A: Yes! Modify colors in `:root` CSS variables. See [Theme Customization](#theme-customization) section.

**Q: Are the colors WCAG compliant?**  
A: Primary color (#6366F1) achieves WCAG AA contrast on white backgrounds.

**Q: What if Freshdesk updates break my styling?**  
A: Test after major Freshdesk updates. Use `!important` flag as last resort to override conflicts.

**Q: Can I preview before publishing?**  
A: Yes! Use browser DevTools to test CSS locally before applying to Freshdesk.

---

## Next Steps

1. **Backup existing CSS** (if any)
2. **Review color palette** in `theme.json`
3. **Apply styles** using steps in [Installation Steps](#installation-steps)
4. **Test on all devices** using [Testing Checklist](#checklist)
5. **Customize as needed** using [Customization Guide](#theme-customization)
6. **Document changes** for future reference

---

## Contact & Support

For questions about the Beyond Intelligence design system:
- Email: support@beyondintelligence.ai
- Website: https://beyondintelligence.ai

For Freshdesk-specific help:
- Freshdesk Support: https://freshdesk.com/support
- Freshdesk Community: https://community.freshdesk.com

---

## License

This design system export is provided for use with Freshdesk support portal customization only. Maintain consistency with the official Beyond Intelligence brand guidelines.

**Last Updated**: March 13, 2026  
**Design System Version**: 1.0.0  
**Freshdesk Compatible**: v2.0+

