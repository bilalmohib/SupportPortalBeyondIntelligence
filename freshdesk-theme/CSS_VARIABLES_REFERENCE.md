# CSS Variables Reference

## Complete Design Token Documentation

This document provides a complete reference of all CSS custom properties (variables) available in the Beyond Intelligence Freshdesk theme.

---

## Color Variables

### Primary Colors

```css
--color-primary: #6366F1;              /* Main brand color (Indigo) */
--color-primary-foreground: #FFFFFF;   /* Text on primary backgrounds */
--color-primary-hover: #4F46E5;        /* Hover state for primary */
--color-primary-disabled: #A5B4FC;     /* Disabled state for primary */
--color-primary-light: #EEF2FF;        /* Light variant for badges/backgrounds */
```

### Secondary Colors

```css
--color-secondary: #F6F6F6;            /* Secondary background */
--color-secondary-gray: #9D9AA6;       /* Secondary gray text */
--color-secondary-foreground: #232323; /* Text on secondary backgrounds */
```

### Background Colors

```css
--color-background: #0B0C26;           /* Main dark background */
--color-background-secondary: #151641; /* Secondary dark background */
--color-background-secondary-2: #07081D; /* Tertiary dark background */
--color-foreground: #1d1d1d;           /* Light text/foreground */
```

### Card Colors

```css
--color-card: #FFFFFF;                 /* Card background */
--color-card-foreground: #1d1d1d;      /* Text on cards */
--color-card-border: #E5E7EB;          /* Card border color */
```

### Border Colors

```css
--color-border: #E5E7EB;               /* Default border */
--color-border-hover: #9CA3AF;         /* Border on hover */
--color-border-focus: #A5B4FC;         /* Border on focus */
--color-border-error: #EF4444;         /* Error border */
--color-border-primary: #7C81E8;       /* Primary-colored border */
```

### Text Colors

```css
--color-text-heading: #1d1d1d;         /* Heading text */
--color-text-body: #1d1d1d;            /* Body text */
--color-text-muted: #9D9AA6;           /* Muted/secondary text */
--color-text-white: #FFFFFF;           /* White text */
```

### Input Colors

```css
--color-input-text: #050620;           /* Input text color */
--color-input-placeholder: #9CA3AF;    /* Input placeholder */
--color-input-label-disabled: #9CA3AF; /* Disabled label text */
--color-input-bg: #FFFFFF;             /* Input background */
--color-input-border-default: #E5E7EB; /* Default input border */
--color-input-border-hover: #9CA3AF;   /* Input border on hover */
--color-input-border-focus: #A5B4FC;   /* Input border on focus */
--color-input-border-active: #9CA3AF;  /* Input border on active */
--color-input-border-disabled: #E5E7EB; /* Disabled input border */
```

### Semantic Colors

```css
--color-accent: #14b8a6;               /* Accent color (Teal) */
--color-accent-foreground: #232323;    /* Text on accent */
--color-destructive: #EF4444;          /* Destructive actions (Red) */
--color-success: #22C55E;              /* Success messages (Green) */
--color-warning: #F59E0B;              /* Warning messages (Amber) */
--color-info: #3B82F6;                 /* Info messages (Blue) */
```

### Muted Colors

```css
--color-muted: #F6F6F6;                /* Muted background */
--color-muted-foreground: #9D9AA6;     /* Muted text */
```

### Special Colors

```css
--color-radio-text: #232323;           /* Radio button text */
--color-white-smoke: #F6F6F6;          /* White smoke background */
--color-multi-select-bg: #232562;      /* Multi-select background */
--color-white-overlay: #FFFFFF1A;      /* White overlay (10% opacity) */
--color-input-underline: #E5E7EB;      /* Input underline variant */
```

### Popover Colors

```css
--color-popover: #FFFFFF;              /* Popover background */
--color-popover-foreground: #1d1d1d;   /* Popover text */
```

### Ring & Focus

```css
--color-ring: #6366F1;                 /* Focus ring color */
--color-ring-focus: rgba(55, 125, 238, 0.5); /* Focus ring with opacity */
```

---

## Freshdesk-Specific Colors

```css
--freshdesk-primary: #6366F1;          /* Primary action color */
--freshdesk-primary-hover: #4F46E5;    /* Primary hover state */
--freshdesk-primary-dark: #3f408f;     /* Darker primary variant */
--freshdesk-primary-light: #EEF2FF;    /* Light primary variant */

--freshdesk-background: #FFFFFF;       /* Content background */
--freshdesk-background-dark: #0B0C26;  /* Dark background (footer) */
--freshdesk-text: #1d1d1d;             /* Primary text */
--freshdesk-text-secondary: #9D9AA6;   /* Secondary text */
--freshdesk-text-light: #A0A0A0;       /* Light text */
--freshdesk-border: #E5E7EB;           /* Border color */
--freshdesk-border-light: #F0F0F0;     /* Light border */
--freshdesk-hover: #F6F6F6;            /* Hover background */

--freshdesk-status-success: #22C55E;   /* Success color */
--freshdesk-status-warning: #F59E0B;   /* Warning color */
--freshdesk-status-error: #EF4444;     /* Error color */
--freshdesk-status-info: #3B82F6;      /* Info color */
```

---

## Typography Variables

