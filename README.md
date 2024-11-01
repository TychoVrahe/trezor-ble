# Trezor BLE Gateway

Welcome to the **Trezor BLE Gateway** project! 
This repository contains the source code and instructions to build and flash the application onto the `t3w1_nrf52833` board.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
    - [Launch the nRF Shell](#launch-the-nrf-shell)
    - [Initialize the Workspace](#initialize-the-workspace)
    - [Update nRF Connect SDK Modules](#update-nrf-connect-sdk-modules)
    - [Build the Application](#build-the-application)
    - [Flash the Application](#flash-the-application)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before you begin, ensure you have met the following requirements:

- **nrfutil**: Install [nrfutil](https://www.nordicsemi.com/Products/Development-tools/nRF-Command-Line-Tools). This tool is essential for managing the nRF Connect SDK and toolchains.
- **Git**: Ensure you have Git installed for cloning repositories.

## Getting Started

Follow these steps to set up the project on your local machine.

### Launch the nRF Shell

First, launch the nRF shell using the `nrfutil` toolchain manager:

```sh
nrfutil toolchain-manager launch --shell
```

### Initialize the Workspace
Initialize your workspace for the Trezor BLE Gateway project:
```sh
west init -m https://github.com/tychovrahe/trzncs --mr main my-workspace
```

### Update nRF Connect SDK Modules

Navigate to your workspace directory and update the modules:
```sh
cd my-workspace
west update
```


### Building the Application
Build the application for the t3w1_nrf52833 board:
```sh
west build ./app -b t3w1_nrf52833
```


### Flashing the Application
Flash the compiled application onto the board:
```sh
west flash
```

## Contributing

## License
