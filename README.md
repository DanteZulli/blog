# dantezulli.ar 🇦🇷

Blog personal de Dante Zulli. Hecho con [Hugo](https://gohugo.io/) + tema [Bear Cub](https://github.com/clente/hugo-bearcub).

## Comandos

| Comando | Qué hace |
|---|---|
| `hugo server -D` | Servidor local con drafts (http://localhost:1313) |
| `hugo` | Build de producción (genera `public/`) |
| `hugo --printI18nWarnings --printPathWarnings` | Build con advertencias (debug) |

## Posts / Proyectos nuevos

```bash
hugo new content blog/mi-post/index.md
hugo new content proyectos/mi-proyecto/index.md
```

Los posts nuevos arrancan como `draft = true`. Para publicarlos, pasalos a `draft = false`.  
Los proyectos pueden tener un `link` en el front matter para redirigir externo.

## Estructura

```
content/
├── _index.md              # Home
├── blog/                  # Posts
├── contacto/              # /contacto/
├── now/                   # /now/
└── proyectos/             # /proyectos/
layouts/                   # HTML templates (Bear Cub copiado acá)
assets/                    # CSS e imágenes
i18n/                      # Traducciones (es.toml)
```

## URLs

`/` · `/blog/` · `/blog/:post/` · `/proyectos/` · `/proyectos/:proyecto/` · `/contacto/` · `/now/` · `/index.xml`

## Performance

Link a [Google PageSpeed Insights](https://pagespeed.web.dev/)
