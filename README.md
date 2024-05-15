# OpenGL Testing

This project is used to learn OpenGL on macOS. My goal is to learn and use Metal, and I think OpenGL is a nice stepping stone from 0 knowledge to some.

## Installation:

1. install [homebrew](https://brew.sh/)

2. using brew, install glfw, cmake, make
```bash
brew install glfw cmake make
```

3. Build
  a. using cmake and make
    ```bash
    cmake . && make
    ```

  b. Or using an inline command
    ```bash
    g++ main.cpp -o app -std=c++17 -framework Cocoa -framework OpenGL -framework IOKit -framework QuartzCore -lglfw3
    ```

4. Run with `./app`
