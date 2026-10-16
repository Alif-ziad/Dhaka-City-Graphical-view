# View of Dhaka — Source, Assets and Report

This directory contains the source code, screenshots, and submitted report for the **Dhaka City Graphical View** OpenGL/GLUT project.

## Recommended integrated entry point

```text
Merged/Merged.cpp
```

The merged application switches among three scenes:

- `Airport/` — standalone Airport implementation
- `Uttara/` — standalone Uttara implementation
- `300ft/` — standalone perspective/3D-style 300 Feet experiment
- `Merged/` — integrated application containing its own unified Airport, Uttara, and 300 Feet scene implementations

> The standalone `300ft/300ft .cpp` and the 300 Feet scene embedded inside `Merged/Merged.cpp` are related but distinct implementations. See the root README for the exact distinction and controls.

## Project report

The submitted academic report is preserved at:

```text
Report/Project Report (1).pdf
```

The report records the project as **Computer Graphics, Section F, Group 06, Summer 2024-25** with the following contributors:

- Fahad Ibne Firoz — `23-52505-2`
- Md. Mahabub Al Hashan Sourov — `23-50693-1`
- MD Alif Ziad Sarkar — `23-50497-1`
- Md. Tauhidul Islam — `22-49388-3`

Course teacher: **Dipta Justin Gomes**.

For screenshots, contribution percentages, controls, dependencies, implementation details, and build instructions, see the [root README](../README.md).
