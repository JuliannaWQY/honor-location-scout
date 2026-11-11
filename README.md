# HONOR Location Scout Map

A lightweight, GitHub Pages-ready interactive map for film-location research.

## Run locally
1. Download/unzip this folder.
2. Open `index.html` in a browser (internet connection required for map tiles and Leaflet CDN).
3. Edit the `locations` array in `index.html` to add your own locations.

## Add a location
Copy one object inside `const locations = [...]` and change:
- `id`: unique, no spaces (e.g. `black-mountain-01`)
- `name`, `province`
- `lat`, `lng`: decimal coordinates
- `landscape`, `daytime`, `altitude`
- `description`, `production`
- `images`: direct image URLs or relative paths to images in your repo

Coordinates are decimal degrees. Leaflet uses `[latitude, longitude]` when placing markers.

Example:
```js
{
  id: "my-location",
  name: "My filming location",
  province: "Guangdong",
  lat: 24.12345,
  lng: 113.12345,
  landscape: "Coast · cliffs",
  daytime: "15–20°C",
  altitude: "Approx. 100 m",
  description: "What makes the location visually interesting.",
  production: "Access, permits, crew, drone notes.",
  images: ["assets/my-location-01.jpg", "assets/my-location-02.jpg"]
}
```

## Use your own images (recommended)
Create an `assets/` folder and add image files. Then reference them as `assets/filename.jpg`.
Use images you own or have permission to use. Sample Unsplash images are placeholders and are not specific to the named Chinese locations.

## Publish on GitHub Pages
1. Create a GitHub repository (e.g. `honor-location-scout`).
2. Upload `index.html`, this README and your `assets/` folder.
3. In GitHub: **Settings → Pages**.
4. Choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
5. GitHub will provide a Pages URL after deployment.

## Map credits / usage
Map library: Leaflet (BSD-2-Clause). Map tiles/data: OpenStreetMap contributors.
The page displays OSM attribution. Standard OSM tiles are intended for normal interactive browsing, not bulk downloads or offline tile packaging. For a larger production audience, consider a dedicated tile provider and review its terms.
