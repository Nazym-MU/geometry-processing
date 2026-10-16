# Geometry Processing

A series of notebooks where I work through classic geometry processing papers from the 1990s and 2000s. Each notebook explains the math behind the paper and reimplements its method from scratch, so you can see where every formula comes from and try it on a real mesh.

The goal is to learn geometry processing, starting from linear algebra, building each idea up step by step, and checking it against the code.

## Papers

| # | Paper | Notebook |
|---|-------|----------|
| 1 | Gabriel Taubin, *Curve and Surface Smoothing Without Shrinkage*, ICCV 1995 | `1 - Smoothing.ipynb` |

More papers will be added as the series continues.

## Setup

The notebooks use NumPy for the math, trimesh to load meshes, and Plotly for interactive 3D plots.

Everything runs on a laptop. The meshes are kept small (a few thousand vertices at most) so the matrices fit in memory as dense arrays.

## Meshes

The meshes were made in Blender and exported as Wavefront OBJ with these settings:

- Selection Only
- Triangulated Mesh
- Apply Modifiers
- UV coordinates, normals, and materials turned off
- Forward Axis Y, Up Axis Z, so coordinates match Blender's viewport

Turning off UVs and normals matters. Otherwise vertices can get split along seams on import, which breaks the neighbor structure the smoothing methods rely on.