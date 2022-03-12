# Configuration of the Marlin firmware for custom Core XY printer
The printer is based on the [D-Bot printer](https://www.thingiverse.com/thing:1001065) by spauda01@thingiverse

This project is forked from the original Marlin firmware.

Click [here](https://github.com/nipfuh/D-Bot-Marlin/blob/2.0.x/README_ger.md) for the German :de: version.

## Prequisits
It is best to compile and upload this using PlatformIO with Visual Studio Code and the Auto Build Marlin extension.

### Installing Visual Studio Code
First, go to the [official VS Code Website](https://code.visualstudio.com/) and install the latest version of VS Code for your operating System.

### Installing needed extensions
After you have installed VS Code, you need to install some extensions in order to compile and upload the firmware.

To do this, open VS Code and select the extensions section on the left.

![extension section](https://github.com/nipfuh/D-Bot-Marlin/blob/2.0.x/compile_doc/extension_section.png?raw=true)

In the search bar, search for "auto build marlin" and select the extension `Auto Build Marlin` by `Marlin Firmware`

Click on `Install`.

![Auto Build Marlin install](https://github.com/nipfuh/D-Bot-Marlin/blob/2.0.x/compile_doc/auto_build_marlin.png?raw=true)

VS Code will then install all needed extensions, including PlatformIO.

Finally, restart VS Code to make the changes take effect.

_Note: It is possible that you need to install the python3-venv package when you are using Ubuntu. VS Code will prompt you for it during the installation, if necessary_

## The Firmware

### Downloading and opening the project

On this page, go to the right. Under releases, select the newest release and download the attached zip file.
Extract the zip file into a folder of your choice.

Next, open VS Code. Select the PlatformIO section on the left and select `Open`.

![opening the project](https://github.com/nipfuh/D-Bot-Marlin/blob/2.0.x/compile_doc/platformio_open.png?raw=true)

In the tab that opens, select `Open Project` and select the folder you just extracted.

If VS Code asks you, if you trust the folder, confirm that you do.

_Note: You need to open the parent directory of the repository, i.e. the folder that contains the `Marlin` folder._


### Compiling and uploading

Now that you have opened the project, it is time to build and upload Marlin. From the bottom toolbar, select `build`.

![building the project](https://github.com/nipfuh/D-Bot-Marlin/blob/2.0.x/compile_doc/platformio_build.png?raw=true)

PlatformIO will now try to compile Marlin and in the process download all of it's dependecies.

_Note: The first build might fail. Just click on build again and it should work._

When the build process finished successfully, you can upload the firmware. To do that, select `upload` from the bottom toolbar.

![uploading the project](https://github.com/nipfuh/D-Bot-Marlin/blob/2.0.x/compile_doc/platformio_upload.png?raw=true)

PlatformIO should automatically detect your connected Arduino and upload the firmware.

If this process finishes without any errors, your Arduino is now running Marlin and you're good to go :)

## Configuration & Options

If you want to change the name of your 3D printer or want to change any other configuration options, you have to open the file `Marlin/Configuration.h` (select it from the file explorer on the left).

### Changing the name of your 3D-Printer
To change the name, go to line 146 of aforementioned Configuration.h file and change the name that is given there.
Note that you must not change anything in that line except the name __between__ the quotes.