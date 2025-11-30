# IoT Security Project – Part I: Data Encryption Simulation

**Student Name**: [israa mohammed Al-Araby]  
**Enrollment Number**: [22202041015]  
**Email**: [issraa703@gmail.com]  
  

---

## Overview

This project simulates a secure data transmission scenario for an IoT sensor device (e.g., temperature and humidity sensor). The sensor encrypts its readings before sending them over a network to a base station (server), ensuring confidentiality and integrity during transmission.

The implementation uses **AES-128 in CBC mode** as a representative lightweight cryptographic method suitable for resource-constrained IoT environments.

---

## What the Code Does

1. Generates random but realistic temperature (15–35°C) and humidity (30–80%) sensor readings.
2. Formats the data as a JSON string.
3. Encrypts the data using AES-128 with a randomly generated key and initialization vector (IV).
4. Simulates transmission of the encrypted payload.
5. Decrypts the data at the receiver (server) side using the same key and IV.
6. Verifies that the decrypted data matches the original sensor readings.

---

## How to Run

1. Open the notebook in Google Colab:  
   `IoT_Security_<israa Al-Araby>_<22202041015>.ipynb`
2. Run all cells sequentially.
3. The output will display:
   - Original sensor data
   - Encrypted data (in hexadecimal format)
   - Decrypted data
   - A verification message confirming successful decryption

> Note: The code automatically installs the required `pycryptodome` library.

---

## Sample Output
=== IoT Device (Sender) ===
Original sensor data:
Temperature: 24.7 C
Humidity: 58.3 %

Plain text: {"temperature": 24.7, "humidity": 58.3}

Encrypted data (hex): d8f3a1c0b2e9...

=== Base Station (Receiver / Server) ===
Simulating reception of encrypted data...
Decrypted data:
Temperature: 24.7 C
Humidity: 58.3 %