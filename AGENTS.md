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

# Validate build and check for issues
hugo --printI18nWarnings --printPathWarnings

# Check general help
hugo help
```

There are no traditional unit tests in this Hugo site. Validate changes by running the dev server.

## Code Style Guidelines

### HTML/Template Files (layouts/)

**Indentation:** 4 spaces

**Hugo Variables and Functions:**
```html
<!-- Variables -->
{{ .Variable }}

<!-- Conditionals - use whitespace trimming - -->
{{- if condition -}}
  content
{{- end -}}

<!-- Partial includes with whitespace trimming -->
{{- partial "name.html" . -}}

<!-- .default for fallback values -->
{{ .Param "description" | default "Fallback" }}

<!-- String operations -->
{{ .Title | lower }}
{{ .Title | title }}
{{ .LinkTitle | truncate 50 }}
```

**Block Definitions:** Use Hugo's `define` block for named sections:
```html
{{ define "title" }}Custom Title{{ end }}
{{ define "main" }}...{{ end }}
```

**Output Formats:**
```html
<!-- RSS autodiscovery -->
{{ with .OutputFormats.Get "rss" -}}
  <link rel="{{ .Rel }}" type="{{ .MediaType.Type }}" href="{{ .Permalink }}" />
{{- end }}
```

### File Naming Conventions

| Type | Convention | Example |
|------|------------|---------|
| Partials | snake_case.html | `social_card.html`, `seo_tags.html` |
| Shortcodes | snake_case.html | `absfigure.html`, `rawhtml.html` |
| Layouts | snake_case.html | `baseof.html`, `single.html` |
| Content | kebab-case/ | `my-post-name/index.md` |
| CSS | kebab-case.css | `syntax.css`, `original.css` |
| i18n keys | kebab-case | `filtering-for`, `no-posts` |

### CSS (assets/)

**Indentation:** 4 spaces  
**Naming:** kebab-case selectors
**Organization:** Group related styles, use comments sparingly
```css
body {
    color: #c9d1d9;
}

a {
    color: #8cc2dd;
}
```

### TOML Front Matter

```toml
+++
date = "YYYY-MM-DD"
draft = false  # false = published, true = draft
title = "Post Title"
description = "SEO description"
tags = ["tag1", "tag2"]
+++
```

## Content Structure

```
content/              # Spanish content (es-AR, default)
content.en/           # English content (en-US)
content/blog/         # Blog posts (page bundles)
content/projects/     # Projects section
archetypes/           # Content templates
layouts/              # HTML templates
  _default/           # Base templates (baseof, single, list, rss.xml)
  partials/           # Reusable components
  shortcodes/         # Custom markdown extensions
i18n/                 # Translation files (en.toml, es.toml)
assets/               # CSS, images, fonts
```

## i18n (Internationalization)

### Translation File Format (TOML)

```toml
[filtering-for]
  other = "Filtering for"

[no-posts]
  other = "No posts yet"
```

### Usage in Templates
```html
{{ i18n "filtering-for" }}
```

### Content Translation
- Mirror directory structure in `content.en/`
- Same filenames as Spanish counterparts
- Default language: `es-AR`, Secondary: `en-US`

## Hugo Shortcodes

```markdown
{{< rawhtml >}}
<p>Raw HTML here</p>
{{< /rawhtml >}}

{{< absfigure src="image.jpg" alt="Description" >}}

{{< highlight "python" "linenos=true" >}}
code here
{{< /highlight >}}
```

## SEO & Social

- Title format: `Page Title | Site Title`
- Social cards generated via `social_card.html` when `generateSocialCard = true`
- Open Graph/Twitter cards via Hugo internal templates
- Always include `description` in front matter

## Configuration (hugo.toml)

- `baseURL`: `https://www.dantezulli.ar`
- `defaultContentLanguage`: `es`
- `enableRobotsTXT`: `true`
- Line numbers in code blocks: `markup.highlight.lineNos = true`

## Common Hugo Functions

```go
// URL helpers
.RelPermalink    // Relative permalink
.AbsPermalink     // Absolute URL

// Collections
.range .GetTerms "tags"    // Iterate taxonomy terms
.with .Param                // Conditional with value

// Date formatting (Go reference date: 2006-01-02)
{{ .Date.Format "2006-01-02" }}
```

## Testing Changes

1. Run `hugo server -D` for live preview at http://localhost:1313
2. Check for warnings: `hugo --printI18nWarnings --printPathWarnings`
3. Verify bilingual content renders correctly
4. Test RSS feed at `/index.xml`
5. Check mobile responsiveness

## Repository Notes

- `/public/` and `/resources/_gen/` are gitignored (generated output)
- Hugo **extended** version required for CSS minification
- **Integrated Theme:** Bear Cub theme code is in `/layouts` and `/assets` (NOT a submodule)
