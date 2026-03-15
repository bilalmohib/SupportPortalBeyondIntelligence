# Freshdesk Theme Implementation Guide

## Overview

This `freshdesk-theme` folder contains customized HTML templates and CSS stylesheets that implement the **Beyond Intelligence Design System** for Freshdesk support portals.

## ✅ What's Been Implemented

### CSS Theme ✨

The `stylesheet/styles.css` file includes:

1. **Design System Variables** - All color tokens, typography scales, spacing, shadows, and border radius from the Beyond Intelligence design system
2. **Freshdesk Portal Styling** - Custom CSS for Freshdesk-specific components:
   - Portal headers and navigation
   - Article lists and search results
   - Category grids
   - Footer styling
   - Button variants (primary, secondary, danger, ghost)
   - Form elements (text inputs, textareas, selects, checkboxes)
   - Card layouts
   - Status alerts and messages
   - Badges and tags
   - Breadcrumbs
   - Pagination

3. **Responsive Design** - Mobile-friendly breakpoints for tablets and phones
4. **Accessibility Features** - Focus states, reduced motion support, semantic HTML compatibility
5. **Dark Mode Support** - CSS custom properties for light and dark theme variants

### Design Tokens Applied

| Token | Value | Usage |
|-------|-------|-------|
| **Primary Color** | #6366F1 (Indigo) | Buttons, links, active states |
| **Primary Hover** | #4F46E5 | Hover states for interactive elements |
| **Background** | #FFFFFF | Main content areas |
| **Text** | #1d1d1d | Body text and headings |
| **Border** | #E5E7EB | Dividers and card borders |
| **Success** | #22C55E | Success messages and badges |
| **Warning** | #F59E0B | Warning alerts |
| **Error** | #EF4444 | Error messages and validation |
| **Font Stack** | Inter, system-ui, sans-serif | Typography throughout |

## 📋 How to Use These Templates

### Installation in Freshdesk

#### Step 1: Apply the CSS

1. Login to your Freshdesk account
2. Go to **Admin** → **Portal Settings** → **Portal Customization**
3. Select the **Custom CSS** tab
4. Copy the entire content from `stylesheet/styles.css`
5. Paste it into the Custom CSS field
6. Click **Save & Publish**

#### Step 2: Apply HTML Templates

Each `.html` file in this folder corresponds to a Freshdesk page type:

**Discussions (Community Forum):**
- `DiscussionsCategory.html` - Category listing page
- `DiscussionsHome.html` - Discussions home page
- `MyTopics.html` - User's topics
- `NewTopic.html` - New topic creation
- `TopicList.html` - Topic listing
- `TopicView.html` - Individual topic view

**General Pages:**
- `LoginPage.html` - Login/authentication
- `NewUserSignup.html` - User registration
- `PortalHome.html` - Portal homepage
- `SearchResults.html` - Search results page

**Solutions (Knowledge Base):**
- `ArticleView.html` - Article/solution view
- `FooterView.html` - Knowledge base footer
- `SolutionsCategory.html` - Solutions category
- `SolutionsHome.html` - Knowledge base home

**Tickets (Support Center):**
- `PublicTicketView.html` - View public ticket
- `SubmitTicket.html` - Submit new ticket
- `TicketList.html` - Ticket listing
- `TicketView.html` - Individual ticket view

**Layout:**
- `Head.html` - HTML head section (includes meta, fonts, styles)
- `Header.html` - Portal header and navigation
- `Footer.html` - Portal footer
- `Layout.html` - Main layout wrapper

### Customization Options

#### Change Primary Color

If you want to use a different primary color, modify the CSS variables at the top of `styles.css`:

```css
:root {
  --freshdesk-primary: #YOUR_COLOR_HEX;
  --freshdesk-primary-hover: #DARKER_VERSION;
  --freshdesk-primary-light: #LIGHTER_VERSION;
}
```

#### Change Font

To use a different font family, update:

```css
:root {
  --font-inter: 'Your Font Name', system-ui, -apple-system, sans-serif;
}
```

Recommended fonts:
- **Sans-serif**: Inter (current), Segoe UI, -apple-system
- **Serif**: Playfair Display, Lora, Georgia

#### Adjust Spacing & Radius

Modify these variables:

```css
:root {
  --freshdesk-spacing: 8px;      /* Base spacing unit */
  --freshdesk-radius: 8px;       /* Border radius */
}
```

