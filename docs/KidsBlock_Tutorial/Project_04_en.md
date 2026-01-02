### Project 04: Anti-theft Alarm System

![Img](./media/4-0.jpg)

#### 1. Description

The anti-theft alarm system is composed of a PIR motion sensor, a buzzer, a LED and a kidsIOT mainboard. When programming via the KidsBlock, you are able to judge whether someone is moving by reading the digital signal detected by the PIR motion sensor. If someone is moving, the buzzer will sound an alarm and the LED will flash to alert the user that someone has entered the area. Thus, a low-cost anti-theft alarm system can be realized, which is suitable for homes or offices.



#### 2. Components

|![Img](./media/A1.png)|![Img](./media/A4.png)|![Img](./media/A10.png)|![Img](./media/A14.png)|
| :--: | :--: | :--: | :--: |
|kidsIOT Mainboard×1|PIR Motion Sensor×1|Passive Buzzer×1|Servo×1|
|![Img](./media/A21.png)|![Img](./media/A19.png)|![Img](./media/A31.png)|  |
|Wire×2|USB Cable×1| Anti-theft Alarm System LEGO Pieces×1 |  |

![Img](./media/4-1.png)

#### 3. Assembly Steps

##### Step 1：Components Needed

![Img](./media/Z-4-1.png)

##### Step 2：Process

Process 1：

![Img](./media/Z-4-2.png)

Process 2：

![Img](./media/Z-4-3.png)

Process 3：

![Img](./media/Z-4-4.png)

Process 4：

![Img](./media/Z-4-5.png)

Process 5：

![Img](./media/Z-4-6.png)

Process 6：Initialize the servo angle

Wiring of  servo(it is the same as project 03)

![Img](./media/Z-4-7.png)

First write the following code in KidsBlock software and upload the code to the kidsIOT mainboard, then the servo will rotate 180° . (<span style="color: rgb(255, 76, 65);">Note: If the servo can not rotate, you can press the RESET button on the kidsIOT board.</span>)

![Img](./media/Z-4-8.png)

Process 7：(Place the three Lego boxes on the same side, then assemble the four gears.)

![Img](./media/Z-4-9.png)

Process 8：

![Img](./media/Z-4-10.png)

Process 9：

![Img](./media/Z-4-11.png)

Process 10：

![Img](./media/Z-4-12.png)

Complete 1：

![Img](./media/Z-4-13.png)

Process 11：Share the LEGO board with project 03

![Img](./media/Z-4-14.png)

Complete 2：

![Img](./media/Z-4-15.png)


#### 4. Wiring Diagram

| Module |kidsIOT Mainboard |
| :--: | :--: |
| PIR Motion Sensor |No.4 port（control pin is io27） |
|Passive Buzzer|No.6 port（control pin is io23）|
|Servo|G/V/io33 port（Brown→G，Red→V，Orange→io33）|

Connect the kidsIOT mainboard to your computer via USB cable.

![Img](./media/4-2.png)

#### 5. Passive buzzer makes sound

![Img](./media/4-3.png)

##### Method 1

###### (1). Knowledge

The passive buzzer is driven by square waves. Let's simulate the square waves below.
The high and low levels of the pin can simulate a square wave: keeping the high level for 1000us and the low level for 1000us can make the buzzer sound.

![Img](./media/4-4.png)

Changing the time of high and low level can change the sound volume of the buzzer. You can try changing it to 1500us, 2000us, 3000us...

###### (2). Write the Program

① Initialize the buzzer's pin **IO23** and "**Output**" mode.

![Img](./media/4-5.png)

② Set the buzzer pin **IO23** to "**High**" and "**Low**". Here we take the delay of 0.001 second (1000 microseconds) as an example to make the buzzer emit sound.

![Img](./media/4-6.png)

The delay function is a microsecond delay, which means the time delay is 1000 microseconds.

<span style="color: rgb(255, 76, 65);">Note: The conversion relationship between seconds, milliseconds and microseconds is: 1 second = 1000 milliseconds = 1000000 microseconds. </span>


By f=1/T, changing high and low levels in 1000us, we can know that the frequency of such a square wave is 1000Hz (that is, the number of high and low level changes per second is 1000 times).

③ Complete Program

![Img](./media/4-7.png)

###### (3). Test Result

Click![Img](./media/1-27.png) to upload the above complete code to the kidsIOT motherboard. After powering up via the USB cable, the passive buzzer will make sound.

##### Method 2

###### (1). Knowledge

Use the "passive buzzer" code block to drive.
The "passive buzzer" code block can generate a fixed-frequency PWM signal to drive the passive buzzer to sound. The sounding time length (beat) and sounding frequency can be controlled via parameters.

![Img](./media/4-9.png)

###### (2). Add “passive buzzer” 

Tap the “Actuator” module in the “Extension” , then select “**<span style="color: rgb(255, 76, 65);">esp32 Passive buzzer</span>**” and click ![Img](media/781.png)to return to the programming interface.

![Img](./media/3-13.png)

![Img](./media/4-13.png)

![Img](./media/4-14.png)

###### (3). Description of the Building Block

![Img](./media/4-9.png)

