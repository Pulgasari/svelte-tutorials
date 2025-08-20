# Create a PWA with SvelteKit

If no directory is mentioned always the `/src` directory of the SvelteKit project directory is referenced. Also all mentioned paths are relative to it.

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

### 3. Create a Service Worker

Create a `service-worker.js` or `sw.js` file.

```js
import { build, files, prerendered, version } from '$service-worker';
import { precacheAndRoute } from 'workbox-precaching';

const precache_list = [
  ...build, ...files, ...prerendered
].map( file => ({
  url: file,
  revision: version
}));

precacheAndRoute(precache_list);
```

### 4. Enable Prerendering

Create `+page.js` in `/routes`.

```js
export const prerender = true;
```
---

## Additional Links and Infos