## 🎨 Color Palette Reference

### Primary Colors
```
#6366F1  - Primary (Indigo)
#4F46E5  - Primary Hover
#3f408f  - Primary Dark
#EEF2FF  - Primary Light
```

### Neutral Colors
```
#FFFFFF  - Background/White
#0B0C26  - Dark Background (Footer)
#1d1d1d  - Text Primary
#9D9AA6  - Text Secondary
#A0A0A0  - Text Light
#E5E7EB  - Border
#F6F6F6  - Hover/Secondary BG
```

### Status Colors
```
#22C55E  - Success
#F59E0B  - Warning
#EF4444  - Error
#3B82F6  - Info
```

## 📱 Responsive Breakpoints

The stylesheet includes responsive styles for:
- **Desktop**: 1024px and up
- **Tablet**: 768px - 1023px
- **Mobile**: Below 768px
- **Small Mobile**: Below 480px

## ♿ Accessibility Features

- Focus states with visible outlines
- Semantic HTML structure support
- Reduced motion preferences respected
- Color contrast compliant (WCAG AA)
- Screen reader optimized (sr-only class)

## 🧪 Testing Checklist

- [ ] Clear browser cache (Cmd+Shift+R on Mac, Ctrl+Shift+R on Windows)
- [ ] Verify all pages load with correct styling
- [ ] Check button colors and hover states
- [ ] Test form elements (inputs, textareas, selects)
- [ ] Verify footer styling and dark background
- [ ] Test responsive layout on mobile devices
- [ ] Verify navigation highlighting
- [ ] Check alert/status message styling
- [ ] Test category grid layout
- [ ] Verify breadcrumb styling
- [ ] Check pagination styles

## 🔧 File Structure

```
freshdesk-theme/
├── stylesheet/
│   └── styles.css              ← Complete CSS with all design tokens
├── layout/
│   ├── Head.html               ← HTML head section
│   ├── Header.html             ← Portal header/navigation
│   ├── Footer.html             ← Portal footer
│   └── Layout.html             ← Main layout template
├── GeneralPages/
│   ├── LoginPage.html
│   ├── NewUserSignup.html
│   ├── PortalHome.html
│   └── SearchResults.html
├── Solutions/
│   ├── ArticleView.html
│   ├── FooterView.html
│   ├── SolutionsCategory.html
│   └── SolutionsHome.html
├── Tickets/
│   ├── PublicTicketView.html
│   ├── SubmitTicket.html
│   ├── TicketList.html
│   └── TicketView.html
└── Discussions/
    ├── DiscussionsCategory.html
    ├── DiscussionsHome.html
    ├── MyTopics.html
    ├── NewTopic.html
    ├── TopicList.html
    └── TopicView.html
```

## 🔗 Resource Links

- **Design System**: `/original-website/docs/THEME_EXPORT.md`
- **Color Tokens**: `/original-website/docs/theme.json`
- **Original CSS**: `/original-website/css/theme.css` and `/original-website/css/freshdesk-theme.css`

## 🆘 Troubleshooting

### Styles not appearing?
1. Clear the browser cache completely
2. Hard refresh the page (Cmd+Shift+R or Ctrl+Shift+R)
3. Check that CSS is properly saved in Freshdesk Settings

### Colors look wrong?
1. Verify the color hex values in `styles.css`
2. Check if there's a portal theme override in Freshdesk settings
3. Ensure custom CSS is saved and published

### Responsive layout broken?
1. Check media query breakpoints at the bottom of `styles.css`
2. Test in different browser viewport sizes
3. Verify mobile-specific styles are applying

## 📞 Support

For questions about the design system or implementation:
- Review original design specs: `/original-website/docs/FRESHDESK_IMPLEMENTATION_GUIDE.md`
- Check color tokens: `/original-website/docs/theme.json`
- Reference Freshdesk documentation: https://support.freshdesk.com/portal/kb/

## ✨ Features

✅ Complete design system implementation  
✅ Responsive mobile-friendly layout  
✅ Freshdesk-specific component styling  
✅ Accessibility compliant  
✅ Dark mode support  
✅ Custom focus and hover states  
✅ Comprehensive color palette  
✅ Print-friendly styles  
✅ Semantic HTML structure  
✅ CSS variable customization support  

---

**Version**: 1.0  
**Last Updated**: March 2026  
**Base System**: Beyond Intelligence Design System