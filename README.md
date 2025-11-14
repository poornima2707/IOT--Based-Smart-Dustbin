# **IOT BASED SMART DUSTBIN**

## **Overview**  
This project utilizes an **Arduino Uno**, an **HC-SR04 Ultrasonic Sensor**, and a **servo motor** to create an automated system that reacts to detected objects. When an object is within a specified distance (50 cm), the servo motor is activated.

## **Components Required**  
- Arduino Uno  
- HC-SR04 Ultrasonic Sensor  
- SG90 Servo Motor  
- 9V Battery with Connector  
- Jumper Wires  

## **Circuit Connections**  
- **HC-SR04 Ultrasonic Sensor**  
  - VCC → 5V (Arduino)  
  - GND → GND (Arduino)  
  - Trig → Digital Pin **5** (Arduino)  
  - Echo → Digital Pin **6** (Arduino)  

- **Servo Motor**  
  - VCC (Red) → **5V (Arduino)**  
  - GND (Black) → **GND (Arduino)**  
  - Signal (Orange) → **Pin 7 (Arduino)**  

- **Power Supply**  
  - 9V Battery → Arduino via Vin and GND  

## **Code Explanation**  
1. **Servo Initialization:**  
   - The **Servo library** is included and initialized.  
   - The servo is set to **0 degrees** initially.  

2. **Ultrasonic Sensor Measurement:**  
   - The **measure()** function calculates the distance using the HC-SR04 sensor.  
   - The **pulseIn()** function is used to determine the time taken for the ultrasonic pulse to return.  

3. **Logic for Servo Activation:**  
   - If an object is detected **within 50 cm**, the servo is activated.  
   - The servo moves to **0 degrees**, waits for **3 seconds**, and then moves to **150 degrees**.  

4. **Serial Output:**  
   - The measured distance is printed on the **Serial Monitor** for debugging.  

## **How to Use**  
1. Connect the components as per the circuit diagram.  
2. Upload the provided Arduino code to your **Arduino Uno**.  
3. Open the **Serial Monitor** in the Arduino IDE (baud rate: **9600**).  
4. Place an object in front of the **HC-SR04 sensor** and observe the **servo movement**.  

**DEMONSTRATION**  

https://github.com/user-attachments/assets/6480b655-031f-4b64-b8b0-6b37525eea0d

