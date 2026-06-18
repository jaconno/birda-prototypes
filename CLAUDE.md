# Birda Prototype Library — Rules

## Back button (required on every prototype)

Every prototype HTML file must include a back button linking to `index.html`. Place it immediately before the main content (after `<body>`), before any header or status bar.

### UK Birds / mobile-style prototypes

Add to `<style>`:
```css
.back-bar { background: var(--bg); padding: 8px 16px 0; }
.back-btn { display: inline-flex; align-items: center; gap: 5px; font-size: 15px; font-weight: 500; color: var(--lime-dark); text-decoration: none; padding: 4px 0; font-family: -apple-system, sans-serif; }
.back-btn svg { width: 10px; height: 16px; }
```

Add to `<body>`:
```html
<div class="back-bar">
  <a class="back-btn" href="index.html">
    <svg viewBox="0 0 10 16" fill="none"><path d="M8 1L2 8L8 15" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
    Prototypes
  </a>
</div>
```

### Desktop / dashboard-style prototypes

Add to `<style>`:
```css
.back-bar { padding: 12px 40px 0; background: var(--bg); }
.back-btn { display: inline-flex; align-items: center; gap: 6px; font-size: 15px; font-weight: 500; color: var(--primary); text-decoration: none; font-family: var(--sans); }
.back-btn svg { width: 10px; height: 16px; }
```

Add to `<body>`:
```html
<div class="back-bar">
  <a class="back-btn" href="index.html">
    <svg viewBox="0 0 10 16" fill="none"><path d="M8 1L2 8L8 15" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
    Prototypes
  </a>
</div>
```

---

## Index page

When a new prototype is added:
1. Save the HTML file in `/Users/jack/Claude/`
2. Add a card to `index.html` — increment the stat counter and section count
3. Match the card preview style to the prototype's colour palette

## Design conventions

- **Primary colour**: blue `#1F87FE` / `#0F6FE8`
- **Background**: off-white `#F4F4EE`
- **Style guide**: Apple HIG — system fonts, rounded corners, blurred sticky nav
- **Mobile prototypes**: max-width 430px, include iOS status bar mock
- **Desktop prototypes**: full-width, responsive grid layout

## Pushing changes

```
cd /Users/jack/Claude && git add . && git commit -m "Description" && git push
```

GitHub Pages publishes automatically to: `https://jaconno.github.io/birda-prototypes/`
