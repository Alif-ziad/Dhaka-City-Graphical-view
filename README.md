<div align="center">

# Dhaka City Graphical View
### Interactive C++ OpenGL / GLUT Computer Graphics Project

![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)
![OpenGL](https://img.shields.io/badge/OpenGL-5586A4?style=flat-square&logo=opengl&logoColor=white)
![GLUT](https://img.shields.io/badge/GLUT-event--driven%20graphics-6e7681?style=flat-square)
![Status](https://img.shields.io/badge/status-academic%20project-blue?style=flat-square)

</div>

An interactive computer-graphics project that models several Dhaka-area environments and combines them into a single scene-switching OpenGL/GLUT application. The repository contains the individual scene implementations, a merged program, screenshots, and the project report.

## Preview

| Airport | Uttara | 300 Feet |
|---|---|---|
| ![Airport scene](View%20of%20Dhaka/Merged/Merged%20Airport.png) | ![Uttara scene](View%20of%20Dhaka/Merged/Merged%20Uttara.png) | ![300 Feet scene](View%20of%20Dhaka/Merged/Merged%20300ft.png) |

## Included scenes

### Airport

The Airport scene includes animated road traffic, aircraft/environment elements, clouds, lighting/weather changes, and rain effects.

### Uttara

The Uttara scene is a 2D city environment with buildings, roads, water/bridge elements, a train station, vegetation and several animated vehicles including cars, buses, a train, boat and airplane.

### 300 Feet Road

The 300 Feet scene uses a perspective/3D-style road environment with buildings, lighting, camera movement and animated scene objects.

### Merged application

`View of Dhaka/Merged/Merged.cpp` combines the three environments into one executable and dispatches drawing, update, keyboard and mouse events to the active scene.

## Controls

### Global scene selection in the merged program

| Key | Action |
|---|---|
| `1` | Switch to Airport |
| `2` | Switch to Uttara |
| `3` | Switch to 300 Feet |
| `Esc` | Exit where supported by the active scene |

### Airport interaction

| Control | Action |
|---|---|
| `s` | Sunny weather |
| `o` | Overcast weather |
| `r` | Rainy weather |
| `+` / `-` | Adjust rain speed |
| Left mouse | Increase animation speed |
| Right mouse | Decrease animation speed |

### Uttara interaction

| Control | Action |
|---|---|
| `d` | Day mode |
| `n` | Night mode |
| Left mouse | Increase animation speed |
| Right mouse | Decrease animation speed |

The individual 300 Feet implementation also contains camera/animation controls in addition to the merged scene behavior.

## Main implementation

```text
View of Dhaka/Merged/Merged.cpp
```

The merged program uses a **1280 × 720** rendering space and an event-driven GLUT loop with scene-specific drawing/update functions, keyboard handling, mouse input, animation timing, and OpenGL rendering primitives.

## Repository structure

```text
.
├── README.md
└── View of Dhaka/
    ├── 300ft/
    │   ├── 300ft .cpp
    │   ├── 300ft Day.png
    │   └── 300ft Night.png
    ├── Airport/
    │   ├── Airport.cpp
    │   └── scene screenshots
    ├── Uttara/
    │   ├── Uttara.cpp
    │   └── scene screenshots
    ├── Merged/
    │   ├── Merged.cpp
    │   └── merged-scene screenshots
    └── Report/
        └── Project Report (1).pdf
```

## Build and run

### Linux / Ubuntu

Install a C++ compiler and FreeGLUT development package. On Debian/Ubuntu systems, the typical dependency is:

```bash
sudo apt update
sudo apt install g++ freeglut3-dev
```

Then compile the merged program:

```bash
cd "View of Dhaka/Merged"
g++ Merged.cpp -o dhaka_view -lGL -lGLU -lglut
./dhaka_view
```

If your platform uses different OpenGL/GLUT library names or IDE configuration, adjust the linker settings accordingly.

## What this project demonstrates

- 2D and perspective OpenGL rendering
- GLUT event handling
- Keyboard and mouse interaction
- Timed animation
- Scene/state switching
- Day/night and weather state changes
- Reusable drawing routines for buildings, roads, vehicles and environmental elements
- Integration of several independently developed scenes into one application

## Project status

**Completed academic computer-graphics project.** The repository preserves both the standalone scene implementations and the integrated version used to demonstrate them together.

## Author

**MD Alif Ziad Sarkar**  
BSc in Computer Science and Engineering, American International University-Bangladesh (AIUB)
