# Dhaka City Graphical View

Interactive **C++ OpenGL/GLUT** computer-graphics project representing several Dhaka locations and combining them into one scene-driven application.

## Included scenes

- Airport
- Uttara
- 300 Feet Road
- Merged application switching between the scenes

The repository also includes screenshots for different scene states and a project report.

## Main implementation

The combined program is:

```text
View of Dhaka/Merged/Merged.cpp
```

It uses a 1280×720 rendering space, OpenGL/GLUT drawing, scene-specific update functions, and keyboard/mouse event handlers.

## Build and run on Linux

Install a C++ compiler and FreeGLUT development package, then run:

```bash
cd "View of Dhaka/Merged"
g++ Merged.cpp -o dhaka_view -lGL -lGLU -lglut
./dhaka_view
```

If your platform uses different OpenGL/GLUT library names, adjust the linker flags accordingly.

## Repository contents

```text
View of Dhaka/
├── 300ft/
├── Airport/
├── Uttara/
├── Merged/
└── Report/
```

## Tech

- C++
- OpenGL
- GLUT / FreeGLUT
- Event-driven keyboard and mouse interaction

## Author

MD Alif Ziad Sarkar — CSE, American International University-Bangladesh (AIUB)
