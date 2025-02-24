---
layout: page
title: Conway's Game of Life
description: A Python QtPY implementation of Conway's Game of Life
img: assets/img/conway.png
importance: 1
category: work
related_publications: true
---

Conway's Game of Life is a cellular automaton simulation. This project features two executable versions:

- `conway_gui.py`: A simple mode for easy execution.
- `conway_gui_complex.py`: A complex mode with additional configuration options.

## Requirements ❗️
Ensure you have the following installed:

- Python
- pip

### Setup Instructions
1. Create a virtual environment:
   ```sh
   python -m venv venv
   ```
2. Activate the virtual environment:
   - On Windows:
     ```sh
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```sh
     source venv/bin/activate
     ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```

### Running the Application
For the simple mode:
```sh
python conway_gui.py
```
Check out how it looks:

{% include figure.liquid loading="eager" path="assets/img/conway_simple.gif" title="Simple Conway Mode" class="img-fluid rounded z-depth-1" %}

For the complex mode:
```sh
python conway_gui_complex.py
```

{% include figure.liquid loading="eager" path="assets/img/conway_complex.gif" title="Complex Conway Mode" class="img-fluid_customized rounded z-depth-1" %}

### Configuration Options
In `conway_gui_complex.py`, configure the following before starting:

- **Rows**: Number of matrix rows.
- **Columns**: Number of matrix columns.
- **Generations**: Number of updates for the matrix.
- **Probability**: Probability of alive cells.

To run:
1. Set matrix size and generations.
2. Click "Draw Matrix."
3. Click "Start Game."
4. Click "Stop Game" to halt execution.

## Project Structure 📦
```
conway/
├── conway.py
├── conway_gui.py
├── conway_gui_complex.py
├── animation_conway_gui.gif
├── animation_conway_gui_complex.gif
├── custom_dialog.py
├── infinity.png
├── readme.md
├── requirements.txt
└── worker.py
```

## About
This implementation of Conway's Game of Life offers both simple and complex modes with enhanced visualization using Python and QtPY. Stay tuned for future updates!
