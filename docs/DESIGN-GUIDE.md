# Design guide

This is the shared visual reference for the travel agency website. The values
are provisional and can be changed later, but new work should use these tokens
instead of inventing separate colors, font sizes, or spacing values.

## Design direction

The visual style should feel welcoming, reliable, and travel-focused:

- Use generous whitespace and clear content hierarchy.
- Use blue as the trustworthy primary color.
- Use teal for travel, nature, and secondary highlights.
- Use warm amber sparingly for calls to action and important emphasis.
- Prefer readable layouts over crowded screens.

## Color palette

| Token | Hex value | Use |
|---|---|---|
| `--color-primary` | `#2563EB` | Main links, primary buttons, active navigation |
| `--color-primary-dark` | `#1D4ED8` | Hover and focus state for primary controls |
| `--color-secondary` | `#0F766E` | Secondary buttons, travel highlights, tags |
| `--color-secondary-dark` | `#115E59` | Hover and focus state for secondary controls |
| `--color-accent` | `#F59E0B` | Featured tour labels and small attention highlights |
| `--color-background` | `#F8FAFC` | Overall page background |
| `--color-surface` | `#FFFFFF` | Cards, forms, panels, and navigation surfaces |
| `--color-text` | `#1E293B` | Main body text and headings |
| `--color-text-muted` | `#64748B` | Supporting text and descriptions |
| `--color-border` | `#E2E8F0` | Input borders, dividers, and card outlines |
| `--color-success` | `#16A34A` | Confirmed or successful states |
| `--color-warning` | `#D97706` | Pending states and warnings |
| `--color-danger` | `#DC2626` | Errors, destructive actions, and cancellations |

When CSS work begins, define these values in `:root` in
`css/style.css`. Do not use pure black for normal text or bright colors for
large backgrounds.

## Typography

### Font family

Use this stack unless the team later chooses a hosted font:

```css
font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont,
  "Segoe UI", sans-serif;
```

The fallback fonts keep the website usable if an external font cannot load.

### Type scale

| Element | Size | Weight | Line height |
|---|---:|---:|---:|
| Page title (`h1`) | `2.25rem` | `700` | `1.15` |
| Section title (`h2`) | `1.75rem` | `700` | `1.2` |
| Subsection title (`h3`) | `1.25rem` | `600` | `1.3` |
| Body text | `1rem` | `400` | `1.6` |
| Small text | `0.875rem` | `400` | `1.5` |
| Button and label text | `0.9375rem` | `600` | `1.2` |

Use sentence case for headings and buttons. Avoid all-caps text except for
short status labels.

## Spacing system

Use multiples of `4px` so layouts remain consistent:

| Token | Value | Typical use |
|---|---:|---|
| `--space-1` | `4px` | Icon-to-text gaps and tiny adjustments |
| `--space-2` | `8px` | Label-to-input and compact gaps |
| `--space-3` | `12px` | Card content gaps |
| `--space-4` | `16px` | Default component spacing |
| `--space-5` | `20px` | Form groups and small sections |
| `--space-6` | `24px` | Card padding and related content |
| `--space-8` | `32px` | Section content gaps |
| `--space-10` | `40px` | Large component spacing |
| `--space-12` | `48px` | Section separation |
| `--space-16` | `64px` | Major page sections |

Recommended page structure:

- Main content max width: `1120px`
- Horizontal page padding: `16px` on mobile, `24px` on larger screens
- Section spacing: `48px` to `64px`
- Card grid gap: `24px`
- Form field gap: `16px`

## Layout and components

### Navigation

- Keep the main navigation visible and consistent across public pages.
- Use the primary color for the active link.
- Keep links easy to scan and provide enough spacing for touch input.

### Buttons

- Use a filled primary button for the main action, such as **Book this tour**.
- Use a secondary or outlined button for less important actions.
- Keep button height at least `44px`.
- Use consistent horizontal padding of `16px` to `24px`.
- Make disabled buttons visibly inactive.

### Tour cards

Each tour card should use the same order:

1. Tour image
2. Destination or category
3. Tour title
4. Short description
5. Price or key information
6. Main action button

Use a white surface, a subtle border, a moderate radius, and a small shadow.
Do not hide essential tour information only in hover effects.

### Forms

- Place a visible label above every input.
- Keep related fields together.
- Show validation messages next to the relevant field.
- Use a clear success or error message after submission.
- Do not remove focus outlines without providing an equally visible replacement.

### Status labels

Use the semantic status colors consistently:

- Confirmed: success green
- Pending: warning amber
- Cancelled or invalid: danger red

Always include text with a status color so meaning is not communicated by color
alone.

## Borders, radius, and shadows

| Token | Value | Use |
|---|---|---|
| `--radius-sm` | `6px` | Inputs, small labels, and compact controls |
| `--radius-md` | `12px` | Cards, forms, and panels |
| `--radius-lg` | `20px` | Hero sections and prominent feature areas |
| `--shadow-sm` | `0 2px 8px rgb(15 23 42 / 0.08)` | Cards and small surfaces |
| `--shadow-md` | `0 8px 24px rgb(15 23 42 / 0.12)` | Featured panels and menus |

Use shadows lightly. Borders are preferred when many cards appear together.

## Responsive behavior

Use the following starting breakpoints in `css/responsive.css`:

| Name | Width | Expected behavior |
|---|---:|---|
| Mobile | below `640px` | One-column content, stacked forms, compact navigation |
| Tablet | `640px` to `1023px` | Two-column card grids where space allows |
| Desktop | `1024px` and above | Full navigation and multi-column layouts |

Design mobile-first, then add larger-screen rules. No page should require
horizontal scrolling.

## Accessibility basics

- Maintain readable contrast between text and backgrounds.
- Use semantic HTML elements.
- Add meaningful `alt` text to informative images.
- Keep keyboard focus visible.
- Do not use color as the only way to communicate status.
- Keep interactive targets at least `44px` high where practical.

## Before opening a pull request

- Check the page at approximately `375px`, `768px`, and `1440px`.
- Confirm that the page uses the shared color and spacing tokens.
- Check hover, focus, disabled, success, warning, and error states where relevant.
- Confirm headings, labels, links, and buttons are easy to understand.
