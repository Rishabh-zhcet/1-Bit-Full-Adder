# Design-implementaion-of-a-1-Bit-Full-Adder-using-28-nm-CMOS-technology
This repository presents the design and implementation of a 1-Bit Full Adder circuit using 28 CMOS technology. All the Simulations are done on Synopsis tool. For the representation of inputs and outputs, we have taken voltage range 0v to 1.8v. The truth table of the 1- Bit Full Adder is verified by the waveform obtained from the simulation. Full adder can be designed using two Half adders but this design is a little modified version with less no of MOSFETs. 

# Table of Contents
* [Introduction](#Introduction)
* [Tool Used](#Tool-Used)
* [Truth table ](#Truth-table)
* [Methodology](#Methodology)
* [Schematic](#Schematic)
* [Output Waveform](#Output-Waveform)
* [Generetaed Netlist](#Generetaed-Netlist)
* [Reference](#Reference)
* [Acknoledgement](#Acknoledgement)
* [Author](#Author)

# Introduction
Addition is one of the fundamental arithmetic operations. Adder is the core element of complex arithmetic circuits like addition, multiplication, subtraction, division, exponentiation address calculation and generation in case of cache memory etc. Adders are classified as Half Adder and Full Adder. The Half adder takes two inputs A and B and generates two outputs such as Sum and Carry, no previous carry is taken in account. But in case of a Full Adder, it takes three inputs like A, B and Cin (previous carry), and generated two outputs such as Sum and Carry. 

# Tool Used
Synopsys Custom Compiler
Version S-2021.09

<b>• Synopsys Custom Compiler</b></br>
&emsp;The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.

<b>• Synopsys Primewave</b></br>
&emsp;PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.

<b>• Synopsys 28nm PDK</b></br>
&emsp;The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.


# Truth table 

<div align="center">
  
|A | B |Cin|Sum|Cout|
|:-|:-:|:-:|:-:|:--:|
|0 | 0 | 0 | 0 | 0 |
|0 | 0 | 1 | 1 | 0 |
|0 | 1 | 0 | 1 | 0 |
|0 | 1 | 1 | 0 | 1 |
|1 | 0 | 0 | 1 | 0 |
|1 | 0 | 1 | 0 | 1 |
|1 | 1 | 0 | 0 | 1 |
|1 | 1 | 1 | 1 | 1 |
  
</div>
<div>
  
  <p align="center">
<b>Table:1 Truth Table of 1-Bit Full Adder</b></br>
</p>

# Output Expression
<p align="center">
Sum=A ⊗ B ⊗ Cin  ........................  (1)
  </p>
<p align="center">
Cout= A.B + (A ⊗ B).Cin ............................ (2)
</p>

# Methodology
We know that a _Full adder_ can be designed using two _Half Adder_ circuits. So first we have to consider an _Half Adder_ Circuit.

<b>•Truth Table of Half Adder</b></br>
<div align="center">
  
|A | B |Sum|Carry|
|:-|:-:|:-:|:-:|
|0 | 0 | 0 | 0 | 
|0 | 1 | 1 | 0 | 
|1 | 0 | 1 | 0 | 
|1 | 1 | 0 | 1 | 
  
</div>
<div>
  
  <p align="center">
<b>Table:2 Truth Table of 1-Bit Half Adder</b></br>
</p>
<b>•Output Expressions for the 1- Bit Half Adder</b></br>

 <p align="center">
Sum=A ⊗ B   ........................  (1)
  </p>
<p align="center">
Carry= A.B ............................ (2)
</p>


<b>•Circuit Diagram of the 1- Bit Half Adder</b></br>

<p align="center" width="100%">
  
<img width="50%" src="https://user-images.githubusercontent.com/65393666/155495727-aaa770b7-1334-4017-b668-d111ae0caca0.png">

</p>

<p align="center">
<b>Fig:1 Half Adder Circuit</b></br>
</p>

<b>•Full Adder using Half Adder</b></br>

<p align="center" width="100%">
  
<img width="100%" src="https://user-images.githubusercontent.com/65393666/155501100-bb537e09-cf9b-4424-a8f4-eb63d73d9eea.png">

</p>

<p align="center">
<b>Fig:2 Full Adder using two Half Adder Circuits</b></br>
</p>

# Schematic

# Output Waveform
# Generetaed Netlist
# Reference
# Acknoledgement
# Author


