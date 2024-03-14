# Embedded Playground

## WSL2

### usbipd

In order to work with embedded systems on WSL2, it's needed to bind the device Serial Port on Windows to the WSL2 host.
The project that allows that is [`usbipd-win`](https://github.com/dorssel/usbipd-win).

To install it, execute `winget install usbipd`.

**List USB Devices**

```sh
usbipd list
```

**Useful Links**

- [Program your microcontrollers from WSL2 with USB support](https://blog.golioth.io/program-mcu-from-wsl2-with-usb-support/)
