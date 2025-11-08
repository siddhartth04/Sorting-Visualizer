 # Sorting Visualizer (C++ / SDL2)

A real-time visualization tool for classic sorting algorithms built using **C++17** and **SDL2**.  
Watch how arrays get sorted step-by-step with smooth animations and color highlights.

##   Features
- Sorting algorithms implemented:  
  **Selection**, **Insertion**, **Bubble**, **Merge**, **Quick**, and **Heap (in-place)**
- Color-coded comparisons and swaps  
- Fixed number of bars (default 130)  
- Simple key controls for switching algorithms  
- Smooth animation speed tuned via `SDL_Delay`

##   Controls
| Key | Action |
|:----|:--------|
| `0` | Generate new random list |
| `1` | Selection Sort |
| `2` | Insertion Sort |
| `3` | Bubble Sort |
| `4` | Merge Sort |
| `5` | Quick Sort |
| `6` | Heap Sort |
| `q` | Exit program |

> ⚠️ Avoid pressing new keys until the current sort finishes — otherwise visuals may lag.

##    Build & Run

### Linux (Ubuntu/Debian)
```bash
sudo apt update
sudo apt install build-essential libsdl2-dev
g++ -std=c++17 -O2 "Sorting Visualizer.cpp" -lSDL2 -o sorting_visualizer
./sorting_visualizer
```

### macOS (Homebrew)
```bash
brew install sdl2
g++ -std=c++17 -O2 "Sorting Visualizer.cpp" $(sdl2-config --cflags --libs) -o sorting_visualizer
./sorting_visualizer
```

### Windows (MSYS2 MinGW)
```bash
pacman -S --needed mingw-w64-ucrt-x86_64-gcc mingw-w64-ucrt-x86_64-SDL2
g++ -std=c++17 -O2 "Sorting Visualizer.cpp" -o SortingVisualizer.exe \
  -lmingw32 -lSDL2main -lSDL2
./SortingVisualizer.exe
```

## ⚙️ Configuration
Modify the constants near the top of the source file:
```cpp
const int SCREEN_WIDTH  = 910;
const int SCREEN_HEIGHT = 750;
const int arrSize  = 130;  // number of bars
const int rectSize = 7;    // bar width
```
Adjust `SDL_Delay(...)` inside algorithms to speed up or slow down the animation.

##   Algorithms Implemented
- **Selection Sort** – find minimum each pass  
- **Insertion Sort** – build sorted prefix  
- **Bubble Sort** – repeated adjacent swaps  
- **Merge Sort** – divide and merge  
- **Quick Sort** – partition around pivot  
- **Heap Sort** – max-heap and pop maximums

##   Repository Structure
```
.
├── Sorting Visualizer.cpp   # main C++ source
└── README.md
```

 