Set the frequency and beat of the passive buzzer to the specified pin.

![Img](./media/4-16.png)
Set the passive buzzer to play specific music to the specified pin.

![Img](./media/4-17.png)

Set the passive buzzer to make no sound to the specified pin.

###### (4). Write the Program

① Initialize the buzzer's pin **IO23** and "**Output**" mode.

![Img](./media/4-5.png)

② Set the sound pin, frequency and beat can be selected by yourself.

![Img](./media/4-19.png)

③ Produce different tones.

![Img](./media/4-20.png)

④ Complete Program

![Img](./media/4-21.png)

###### (5). Test Result

Click![Img](./media/1-27.png) to upload the above complete code to the kidsIOT motherboard. After powering up via the USB cable, the passive buzzer will make sounds with different tones.

#### 6. Passive buzzer plays music

![Img](./media/4-23.png)

###### (1). Write the Program
① The buzzer pin is <span style="color: rgb(255, 76, 65);">**IO23**</span>, and then select a piece of music (we take **Birthday** as an example here) .

![Img](./media/4-24.png)

② Complete Program

![Img](./media/4-25.png)

###### (2). Test Result

Click![Img](./media/1-27.png) to upload the above complete code to the kidsIOT mainboard. After powering up via the USB cable, the passive buzzer will play a "Happy Birthday" music.



#### 7. Read the value of PIR Motion Sensor

![Img](./media/4-27.png)

###### Step 1：Write the Program

① Set the baud rate to 15200.

![Img](./media/1-68.png)

② Set the pin IO27 connected to the PIR motion sensor to "**input**" mode.

![Img](./media/4-29.png)

③ Define a "<span style="color: rgb(255, 76, 65);">PIR_motion_sensor</span>" global variable to store the value of the sensor.

![Img](./media/4-30.png)

④ Store the read value of the sensor in the <span style="color: rgb(255, 76, 65);">"PIR_motion_sensor</span>" variable and print it on the serial port.

![Img](./media/4-31.png)

⑤ Complete Program

![Img](./media/4-32.png)

###### Step 2：Test Result

Click![Img](./media/1-27.png) to upload the above complete code to the kidsIOT motherboard. After powering up via the USB cable, click ![Img](./media/1-87.png) in the serial monitor and set the baud rate to 15200. 

When the sensor detects movement of a person or animal, the serial monitor window prints 1, and the red LED on the sensor will be off; otherwise, the monitor prints 0, and the red LED on the sensor will be on.

<span style="color: rgb(255, 76, 65);">Note: The sensor does not have penetrating capabilities. When detecting human movement, please do not block it.</span>


![Img](./media/4-35.png)

#### 8. Anti-theft Alarm System

![Img](./media/4-36.png)

##### (1). Programming Steps

###### Step 1：Flow Chart

![Img](./media/4-37.png)

###### Step 2：Write the Program

①Set the baud rate to 15200, the IO27 pin of PIR motion sensor to "**input**" mode.

![Img](./media/4-29.png)

② Set the pin IO33 connected to the servo to "**Output**" mode, initialize the control channel of the servo to CH2 (LT1) and the initial angle to <span style="color: rgb(255, 76, 65);" >90°</span>, delay 0.5 seconds.

![Img](./media/4-39.png)

② Define a "<span style="color: rgb(255, 76, 65);">PIR_motion_sensor</span>" global variable to store the value of the PIR motion sensor.

![Img](./media/4-40.png)

③ Store the read value of the sensor in the <span style="color: rgb(255, 76, 65);">"PIR_motion_sensor</span>" variable.

![Img](./media/4-41.png)

④ Judge whether the sensor detects that a person or animal is moving. When someone or an animal is moving, the buzzer sounds, the servo rotates to close the door, and the serial monitor prints "Someone"; otherwise, the buzzer does not sound, the servo rotates to open the door, and the monitor prints " No one".

![Img](./media/4-42.png)

⑤ Complete Program

![Img](./media/4-43.png)

##### (2). Test Result

Click![Img](./media/1-27.png) to upload the above complete code to the kidsIOT mainboard. After powering up via the USB cable, click ![Img](./media/1-87.png) in the serial monitor and set the baud rate to 15200. 

When the sensor detects that someone or an animal is moving, the buzzer sounds, the servo rotates to close the door, and the serial monitor prints "Someone"; otherwise, the buzzer does not sound, the servo rotates to open the door, and the monitor prints "No one".

![Img](./media/4-46.png)

![Img](./media/4-47.jpg)

#### 9. Common Problems　

##### Q1: The tone of the passive buzzer is not accurate to the actual tone?

A: The tones simulated by ordinary passive buzzers cannot meet the requirements of professional tones. If you need accurate tones, you need to use a more professional passive buzzer.

##### Q2: Does the PIR motion sensor make false alarms?

A: ① Non-professional PIR motion sensor.

② The requirements for the sensor to avoid false alarms are as follows:
Within the detection range, avoid objects that are caused by the wind, such as curtains, clothing, flowers, etc.
Avoid interference from strong light within the detection range, such as sunlight, car lights, spotlights, lighting and other light sources.
