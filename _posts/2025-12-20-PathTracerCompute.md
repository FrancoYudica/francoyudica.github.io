---
title: Path Tracer Compute
date: 2025-12-20 12:00:00 -0300
categories: [Computer graphics, tool]
tags: [
    path tracing,
    compute shader, 
    godot,
    computer graphics,
    rendering,
    c++,
    open source,
    parallel programming,
    low level programming
]
description: A compute shader based path tracer

image:
  path: /assets/path-tracer-compute/sample.png
---

# GPU Path Tracer in Godot

This project is a custom **Compute Shader-based path tracer** built from the ground up within the Godot engine. By moving the light transport calculations to the GPU, the renderer achieves photorealistic effects like global illumination, soft shadows, and true reflections through progressive accumulation.

![](/assets/path-tracer-compute/sample1.png)


### Key Features

* **Physically-Based Rendering (PBR):** A complete metallic-roughness workflow supporting:
    * **Lambertian & Metallic:** Realistic diffuse and reflective surfaces.
    * **Dielectrics:** High-fidelity glass and transparent materials using **Schlick's approximation**.
    * **Emissive Materials:** Any geometry can act as a light source within the scene.
* **Spatial Acceleration (BVH):** Implemented a **Surface Area Heuristic (SAH)** based Bounding Volume Hierarchy. The tree is built on the CPU and traversed on the GPU using a stack-based iterative algorithm, drastically reducing intersection tests for complex meshes.
* **Advanced Camera Model:** Supports **Depth of Field** with configurable aperture and focal distance, alongside **MSAA** with per-pixel jittering for clean, anti-aliased edges.
* **Environment Lighting:** Integrated support for **HDRI Skyboxes**, sampling Godot’s `PanoramaSkyMaterial` for realistic ambient lighting.

![](/assets/path-tracer-compute/sample2.png)

### Technical Implementation

The engine leverages **C++ via the GDExtension API**, allowing for a high-performance bridge between Godot’s core and custom rendering logic.

| Component | Implementation Detail |
| :--- | :--- |
| **Shading** | Barycentric interpolation for smooth vertex normals and attributes. |
| **Sampling** | PCG-based pseudo-random number generation for stratified sampling. |
| **Transparency** | Alpha masking for cutout textures; rays pass through transparent texels during intersection. |
| **Optimization** | Adjustable max-bounce depth and iterative GPU traversal. |

![](/assets/path-tracer-compute/sample3.png)

### Debug & Analysis
To optimize performance and verify accuracy, the renderer includes several specialized visualization modes:
* **BVH Heatmap:** Analyzes traversal efficiency and "hot spots" in the acceleration structure.
* **Normal & Depth Maps:** Visualizes surface orientations and scene thickness for debugging geometry.
* **Gamma Correction:** Final output is processed with proper sRGB (2.2) correction for accurate color display.

---

### Project Architecture
The project is built using **SCons** and **C++**, following the GDExtension standard. This architecture allows the path tracer to exist as a high-performance plugin that extends Godot's native capabilities without modifying the engine's source code.

