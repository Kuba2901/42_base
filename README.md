# 42_base

This repository is a GitHub template for setting up a **42 School development environment** on macOS using **DevContainers** and **Docker**. It provides a pre-configured Linux environment with essential settings for **C / C++ development** and debugging.

## Features

- **DevContainer support**: Run a full Linux development environment inside VS Code using the `.devcontainer` setup.
- **Docker-based Linux environment**: Allows running and testing code in a consistent Linux environment on macOS.
- **Pre-configured settings for C / C++**:
  - Compiler configurations for **GCC/Clang**.
  - Formatting and linting tools.
  - Debugger setup for **GDB / LLDB**.
- **VS Code Integration**:
  - DevContainer includes useful extensions.
  - Debugging configurations for seamless development.
  
## Getting Started

### Prerequisites

1. **Docker** installed on your system ([Install Docker](https://docs.docker.com/get-docker/)).
2. **VS Code** with the **DevContainers extension** ([Install VS Code](https://code.visualstudio.com/) and [DevContainers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)).

### Setup

1. **Create a new repository using this template**:
   - Click the "Use this template" button on the GitHub repository page.
   - Create your own repository from this template.

2. **Clone your new repository**:
   ```sh
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

3. **Open in VS Code**:
   ```sh
   code .
   ```

4. **Reopen in DevContainer**:
   - When prompted, click "Reopen in Container."
   - If not prompted, open the command palette (`Cmd + Shift + P`) and select `Dev Containers: Reopen in Container`.

5. **Start coding** inside a fully configured Linux environment!

## Included Configurations

### DevContainer (`.devcontainer`)
- **Base Image**: Debian-based container with necessary development tools.
- **Pre-installed tools**:
  - `gcc`, `clang`, `make`, `gdb`, `lldb`, `valgrind`
  - `vim`, `nano`, `git`
  - VS Code extensions for **C/C++ debugging and formatting**.

### Docker (`Dockerfile`)
- **Base Image**: `debian:bullseye-slim` for a smaller footprint.
- **Pre-installed tools**:
  - `build-essential`, `libreadline-dev`, `valgrind`, `make`, `gdb`, `git`
  - Cleans up package lists to reduce image size.
- **Working Directory**: `/app` where project files are stored.
- **Benefits**:
  - Provides a lightweight and isolated Linux environment.
  - Ensures dependency consistency across different machines.
  - Eliminates compatibility issues between macOS and Linux development setups.

### C / C++ Settings
- `.vscode/settings.json`: Pre-configured settings for formatting, linting, and debugging.
- `.vscode/launch.json`: Debugger configuration for running C / C++ projects.

## Contributing
If you find any issues or want to improve the setup, feel free to open an issue or submit a pull request.

## License
This project is open-source and available under the [MIT License](LICENSE).

