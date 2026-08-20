# 🌀 Mandelbrot Evolution & Complex Function Visualizer

An interactive 3D WebGL mathematical playground and 3D print generator for exploring the Mandelbrot set, escape-time complex dynamics, and dual-plane polynomial vector transformations $f(z)$.

Built with Three.js, WebGL, and analytical complex polynomial evaluation.

---

## 🌟 Features

### 1. ⛰️ 3D Mandelbrot Landscape & Sculpture Generator (`index.html`)
- **Iterative Terrain Evolution**: Morph seamlessly through recurrence iterations ($z_{k+1} = z_0 + z_k^2$) to watch chaotic satellite bulbs, organic lobes, and fractal valleys form in real time.
- **Watertight 3D Print `.OBJ` Exporter**:
  - Automatically exports closed, 2-manifold solid meshes with clean planar bases for FDM/SLA 3D printing.
  - **Disjoint Satellite Bridging**: Connects isolated satellite islands directly to the main body via narrow physical structural ribbons without adding any bulky outer skirt to the main cardioid.
  - **Golden Ratio Auto-Squish**: Calculates proportional height based on active fractal footprint width $\times \phi^{-1} \approx 0.618$.
- **Interactive Orbit Trajectory Inspector**: Click any point $z_0$ on the terrain to trace elevated 3D vector trajectories with future step projection and orbit dispersion metrics.

### 2. 📐 Dual-Plane Complex Vector Mapping (`complex-mapping.html`)
- **Dual $3 \times 3$ Complex Grid Planes**: Input plane $z = x + iy$ and Output plane $w = f(z) = u + iv$.
- **Analytical Polynomial Evaluator**: Evaluates expressions like $z^2$, $z^3 - z$, $z^2 - 1$, $0.5z^2 - 2z + 1.5$ in real time.
- **Sub-Region Filtering**: Isolate and explore specific mathematical domains (Unit Disc $|z| \le 1$, Unit Square $[-1,1]^2$, Real Axis, Imaginary Axis, Quadrants, or custom clicked points).
- **Customizable Vector Field**: Control point counts ($1 \times 1$ to $40 \times 40 = 1,600$ points), arrow shaft/head diameters, opacities, and phase/magnitude color heatmaps.
- **Cross-Tab State Persistence**: Automatically preserves all slider settings, formulas, and camera positions in `localStorage`.

---

## 🚀 Live Demo & GitHub Pages

To view the live web application on GitHub Pages:
1. Go to **Settings** $\to$ **Pages** in this repository.
2. Set Source to **Deploy from a branch** $\to$ **`main`** $\to$ **`/(root)`** $\to$ **Save**.
3. Visit:
   - **3D Mandelbrot Sculpture**: `https://b0ri5.github.io/mandlebrot-evoltuion/`
   - **Complex Vector Mapping**: `https://b0ri5.github.io/mandlebrot-evoltuion/complex-mapping.html`

---

## 🖨️ 3D Printing Guide (Bambu Studio / PrusaSlicer)

1. Open the visualizer, adjust desired iterations, resolution, and height, then click **Export Watertight .OBJ**.
2. Open the `.obj` file in Bambu Studio / OrcaSlicer.
3. Under the **Support** tab, check **Enable Support** and select **Tree (auto)** $\to$ **Tree Slim**.
   - *Why?* High iteration fractal steps form microscopic overhang needles and mushroom-shaped satellite tops that tree supports hold during printing with minimal (~1g) snap-away filament.
4. Slice and print!

---

## 📄 License
MIT License. Open source and free for educational and personal use.
