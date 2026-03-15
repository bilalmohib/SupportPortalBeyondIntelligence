# Beyond Intelligence - Design System Export

## Overview
This document provides the complete design system specification for Beyond Intelligence website, extracted for use in external systems like Freshdesk support portal.

---

## 1. Color Palette

### Primary Colors
- **Primary**: `#6366F1` (Indigo)
- **Primary Hover**: `#4F46E5` 
- **Primary Disabled**: `#A5B4FC`

### Background Colors
- **Background (Dark)**: `#0B0C26` (Darkest Blue)
- **Background Secondary**: `#151641` (Dark Blue)
- **Background Secondary 2**: `#07081D` (Even Darker Blue)
- **White/Light**: `#F6F6F6` (Off-white)

### Text Colors
- **Heading**: `#1d1d1d` (Very Dark Gray/Black)
- **Body Text**: `#1d1d1d` (Very Dark Gray/Black)
- **Secondary Gray**: `#9D9AA6` (Muted Grayish)
- **Input Text**: `#050620` (Dark Blue-black)
- **Radio Text**: `#232323` (Almost Black)

### Input States
- **Input Border Default**: `#E5E7EB` (Light Gray)
- **Input Border Hover**: `#9CA3AF` (Medium Gray)
- **Input Border Focus**: `#A5B4FC` (Light Indigo)
- **Input Border Error**: `#EF4444` (Red)
- **Input Placeholder**: `#9CA3AF` (Medium Gray)
- **Input Label Disabled**: `#9CA3AF` (Medium Gray)

### Additional Colors
- **Base White**: `#FFFFFF`
- **Border**: `#7C81E8` (Light Indigo)
- **Multi-select Item Background**: `#232562` (Dark Indigo)
- **Gradient CTA Section**: Linear gradient from `#07081D` to `#07081D` with `#6366F1`

### Gradients
- **CTA Section Gradient Border**: Conic gradient (180deg)
  - Teal/Green → Yellow/Gold → Brown/Red → Indigo → Purple transitions
  - Primary colors: `#14b8a6`, `#22c55e`, `#f59e0b`, `#6366f1`, `#8b5cf6`

---

## 2. Typography System

### Font Family
- **Primary Family**: `Inter` (Google Fonts)
- **Web Font Variable**: `--font-inter`
- **Font Weight Usage**: 400 (normal), 500 (medium), 600, 700 (bold)

### Typography Scales

#### Headings
| Level | Mobile | Tablet | Desktop | Weight | Line Height |
|-------|--------|--------|---------|--------|-------------|
| H1 | 28px | 32px | 52px | 700 Bold | 142% |
| H2 | 28px | 36px | 46px | 700 Bold | 142% |
| H3 | 24px | 28px | 32px | 700 Bold | 142% |
| H4 | 20px | 24px | 28px | 700 Bold | 142% |
| H5 | 20px | 20px | 24px | 700 Bold | 142% |
| H6 | 16px | 16px | 20px | 700 Bold | 142% |

#### Body Text
| Type | Size | Weight | Line Height |
|------|------|--------|------------|
| Paragraph | 15px (md) / 16px (lg) / 18px | 400 Normal | 142% |
| Small Text | 12-14px | 400 Normal | 142% |
| Button Text | 14px (sm) / 16px (lg) | 500 Medium | 1.5 |

### Line Height
- Default: `normal` (1.4)
- Improved readability: `142%` (1.42)

### Letter Spacing
- H1, H4, H5: `0%` (0)
- H2, H3, Body: `0%` (0)
- Footer Logo: `0.09em` (9% of font size)

---

## 3. Spacing System

