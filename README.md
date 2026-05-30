# Iron-Man-MK85-with-Jarvis-Integration
Iron Man MK85 Helmet with HUD Display AI/Jarvis Integration made using Raspberry Pi-4 and Arduino having features like Voice command, GPS interface, etc.

## Our Project Design

## Why?
We, being die-hard fans of the Marvel Cinematic Universe (MCU), especially Iron Man, have always dreamed of making this Iron Man helmet one day with all the features shown in the movies (except the flying one). This Iron Man helmet symbolizes the idea that humans can create extraordinary things through innovation and determination. Ever since we first saw the MK85 suit, we have been inspired by its futuristic design and the technology behind it. It sparked our curiosity about engineering. What inspired us the most was the relationship between Tony Stark and J.A.R.V.I.S., the artificial intelligence that assisted him in creating, improving, and controlling his inventions. This showed us how technology and human creativity can push beyond normal limits.

## Background
As students deeply interested in technology and engineering, we wanted to challenge ourselves with something beyond ordinary school projects. We did not want to simply make a static model; we wanted to build something that feels alive. Every stage — from CAD modeling to circuit wiring and programming — has introduced us to the practical side of engineering problem-solving.

What makes this project meaningful is not only the final product, but also the journey behind it. There are moments when measurements fail, code does not work, parts do not fit correctly, or entire systems stop functioning. Just like Tony Stark consistently improved his suits through trial and error, we are learning that innovation is built through persistence, patience, and countless experiments.

This project teaches us that engineering is not just about machines — it is about imagination becoming reality.

## How it Works
The helmet operates on a dual-controller architecture to split low-level hardware tasks from high-level computational processing.
- ### The Primary Brain:
**A Raspberry Pi 4 (4GB)** processes the video feed from the Raspberry Pi Camera module v2 for object recognition and eye tracking runs the JARVIS voice command engine via a **USB microphone**, and outputs audio feedback through a **Small 3W Speaker Driven by a PAM8403 Amp Module**. It also handles complex software rendering for the main Heads-Up-Display.

- ### The Secondary Controller:
An **Arduino(Uno or Nano)** handles low-latency hardware tasks. It reads data from the **GY-521 MPU 6050**(for the artificial hroizon), the **QMC5883L**(for the directional compass), and the **HC-SR04 Ultrasonic Sensor** (for the simulated radar feature. It also processes incoming environmental data from the **DHT22**(temperature/humidity),**BMP180/BMP280**(Altitude/Pressure), and **MQ-135**(air quality) sensors, alongside vital signs via the **MAX30102 Heart Rate Module**. Because Pi operates on 3.3V Logic, An **ADS1115 4-Channel ADC Module** converts critical analog sensor data into the digital format the Pi can read.

- ### Actuators and Display:
Based on real-time sensor processing, The Arduino drives a **1-meter strip of WS2812B RGB LEDs** segmented t illuminate the eyes, and coordinates twin **SG90/MG90S Servo Motors** to mechanicaly actuate the faceplate. Visual telementry is pushed to a **0.96" SSD1306 12C OLED Display**(or an upgraded **2.4" ILI9341 TFT SPI Display) acting as the primary HUD.

## How to Use
### Daily Use:
Simply toggle the master switch on your USB power bank to boot up the dual-complete system. Align the EVA foam helmet shell and let the 10mm  X 3mm **Neodymium disc magnets** snap the faceplate securely into position.
Once the system initializes, look directly through your HUD lens:
- The **0.96" SSD1306 12C OLED Display** will render a telementry dashboard.
- The **GY-521 MPU 6050** instantly stabilizes the flight-inspired artificial horizon, adapting smoothly to your head's roll,pitch and tilt.
- Real-time structural navigation data will stream in via the **QMC5883L/HMC5883L digital compass** and the **NEO-6M GPS module**
- The **DHT22,BMP180/BMP280** and **MQ-135** sensors will populate your environmental protection overlay, displaying ambient temperature, relative humidity, atmospheric altitude, and current pollution/air quality indexes.
- Your biometrics, tracking heart rate and vital signs via the **MAX30102 module**, will display in a dedicated corner of the screen.

To trigger the spatial radar display, look toward nearby obstacles; the **HC-SR04 Ultrasonic sensor** will automatically overlay proximity warnings onto your display.

To engage the **JARVIS AI**, simply speak into the mask. The integrated **USB Microphone** processes your voice commands for real-time object recognition  using the **Raspberry Pi Camera module V2**, while the **PAM8403 Amp and 3W speaker** deliver JARVIS's voice responses directly to you. Activating teh system or triggering specific voice commands will signal the Arduino to cycle the **WS2812B RGB LED eyes** or engage the twin **SG90/MG90S servos to mechanically flip open the faceplate.

### How to charge the battery:
Plug a standard USB-C cable into the main input port of the 20,000mAh power bank(or your alternative 18650 Li-ion charging rig). Thanks to built-in-power-path management and load sharing, you can ru diagnostics, update python scripts on the Pi 4, or calibrate the Arduino sensor threshlolds via a wall adapter without draining your cell capacity during desktop testing.

## Key Features:
- Heads-Up Display(HUD)
- Enviromental Protection/ Pollution-Adaptive Screen
- Sensor Activated Eyes
- Radar Feature
- Retina/Eye Tracking
- Communication Interface/ Jarvis Voice Itegration
- Object Recognition
- Map with GPS coordinates
- Directional Compass
- Artificial Horizon with Roll & Tilt

## License
MIT
  


 






