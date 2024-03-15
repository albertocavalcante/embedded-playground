# ESP32 with the Go Programming Language

## TinyGo

[TinyGo](https://github.com/tinygo-org/tinygo) is a Go compiler for microcontrollers and small single-board computers. It is a work in progress, but can compile some Go code into a binary that is 10-15x smaller than an equivalent C program.

### Installation

To install it on Ubuntu, execute the following in a `bash` terminal:

```bash
TINYGO_VERSION=0.31.2
wget https://github.com/tinygo-org/tinygo/releases/download/v${TINYGO_VERSION}/tinygo_${TINYGO_VERSION}_amd64.deb
sudo dpkg -i tinygo_${TINYGO_VERSION}_amd64.deb
rm tinygo_*_amd64.deb
```

### Usage

List available targets for ESP32

```sh
tinygo targets | grep -i esp32
```

## Reference

- [Let’s Go Embedded With ESP32](https://medium.com/vacatronics/lets-go-embedded-with-esp32-cb6bb3043bd0)
