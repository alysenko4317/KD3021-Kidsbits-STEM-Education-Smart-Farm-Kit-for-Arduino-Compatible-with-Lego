### Project 03:  Automatic Feeding System

![Img](./media/3-0.webp)

#### 1. Description

The automatic feeding system is composed of a kidsIOT main board, an ultrasonic sensor and a servo. The ultrasonic sensor is used to detect the distance of pets in the feeding area. When the pet approaches the food bowl, the sensor detects that the distance is getting closer. After triggering the signal, it controls the servo to open the feed box and automatically feed the animals.

#### 2. Components

|![Img](./media/A1.png)|![Img](./media/A6.png)|![Img](./media/A7.png)|![Img](./media/A14.png)|
| :--: | :--: | :--: | :--: |
|kidsIOT Mainboard×1|Ultrasonic Adapter Board×1|Ultrasonic Sensor×1|Servo×1|
|![Img](./media/A21.png)|![Img](./media/A19.png)|![Img](./media/A32.png)| |
|Wire×1|USB Cable×1| Automatic Feeding System LEGO Pieces×1 | |

![Img](./media/3-1.png)

#### 3. Assembly Steps

##### Step 1：Components Needed

![Img](./media/Z-3-1.png)

##### Step 2：Process

Process 1：

![Img](./media/Z-3-2.png)

Process 2：

![Img](./media/Z-3-3.png)

Process 3：

![Img](./media/Z-3-4.png)

Process 4：

![Img](./media/Z-3-5.png)

Process 5：

![Img](./media/Z-3-6.png)

Process 6：

![Img](./media/Z-3-7.png)

Process 7：

![Img](./media/Z-3-8.png)

Process 8：

![Img](./media/Z-3-9.png)

Process 9：

![Img](./media/Z-3-10.png)

Process 10：

![Img](./media/Z-3-11.png)

Process 11：

![Img](./media/Z-3-12.png)

Process 12：

![Img](./media/Z-3-13.png)

Process 13：

![Img](./media/Z-3-14.png)

Process 14：

![Img](./media/Z-3-15.png)

Process 15：

![Img](./media/Z-3-16.png)

Process 16：Initialize the servo angle

Wiring of servo
![Img](./media/Z-3-17.png)

First write the following code in KidsBlock software and upload the code to the kidsIOT mainboard, then the servo will rotate 190° . (<span style="color: rgb(255, 76, 65);">Note: If the servo can not rotate, you can press the RESET button on the kidsIOT board.</span>)

![Img](./media/Z-3-18.png)

Process 17：

![Img](./media/Z-3-19.png)

Process 18：

![Img](./media/Z-3-20.png)

Process 19：

(<span style="color: rgb(255, 76, 65);">Note: Do not twist the servo</span>)

![Img](./media/Z-3-21.png)

Process 20：

![Img](./media/Z-3-22.png)

Process 21：

![Img](./media/Z-3-23.png)

Complete

![Img](./media/Z-3-24.png)

#### 4. Wiring Diagram

| Module |kidsIOT Mainboard |
| :--: | :--: |
| Ultrasonic Adapter Board |No.9 port（Trig--io18，Echo--io19） |
|Servo|G/V/io33 port（Brown→G，Red→V，Orange→io33）|



| Ultrasonic Sensor | Ultrasonic Adapter Board |
| :--: | :--: |
| Vcc | VCC |
| Trig | Trig |
| Echo | Echo |
| Gnd | GND |

Connect the kidsIOT mainboard to your computer via USB cable.

![Img](./media/3-2.png)

#### 5. Servo rotation

![Img](./media/3-3.png)

##### (1). Programming Steps

###### Step 1：Description of the Building Block

![Img](./media/1-38.png)

Set the servo's channel and output (rotation) angle to the specified PWM pin.

###### Step 2：Write the Program

① Set the pin IO33 (<span style="color: rgb(255, 76, 65);">control pinio33</span>) connected to the servo to "**Output**" mode.

![Img](./media/3-5.png)

② Initialize the control channel of the servo to CH2 (LT1) and the initial angle to <span style="color: rgb(255, 76, 65);">190°</span>, with a delay of 0.5 seconds.

![Img](./media/3-6.png)