### Base Spacing Unit
- **Unit**: 4px (based on Tailwind's rem scale)
- **Root Font Size**: 16px = 1rem

### Common Spacing Values
```
0.25rem = 4px
0.375rem = 6px
0.5rem = 8px
0.625rem = 10px
0.75rem = 12px
1rem = 16px
1.5rem = 24px
2rem = 32px
2.5rem = 40px
3rem = 48px
4rem = 64px
5rem = 80px
6rem = 96px
```

### Container & Layout
- **Max Container Width**: `1350px`
- **Container Padding** (responsive):
  - Mobile: `px-6` (24px)
  - Tablet (sm): `px-8` (32px)
  - Tablet+ (lg): `px-10` (40px)
  - Desktop (xl): `px-12` (48px)
  - Specific breakpoint (xxlg): `px-6` (revert)
  - Desktop (xlg): `px-0` (no padding)

### Section Padding Examples
- Footer Top Padding: `pt-18` → `pt-30` (72px → 120px)
- Footer Bottom Padding: `pb-6` → `pb-15` (24px → 60px)
- Main Content Gap: `gap-3` → `gap-10` (12px → 40px)

---

## 4. Border Radius

### Radius Values
- **Base Radius**: `0.625rem = 10px`
- **Radius Small**: `calc(var(--radius) - 4px) = 6px`
- **Radius Medium**: `calc(var(--radius) - 2px) = 8px`
- **Radius Large**: `var(--radius) = 10px`
- **Radius XL**: `calc(var(--radius) + 4px) = 14px`

### Component-Specific
- **Button Radius**: `rounded-lg` (8px-10px)
- **Input Radius**: `rounded-lg` (8px-10px)
- **Card Radius**: `rounded-xl` (12px)
- **CTA Section**: `20px` border-radius with `19px` inner content
- **Slider Overlay**: `rounded-[20px]` (20px)

---

## 5. Shadows & Elevation

### Shadow Definitions
- **Shadow-xs**: `0 1px 2px 0 rgba(16, 24, 40, 0.08)` (light shadow)
- **Input Focus Shadow**: `0px 0px 0px 4px #E1E1FEB2` (blue glow)
- **Input Error Shadow**: `0px 1px 2px 0px #10182814` (subtle dark shadow)

### Glow Effects
- **Pulse Glow**: Box shadow animation
  ```
  0 0 5px rgba(55, 125, 238, 0.3) → 0 0 20px rgba(55, 125, 238, 0.6), 0 0 30px rgba(55, 125, 238, 0.4)
  ```

### Button States
- **Hover Shadow**: Implicitly handled via background color change
- **Focus Shadow**: Ring of `3px` with `ring-ring/50` opacity
- **Ripple Effect**: White ripple at 60% opacity, scales from 0 to 2, duration 0.6s

---

## 6. Breakpoints

### Responsive Breakpoints
| Name | Width | Tailwind |
|------|-------|----------|
| Mobile | 320-639px | - |
| SSM | 330px | `sssm` |
| SSMD | 375px | `sssmd` |
| SM | 400px | `ssm` |
| Small | 480px | `ssmd` |
| Medium | 640px | `sm` |
| MD | 768px | `md` |
| MLG | 880px | `mllg` |
| Large | 970px | `mlg` |
| 1050px | 1050px | `lllg` |
| Medium-Large | 1150px | `llg` |
| Large+ | 1185px | `lllxg` |
| Desktop | 1200px | `lxg` |
| XL | 1280px | `xl` |
| 1350px | 1350px | - |
| XLG | 1366px | `xxlg` |
| XLG+ | 1376px | `xlsm` |
| Desktop+ | 1440px | `xlg` |
| 2XL | 1536px | `2xl` |
| 3XL | 1700px | `3xl` |
| 4XL | 1920px | `4xl` |

---

## 7. Component Specifications

### Button Component

**Variants:**
1. **Default (Primary)**
   - Background: `#6366F1`
   - Text: White
   - Hover: `#4F46E5`
   - Shadow: `shadow-xs`

2. **Outline**
   - Background: Transparent
   - Border: `border-white/30` or `border-black/30` (light mode)
   - Text: White or Black
   - Hover: Background opacity increases

3. **Secondary**
   - Background: `#F6F6F6` or similar secondary color
   - Text: `text-secondary-foreground`
   - Hover: `bg-secondary/80`

4. **Ghost**
   - Background: Transparent
   - Hover: Slight background accent

5. **Destructive**
   - Background: Red `#EF4444`
   - Text: White
   - Hover: `bg-destructive/90`

6. **Link**
   - Color: Primary indigo
   - Text decoration: Underline on hover
   - No background

**Sizes:**
- **Small**: `h-9.5` (38px), `px-3.5`, `rounded-lg`
- **Default**: `h-11.5` (46px), `px-3.5`, `rounded-lg`
- **Large**: `h-13.5` (54px), `px-3.5`, `rounded-lg`
- **Icon**: `size-10` (40px)

**Features:**
- Ripple effect on click
- Focus ring: 3px blue ring
- Icon support (start/end)
- Transitions enabled
- Disabled state: 50% opacity

### Input Component

**States:**
- **Default**: White background, gray border, 8px padding
- **Focus**: Blue border focus state with shadow glow
- **Error**: Red border with error shadow
- **Disabled**: Light gray border, disabled state styling

**Features:**
- Label support
- Placeholder text styling
- Full width, responsive padding
- Smooth transitions
- Error state indication

### Navigation Bar

**Structure:**
- Logo on left
- Nav items centered (desktop only)
- Help Center button
- Mobile menu toggle

**Styling:**
- Background: Transparent by default, can be dark/light
- Responsive padding: `py-4`
- Sticky positioning (implicit)
- Shadow on non-transparent state

### Footer

**Sections:**
1. Header: Logo + Help Center button
2. Main Grid: Multiple column layout
3. Bottom Bar: Copyright + links + social icons

**Colors:**
- Background: Dark (`#0B0C26` implied)
- Text: White
- Border: `#7C81E8` (light indigo)

**Typography:**
- Logo: 21px, bold, `font-inter`, white text
- Links: Small text, white
- Copyright: Small text, white, centered on mobile

### Form Elements

**Labels:**
- Color: Inherited or explicit
- Disabled state: `#9CA3AF`
- Size: Responsive to input

**Multi-Select:**
- Selected item background: `#232562`
- Border: Adjusts on focus

---

## 8. Dark Mode

The design system supports dark mode via `.dark` class.

**Dark Mode Color Overrides:**
- Background: Dark navy (`#0B0C26`)
- Text: Light/White
- Cards: Darker shade of primary color
- Borders: Lighter with opacity
- Inputs: Darker backgrounds with light borders

---

## 9. Animation & Transitions

### Transition Timings
- **Default Transition**: `transition-all duration-200`
- **Accordion**: `0.2s ease-out`
- **Float Animation**: `6s ease-in-out infinite`
- **Ripple Effect**: `0.6s ease-out`
- **Slider**: `0.6s cubic-bezier(0.4, 0, 0.2, 1)`

### Keyframe Animations
- **Float**: Moves up/down 10px
- **Pulse Glow**: Box shadow expansion/contraction
- **Ripple**: Scale from 0 to 2, opacity fade
- **Marquee**: Horizontal scroll
- **Accordion Down/Up**: Height collapse/expand

---

## 10. Accessibility

### Focus States
- **Focus Ring**: 3px ring with `ring/50` opacity
- **Keyboard Navigation**: Supported via outline-none + focus-visible
- **Disabled State**: 50% opacity, pointer-events-none
- **Aria Labels**: ARIA invalid states support destructive ring color

---

## 11. Variables & Tokens Reference

### CSS Custom Properties (in `globals.css`)
```css
--color-primary: #6366F1
--color-primary-foreground: White
--color-secondary-gray: #9D9AA6
--color-heading: #1d1d1d
--color-background: #0B0C26
--color-background-secondary: #151641
--color-background-secondary-2: #07081D
--color-buttonHover: #4F46E5
--color-buttonDisabled: #A5B4FC
--color-inputUnderline: #E5E7EB
--color-inputPlaceholder: #9CA3AF
--color-radio-text: #232323
--color-white-smoke: #F6F6F6
--font-inter: Inter (via next/font)
--radius: 0.625rem (10px)
--shadow-input-focus: 0px 0px 0px 4px #E1E1FEB2
--shadow-input-error: 0px 1px 2px 0px #10182814
```

---

## Implementation Guide for Freshdesk

1. **Copy `theme.css`** into Freshdesk's custom CSS section
2. **Map Freshdesk classes** to Beyond Intelligence theme using `freshdesk-theme.css`
3. **Use `theme.json`** as reference for color values and token names
4. **Test dark mode** by toggling the `.dark` class on the root element
5. **Verify button and input states** across different interaction scenarios

---

## Tools & Libraries Used
- **Next.js**: App Router with TypeScript
- **React**: 19.2.3
- **Tailwind CSS**: v4 with PostCSS
- **Radix UI**: Component primitives
- **Class Variance Authority**: Component variant management
- **Framer Motion**: Animations
- **React Hook Form**: Form management

