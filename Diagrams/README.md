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

## Switch power off

|||
| --     | -- |
| Timer2 | Normal mode, no clk source, TOV2=0, interrupt = wdr |

## Variable

| Name  ||
| ---   | --- |
| rx    | 768 x 16 = 12288 = MIN_RC_PULS x CPU_MHZ < PWM duty cycle < MAX_RC_PULS x CPU_MHZ = 2400 x 16 = 38400 |
| puls_high | (rx1+rx2+...+rx31) x 256 / 256 |
| puls_low | (rx1+rx2+...+rx34) x 256 / 256 |
| puls_high | puls_high >= PROGRAM_RC_PULS x CPU_MHZ = 1460 x 16 = 23360 |
| neutral | neutral = puls or neutral = puls_low / 8
| rc_duty   | rx x fwd_scale + MIN_DUTY |
