# IBT2 BTS7960 Driver Library

This is an easy to use motor driver library made for the BTS7960 motor driver (and other motor drivers with similar pinout). 

This driver library is built for beginners as well as for more complex code as it speeds up the development process. 

## Installation

To install the library on to your IDE, click on the "Download ZIP" and download the repository as a .zip folder. After doing so, refer to the "Manual Installation" section of the following [link here](https://docs.arduino.cc/software/ide-v1/tutorials/installing-libraries)

## Usage

```c
#include <IBT.h>

// LPWM --> 6, RPMW --> 9, LEN --> 5V, REN --> 5V

IBT motor1(6, 9); // IBT motor(int LPWM, int RPWM, int LEN, int REN)

// Initializes pin 6 and 9 as LPWM and RPWM pins respectively
// If your LEN and REN are shorted to 5V you do not have include those such as the above


// If your LEN and REN are connected to digital pins, you may use the following:
// IBT motor1(6, 9, 2, 4); // LPWM --> 6, RPMW --> 9, LEN --> 2, REN --> 4

// Initializes pin 6, 9, 2 and 4 as LPWM, RPWM, LEN and REN pins respectively



void setup(){

}
void loop(){
    motor1.setSpeedLevel(5); // choose a level from -10 to 10. Negative levels will cause the motor to rotate in the opposite direction
    delay(2000);
    motor1.stop_(); // stops the motor
    delay(500);
    motor1.setRawSpeed(-100); // choose a value from -255 to 255. Negative levels will cause the motor to rotate in the opposite direction
    delay(2000);
    motor1.stop_();
}
```

### Contact

Email: mahirgored@gmail.com