③ The servo rotates from 190° to 120° and then to 60° every 0.5 seconds.

![Img](./media/3-7.png)

④ Complete Program

![Img](./media/3-8.png)

##### (2). Test Result

Click![Img](./media/1-27.png) to upload the above complete code to the kidsIOT motherboard, then power up via the USB cable, then servo will rotate.

#### 6. Read the Value of Ultrasonic Sensor

![Img](./media/3-10.png)

##### (1). Programming Steps

###### Step 1：Add the Ultrasonic Sensor

Tap the “Sensor” module in the “Extension” , then select “**Ultrasonic Sensor**” and click ![Img](media/781.png)to return to the programming interface.

![Img](./media/3-13.png)

![Img](./media/3-14.png)

![Img](./media/3-15.png)

###### Step 2：Description of the Building Block

![Img](./media/3-16.png)

This block is used to measure distance to the specified pin, and the distance unit can be cm or inch.

###### Step 3：Write the Program

① Set the baud rate to 15200.

![Img](./media/1-68.png)

② Set the Trig pin of the ultrasonic sensor <span style="color: rgb(255, 76, 65);">IO18</span> to "**output**" mode, and the Echo pin <span style="color: rgb(255, 76, 65);">IO19</span> to "**input**" mode.

![Img](./media/3-18.png)

③ Set Trig to <span style="color: rgb(255, 76, 65);">IO18</span> and Echo to <span style="color: rgb(255, 76, 65);">IO19</span>, and the serial port prints the distance value detected by the ultrasonic sensor at 0.1 second intervals.

![Img](./media/3-19.png)

④ Complete Program

![Img](./media/3-20.png)

##### (2). Test Result

Click![Img](./media/1-27.png) to upload the above complete code to the kidsIOT motherboard. After powering up via the USB cable, click ![Img](./media/1-87.png) in the serial monitor and set the baud rate to 15200. Move your hand in front of the ultrasonic sensor. When you are close to it, the displayed distance value becomes smaller. When you move away from it, the value becomes larger.

![Img](./media/3-23.png)

#### 7. Automatic Feeding System

![Img](./media/3-24.png)

##### (1). Programming Steps

###### Step 1：Flow Chart

![Img](./media/3-25.png)

###### Step 2：Programming Steps

① Set the baud rate to 15200, the Trig pin of the ultrasonic sensor <span style="color: rgb(255, 76, 65);">IO18</span> to "**output**" mode, and the Echo pin <span style="color: rgb(255, 76, 65);">IO19</span> to "**input**" mode.

![Img](./media/3-26.png)

② Set the pin IO33 connected to the servo to "**Output**" mode, initialize the control channel of the servo to CH2 (LT1) and the initial angle to <span style="color: rgb(255, 76, 65);" >190°</span>, delay 0.5 seconds.

![Img](./media/3-27.png)

③ Define a "<span style="color: rgb(255, 76, 65);">Distance</span>" global variable to store the distance value detected by the ultrasonic sensor.

![Img](./media/3-28.png)

④ Set the Trig pin and Echo pin of the ultrasonic sensor, and print the read distance value of the ultrasonic sensor on the serial port.

![Img](./media/3-29.png)

⑤ Determine the distance detected by the ultrasonic sensor. If 2cm < distance value < 7cm, the feed box will be opened; otherwise, it will be closed.

![Img](./media/3-30.png)

⑥ Complete Program

![Img](./media/3-31.png)

##### (2). Test Result

Click![Img](./media/1-27.png) to upload the above complete code to the kidsIOT motherboard. After powering up via the USB cable, click ![Img](./media/1-87.png) in the serial monitor and set the baud rate to 15200. If an animal is detected within 2cm-9cm, the feed box will be opened  to feed the animal.

![Img](./media/3-34.jpg)

#### 8. Common Problems　

##### Q1: Why doesn’t the servo work?

A: It may be stuck. Before assembling the servo, use the code to adjust it to 80°.

##### Q2: Why is the detection distance inaccurate when using the ultrasonic sensor?

A: Measurement should be started from the transmitting head of the ultrasonic sensor. This module is not a high-precision ultrasonic distance detection module and may exist errors.

![Img](./media/3-34.png)