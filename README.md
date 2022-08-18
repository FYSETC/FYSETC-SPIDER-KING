# FYSETC-SPIDER-KING

## 1. Product introduction

10 axis industrial grade 3D printer motherboard

### Advantage

1. Replaceable control core:
   It has a replaceable control core(Named 'King' core).You can freely choose between 4xRP2040(King-R) / STM32F446(King-446) / STM32F407(King-407) / STM32H7XX(King-H7xx), and even you can make your own control core(We will open source the interface).

2. Intelligent identification of stepper driver type:
   With an additional MCU, Spider-King can identify the driver type and switch the SPI/UART channel automatically.
   This feature save you time on searching doc of how to set the jumppers, keep you away from borning setting jumppers. No longer has problems with stepper driver setting. (If you want to use this feature, you need our new stepper driver)

3. Multiple firmware support:
   It supports multiple firmwares.You can choose to use Klipper / Marlin 2.0 / Reprap Firmware / GRBL and other firmware according to your preferences and needs.

4. Industrial-grade standard design, 5000V full IO isolation:
   It provides a more secure hardware base: equiped with onboard high-power isolated power supply, and the control core is isolated from all high-voltage peripherals, including stepper motor drive, MOSFET output, high-voltage input signal, CAN bus, etc.

5. 10 way stepper motor drive support:
   Onboard 10 way stepping motor drive socket, 6x 3A max (maximum 35V), 4x 6A max (maximum 55V). Any socket supports SPI / UART mode.It has a new 6A drive design. It can drive 57 or even 86 step motors without external drive;

6. A variety of communication interfaces support:
   It supports onboard 5000V isolated CAN interface, supports wireless WI-FI interface, supports ESP32 high-speed communication module, supports multiple connection to Raspberry Pi, including UART, SPI and USB.

7. Centralized heat dissipation of heat-generating components:
   We centralized most heating components like 5V power supply, stepper driver in the middle area of the board, this area can be covered with the 12CM fan for cooling. You don't need to rack your brains to design the air duct, you can get better and more stable output performance.

8. Compatible with RRF firmware standard socket design:
   The socket layout is set according to Duet wiring and layout, which is more convenient to use the RRF. And more, we adds two DUET type fan ports which have feedback signal.

9. All Solid Capacitors: Power Section：
   It can provide more stable power supply and higher efficiency.

10. Compact Design:
    It has a very small size of 177mm*108mm, realizes multiple MOSFET outputs, and supports up to 10 stepper drivers.
