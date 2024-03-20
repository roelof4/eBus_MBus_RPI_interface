# eBus_MBus_RPI_interface
Raspberry PI interface for eBus and M-Bus.

The interface combines a slave eBus interface and a master Mbus interface. This combination
is often present in heating systems such as gas boilers and heatpumps. For example, Vaillant
uses eBus to read and control.
The Mbus master is ideal to read heat meters, water meters and other sensors.
This interface provides power to the sensors and is thus classified as the master.
For safety purposes the eBus interface is fully galvanically shielded using optocouplers.

Both interfaces can be linked to serial (UART) ports on the Raspberry Pi. Version 4 and beyond
provide more than two UARTS and the user can select which one is used for either interface.
Older Raspberries can typically only use one UART. For these case the user can use serial to usb
cables using a separate 4-pin connector. Two are provided such that in principle the board
can be used standalone provided a 5V powersupply is present. When mounted as a HAT on the
Raspberry the 5V supply provided through the GPIO connector is used.

Note: the I2C EEPROM is optional and used for a system with automatic recognition.
