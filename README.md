**Name:** GHANTASALA N.S DEEPA JAYA SRI                                                                                                                                                                                              
**Company:** CODTECH IT SOLUTIONS                                                                                                                                                                                            
**ID:** CT08TDS1607                                                                                                                                                                                                                            
**Domain:** VLSI                                                                                                                                                                                                                      
**Duration:** 5th June to 5th July 2024                                                                                                                                                                                                      
**Mentor:** MUZZAMIL AHEMED                                                                                                                                                                                                                                                                                   
## **Overview of the Project**                                                                                                                                              
### **Project**: UART(UNIVERSAL ASYNCHRONOUS RECEIVER TRANSMITTER) DESIGN                                                                                                                                  
### *Objective*                                                                                                                                                                                                        
The objective of this project is to design, implement, and verify a UART (Universal Asynchronous Receiver/Transmitter) module using Verilog in a VLSI software environment. The project aims to develop both the transmitter and receiver parts of the UART module, simulate their functionality, verify the design using waveform analysis, and emulate UART communication through VLSI software.                                                                                                                 
### Key Activities                                                                                                                                                                                                                                                                                                                      
-**Design a UART Transmitter and Receiver**: Develop the Verilog code for the UART transmitter and receiver modules.                                      
-**Simulation and Verification**: Simulate the Verilog designs to ensure they function correctly.                                                                     
-**Waveform Analysis**: Use the waveform viewer to analyze simulation results and verify expected behavior.                                                                  
### Technologies Used                                                                                                                                                                                                                                                                                                                   
-**Verilog**: The Primary Programming Language for Digital Logic Design.                                                                                            
-**ModelSim**: For simulation and analysis of Verilog designs. 

### Key Insight                                                                                                                                                             
**Introduction**                                                                                                                                                     
UART (Universal Asynchronous Receiver/Transmitter) is a hardware communication protocol used for serial communication between devices. It allows data exchange over a serial interface, typically using two wires: one for transmitting data (TX) and one for receiving data (RX). Below is a detailed explanation of UART, including its basic operation and the design of UART modules in Verilog.

**#Basic Operation of UART**                                                                                                                                            

**1.Asynchronous Communication**

UART operates asynchronously, meaning there is no shared clock signal between the transmitting and receiving devices. Instead, both devices must agree on a common baud rate (the rate at which data is transmitted or received).                                                                                                      

**2.Data Framing**

UART frames data for transmission in a specific format, which typically includes:

Start Bit: A single bit indicating the beginning of a data frame. It is usually 0.

Data Bits: 5 to 9 bits representing the actual data. Commonly, 8 bits are used.

Parity Bit (optional): A single bit used for error checking. It can be even or odd parity.

Stop Bit(s): One or more bits indicating the end of a data frame. It is usually 1.                                                                                      

**3.Baud Rate**

The baud rate defines the speed of communication in bits per second (bps). Both the transmitter and receiver must operate at the same baud rate for successful communication.

**#Design Phase**                                                                                                                                                                

**1.UART Transmitter Design**

*Inputs                                                                                                                                                             
**clk**: System clock                                                                                                                                               
**reset**: System reset                                                                                                                                             
**tx_start**: Start transmission signal                                                                                                                             
**tx_data**: Data to be transmitted (8 bits)                                                                                                                            

*Outputs                                                                                                                                                            
**tx**: UART transmit line                                                                                                                                          
**tx_done**: Transmission complete signal                                                                                                                               

*Functionality                                                                                                                                                      
On **tx_start**, send a start bit (0), followed by 8 data bits **tx_data**, and stop bit (1).                                                                                        

**2.UART Receiver Design**


*Inputs                                                                                                                                                             
**clk**: System clock                                                                                                                                               
**reset**: System reset                                                                                                                                             
**rx**: UART receive line                                                                                                                                            

*Outputs                                                                                                                                                            
**rx_data**: Received data (8 bits)                                                                                                                                 
**rx_done**: Reception complete signal                                                                                                                              

*Functionality                                                                                                                                                      
Detect **start bit**, sample 8 data bits, and check **stop bit(s)** to complete reception.
