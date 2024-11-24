# CRC
This is a simple implementation of Cyclic Redundancy Check (CRC) using C programming language. CRC is a popular error-detecting code used to detect accidental changes to raw data. The program demonstrates the encoding and decoding process, ensuring data integrity during transmission.
Features
Encode data using a user-defined generator polynomial.
Append CRC to the data for transmission.
Verify the integrity of received data.
Detect errors in the transmitted data.
How It Works
Input Data:
The user inputs the data to be transmitted and the generator polynomial.
Padding:
The program appends (N-1) zeros to the input data, where N is the length of the generator polynomial.
CRC Calculation:
A bitwise XOR operation is performed between the data and the generator polynomial to compute the CRC.
Data Transmission:
The CRC is appended to the original data for transmission.
Receiver Verification:
The receiver verifies the transmitted data by recalculating the CRC.
If the remainder after XOR is zero, the data is valid; otherwise, an error is detected.
Input/Output Format
Input
Data to be transmitted (e.g., 1011101)
Generator Polynomial (e.g., 1001)
Output
Padded data with (N-1) zeros.
Computed CRC (Check value).
Final transmitted data (data + CRC).
Verification results (Error detected or No error detected).
Program Flow
Main Function:
Accepts data and generator polynomial from the user.
Computes the CRC and displays the final data to be transmitted.
Calls the receiver function to verify the data.
CRC Function:
Performs bitwise XOR operations to calculate the CRC.
Shifts the data bits to process the entire data.
Receiver Function:
Accepts the transmitted data.
Recalculates the CRC to verify the data integrity.
XOR Function:
Implements the XOR logic for CRC calculation.
Example
Input:
Enter data to be transmitted: 1011101
Enter the Generating polynomial: 1001
Output:
----------------------------------------
Data padded with n-1 zeros : 1011101000
----------------------------------------
CRC or Check value is : 011
----------------------------------------
Final data to be sent : 1011101011
----------------------------------------
Enter the received data: 1011101011
-----------------------------
Data received: 1011101011
No error detected
If data is altered during transmission:
Enter the received data: 1011101000
-----------------------------
Data received: 1011101000
Error detected
Compilation and Execution
Compile the Code:
gcc crc.c -o crc
Run the Program:
./crc
