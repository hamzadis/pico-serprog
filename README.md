# pico-serprog

This is a basic flashrom/serprog compatible SPI flash reader/writer for the Raspberry Pi Pico.

Pinout changed for easier breadboarding.

It does not require a custom version of flashrom, just drag the compiled uf2 onto your Pico and you're ready to go.

The default pin-out is:

| GPIO | Pico Pin | Function |
|------|----------|----------|
| 16   |    21    | CS       |
| 15   |    20    | SCK      |
| 14   |    19    | MOSI     |
| 17   |    22    | MISO     |

## Usage

Dump a flashchip:

```
flashrom -p serprog:dev=/dev/ttyACM0:115200,spispeed=12M -r foo.bin
```

## License

The project is based on the spi_flash example by Raspberry Pi (Trading) Ltd. which is licensed under BSD-3-Clause.

As a lot of the code itself was heavily inspired/influenced by `stm32-vserprog` this code is licensed under GPLv3.
