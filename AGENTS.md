# AGENTS.md - Dante's Blog

Hugo-based bilingual blog (Spanish/English) using the Bear Cub theme.

## Critical Rule: Human-Written Content

**NEVER modify, edit, rephrase, rearrange, or write any content in blog posts.**

All text in `content/blog/`, `content/projects/`, and `content/*/` directories is human-written and must remain untouched. This includes:
- Body text and paragraphs
- Titles, headings, and captions
- Blockquotes and asides
- Image alt text and descriptions

AI may assist with technical changes (front matter, templates, layouts, shortcodes, i18n) based on user input, but **never** the actual article content itself.

## Build Commands

```bash
# Development server with live reload
hugo server -D

# Production build (outputs to /public/)
hugo

# Build with drafts included
hugo --buildDrafts

# Check for broken links
hugo --printI18nWarnings --printPathWarnings

# Get help
hugo help
```

## Content Structure

```
content/           # Spanish content (es-AR, default)
content.en/        # English content (en-US)
content/blog/      # Blog posts (page bundles)
content/projects/  # Projects section
archetypes/        # Content templates
layouts/           # HTML templates
i18n/              # Translation files (en.toml, es.toml)
```

## Content Guidelines

### Front Matter (TOML)
```toml
+++
date = "YYYY-MM-DD"
draft = false  # false for published, true for drafts
title = "Post Title"
description = "SEO description"
+++
```

### File Naming
- Use kebab-case: `my-post-name/index.md`
- Each post in its own folder with `index.md` (Page Bundle)
- Images alongside content files

## Template Conventions

### Hugo Template Syntax
- Variables: `{{ .Variable }}`
- Conditionals: `{{ if condition }}...{{ end }}`
- Partial includes: `{{- partial "name.html" . -}}`
- The `-` in `{{-` trims whitespace

### Partial Files (layouts/partials/)
- snake_case naming: `custom_head.html`, `seo_tags.html`
- Each partial handles one concern
- User-overridable partials: `custom_head.html`, `custom_body.html`
- **Dynamic Social Card:** `social_card.html` generates a custom image with title, author, and date.

### Block Definitions
Use Hugo's `define` block for named sections:
```html
{{ define "title" }}Custom Title{{ end }}
{{ define "main" }}...{{ end }}
```

### Output Formats
- Default: HTML
- RSS via `{{ .OutputFormats.Get "rss" }}`
- Date formatting: `{{ .Date.Format "2006-01-02" }}` (Go's reference date)

## i18n (Internationalization)

### Translation Files (i18n/*.toml)
- TOML format with `[key]` sections and `other = "value"`
- Key naming: kebab-case with descriptive names
  - `filtering-for`, `no-posts`, `email-subject`, `email-reply`

### Usage in Templates
```html
{{ i18n "filtering-for" }}
```

### Content Translation
- Mirror directory structure in `content.en/`
- Same filenames as Spanish counterparts
- `hideUntranslated = false` shows untranslated content
- Default language: `es-AR` (Spanish - Argentina)
- Secondary language: `en-US` (English - US)

## Code Blocks

Hugo uses Chroma for syntax highlighting:
- Enable line numbers in `hugo.toml`: `lineNos = true`
- Code blocks use standard markdown triple backticks with language
- Custom rendering in `layouts/_default/_markup/render-codeblock.html`
- Highlighting styles in `assets/syntax.css`

## Hugo Shortcodes

### Available Shortcodes
- `rawhtml`: Raw HTML output
- `highlight`: Custom highlighting
- `absfigure`: Absolute positioned figures

### Usage
```markdown
{{< rawhtml >}}
<p>Raw HTML here</p>
{{< /rawhtml >}}

{{< absfigure src="image.jpg" alt="Description" >}}
```

## SEO & Meta

- Title format: `Page Title | Site Title`
- Open Graph tags via `partials/seo_tags.html`
- RSS autodiscovery in head
- `description` front matter for meta description
- **Social Card generation:** Controlled by `generateSocialCard = true` in `hugo.toml` (Params section). Requires FiraMono-Bold.ttf from Google Fonts.

## Configuration (hugo.toml)

- `baseURL = "https://www.dantezulli.ar"`
- `copyright = "Dante Zulli (CC BY 4.0)"`
- `author.name = "Dante Zulli"`
- `author.email = "dantezulli2004@gmail.com"`
- `social.linkedin = "dante-zulli"`

## Theme Parameters (hugo.toml)

- `themeStyle`: CSS theme variant (default: "original")
- `dateFormat`: Date display format ("2006-01-02")
- `hideUntranslated`: Show untranslated pages
- `madeWith`: Badge text for the footer (translatable per language)

## CSS Assets

- Main styles: `print themeStyle .css | resources.Get | minify` (uses `assets/original.css`)
- Syntax highlighting: `syntax.css | minify`
- Extra per-page: `{{ with .Params.style }}`

## Common Hugo Functions

```go
// URL helpers
.RelPermalink  // Relative permalink
.AbsPermalink  // Absolute URL

// String operations
.default "fallback"  // Default value
.lower .LinkTitle   // Lowercase
.title "text"       // Title case

// Collections
.range .GetTerms "tags"  // Iterate taxonomy terms
.with .Param          // Conditional with value
```

## Testing Changes

1. Run `hugo server -D` for live preview
2. Check for warnings: `hugo --printI18nWarnings --printPathWarnings`
3. Verify bilingual content renders correctly
4. Test RSS feed generation
5. Check mobile responsiveness

## Repository Notes

- `/public/` is gitignored (generated output)
- `/resources/_gen/` is gitignored
- Hugo extended version required for SCSS/CSS minification
- **Integrated Theme:** The Bear Cub theme code is directly integrated into `/layouts` and `/assets`. It is NOT a submodule or an external theme. All template and style modifications should be made directly in these directories.
