# Arduino Closed-Loop Distance PID Control (Robot Tour)

An Arduino-based autonomous robot control script designed for the **Science Olympiad Robot Tour** event. It utilizes quad encoders, a proportional-derivative (PD) distance tracking loop, and automated stall detection to navigate and stop at a precise target point.

## Features
- **Precise Odometry:** Calculates traveled distance in feet (or easily converted to cm/inches) using configurable wheel diameters and pulses-per-revolution (PPR) encoder specs to optimize distance scoring.
- **PID Distance Controller:** Smoothly accelerates and decelerates the vehicle to approach the target distance threshold without overshooting.
- **Safety Features:** Built-in stall detection that halts motors safely if movement drops near the target zone, avoiding penalties.
- **Interrupt-Driven Encoders:** Uses hardware interrupts on quadrature encoders to prevent missed ticks during movement.

## Pin Mapping

| Component | Pin | Arduino Function |
| :--- | :--- | :--- |
| **Motor A Enable** | 10 | PWM Speed Control |
| **Motor A In 1** | 9 | Direction 1 |
| **Motor A In 2** | 8 | Direction 2 |
| **Motor B Enable** | 11 | PWM Speed Control |
| **Motor B In 3** | 12 | Direction 1 |
| **Motor B In 4** | 13 | Direction 2 |
| **Encoder Left A** | 2 | Interrupt Pin (RISING) |
| **Encoder Left B** | 3 | Direction Pin |
| **Encoder Right C** | 4 | Interrupt Pin (RISING) |
| **Encoder Right D** | 7 | Direction Pin |

## Getting Started
1. Clone or download this repository.
2. Open `Arduino-ClosedLoop-Distance-PID.ino` in the Arduino IDE.
3. Verify your hardware pin connections match the table above, adjust the wheel diameter and PPR constants to match your specific drivetrain build, and upload the sketch to your microcontroller.
