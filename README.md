# Edge_BSP_VSCode


[SparkFun_Edge_BSP](https://github.com/sparkfun/SparkFun_Edge_BSP) with rough Visual Studio Code support on Windows.

**Only `SparkFun_Edge_Project_Template` is working for now**

# Associated Documentation
* **[Edge Board Hookup Guide](https://learn.sparkfun.com/tutorials/sparkfun-edge-hookup-guide)** - Basic hookup guide for the SparkFun Edge.
* **[Software Development Kit (SDK) Setup Guide](https://learn.sparkfun.com/tutorials/using-sparkfun-edge-board-with-ambiq-apollo3-sdk)** - Software Development Kit for working with the SparkFun Edge.


## Installation

Clone or download then extract or symlink this repo into the ```SDK/boards/``` directory. 

## VS Code Usage

Follow the Sparkfun Steps for the rest of the toolchain.

- [x] Supports Windows, with Git Bash, GNU MCU Eclipse [Build Tools](https://gnu-mcu-eclipse.github.io/windows-build-tools/) and [ARM Toolchain](https://gnu-mcu-eclipse.github.io/toolchain/arm/install/) installed via [xpack](https://github.com/xpack/xpm-js). Should be very easy to change toolchain in `task.json` if needed.
- [x] Tasks for make, clean and bootloader
  - [x] Tasks autodetects users installation of ARM Toolchain, provided it is installed with xpack
- [x] Intellisense, with correct headers
  - [x] Correct defines to match Makefile
  - [x] No multiple definitions for BSP functions, as other boards are excluded.
- [ ] Find way of automatically locating toolchain for `c_cpp_properties.json` also
- [ ] Debugging with [Cortex-Debug](https://marcelball.ca/projects/cortex-debug/) and J-Link hardware
- [ ] Get TensorFlow example C complilation/debug working
  - [ ] Integrate all TensorFlow build steps in VS Code.

## Examples
This repo contains several example projects. 

* **tensorflow_demo** uses a pre-trained model to identify "yes" and "no" and blink a corresponding LED on the board. Using GPIO you could easily expand this example to control a device.  **NOT YET WORKING WITH VS CODE**

* **SparkFun_Edge_Project_Template** has a relatively easy to set up makefile with some example header files and source files included. You can copy this directory to an arbitraty location on your filesystem to begin a new project. 
  * You must provide the absolute path to the SDK root directory in the 'SDKPATH' variable
  * Also update the COM_PORT variable to match your setup
