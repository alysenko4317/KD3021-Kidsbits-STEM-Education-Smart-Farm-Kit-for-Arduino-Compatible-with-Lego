### Project 06：Temperature and Humidity Control System

![Img](./media/6-0.png)

#### 1. Description

This project introduces how to use a kidsIOT mainboard, a temperature and humidity sensor, a fan and an OLED display to build an intelligent temperature and humidity control system.

The system can measure ambient temperature and humidity and control fans to cool down and dehumidify based on demand. When the temperature or humidity exceeds the set threshold, it will automatically turn on the fan to reduce the temperature or humidity in the environment below the set value to protect the animals and plants on the farm. 

What's more, it enables to adjust the ambient temperature and humidity and display them on the OLED display.


#### 2. Components

|![Img](./media/A1.png)|![Img](./media/A11.png)|![Img](./media/A12.png)| ![Img](./media/A21.png)|![Img](./media/A20.png)|
| :--: | :--: | :--: |:--: |:--: |
|kidsIOT Mainboard×1|Motor×1|Temperature and Humidity Sensor×1|Wire×2|Battery Holder×1|
|![Img](./media/A27.png)|![Img](./media/A19.png)|![Img](./media/A34.png)|![Img](./media/A28.png) | |
|Fan×1|USB Cable×1| Temperature and Humidity System LEGO Pieces×1 | AA Battery（<span style="color: rgb(255, 76, 65);">Not provide</span>）×6 | |

![Img](./media/6-1.png)

#### 3. Assembly Steps

##### Step 1：Components Needed

![Img](./media/Z-6-1.png)

##### Step 2：Process

Process 1：

![Img](./media/Z-6-2.png)

Process 2：

![Img](./media/Z-6-3.png)

Process 3：

![Img](./media/Z-6-4.png)

Process 4：

![Img](./media/Z-6-5.png)

Complete：

![Img](./media/Z-6-6.png)

#### 4. Wiring Diagram

| Module |kidsIOT Mainboard |
| :--: | :--: |
| Temperature and Humidity Sensor |No.6 port（control pin is io23） |
|Motor|No.9 port（IN+control pin is io18，IN-control pin is io19）|

Connect the kidsIOT mainboard to your computer via USB cable, connect the external power supply and turn the DIP switch on the mainboard to ON end.

![Img](./media/6-2.png)

#### 5. OLED Display

![Img](./media/6-3.png)

##### (1). Programming Steps

###### Step 1：Description of the Building Block

![Img](./media/6-4.png)

This block is used to initialize the OLED’s width, height and an I2C address.

![Img](./media/6-5.png)

This is a command block for drawing a straight line from the initial position x0:0 y0:0 to the final position x1:32 y1:16. The number in the  block can be changed.

![Img](./media/6-6.png)

This is a command block that draws a recta with a width of 32 and a  height of 16 from the initial position x:0 y:0, the numbers can be  changed.

![Img](./media/6-7.png)

This is a command block that draws a rectangle with a width of 32 and a  height of 16 from the initial position x:0 y:0, the numbers can be  changed.

![Img](./media/6-8.png)

This is the command block that draws a circle with a radius of 8 starting from the initial position x:16 y:16.

![Img](./media/6-9.png)

This is the command block that fills a circle with a radius of 8 starting at an initial position of x:16 y:16.

![Img](./media/6-10.png)

This is the command block that draws a round rectangle with width 32,  height 16, and radius 4 starting from an initial position of x:16 y:16.

![Img](./media/6-11.png)

This is the command block that fills a round rectangle with width 32,  height 16 and radius 4 starting from initial position x:16 y:16.

![Img](./media/6-12.png)

This is the command block to draw a triangle from three positions x0:0 y0:0, x1:16 y1:0 and x2:8 y2:16.

![Img](./media/6-13.png)

This is the command block that fills the triangle between the three positions x0:0 y0:0, x1:16 y1:0 and x2:8 y2:16.

![Img](./media/6-14.png)

This is a command block for setting text size and color and background color.

![Img](media/6-15.png)

This is the command block that sets the cursor position.

![Img](./media/6-16.png)

This is a command block for setting the way of printing strings on the OLED screen. “**warp”** means newline printing, “**no-warp**” means no newline printing.

![Img](./media/6-17.png)

This is the command block to set the OLED display pattern.

