# CRC Error Detection Code

This program implements error detection using the Cyclic Redundancy Check (CRC) algorithm. It supports both CRC-CCITT (8-bit) and CRC-CCITT (16-bit) versions.

## Description

Cyclic Redundancy Check (CRC) is an error-detecting code used to verify the accuracy of data. It involves using a generator polynomial to compute a check value (CRC) that is appended to the data. The recipient can use the same polynomial to check for errors in the received data.

## How It Works

1. **CRC Encoding:**
   - The input message is appended with zeros based on the polynomial length.
   - Perform XOR operations with the polynomial to compute the CRC.
   - The CRC is appended to the original message for transmission.

2. **CRC Checking:**
   - The received message (including the CRC) is checked by performing XOR operations with the polynomial.
   - The presence of any non-zero bits in the remainder indicates an error in the data transmission.

## Usage

1. **Compile the Code:**

   Use a C++ compiler like `g++`:

   ```sh
   g++ -o crc crc.cpp
   ./crc
