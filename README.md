# Space_Invaders_Project

## Overview
This project is a simple game demo for the TM4C123 launchpad ARM Cortex m4 microcontroller, utilizing a Nokia 5110 LCD display to render an enemy ship graphic. The code includes a few essential modules for hardware interfacing, including SysTick for timing, PLL for clock management, and basic delays. The enemy ship graphic is displayed on the LCD at the top of the screen, and the code includes data structures to define multiple enemy ship images.

### Key Features:
- Uses the TM4C123 microcontroller and a Nokia 5110 LCD for graphical output.
- The enemy ship graphics are stored in 2D arrays, defining pixel data for multiple versions of the enemy ship.
- System clock management using PLL and delay functions.
- Configured for the use of SysTick timer to handle timing delays.

## Required Hardware:
- **TM4C123 Microcontroller**: This is the core microcontroller used for processing and displaying the graphics.
- **Nokia 5110 LCD**: A graphical LCD used for rendering the game output.
- **SysTick Timer**: Utilized for handling timing delays in the system.
- **PLL Clock**: Configured to operate at the appropriate speed for the game.

## Setup Instructions:
1. **Hardware Connections**:  
   - Connect the Nokia 5110 LCD to the TM4C123 microcontroller's GPIO pins. The specific pin connections should be configured based on the wiring of the display to the microcontroller.
2. **Software Setup**:  
   - Download and include the following libraries in your project:
     - `tm4c123gh6pm.h`: This is the header for the TM4C123 microcontroller.
     - `Nokia5110.h`: For controlling the Nokia 5110 LCD.
     - `PLL.h`: For configuring the Phase-Locked Loop (PLL) system clock.
     - `SysTick.h`: For initializing and configuring the SysTick timer.
3. **Compiling the Code**:  
   - Ensure that your project is set up to include these header files.
   - Use an IDE that supports ARM Cortex-M development, such as Keil uVision or Code Composer Studio.
4. **Program the Microcontroller**:  
   - Load the code onto the TM4C123 microcontroller using your preferred programming tool (e.g., a JTAG debugger).

## Code Structure:
- **Enemy Ship Graphics**:  
   The `SmallEnemyPointA`, `SmallEnemy20PointA`, and `SmallEnemy10PointA` arrays contain pixel data for various sizes of the enemy ship.
- **Timing**:  
   The `Delay100ms()` function is used to create pauses between actions, ensuring that the display is refreshed at appropriate intervals.
- **PLL & SysTick**:  
   The system clock is managed using the PLL configuration, and timing is handled by the SysTick timer.

## How to Use:
1. When the program is running, the enemy ship will be displayed at the top of the screen.
2. The system uses a simple delay function to control how frequently the screen updates.
3. The game logic, such as movement of the enemy ship, can be further developed based on this initial setup.
