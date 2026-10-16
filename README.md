<div align="center">

# Dhaka City Graphical View
### Interactive C++ OpenGL / GLUT Computer Graphics Project

![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)
![OpenGL](https://img.shields.io/badge/OpenGL-5586A4?style=flat-square&logo=opengl&logoColor=white)
![GLUT](https://img.shields.io/badge/GLUT-event--driven%20graphics-6e7681?style=flat-square)
![Status](https://img.shields.io/badge/status-completed%20academic%20project-2ea44f?style=flat-square)

</div>

An interactive computer-graphics project representing several Dhaka-area environments with **C++**, **OpenGL**, and **GLUT**. The repository preserves the individual Airport, Uttara, and 300 Feet implementations together with a merged application that switches among the three scenes.

The project demonstrates scene composition, event-driven interaction, timed animation, weather/day-night state changes, 2D drawing, perspective rendering, and integration of independently developed graphics scenes.

## Preview

| Airport | Uttara | 300 Feet |
|---|---|---|
| ![Airport scene](View%20of%20Dhaka/Merged/Merged%20Airport.png) | ![Uttara scene](View%20of%20Dhaka/Merged/Merged%20Uttara.png) | ![300 Feet scene](View%20of%20Dhaka/Merged/Merged%20300ft.png) |

## Project snapshot

| Area | Details |
|---|---|
| Language | C++ |
| Graphics | OpenGL + GLUT / FreeGLUT |
| Integrated window | 1280 × 720 |
| Main scenes | Airport, Uttara, 300 Feet |
| Interaction | Keyboard + mouse |
| Animation | Timer/update-driven movement |
| Environment states | Weather and day/night modes |
| Main entry point | `View of Dhaka/Merged/Merged.cpp` |
| Status | Completed academic Computer Graphics project |

## Scene implementations

### 1. Airport

The Airport scene is a detailed 2D OpenGL environment containing airport terminals, runway/taxiway elements, vehicles, multiple aircraft, clouds, vegetation, lighting elements, and animated environmental effects.

Implemented interaction includes:

- sunny, overcast, and rainy weather states;
- generated raindrops with adjustable falling speed;
- animated cars, buses, aircraft, sun, clouds, and vegetation;
- mouse-controlled animation-speed changes.

### 2. Uttara

The Uttara scene uses a native **1280 × 720** 2D coordinate space. It includes buildings, roads, a lake, bridges, railway tracks, a train station, trees, lampposts, and multiple animated objects.

Animated elements include:

- cars and buses;
- train;
- boat;
- airplane;
- clouds.

The scene supports both **day** and **night** rendering modes.

### 3. 300 Feet

This repository contains **two related 300 Feet implementations**, and they should not be treated as identical programs.

#### Standalone 300 Feet experiment

`View of Dhaka/300ft/300ft .cpp`

The standalone version is a perspective/3D-style OpenGL experiment using depth testing, `gluPerspective`, camera movement, scene rotation, lighting, a moving car, clouds, sun movement, and building/parallax animation.

#### 300 Feet scene inside the merged application

The integrated 300 Feet implementation is contained directly inside `Merged.cpp`. It is a separate 2D scene built in a 160 × 90 logical coordinate space and scaled to the unified 1280 × 720 window.

It contains roads and crossings, buildings, traffic, trees, lamp posts, a traffic light, aircraft, day/night state changes, and animated vehicles.

## Unified application

The recommended portfolio/demo entry point is:

```text
View of Dhaka/Merged/Merged.cpp
```

The merged program implements a scene manager:

```text
                    ┌───────────┐
                    │  Merged   │
                    │  Program  │
                    └─────┬─────┘
                          │
              ┌───────────┼───────────┐
              │           │           │
              ▼           ▼           ▼
           Airport      Uttara     300 Feet
```

The unified update loop runs on a GLUT timer at roughly **60 FPS** and dispatches drawing, animation updates, keyboard input, and mouse input to the active scene.

Airport and the integrated 300 Feet scene use 160 × 90 logical coordinate spaces that are scaled to the 1280 × 720 unified window. Uttara is already implemented directly in 1280 × 720 coordinates.

## Controls

### Global scene selection - merged program

| Key | Action |
|---|---|
| `1` | Switch to Airport |
| `2` | Switch to Uttara |
| `3` | Switch to 300 Feet |

### Airport - merged program

| Control | Action |
|---|---|
| `s` | Sunny weather |
| `o` | Overcast weather |
| `r` | Rainy weather |
| `+` / `-` | Increase/decrease rain speed |
| Left mouse | Increase vehicle animation speed |
| Right mouse | Decrease vehicle animation speed |
| `Esc` | Exit |

### Uttara - merged program

| Control | Action |
|---|---|
| `d` | Day mode |
| `n` | Night mode |
| Left mouse | Increase animation speed |
| Right mouse | Decrease animation speed |

### 300 Feet - merged program

| Control | Action |
|---|---|
| `d` | Day mode |
| `n` | Night mode |
| Left mouse | Increase selected vehicle animation speeds |
| Right mouse | Decrease selected vehicle animation speeds |

### Standalone 300 Feet controls

| Key | Action |
|---|---|
| `Space` | Pause/resume animation |
| `a` / `d` | Rotate the scene |
| `w` / `s` | Raise/lower the camera |
| `z` / `x` | Move the camera closer/farther |
| `Esc` | Exit |

## Repository structure

```text
.
├── README.md
├── .gitignore
└── View of Dhaka/
    ├── README.md
    ├── Airport/
    │   ├── Airport.cpp
    │   ├── Airport Day.png
    │   ├── Airport Night.png
    │   └── Airport Rainy.png
    ├── Uttara/
    │   ├── Uttara.cpp
    │   ├── Uttara Day.png
    │   └── Uttara Night.png
    ├── 300ft/
    │   ├── 300ft .cpp
    │   ├── 300ft Day.png
    │   └── 300ft Night.png
    ├── Merged/
    │   ├── Merged.cpp
    │   ├── Merged Airport.png
    │   ├── Merged Uttara.png
    │   └── Merged 300ft.png
    └── Report/
        └── Project Report (1).pdf
```

## Build and run

### Linux / Ubuntu

Install a C++ compiler and FreeGLUT development package:

```bash
sudo apt update
sudo apt install g++ freeglut3-dev
```

Compile and run the merged application:

```bash
cd "View of Dhaka/Merged"
g++ Merged.cpp -o dhaka_view -lGL -lGLU -lglut
./dhaka_view
```

The standalone scene files can be compiled in the same way by replacing `Merged.cpp` with the corresponding source file.

On Windows or another platform, configure the OpenGL/GLU/GLUT linker libraries for the compiler or IDE being used.

## What this project demonstrates

- C++ graphics programming with OpenGL/GLUT
- 2D primitive composition and scene construction
- Perspective rendering and depth testing in the standalone 300 Feet experiment
- GLUT keyboard and mouse event handling
- Timer/update-driven animation
- Scene/state switching
- Day/night and weather-state transitions
- Reusable drawing functions for roads, buildings, vehicles, aircraft, vegetation, and environmental elements
- Integration of independently developed scenes into a single program

## Project team

This was a **group academic project** for **Computer Graphics, Section F, Group 06, Summer 2024-25** at American International University-Bangladesh (AIUB). The contribution percentages below are reproduced from the submitted project report rather than inferred from Git commit history.

| Contributor | Student ID | Recorded contribution |
|---|---|---:|
| **Fahad Ibne Firoz** | `23-52505-2` | 28% |
| **Md. Mahabub Al Hashan Sourov** | `23-50693-1` | 27% |
| **MD Alif Ziad Sarkar** | `23-50497-1` | 25% |
| **Md. Tauhidul Islam** | `22-49388-3` | 20% |

**Course teacher:** Dipta Justin Gomes  
**Project report submission:** 12 October 2025

The original report is preserved at [`View of Dhaka/Report/Project Report (1).pdf`](View%20of%20Dhaka/Report/Project%20Report%20(1).pdf).

## Project status

**Completed academic computer-graphics project.** The repository intentionally preserves the individual scene implementations, screenshots, submitted report, and the integrated application used to demonstrate the scenes together.

## Repository maintainer

**MD Alif Ziad Sarkar**  
BSc in Computer Science and Engineering, American International University-Bangladesh (AIUB)
