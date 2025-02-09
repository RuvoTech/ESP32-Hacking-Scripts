
ESP32 Hacking Scripts

A collection of hacking-related scripts for the ESP32, including WiFi attacks, Bluetooth scanning, and IR (Infrared) scripts.

Features
	•	WiFi Attacks
	•	Deauthentication
	•	Beacon spamming
	•	Packet sniffing
	•	Bluetooth Scanning & Attacks
	•	BLE scanning
	•	Bluetooth MAC address spoofing
	•	Infrared (IR) Scripts (New!)
	•	IR signal sending
	•	IR remote replay attacks
	•	IR brute force techniques
	•	Miscellaneous
	•	Packet injection
	•	ESP-NOW communication

Hardware Requirements
	•	ESP32 Development Board (M5StickC Plus 2, ESP32-WROOM, or ESP32-S2/S3)
	•	Optional:
	•	IR Transmitter/Receiver (for IR scripts)
	•	External Antenna (for better WiFi range)

Installation

1. Flashing the ESP32
	1.	Install Arduino IDE or ESP-IDF.
	2.	Install ESP32 board support via the Board Manager.
	3.	Clone this repository:

git clone https://github.com/RuvoTech/ESP32-Hacking-Scripts.git
cd ESP32-Hacking-Scripts


	4.	Open the relevant script and upload it to your ESP32.

2. Required Libraries

Make sure you have the following libraries installed:
	•	WiFi.h (for WiFi attacks)
	•	BluetoothSerial.h (for Bluetooth functionality)
	•	IRremoteESP8266.h (for IR scripts)

Usage

WiFi Attacks
	•	Run the WiFi Deauth script to disconnect nearby devices:

python wifi_deauth.py --target MAC_ADDRESS



Bluetooth Scanning
	•	Scan for nearby Bluetooth devices:

python ble_scan.py



IR Remote Attack
	1.	Record an IR signal from a remote:

irrecv.enableIRIn();  // Start the receiver
if (irrecv.decode(&results)) {
    Serial.println(results.value, HEX);
    irrecv.resume();
}


	2.	Replay the recorded signal:

irsend.sendNEC(0x20DF10EF, 32);  // Send stored IR code



Contributing

Feel free to submit issues, feature requests, or pull requests to improve this repository!

Legal Disclaimer

This repository is for educational purposes only. The use of these scripts for unauthorized access or disruption is strictly prohibited.

