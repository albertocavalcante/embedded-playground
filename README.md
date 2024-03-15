# Embedded Playground

## WSL2

### usbipd

In order to work with embedded systems on WSL2, it's needed to bind the device Serial Port on Windows to the WSL2 host.
The project that allows that is [`usbipd-win`](https://github.com/dorssel/usbipd-win).

To install it, open a new PowerShell terminal and execute `winget install usbipd`.

Once installed, list the available USB devices:

```sh
usbipd list
```

You should see an output should be similar to this:

```sh
Connected:
BUSID  VID:PID    DEVICE                                                        STATE
2-3    0d28:0204  USB Mass Storage Device, Dispositivo Serial USB (COM3), D...  Not shared
2-4    046d:c52b  Logitech USB Input Device, Dispositivo de Entrada USB         Not shared
2-5    1bcf:2a02  Integrated Webcam                                             Not shared
```

On this example, the Serial Port `BUSID` is `2-3`. Then, you must first open an elevated PowerShell promt and execute:

```sh
usbipd bind --busid 2-3
```

Then you can attach it to your WSL2 host without administrator privileges by running:

```sh
usbipd attach --wsl --busid 2-3
```

Expected output:

```txt
usbipd: info: Using WSL distribution 'Ubuntu' to attach; the device will be available in all WSL 2 distributions.
usbipd: info: Using IP address 192.168.64.1 to reach the host
```

Now, you can use the Serial Port on your WSL2 host.

**Useful Links**

- [Program your microcontrollers from WSL2 with USB support](https://blog.golioth.io/program-mcu-from-wsl2-with-usb-support/)
