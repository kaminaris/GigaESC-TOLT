# Card interface footprints

Derived from the placed connectors in GigaDFN56. Coordinates, pad geometry, holes, and connector graphics are preserved; reference project and live GigaTOLT board are unchanged.

Use these motherboard footprints with matching module symbols. Pad identifiers retain their source connector, e.g. J31_1. Unnumbered J41 holes remain non-plated mechanical holes, not electrical pins.

These footprints describe the motherboard connector interface only. They do not include a validated card mechanical envelope or 3D models. Purchase three connectors for the control interface and two for the power interface; account for the depopulated HV connector separately.

## GigaControl_Card_Interface

| Original pin | Module pad | Reference net |
|---|---|---|
| J31.1 | J31_1 | +5V |
| J31.2 | J31_2 | GND |
| J31.3 | J31_3 | +3.3V |
| J31.4 | J31_4 | +3.3REF |
| J31.5 | J31_5 | POWER-STAGE-DISABLE |
| J31.6 | J31_6 | POWER-STAGE-LOCKOUT |
| J31.7 | J31_7 | MOSTEMP1 |
| J31.8 | J31_8 | IN-V |
| J31.9 | J31_9 | H1 |
| J31.10 | J31_10 | GND |
| J31.11 | J31_11 | L1 |
| J31.12 | J31_12 | GND |
| J31.13 | J31_13 | CURR1-FILTERED |
| J31.14 | J31_14 | GND |
| J31.15 | J31_15 | VSENSE1 |
| J31.16 | J31_16 | GND |
| J31.17 | J31_17 | MOSTEMP2 |
| J31.18 | J31_18 | GND |
| J31.19 | J31_19 | H2 |
| J31.20 | J31_20 | GND |
| J32.1 | J32_1 | L2 |
| J32.2 | J32_2 | GND |
| J32.3 | J32_3 | CURR2-FILTERED |
| J32.4 | J32_4 | GND |
| J32.5 | J32_5 | VSENSE2 |
| J32.6 | J32_6 | GND |
| J32.7 | J32_7 | MOSTEMP3 |
| J32.8 | J32_8 | GND |
| J32.9 | J32_9 | H3 |
| J32.10 | J32_10 | GND |
| J32.11 | J32_11 | L3 |
| J32.12 | J32_12 | GND |
| J32.13 | J32_13 | CURR3-FILTERED |
| J32.14 | J32_14 | GND |
| J32.15 | J32_15 | VSENSE3 |
| J32.16 | J32_16 | GND |
| J32.17 | J32_17 | SPI1-NSS |
| J32.18 | J32_18 | SPI1-MOSI |
| J32.19 | J32_19 | SPI1-SCK-ADC |
| J32.20 | J32_20 | SPI1-MISO-ADC2 |
| J33.1 | J33_1 | USBD+ |
| J33.2 | J33_2 | USBD- |
| J33.3 | J33_3 | SWDIO |
| J33.4 | J33_4 | GND |
| J33.5 | J33_5 | SWCLK |
| J33.6 | J33_6 | I2C2-SDA{slash}USART3-RX |
| J33.7 | J33_7 | GND |
| J33.8 | J33_8 | I2C2-SCL{slash}USART3-TX |
| J33.9 | J33_9 | HALL1-IN |
| J33.10 | J33_10 | GND |
| J33.11 | J33_11 | HALL2-IN |
| J33.12 | J33_12 | SERVO |
| J33.13 | J33_13 | HALL3-IN |
| J33.14 | J33_14 | IN-CANL |
| J33.15 | J33_15 | TEMPMOTOR-IN |
| J33.16 | J33_16 | IN-CANH |
| J33.17 | J33_17 | NRST |
| J33.18 | J33_18 | GND |
| J33.19 | J33_19 | ESP-TX |
| J33.20 | J33_20 | ESP-RX |

## GigaPower_Card_Interface

| Original pin | Module pad | Reference net |
|---|---|---|
| J41.3 | J41_3 | +VSW |
| J41.5 | J41_5 | +VSW |
| J41.13 | J41_13 | unconnected-(J41-Pin_13-Pad13) |
| J41.14 | J41_14 | unconnected-(J41-Pin_14-Pad14) |
| J41.15 | J41_15 | unconnected-(J41-Pin_15-Pad15) |
| J41.16 | J41_16 | unconnected-(J41-Pin_16-Pad16) |
| J41.17 | J41_17 | GND |
| J41.18 | J41_18 | GND |
| J41.19 | J41_19 | GND |
| J41.20 | J41_20 | GND |
| J42.1 | J42_1 | GND |
| J42.2 | J42_2 | GND |
| J42.3 | J42_3 | +12V |
| J42.4 | J42_4 | +12V |
| J42.5 | J42_5 | GND |
| J42.6 | J42_6 | GND |
| J42.7 | J42_7 | +5V |
| J42.8 | J42_8 | +5V |
| J42.9 | J42_9 | GND |
| J42.10 | J42_10 | GND |
| J42.11 | J42_11 | +3.3V |
| J42.12 | J42_12 | +3.3V |
| J42.13 | J42_13 | GND |
| J42.14 | J42_14 | GND |
| J42.15 | J42_15 | GND |
| J42.16 | J42_16 | GND |
| J42.17 | J42_17 | unconnected-(J42-Pin_17-Pad17) |
| J42.18 | J42_18 | unconnected-(J42-Pin_18-Pad18) |
| J42.19 | J42_19 | GND |
| J42.20 | J42_20 | GND |


## Matching symbols

The project-local `GigaCardInterfaces` symbol library contains both matching symbols, with footprints assigned. Every numbered electrical pad has one visible pin; unnumbered mechanical holes have none. Pins are passive because these represent connector interfaces, not an ERC model of the circuitry on the cards. NC labels identify currently unused physical contacts; add schematic no-connect flags when unused. Control pins are grouped by phase/system (left), external I/O and SPI (right), supplies (top), and ground (bottom). Power pins are grouped by HV connector (left), output rails and spare contacts (right), and ground (bottom).

Implemented in GigaTOLT: J301 replaces J31/J32/J33, and J401 replaces J41/J42. Symbols are on the Card interfaces sheet; the original connector wiring is retained with named endpoints on the root sheet. Combined footprints are staged below the existing layout for placement. Verified all 116 net connectivity groups against the original schematic (with the connector-to-module pin mapping), and checked module PCB pad nets against the exported schematic netlist. This is an interface migration, not completed PCB routing or a clean DRC sign-off. Module BOM entries must be expanded into three or two physical connectors respectively when procuring the motherboard.

