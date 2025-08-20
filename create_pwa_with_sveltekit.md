# Create a PWA with SvelteKit

### 1. Create Manifest (`manifest.json`)

Create a `/static/manifest.json` file. 

```json
{
  "name": "ExampleSvelteApp",
  "short_name": "SvelteApp",
  "start_url": "/",
  "display": "standalone",
  "theme_color": "#DC2F2F",
  "background_color": "#FFFFFF"
```

(More infos about `manifest.json` files in general [here](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Manifest).)

### 2. Link Manifest in `<head>`

Link the Manifest file in `<head>` of the `app.html` file.

```html
<link rel='manifest' href='%sveltekit.assets%/manifest.json' />
```

---

## Additional Links and Infos
