# Demo LittleFS Example
This demo is intended to help you get a feel for the working of littlefs using the esp_littlefs wrapper.

Prints "Demo LittleFs". then procedes to print some
Chip, Flash and Heap info, then we get to the actual
demo of the LittleFs library. 

(See the README.md file in the upper level 'examples' directory for more information about examples.)

## How to use example

Open your projects folder, and then clone this demo in.

```
git clone https://github.com/wreyford/demo_esp_littlefs.git
```
Make a folder components folder in the root of your demo_esp_littlefs folder created by the clone.
Make sure you open this folder in the terminal, then follow the instructions below specific to the 
esp_littlefs repository.

In your project, add this as a submodule to your `components/` directory.

```
git submodule add https://github.com/joltwallet/esp_littlefs.git
git submodule update --init --recursive
```

The library can be configured via `make menuconfig` under `Component config->LittleFS`.

Follow detailed instructions provided specifically for this example. 

Select the instructions depending on Espressif chip installed on your development board:

- [ESP32 Getting Started Guide](https://docs.espressif.com/projects/esp-idf/en/stable/get-started/index.html)
- [ESP32-S2 Getting Started Guide](https://docs.espressif.com/projects/esp-idf/en/latest/esp32s2/get-started/index.html)


## Example folder contents

The project **demo_littlefs** contains one source file in C language [demo_littlefs.c](main/demo_littlefs.c). The file is located in folder [main](main).

ESP-IDF projects are build using CMake. The project build configuration is contained in `CMakeLists.txt` files that provide set of directives and instructions describing the project's source files and targets (executable, library, or both). 

Below is short explanation of remaining files in the project folder.

```
├── CMakeLists.txt
├── example_test.py            Python script used for automated example testing
├── main
│   ├── CMakeLists.txt
│   ├── component.mk           Component make file
│   └── hello_world_main.c
├── Makefile                   Makefile used by legacy GNU Make
└── README.md                  This is the file you are currently reading
```

For more information on structure and contents of ESP-IDF projects, please refer to Section [Build System](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-guides/build-system.html) of the ESP-IDF Programming Guide.

## Troubleshooting

* Program upload failure

    * Hardware connection is not correct: run `idf.py -p PORT monitor`, and reboot your board to see if there are any output logs.
    * The baud rate for downloading is too high: lower your baud rate in the `menuconfig` menu, and try again.

## Technical support and feedback

Please use the following feedback channels:

* For technical queries, go to the [esp32.com](https://esp32.com/) forum
* For a feature request or bug report, create a [GitHub issue](https://github.com/espressif/esp-idf/issues)

We will get back to you as soon as possible.
