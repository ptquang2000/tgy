# Description

## Inital Start

| I/O   |                   |           |
| ---   | ---               | ---       |
| PORTB | Output nFET A,B,C | pin 2,1,0 |
| PINC  | Input             | all 8 pins|
| PORTD | Output pFET A,B,C | pin 5,4,3 |

| Timer    |                             |
| ---      | ---                         |
| Time0    | Normal mode, Internal clock |
| Time1    | No clock source             |
| Time2    | No clock source             |
| Watchdog | 16.3ms                      |

## Control Start

| INT    |                          |
| ---    | ---                      |
| INT0   | Enable on rising edge    |
| INT1   |                          |
| Timer0 |                          |
| Timer1 | Enable + Compare match A |
| Timer2 | Enable                   |
