#  💡 Smart Classroom Environment Control System  🌍💡
## Transforming educational spaces into eco-friendly, energy-efficient, and adaptive learning environments.
An innovative solution for optimizing energy consumption and enhancing user comfort in large spaces, such as classrooms or expansive rooms with multiple fans, lights, and AC units. Developed a system that integrates IoT devices and AI algorithms to intelligently control individual appliances based on occupancy. The objective is to dynamically activate and deactivate fans, lights, and AC units in response to the presence or absence of individuals within specific zones, ensuring efficient resource utilization and a comfortable environment.

## Global significance and Necessity 🌟
- **Sustainability & Cost Savings**: Dramatically reduces energy usage and operational costs, supporting global sustainability efforts. 🌱💰
- **Enhanced Learning Environments**: Optimizes classroom conditions for improved student engagement and academic performance. 📚👩‍🏫
- **Flexibility for Future Education**: Adapts to changing occupancy, supporting hybrid learning models and efficient space utilization. 🔄🏫

## Applications 📈
- **Educational Institutions**: From K-12 to universities, optimizing resource use and improving the learning atmosphere. 🏫✨
- **Corporate & Public Spaces**: Applies to training facilities and libraries, enhancing the learning experience while managing costs. 💼📚
- **Conference & Community Centers**: Ensures comfort and energy efficiency in spaces hosting educational and professional events. 🎤🌍

## 🚀 Features
- **Automated Classroom Monitoring:** Detects motion in classrooms and triggers image capture for real-time monitoring.
- **Advanced Face Detection:** Utilizes two Intel-developed face detection models using OneAPI for enhanced accuracy in identifying student presence.
- **Dynamic Environmental Control:** Automatically adjusts cooling (fans) and lighting based on indoor temperature and motion detection.
- **Real-time Display and Feedback:** Provides instant feedback on presence detection and displays the count of recognized faces on an OLED screen.
- **Seamless Wireless Communication:** Enables wireless communication between components for efficient data transfer and control.
- **Energy efficiency and Sustainability:** Optimizes energy use by activating lights and fans only when needed, contributing to sustainability and cost-effectiveness.

## 🎥 Demonstration of the project
//video  
YOUTUBE URL: https://www.youtube.com/watch?v=s2yacyNkLz0

