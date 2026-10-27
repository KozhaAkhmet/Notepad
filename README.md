# Notepad

A minimal Notepad-style text editor built with Qt Widgets — my first project with the Qt framework, built to learn its widget system and signal/slot architecture.

## Features

- **File:** New, Open, Save As, Exit (`on_action*_triggered` slots in `mainwindow.cpp`)
- **Edit:** Cut, Copy, Paste, Undo, Redo — all delegated straight to the central `QTextEdit` widget
- Open/Save use `QFileDialog` + `QTextStream`, with the window title updated to the current file path

## Tech Stack

- C++17, Qt Widgets (`Qt6`/`Qt5`, auto-detected)
- CMake build (`Notepad/CMakeLists.txt`)

## Build

```sh
cd Notepad
mkdir build && cd build
cmake ..
cmake --build .
```

Requires Qt (6 or 5) with the `Widgets` component installed and discoverable by CMake (e.g. via `CMAKE_PREFIX_PATH` pointing at your Qt install).
