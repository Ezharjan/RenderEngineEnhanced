
# RenderEngineEnhanced

RenderEngineEnhanced is a render engine written in C++. It implements core computer graphics concepts from scratch, including 3D model loading, transformation, rasterization, lighting, and texture mapping. The project is designed for learning, experimentation, and as a foundation for further graphics research or development.

## Features

- **Software Rendering Pipeline**: Implements a full 3D rendering pipeline in software, including model loading, transformation, projection, rasterization, and shading.
- **OBJ Model Support**: Loads and renders 3D models in the OBJ format (see `assets/` for examples).
- **Texture Mapping**: Supports BMP textures for models and shadow planes.
- **Lighting**: Directional light with Lambertian shading and support for ambient, diffuse, and specular components.
- **Custom Math Library**: Includes custom vector, matrix, and color math utilities.
- **Window Management**: Native Win32 window creation and framebuffer management.
- **Configurable Rendering States**: Switch between wireframe, textured, and colored rendering modes.
- **Shadow Plane Rendering**: Renders a shadow-receiving plane with its own texture.
- **Debugging Support**: Optional debug console for development builds.

## Project Structure

- `RenderEngine/` — Main source code directory
	- `Main.cpp` — Application entry point
	- `Device.*` — Core rendering device and pipeline logic
	- `Window.*` — Window and framebuffer management
	- `ModelInfos.h`, `GeoBase.h` — Model and geometry loading utilities
	- `Math.h`, `Vector.h`, `Matrix.h` — Math utilities
	- `Light.h` — Lighting and shading
	- `Colour.h` — Color representation and operations
	- `Transform.*` — Transformation and camera logic
	- `assets/` — Example OBJ models and BMP textures

## Getting Started

### Prerequisites

- Visual Studio (2017 or later recommended)
- C++17 compatible compiler

### Build Instructions

1. Open `RenderEngine.sln` in Visual Studio.
2. Select the desired build configuration (Debug/Release).
3. Build the solution (Ctrl+Shift+B).
4. Run the project (F5 or Ctrl+F5).

### Usage

On launch, the renderer will open a window and display a 3D model loaded from the `assets/` directory (default: `Tonny.obj`).

#### Controls

- The renderer may support mouse or keyboard controls for model rotation, camera movement, or toggling rendering states (see code for details).
- To change the loaded model or texture, modify the paths in `RenderEngine/Config.h`:
	- `MODEL_PATH` for OBJ model
	- `TEXTURE_PATH` and `TEXTURE_PATH_4_SHADOWPLANE` for textures

#### Assets

- Place additional OBJ or BMP files in the `assets/` directory and update `Config.h` as needed.

## Code Overview

- **Main Loop**: See `Main.cpp` for initialization and main rendering loop.
- **Rendering**: The `Device` class handles all drawing, rasterization, and shading.
- **Model Loading**: `GeoBase.h` and `ModelInfos.h` provide OBJ parsing and model data structures.
- **Math**: All vector, matrix, and color operations are implemented in custom classes.

## Contributing

Contributions, bug reports, and suggestions are welcome! Please open an issue or submit a pull request.

## License

This project is for educational and research purposes. See source files for individual author credits.

## Credits

- Original author: Alexander Ezharjan
- See source file headers for additional contributors.

---
*This project demonstrates fundamental computer graphics techniques and is ideal for students, educators, and graphics enthusiasts who want to understand how 3D rendering works under the hood.*
