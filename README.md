Bluetooth-Based Home and Industry Appliances Control System

The main objective of this project is to develop a home automation system using an Arduino board with Bluetooth being remotely controlled by any Android OS smartphone. As technology is advancing so houses are also getting smarter. Modern houses are gradually shifting from conventional switches to centralized control system, involving remote controlled switches. Presently, conventional wall switches located in different parts of the house makes it difficult for the user to go near them to operate. Even more it becomes more difficult for the elderly or physically handicapped people to do so. Remote controlled home automation system provides a most modern solution with smartphones.

In order to achieve this, a Bluetooth module is interfaced to the Arduino board at the receiver end while on the transmitter end, a GUI application on the cell phone sends ON/OFF commands to the receiver where loads are connected. By touching the specified location on the GUI, the loads can be turned ON/OFF remotely through this technology.

Description

This project presents the implementation of a Bluetooth-based home and industry automation system using an Android smartphone and Arduino Uno. It is designed to provide a cost-effective, user-friendly, and easy-to-install solution for controlling electrical appliances remotely.

The system is particularly beneficial for elderly and physically challenged individuals, enabling them to operate home or industrial devices such as lights, fans, and other appliances without physical effort, simply through Bluetooth communication.

A Bluetooth module (HC-05) is used to establish wireless communication between the Android device and an Arduino Uno. The Arduino receives serial commands and controls relays that switch ON/OFF the connected devices. A 16x2 LCD display is used to provide visual feedback about the device status. The user interacts with the system through a mobile app or Bluetooth terminal, making the whole process seamless and responsive.

This system improves safety, reduces manual effort, and enhances the living standard through smart automation, all while remaining affordable and efficient.
Components
| Component                        | Description                                                                   |
| -------------------------------- | ----------------------------------------------------------------------------- |
| **Arduino Uno (ATmega328)**      | Microcontroller board used to control relays and handle serial communication. |
| **HC-05 Bluetooth Module**       | Wireless module used for serial Bluetooth communication with Android device.  |
| **Relay Modules (2-channel)**    | Used to switch AC and DC loads (e.g., bulb and fan) ON or OFF.                |
| **16x2 LCD Display**             | Displays system status and appliance control feedback.                        |
| **Android Smartphone**           | Sends commands via Bluetooth to control appliances.                           |
| **Bluetooth Terminal App**       | Or custom app to send control signals (e.g., 'L', 'F', 'A')                   |
| **Light Bulb (AC Load)**         | Acts as one of the controlled devices (AC-powered).                           |
| **DC Fan (DC Load)**             | Another controlled device (DC-powered).                                       |
| **Regulated Power Supply (RPS)** | Provides appropriate voltage and current to the Arduino and peripherals.      |

Software
| Software/Tool                                        | Purpose                                                      |
| ---------------------------------------------------- | ------------------------------------------------------------ |
| **Arduino IDE**                                      | To write, compile, and upload code to the Arduino Uno board. |
| **Bluetooth Terminal App** *(or custom Android app)* | To send Bluetooth commands from Android phone to Arduino.    |
| **Proteus / Fritzing** *(optional)*                  | For designing and simulating the circuit (if applicable).    |
| **Windows/Linux OS**                                 | For running Arduino IDE and handling serial communication.   |

Implementation
Hardware & Software Workflow
Circuit Design & Hardware Setup

Assembled components including:

Arduino Uno (ATmega328)

HC-05 Bluetooth module

Relay modules to control AC/DC loads

16x2 LCD for displaying device status

RPS (Regulated Power Supply) for stable voltage

Connected relays to digital output pins of Arduino to control:

Light Bulb (AC load)

DC Fan (DC load)

Integrated the LCD with Arduino using LiquidCrystal library to show real-time feedback.

Arduino Programming

Developed an Arduino sketch that:

Initializes the LCD and serial communication.

Waits for command input via Bluetooth (from smartphone).

Controls relays based on commands:

'L'/'l' → Turn ON/OFF Light

'F'/'f' → Turn ON/OFF Fan

'A'/'a' → Control both Light & Fan

Displays current status on LCD (e.g., “BULB ON”, “FAN OFF”).

Bluetooth Communication

Paired smartphone with HC-05 module (default PIN: 1234 or 0000).

Used a Bluetooth Terminal App or custom-built Android app to send control commands.

Arduino receives characters via serial (Serial.read()) and takes corresponding action.

Testing & Validation

Verified real-time control of appliances.

Ensured the LCD provides correct status updates.

Confirmed safe operation of relays and isolation between AC and control circuit.




