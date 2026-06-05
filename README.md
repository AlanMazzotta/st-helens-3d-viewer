# Mt. St. Helens — 3D Print Progression

**GEO 267 | Portland Community College | 2026**

An interactive 3D viewer displaying a progression of terrain models of Mt. St. Helens derived from USGS survey epochs spanning 1952 through the 1980s. The models document how the summit and crater changed following the May 18, 1980 eruption and the effect of the geomorphic processes that followed.

## Live Viewer

[https://AlanMazzotta.github.io/st-helens-3d-viewer](https://AlanMazzotta.github.io/st-helens-3d-viewer)

## Embedding in ArcGIS StoryMaps

Paste the following iframe into a StoryMap embed block:

```html
<iframe
  src="https://AlanMazzotta.github.io/st-helens-3d-viewer/model.html"
  width="100%"
  height="600px"
  frameborder="0"
  allowfullscreen>
</iframe>
```

## About the Models

Five mesh objects are arranged chronologically, each colored to match the hex code of the filament used for the physical 3D print (or the distinguishing color applied in Blender). Together they allow direct visual comparison of summit and crater geometry across survey epochs.

| Epoch | Notes |
|-------|-------|
| 1952  | Pre-eruption baseline |
| 1980  | Post-eruption collapse |
| 1981+ | Dome growth and recovery |

## Data & Processing

- **Source:** [USGS ScienceBase](https://www.usgs.gov/tools/sciencebase)
- **GIS processing:** QGIS
- **3D modeling:** Blender 5.1.2
- **Export format:** Draco-compressed glTF 2.0 binary (`.glb`)
- **Print slicing:** PrusaSlicer

## Technical Stack

| Component | Details |
|-----------|---------|
| 3D viewer | [model-viewer](https://modelviewer.dev/) v3.4.0 (Google) |
| Hosting | GitHub Pages (HTTPS) |
| Compression | Draco level 10, position quantize 10, normals 8 |
| Web server | GitHub Pages |

## Controls

| Action | Result |
|--------|--------|
| Click + drag | Orbit |
| Scroll / pinch | Zoom |
| Auto-rotate | Starts after 3 s idle |

## Repository Structure

```
/
├── index.html          # Narrative landing page
├── model.html          # Standalone viewer (iframe target)
└── Line_up_Draco.glb   # Draco-compressed 3D model
```

## Course Context

Created for GEO 267 at Portland Community College as part of a project documenting the geomorphic evolution of Mt. St. Helens through physical 3D prints derived from USGS digital elevation data.