## 👤 Models
1. Face-Detection Model
   - Folder URL: [SmartSpark/model/face-detection-0200.xml](https://github.com/NimithB/SmartSpark/blob/main/model/face-detection-0200.xml)
   - Folder URL: [SmartSpark/model/face-detection-0200.bin](https://github.com/NimithB/SmartSpark/blob/main/model/face-detection-0200.bin)

## 🤖 Face detection model
The face detection model works by scanning images in real-time to locate human faces within them. These models are typically trained on vast datasets containing millions of images to learn various facial features and structures. It is built using OneAPI.

By employing sophisticated machine learning algorithms, such as convolutional neural networks (CNNs), the model identifies patterns that correspond to faces by analyzing different aspects like shapes, contours, and textures.

Once a face is detected, the model can mark its position within the image or frame, often drawing a bounding box around each detected face. This capability is foundational for various applications, including security systems, user authentication, crowd monitoring, and enhancing user experiences in gadgets and software by enabling interactive, face-based commands and settings.

## IMAGE BEFORE FACE DETECTION
<div align="center">    
  <img src="https://github.com/NimithB/SmartSpark/blob/main/testimages/3%20(1).jpg" alt="Image" style="max-width: 1000000px;">
</div>

## IMAGE AFTER FACE DETECTION
<div align="center">
  <img src="https://github.com/NimithB/SmartSpark/blob/main/testimages/result/3%20(2).jpg" alt="Image" style="max-width: 1000000px;">
</div>


## **Hardware Requirements** 💻🔧

- **ESP32-CAM:** AI-enabled microcontroller for image capture and processing.
- **Ultrasonic Sensor:** Detects motion in the classroom environment.
- **OLED Display:** Provides visual feedback on presence detection and face count.
- **Arduino Uno WiFi (ESP8266):** Facilitates communication between ESP32-CAM and other components.
- **Temperature Sensor:** Monitors indoor temperature for environmental control.
- **Buzzer and LED:** Provides auditory and visual alerts for presence detection.

## **Software Tools Requirements and Libraries** 💻🧰📚

- **Arduino IDE:** Integrated Development Environment for programming ESP32-CAM and Arduino Uno WiFi.
- **Intel OpenVINO Toolkit:** Toolkit for developing and deploying AI models, including face detection models.
- **U8glib Library:** Library for interfacing with OLED displays.
- **DHT Library:** Library for reading data from DHT temperature and humidity sensors.
- **Requests Library:** Python library for making HTTP requests for communication between microcontrollers and the AI model.
- **OpenCV Library:** Library for image processing tasks such as face detection.

## **Installation Instructions** 📥
## 📋 Prerequisites
Before diving in, ensure the following are ready:
- **Arduino IDE**: Installed on your computer for code uploading.
- **Intel oneAPI Base Toolkit**: Set up for AI model development, crucial for the smart decision-making aspect of the project.
- **Intel DevCloud Access**: Optional, for those preferring to train models in the cloud.

## 🎛 Hardware Setup
**Step 1**: Connect your Arduino Uno Wi-Fi to the computer via USB, preparing it for programming.

**Step 2**: Assemble **Sensors and Modules**:
- connect the ultrasonic sensor, ESP32-CAM, DHT sensor, LEDs, and buzzer to your Arduino.
- This step is crucial for the physical interaction part of the project.
- //image

## 💾 Software Setup
**Step 1**: **Arduino Configuration**:
   - Launch the Arduino IDE, selecting `Arduino Uno Wi-Fi` as your board.
   - Through the Library Manager, install necessary libraries (e.g., ESP32, DHT sensor libraries), ensuring your software can communicate with the hardware seamlessly.

**Step 2**: **Intel AI Analytics Toolkit**:
   - Install the toolkit by following the guide at [Intel's official site](https://software.intel.com/content/www/us/en/develop/tools/oneapi/base-toolkit.html). This toolkit is the backbone of our AI functionalities.

## 🧠 Model Training (Optional)
- **Intel DevCloud**: For cloud enthusiasts, log in and navigate to `model_training` for instructions on model training.
- **Locally**: Ensure Python is ready and initialize the environment with `requirements.txt`, setting the stage for local model development.

## 🚀 Deployment
**Step 1**: **Load the AI Model**:
   - Transfer the AI model to your Arduino or an external server. This is where your project comes to life, making intelligent decisions based on sensor data.

**Step 2**: **Arduino Sketch**:
   - Open `smart_classroom_control.ino` with the Arduino IDE. Here, you'll input your environment's specifics like Wi-Fi credentials.
   - Upload the sketch to your board, a critical step to bring your code into the real world.

## 🧪 Testing
- Test your setup by simulating occupancy. Watch as the system intelligently responds to the presence of individuals, controlling the environment accordingly.
  Your Smart Classroom Environment Control System is now operational.
For a deep dive into operation instructions and troubleshooting, refer to the [instruction.txt]https://github.com/NimithB/SmartSpark/blob/main/Hardware/instruction.txt) in our Hardware folder.

## **Troubleshooting** 💻🛠️❓

- **Camera Not Capturing Images:**
Verify camera connections and compatibility with ESP32-CAM. Check for proper power supply and ensure camera initialization in code.

- **Face Detection Inaccuracies:**
Optimize lighting conditions and camera positioning. Consider retraining models with diverse datasets for improved accuracy.

- **Communication Issues Between Devices:**
Double-check wiring connections and communication protocols (e.g., UART, SPI). Ensure correct Wi-Fi setup for wireless communication.

- **OLED Display Showing Incorrect Information:**
Confirm display connections and check for damaged pins. Ensure correct library usage and code referencing.

- **AI Model Inference Errors:**
Verify model files loaded correctly and implement inference code accurately. Check for memory constraints and optimize model for performance.

## **System Workflow** 🔄
**1. Presence Detection:** 🚶‍♂️
- The ultrasonic sensor detects motion in the classroom.
- If motion is detected, it triggers the ESP32-CAM to capture an image of the classroom.

**2. Image Capture and Processing:** 📸
- ESP32-CAM captures an image upon motion detection.
- The captured image is processed using two face detection models to identify the presence of faces.
- The average output of the two models is calculated for improved accuracy.

**3. Data Transmission:** 📡
- Detected face count is sent from ESP32-CAM to Arduino Uno WiFi (ESP8266) over Wi-Fi communication.
- Arduino Uno WiFi receives the face count data from ESP32-CAM.

**4. Display and Control:** 💡
- Arduino Uno WiFi displays the number of detected faces on the OLED display.
- If the temperature exceeds 30°C, the fan is turned on to regulate temperature.
- Presence detection triggers the light to turn on in the classroom.

**5. Error Handling:** ⚠️
- System checks for errors in sensor readings, image processing, and data transmission.
- Error messages or alerts are displayed on the OLED screen for troubleshooting.

**6. Continuous Monitoring:** 🔍
- The system continuously monitors for motion using the ultrasonic sensor.
- It repeats the process of presence detection, image capture, and face counting in a loop.

<div align="center">
  <img src=" https://github.com/NimithB/SmartSpark/blob/main/Hardware/blockdiagram.jpeg" alt="Image" style="max-width: 1000px;">
</div>
 

**Results**
Following the initial detection and image capture, the system swiftly processes the image through a sophisticated AI model designed for facial recognition. This model accurately counts and analyzes the faces within the image, showcasing the power of machine learning in real-time data analysis. The integration of these technologies not only enhances security measures but also offers insights into the environment it monitors.

url for result images: [SmartSpark/testimages/result at main · NimithB/SmartSpark (github.com)](https://github.com/NimithB/SmartSpark/tree/main/testimages/result)

//add an image where the faces are boed and the fan and led is on

**Hardware**

**ESP32 Camera Module:** The ESP32 camera module integrates a high-resolution camera sensor with the ESP32 microcontroller, enabling users to capture images and videos, stream live feeds, and perform machine vision tasks directly. With its compact form factor and versatile capabilities, it is well-suited for applications ranging from surveillance and monitoring to image recognition and augmented reality.

**Arduino Uno WiFi:** Offering the familiarity of the Arduino platform coupled with onboard Wi-Fi capabilities, the Arduino Uno WiFi empowers users to seamlessly connect their projects to the internet, enabling remote monitoring, control, and data logging without additional shields or modules. Furthermore, the integration of Wi-Fi connectivity simplifies the development process, allowing for rapid prototyping and deployment of IoT solutions

**IR Sensor:** A staple in automation and robotics, IR sensors detect infrared radiation emitted by objects, converting it into electrical signals to trigger actions such as activating lights, opening doors, or detecting intruders, making them indispensable components in smart home and security systems.