```css
--font-inter: 'Inter', system-ui, -apple-system, sans-serif;
```

---

## Spacing & Sizing

### Border Radius

```css
--radius: 0.625rem;              /* 10px - Base radius */
--radius-sm: 0.375rem;           /* 6px - Small radius */
--radius-md: 0.5rem;             /* 8px - Medium radius */
--radius-lg: 0.625rem;           /* 10px - Large radius */
--radius-xl: 0.875rem;           /* 14px - Extra large radius */

--freshdesk-radius: 8px;         /* Freshdesk standard radius */
```

### Spacing

```css
--freshdesk-spacing: 8px; /* Base spacing unit */
```

---

## Shadows

```css
--shadow-xs: 0 1px 2px 0 rgba(16, 24, 40, 0.08);
--shadow-sm: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
--shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
--shadow-input-focus: 0px 0px 0px 4px #E1E1FEB2;
--shadow-input-error: 0px 1px 2px 0px #10182814;

--freshdesk-shadow: 0 1px 2px 0 rgba(16, 24, 40, 0.08);
```

---

## Usage Examples

### Using Colors in Components

```css
/* Button with primary color */
.btn-primary {
  background-color: var(--freshdesk-primary);
  color: var(--color-primary-foreground);
}

.btn-primary:hover {
  background-color: var(--freshdesk-primary-hover);
}

/* Card styling */
.card {
  background-color: var(--color-card);
  border: 1px solid var(--color-card-border);
  color: var(--color-card-foreground);
}

/* Input styling */
input {
  background-color: var(--color-input-bg);
  border: 1px solid var(--color-input-border-default);
  color: var(--color-input-text);
}

input:focus {
  border-color: var(--color-input-border-focus);
  box-shadow: var(--shadow-input-focus);
}

/* Text styling */
h1 {
  color: var(--color-text-heading);
}

p {
  color: var(--color-text-body);
}

.text-muted {
  color: var(--color-text-muted);
}

/* Border radius */
.rounded {
  border-radius: var(--radius-lg);
}

.rounded-sm {
  border-radius: var(--radius-sm);
}

/* Status messages */
.alert-success {
  background-color: rgba(var(--color-success), 0.1);
  border-color: var(--color-success);
  color: #15803d;
}

.alert-error {
  background-color: rgba(var(--color-destructive), 0.1);
  border-color: var(--color-destructive);
  color: #b91c1c;
}
```

---

## Dark Mode Overrides

When the `.dark` class is applied to the root element, these values are overridden:

```css
.dark {
  --color-background: #0B0C26;
  --color-foreground: #FFFFFF;
  --color-card: #151641;
  --color-card-foreground: #FFFFFF;
  --color-card-border: rgba(255, 255, 255, 0.1);
  --color-popover: #1d1d2e;
  --color-popover-foreground: #FFFFFF;
  --color-border: rgba(255, 255, 255, 0.1);
  --color-border-hover: #7C81E8;
  --color-muted: #151641;
  --color-muted-foreground: #A0A0A0;
  --color-input-bg: rgba(255, 255, 255, 0.15);
  --color-input-border-default: rgba(255, 255, 255, 0.2);
  --color-input-border-hover: #7C81E8;
  --color-input-border-focus: #A5B4FC;
  --color-input-placeholder: #A0A0A0;
}
```

---

## Color Palette Color Codes

| Use Case | Primary | Hover | Light | Dark |
|----------|---------|-------|-------|------|
| Primary | #6366F1 | #4F46E5 | #EEF2FF | #3f408f |
| Success | #22C55E | #16A34A | rgba(34, 197, 94, 0.1) | #15803d |
| Warning | #F59E0B | #D97706 | rgba(245, 158, 11, 0.1) | #b45309 |
| Error | #EF4444 | #DC2626 | rgba(239, 68, 68, 0.1) | #b91c1c |
| Info | #3B82F6 | #2563EB | rgba(59, 130, 246, 0.1) | #1e40af |

---

## How to Customize

### Change Primary Brand Color

Edit `:root` section in `styles.css`:

```css
:root {
  --color-primary: #YOUR_HEX;
  --color-primary-hover: #DARKER_HEX;
  --color-primary-disabled: #DISABLED_HEX;
  --color-primary-light: #LIGHT_HEX;
  --freshdesk-primary: #YOUR_HEX;
  --freshdesk-primary-hover: #DARKER_HEX;
  --freshdesk-primary-light: #LIGHT_HEX;
}
```

### Change Font

```css
:root {
  --font-inter: 'Your Font Name', system-ui, -apple-system, sans-serif;
}
```

### Change Border Radius Globally

```css
:root {
  --radius: 0.5rem;     /* 8px instead of 10px */
  --radius-sm: 0.25rem; /* Adjust proportionally */
  --radius-lg: 0.75rem; /* Adjust proportionally */
}
```

### Change Spacing

```css
:root {
  --freshdesk-spacing: 10px; /* Base unit for margins/padding */
}
```

---

## Browser Compatibility

- ✅ Chrome 49+
- ✅ Firefox 31+
- ✅ Safari 9.1+
- ✅ Edge 15+
- ✅ Mobile browsers (iOS Safari, Chrome)

CSS custom properties (variables) are supported by all modern browsers.

---

**Last Updated**: March 2026  
**Design System Version**: Beyond Intelligence v1.0