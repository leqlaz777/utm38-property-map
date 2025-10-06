# UTM38 Property Map — Polygon Editor

A **single-page web application** to visualize and edit property polygons using **UTM Zone 38N coordinates (Easting/Northing)**. The app converts UTM coordinates to WGS84 and displays the property shape on a **satellite map**. Area and perimeter are calculated in meters.

---

## Features

- Add polygon points using **Easting (X)** and **Northing (Y)** in **UTM Zone 38N (EPSG:32638)**.
- **Draggable markers** on the map update the coordinates automatically.
- **Reorder points** via drag-and-drop in the list.
- Polygon is always **closed** (first and last points connected).
- **Live stats**:
  - Number of points
  - Perimeter (meters)
  - Area (m²)
- **Import / Export JSON** in UTM coordinates.
- **Clear all points** with a single click.
- **Responsive design** with modern glassy panel and ESRI World Imagery satellite map.

---

## Usage

1. Open [`index.html` in a modern web browser](https://leqlaz777.github.io/utm38-property-map/).
2. Enter **Easting (X)** and **Northing (Y)** coordinates in meters and click **Add**.
3. Drag points in the list to reorder — the polygon updates automatically.
4. Drag markers on the map to update the corresponding coordinates.
5. Use **Import JSON** to load points or **Export JSON** to copy your polygon data.
6. Clear all points with the **Clear** button.

---

## Coordinate System

- **Input / Export**: UTM Zone 38N (EPSG:32638), Easting/Northing in meters.
- **Map display**: Converted to **WGS84 (latitude/longitude)** for correct overlay on satellite imagery.
- **Area / Perimeter**: Computed using UTM coordinates for accurate metric measurements.

---

## Dependencies

- [Leaflet.js](https://leafletjs.com/) — Interactive maps.
- [Proj4.js](https://proj4js.org/) — Coordinate transformations (UTM ↔ WGS84).
- ESRI World Imagery tiles (satellite view).

All dependencies are loaded via CDN — no build tools required.

---

## Example JSON for Import

```json
[
  [492000, 4470000],
  [492500, 4470100],
  [492600, 4470200]
]
```
