# Create a PWA with SvelteKit

### 1. manifest.json

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

(More infos about `manifest.json` filesin general [here](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Manifest).)
