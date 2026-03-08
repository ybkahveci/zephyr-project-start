# Zephyr Starter Template

Personal starter template for Zephyr RTOS projects. Based on the [Zephyr Example Application](https://github.com/zephyrproject-rtos/example-application), stripped down to a clean minimal skeleton.

## Project Structure

```
├── app/                 # Application source code and config
│   ├── src/main.c       # Entry point
│   ├── CMakeLists.txt   # App build configuration
│   ├── Kconfig          # App Kconfig options
│   ├── prj.conf         # Kconfig settings
│   └── VERSION          # App version
├── boards/              # Custom board definitions
├── drivers/             # Out-of-tree drivers
├── dts/                 # Devicetree bindings
├── include/             # Public headers
├── lib/                 # Out-of-tree libraries
├── scripts/             # West extensions and custom runners
├── tests/               # Test suites
├── doc/                 # Documentation
├── zephyr/module.yml    # Zephyr module registration
├── CMakeLists.txt       # Root CMake (module entry point)
├── Kconfig              # Root Kconfig (module entry point)
└── west.yml             # West workspace manifest
```

## Usage

### Create a new project

```shell
west init -m <this-repo-url> --mr main my-project
cd my-project
west update
```

### Build

```shell
cd <project-name>
west build -b $BOARD app
```

### Flash

```shell
west flash
```

## License

Apache-2.0
