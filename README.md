# 🍪 Biscuit Theme CSS Port

> **⚠️ Before you use:** This theme is licensed under the Biscuit License which requires proper attribution. [See license requirements](#tldr-license-requirements) before using this theme in your project.

A warm and inviting color palette designed to be easy on the eyes. Perfect for coding, designing, and creating projects that feel like a cozy afternoon with a cup of tea and a biscuit.

This is a CSS port of the [Biscuit Theme](https://github.com/Biscuit-Theme/biscuit).

## 🎨 Flavors

This CSS port provides four variants of the Biscuit Theme:

- **Biscuit Sol Dark** - Sun-soaked, vibrant dark theme
- **Biscuit Sol Light** - Sun-soaked, vibrant light theme
- **Biscuit Mar Dark** - More muted, sea-washed dark variant
- **Biscuit Mar Light** - More muted, sea-washed light variant

## 📥 Installation

1. Download the `biscuit.css` file
2. Include it in your HTML file:

```html
<link rel="stylesheet" href="path/to/biscuit.css">
```

## 🎨 Theme Usage

You have two ways to use the Biscuit themes:

### Method 1: Using Theme Classes

Theme classes can be applied to any HTML element or container:

```html
<!-- Apply theme to the body for site-wide styling -->
<body class="theme-biscuit-sol-dark">...</body>

<!-- For Biscuit Sol Light theme -->
<body class="theme-biscuit-sol-light">...</body>

<!-- For Biscuit Mar Dark theme -->
<body class="theme-biscuit-mar-dark">...</body>

<!-- For Biscuit Mar Light theme -->
<body class="theme-biscuit-mar-light">...</body>

<!-- Apply different themes to different sections -->
<div class="container">
  <section class="theme-biscuit-sol-dark">
    <h2>Dark Section</h2>
    <p>This section uses the Sol Dark theme.</p>
  </section>

  <section class="theme-biscuit-sol-light">
    <h2>Light Section</h2>
    <p>This section uses the Sol Light theme.</p>
  </section>

  <!-- Nested themes - inner elements can override parent themes -->
  <section class="theme-biscuit-mar-dark">
    <h2>Mar Dark Section</h2>
    <p>This section uses the Mar Dark theme.</p>

    <div class="theme-biscuit-mar-light">
      <h3>Nested Light Section</h3>
      <p>This div uses the Mar Light theme despite being inside a Mar Dark section.</p>
    </div>
  </section>
</div>
```

When using theme classes, you can access colors with standard variable names in the element and its children:

```css
/* Using semantic alias variables */
.my-element {
  color: var(--text);
  background-color: var(--background);
}

/* Using base color variables directly */
.my-syntax-highlight {
  --keyword-color: var(--base0E);    /* Keywords */
  --string-color: var(--base0B);     /* Strings */
  --variable-color: var(--base08);   /* Variables */
  --function-color: var(--base0D);   /* Functions */
  --comment-color: var(--base03);    /* Comments */
  --background-color: var(--base00); /* Background */
}

.my-syntax-highlight .keyword { color: var(--keyword-color); }
.my-syntax-highlight .string { color: var(--string-color); }
.my-syntax-highlight .variable { color: var(--variable-color); }
.my-syntax-highlight .function { color: var(--function-color); }
.my-syntax-highlight .comment { color: var(--comment-color); }
```

This is the recommended approach for:
- Applying a consistent theme throughout your application
- Creating theme-switching functionality
- Maintaining clean, readable CSS without long variable names
- Creating sections with different themes on the same page

### Method 2: Using Direct Theme Variables

All theme colors are also directly available at the root level with prefixed names, allowing you to use any color from any theme variant without applying theme classes:

```css
/* Using specific theme colors directly from any variant */
.element {
  color: var(--biscuit-sol-dark-text);
  background-color: var(--biscuit-mar-light-background);
}

.button {
  background-color: var(--biscuit-sol-dark-primary);
  color: var(--biscuit-mar-light-text);
  border: 2px solid var(--biscuit-mar-dark-accent);
}

/* Using specific base colors directly */
.code-block {
  color: var(--biscuit-sol-light-base0B); /* Strings from Sol Light */
  background-color: var(--biscuit-mar-dark-base01); /* Background from Mar Dark */
}
```

This approach is useful for:
- Creating mixed theme elements
- Using colors from multiple theme variants simultaneously
- Creating custom color schemes based on Biscuit colors
- For more direct control while using colors

## 🎨 Theme Structure

### Root Level Variables

Every theme color is available directly at the root level with the following naming pattern:

- Base colors: `--biscuit-[variant]-base[00-0F]`
  - Example: `--biscuit-sol-dark-base08`
  
- Semantic aliases: `--biscuit-[variant]-[purpose]`
  - Example: `--biscuit-mar-light-text`

Where `[variant]` can be:
- `sol-dark`
- `sol-light`
- `mar-dark`
- `mar-light`

And `[purpose]` can be:
- `text`
- `primary`
- `secondary`
- `background`
- `accent`

### Theme Class Variables

The standard Base16 variables (`--base00` through `--base0F`) and semantic aliases (`--text`, `--primary`, etc.) are only available when you apply one of the theme classes on the element or one of its parents. 

## 📊 Color Meaning

The Base16 colors follow these conventions:

- `base00`: Default Background
- `base01`: Lighter Background (Status bars, line numbers)
- `base02`: Selection Background
- `base03`: Comments, Invisibles, Line Highlighting
- `base04`: Dark Foreground (Used for status bars)
- `base05`: Default Foreground, Caret, Delimiters, Operators
- `base06`: Light Foreground
- `base07`: Light Background
- `base08`: Variables, XML Tags, Markup Link Text, Markup Lists
- `base09`: Integers, Boolean, Constants, XML Attributes
- `base0A`: Classes, Markup Link Url
- `base0B`: Strings, Inherited Class, Markup Code
- `base0C`: Support, Regular Expressions, Escape Characters, Markup Quotes
- `base0D`: Functions, Methods, Attribute IDs, Headings
- `base0E`: Keywords, Storage, Selector, Markup Italic
- `base0F`: Deprecated, Opening/Closing Embedded Language Tags

## 👨‍🎨 Design Philosophy

The Biscuit Theme was designed with these principles in mind:

- **☀️ As Warm as a Summer's Day**: Biscuit uses warm tones that go easy on the eyes and invoke feelings of warmth.
- **🍫 Chocolatey**: Background colors are the cornerstone of the theme, designed to be easy on the eyes as they're the colors you'll see the most.
- **🥛 Milky**: Foreground colors are chosen to comfort the eyes while reading text.

## 💝 Thanks To

- The original [Biscuit Theme](https://github.com/Biscuit-Theme/biscuit) creators for their wonderful color scheme
- [Base16](https://github.com/chriskempson/base16) for the styling guidelines

## 📝 License

This is a port of the Biscuit Theme and follows the Biscuit License.

### TL;DR License Requirements
- You **MUST** credit the Biscuit Project as the source of the color scheme in your application
- Include attribution to the Biscuit Project and link to the official repository: https://github.com/Biscuit-Theme/biscuit
- Your project must be open source
- You cannot redistribute Biscuit under other names

Please review the [LICENSE.md](./LICENSE.md) file for complete terms and conditions before using this theme.