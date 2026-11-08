# Conch Shell 3D Reconstruction using Photogrammetry

**A multi-view photogrammetry project using COLMAP and OpenMVS**

## 1. Project Overview

This project explores the reconstruction of a three-dimensional conch shell model from multiple photographs using photogrammetry.

Photographs captured from different viewing angles are processed to identify common visual features, estimate camera positions, and reconstruct the object's 3D geometry.

The reconstruction pipeline uses COLMAP for Structure-from-Motion (SfM) and OpenMVS for Multi-View Stereo (MVS) processing.

The objective is to create a 3D representation of the conch shell from ordinary 2D images without using a dedicated 3D scanner.

## 2. Technologies Used

| Technology | Purpose |
|---|---|
| COLMAP | Feature extraction, image matching and sparse reconstruction |
| OpenMVS | Dense point cloud and mesh reconstruction |
| MeshLab | 3D model inspection and visualization |
| Windows 10 | Development environment |

## 3. Project Workflow

The reconstruction process consists of the following stages:

1. **Image Acquisition:** Capture multiple overlapping photographs of the conch shell from different angles.
2. **Feature Extraction:** COLMAP detects distinctive visual features in each photograph.
3. **Feature Matching:** Corresponding features are identified between photographs.
4. **Sparse Reconstruction:** COLMAP estimates camera positions and creates a sparse 3D point cloud.
5. **Image Undistortion:** Images and camera parameters are prepared for dense reconstruction.
6. **COLMAP to OpenMVS Conversion:** The sparse reconstruction and undistorted images are imported into OpenMVS.
7. **Dense Reconstruction:** OpenMVS estimates additional 3D points using multiple views.
8. **Mesh Reconstruction:** A surface is generated from the dense point cloud.
9. **Texturing:** Image information is projected onto the reconstructed surface.

## 4. Software Requirements

- Windows 10 64-bit
- COLMAP
- OpenMVS
- MeshLab 

## 5. Repository Structure

```text
conch-shell-3d-reconstruction/
│
├── README.md
├── images/
│   └── original photographs
│
├── shell_project/
│   ├── database.db
│   ├── sparse/
│   ├── dense/
│   ├── scene.mvs
│   └── reconstruction outputs
│
├── results/
│   └── reconstruction screenshots
│
└── workflow/
    ├── colmap.md
    └── openmvs.md
```

## 6. Reconstruction Results

The project uses a conch shell as the reconstruction subject.

The results section includes:
- Original photographs
- COLMAP sparse point cloud
- OpenMVS dense point cloud
- Reconstructed 3D mesh
- Final textured model

## 7. Applications

Photogrammetry-based reconstruction can be applied to:

- 3D documentation of natural objects
- Digital preservation of shells and artifacts
- Object modelling
- Environmental documentation
- Terrain and landscape reconstruction

## 8. Future Scope

- Improve reconstruction completeness and surface detail.
- Experiment with different image counts and camera viewpoints.
- Evaluate reconstruction quality under varying lighting conditions.
- Extend the workflow to larger outdoor scenes and terrain mapping.

## 9. Acknowledgements

This project uses the open-source COLMAP and OpenMVS photogrammetry software.

- COLMAP: https://github.com/colmap/colmap
- OpenMVS: https://github.com/cdcseacave/openMVS