![Img](./media/6-18.png)

This is the command block to clear the OLED screen.

![Img](./media/6-19.png)

This is the command block to refresh the OLED screen and display the next content.

![Img](./media/6-20.png)

This is a command block that sets strings to start scrolling in a certain direction.

![Img](./media/6-21.png)

This is the command block to set stop scrolling.

###### Step 2：Write the Program

① Initialize the OLED with width 128, height 64 and I2C address 0x78 (0x3c).

![Img](./media/6-22.png)

② Set the text size displayed on the OLED to 6x8, the text color to white and the background color to black.

![Img](./media/6-23.png)

③ OLED displays straight lines.

![Img](./media/6-24.png)

④ The OLED displays the straight line and delays 1 second.

![Img](./media/6-25.png)

⑤ The OLED displays rectangle and delays 1 second.

![Img](./media/6-26.png)

⑥ The OLED displays fill rectangle and delays 1 second.

![Img](./media/6-27.png)

⑦ The OLED displays circle and delays 1 second.

![Img](./media/6-28.png)

⑧ The OLED displays fill circle and delays 1 second.

![Img](./media/6-29.png)

⑨ The OLED displays round rectangle and delays 1 second.

![Img](./media/6-30.png)

⑩ The OLED displays fill round rectangle and delays 1 second.

![Img](./media/6-31.png)

⑪ The OLED displays triangle and delays 1 second.

![Img](./media/6-32.png)

⑫ The OLED displays fill triangle and delays 1 second.

![Img](./media/6-33.png)

⑬ The OLED displays smile face and delays 1 second.

![Img](./media/6-34.png)

⑭The OLED displays angry face and delays 1 second.

![Img](./media/6-35.png)

⑮ The OLED displays cry face and delays 1 second.

![Img](./media/6-36.png)

⑯ The OLED displays “↑” and delays 1 second.

![Img](./media/6-37.png)

⑰ The OLED displays “↓” and delays 1 second.

![Img](./media/6-38.png)

⑱ The OLED displays “←” and delays 1 second.

![Img](./media/6-39.png)

⑲ The OLED displays “→” and delays 1 second.

![Img](./media/6-40.png)

⑳ The OLED displays “❤” and delays 1 second.

![Img](./media/6-41.png)

㉑ Set the cursor position of the OLED to display the "Hello, KidsBlock" string at x:0 y:30 with a delay of 1 second.

![Img](./media/6-42.png)

㉒ Complete Program

![Img](./media/6-43.png)

##### (2). Test Result

Click![Img](./media/1-27.png) to upload the above complete code to the kidsIOT motherboard. After powering up via the external power supply, the OLED display on the kidsIOT board displays various patterns and English letters.


#### 6. Fan rotates

![Img](./media/6-45.png)

##### (1). Programming Steps

###### Step 1：Add “DC Motor” 

Tap ![Img](./media/6-46.png), click the “Actuator” module in the “Extension” , then select “**<span style="color: rgb(255, 76, 65);">DC Motor for esp32</span>**” and click ![Img](media/781.png)to return to the programming interface.

![Img](./media/6-48.png)

![Img](./media/6-49.png)

![Img](./media/6-50.png)

###### Step 2：Description of the Building Block

![Img](./media/6-51.png)

Set the high and low level states of the motor INA pin and INB pin.

![Img](./media/6-52.png)

Set the high and low level status of the motor INA pin and the analog output value of the INB pin in certain channels.
If the INA pin is in a high-level state, the smaller the INB analog output value, the faster the fan rotates; and if the INA pin is in a low-level state, the larger the INB analog output value, the faster the fan rotates.

###### Step 3：Write the Program

① The pin INA of the motor module is IO18, the level is low, the INB pin is IO19, the channel is CH0 (LT0), and the analog output value is 0, then the motor does not rotate.

![Img](./media/6-53.png)

② Set the motor pin INA to low level and the analog output value of the INB pin to different values, then the motor rotates clockwise at different speeds.

![Img](./media/6-54.png)

③ Set the motor to stop rotating for 3 seconds.

![Img](./media/6-55.png)

④ Set the motor pin INA to high level and the analog output value of the INB pin to different values, then the motor rotates anticlockwise at different speeds.

![Img](./media/6-56.png)

⑤ Set the motor to stop rotating for 3 seconds.

![Img](./media/6-57.png)

