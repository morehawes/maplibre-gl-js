# Your First MapLibre Map

## Adding MapLibre to Your Project

To get started with MapLibre, you can include it in your project either by adding it via a CDN link in your HTML file, or by installing it through npm if you're using a build system.

The library consists of a JavaScript file and a CSS file that styles various map elements.

### Using npm

Install the MapLibre GL JS package via [npm](https://www.npmjs.com/package/maplibre-gl).

```bash
npm install maplibre-gl
```

You can then import the MapLibre GL JS module in your project.

```html
<div id="map" style="width: 400px; height: 300px;"></div>
```

```javascript
import maplibregl from "maplibre-gl";
import "maplibre-gl/dist/maplibre-gl.css";

const map = new maplibregl.Map({
  container: "map", // container id
  style: "https://demotiles.maplibre.org/globe.json", // style URL
  center: [0, 0], // starting position [lng, lat]
  zoom: 1, // starting zoom
});
```

### Using CDN

To use MapLibre via a CDN, you can include the following tags in the `<head>` of your HTML document.

```html
<script src="https://unpkg.com/maplibre-gl@latest/dist/maplibre-gl.js"></script>
<link
  href="https://unpkg.com/maplibre-gl@latest/dist/maplibre-gl.css"
  rel="stylesheet"
/>
```

You can then initialize a map in your HTML file as follows:

```html
<div id="map" style="width: 400px; height: 300px;"></div>
<script>
  var map = new maplibregl.Map({
    container: "map",
    style: "https://demotiles.maplibre.org/style.json", // stylesheet location
    center: [-74.5, 40], // starting position [lng, lat]
    zoom: 9, // starting zoom
  });
</script>
```
