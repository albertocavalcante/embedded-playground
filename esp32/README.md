# ESP32

## Required Software

### esptool

esptool is a command line tool to communicate with ESP32.

The official installation instructions can be found at [`Esptool.py` Quick Start](https://docs.espressif.com/projects/esptool/en/latest/esp32/#quick-start).
In summary, considering you already have Python installed, execute:

```sh
pip install esptool
```

Validate the installation by executing:

```sh
esptool.py flash_id
```

### ESP32 Toolchain

**Prerequisites**

Always make sure to check the official documentation at [Standard Setup of Toolchain for Linux](https://espressif-docs.readthedocs-hosted.com/projects/esp-idf/en/stable/get-started/linux-setup.html#standard-setup-of-toolchain-for-linux).
Modified list as of 14 March 2024, for my personal environment (dropped `git`, `python`, `python-pip` and `python-setuptools`):

```sh
sudo apt install wget flex bison gperf cmake ninja-build ccache libffi-dev libssl-dev
```

#### Get ESP-IDF

- [ESP-IDF Releases](https://github.com/espressif/esp-idf/releases)

**IDE Installation using Visual Studio Code**

I haven't tried yet, but you should refer to this [installation guide](https://github.com/espressif/vscode-esp-idf-extension/blob/master/docs/tutorial/install.md).

**Manual Installation**

Manual installation documentation for Linux can be found [here](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/linux-macos-setup.html#step-2-get-esp-idf).
For `ESP32-C3`, [refer to this link instead](https://docs.espressif.com/projects/esp-idf/en/stable/esp32c3/get-started/linux-macos-setup.html).

```sh
mkdir -p ~/esp
cd ~/esp
git clone -b v5.2.1 --recursive https://github.com/espressif/esp-idf.git esp-idf-v5.2.1
```

Installation using the script for the Fish Shell:

```sh
cd ~/esp/esp-idf-v5.2.1
./install.fish esp32,esp32c3
```

**NOTE**: Make sure also to execute `. ~/esp/esp-idf-v5.2.1/export.fish`

## Reference

- [nanoESP32-C3](https://github.com/wuxx/nanoESP32-C3)