⑥ Complete Program

![Img](./media/6-58.png)

##### (2). Test Result

Click![Img](./media/1-27.png) to upload the above complete code to the kidsIOT motherboard. After powering up via the external power supply, the motor rotates clockwise at different speeds and stops for 3 seconds, and then rotates counterclockwise at different speeds and stops for 3 seconds.

#### 7. Read data from the temperature and humidity sensor

![Img](./media/6-60.png)

##### (1). Programming Steps

###### Step 1：Add “temperature and humidity sensor” 

Tap ![Img](./media/6-46.png), click the “Sensor” module in the “Extension” , then select “**<span style="color: rgb(255, 76, 65);">DHT sensor for esp32</span>**” and click ![Img](media/781.png)to return to the programming interface.

![Img](./media/6-63.png)

![Img](./media/6-64.png)

![Img](./media/6-65.png)

###### Step 2：Description of the Building Block

![Img](./media/6-66.png)

Initialize the pin and mode of the temperature and humidity sensor (dht11, dht21 or dht22).

![Img](./media/6-67.png)

Read the temperature and humidity from the temperature and humidity sensor.

###### Step 3：Write the Program

① Set the baud rate to 15200.

![Img](./media/1-68.png)

② Initialize pin IO23 of the temperature and humidity sensor, and select the dht11 mode.

![Img](./media/6-69.png)

③ The serial port prints the read temperature and humidity in the current environment every 1 second.

![Img](./media/6-70.png)

④ Complete Program

![Img](./media/6-71.png)

##### (2). Test Result

Click![Img](./media/1-27.png) to upload the above complete code to the kidsIOT mainboard. After powering up via the USB cable, click ![Img](./media/1-87.png) in the serial monitor and set the baud rate to 15200. Then the serial port prints the temperature and humidity in the current environment.

![Img](./media/6-74.png)

#### 8. Temperature and Humidity Control System

![Img](./media/6-75.png)

##### (1). Programming Steps

###### Step 1：Flow Chart

![Img](./media/6-76.png)

###### Step 2：Write the Program
①Initialize pin IO23 of the temperature and humidity sensor, and select the dht11 mode.

![Img](./media/6-77.png)

② Initialize the width, height, I2C address, text size and color as well as background color of the OLED display.

![Img](./media/6-78.png)

③ Set the strings "Temper:" and "Humid:" to be displayed on the OLED.

![Img](./media/6-79.png)

④ Define variables "**temperature**" and "**humidity**".

![Img](./media/6-80.png)

⑤ Store the read <span style="color: rgb(255, 76, 65);">temperature data</span> into the "temperature" variable. The read <span style="color: rgb(255, 76, 65);">humidity data</span> is stored in the "humidity" variable.

![Img](./media/6-81.png)

⑥  Display <span style="color: rgb(255, 76, 65);">temperature data</span> and <span style="color: rgb(255, 76, 65);">humidity data</span> at the corresponding position on the OLED.

![Img](./media/6-82.png)

⑦ Determine the temperature and humidity value in the environment detected by the temperature and humidity sensor. When the temperature is greater than 29°C, or the humidity is greater than 80%RH, the fan will be turned on.

![Img](./media/6-83.png)

⑧ Complete Program

![Img](./media/6-84.png)

##### (2). Test Result

Click![Img](./media/1-27.png) to upload the above complete code to the kidsIOT mainboard. After powering up via the external power, the OLED displays the temperature and humidity in the current environment. 

When the temperature reaches 29°C or the humidity reaches 80%RH, the motor will turn on to dissipate heat or dehumidify (the fan simulates heat dissipation and dehumidification, and the heat dissipation and dehumidification effect is average); otherwise, the motor will turn off to achieve automatic farm temperature  and humidity control effect.

![Img](./media/6-86.jpg)

#### 9. Common Problems　

##### Q1: Is the temperature and humidity sensor waterproof?

A: The sensor detects the temperature and humidity in the air, which is not waterproof. Please do not put the module into water.

##### Q2: Does the rotation of the motor cause the kidsIOT mainboard to reset?

A: When the motor rotates, it requires a larger current than other sensors, which will cause voltage and current fluctuations in the circuit. Especially when the motor rotates forward and reverse, the voltage and current fluctuations are too large, causing the voltage and current of the kidsIOT mainboard to be too low, thus causing a reset.
