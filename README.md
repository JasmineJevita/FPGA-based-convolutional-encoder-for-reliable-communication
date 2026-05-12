# FPGA-based-convolutional-encoder-for-reliable-communication
Department of Electronics and Communication Engineering
Course: DDHDL Verilog (22ECE42) | Semester: Fourth
Guide: P.C. Vijay Ganesh, Assistant Professor (B.E., M.Tech, MIEEE)

# Project Overview
This project implements a Rate 1/2 Convolutional Encoder on FPGA to improve the reliability of digital data transmission over noisy communication channels. The system takes an 8-bit input, encodes it using shift registers and XOR logic, and passes it through BPSK modulation and an AWGN channel model. The encoder operates at 80 MHz clock and is verified through simulation using Vivado 2018.2.

# System Flow
The 8-bit input is first converted from parallel to serial using a P/S Converter, then passed through a PCM Encoder. The serial data enters the Convolutional Encoder, where two D flip-flops (M1, M2) store delayed bits x(n-1) and x(n-2), and three XOR gates generate two encoded outputs Y1(n) and Y2(n). A 2:1 MUX serializes these outputs, which are then given to WGN channel.

# Encoding Equations:
Y1(n) = x(n) ⊕ x(n-1) ⊕ x(n-2)
Y2(n) = x(n) ⊕ x(n-2)
Code Rate R = 1/2
Constraint Length K = 3

# Tools Used
Xilinx Vivado 2018.2 
MATLAB/Simulink
Powerpoint.



