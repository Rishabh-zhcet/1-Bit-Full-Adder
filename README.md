# Design-implementaion-of-a-1-Bit-Full-Adder-using-28-nm-CMOS-technology
This repository presents the design and implementation of a 1-Bit Full Adder circuit using 28 CMOS technology. All the Simulations are done on Synopsis tool. For the representation of inputs and outputs, we have taken voltage range 0v to 1.8v. The truth table of the 1- Bit Full Adder is verified by the waveform obtained from the simulation. Full adder can be designed using two Half adders but this design is a little modified version with less no of MOSFETs. 

# Table of Contents
* [Introduction](#Introduction)
* [Tool Used](#Tool-Used)
* [Truth table ](#Truth-table)
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
<p align="center">
<b>• Truth Table of 1-Bit Full Adder</b></br>

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

</p>

# Methodology
We know that a _Full adder_ can be designed using Two _Half Adder_ circuits. So first we have to consider an _Half Adder_ Circuit.

<b>•Truth Table of Half Adder</b></br>


The output expressions for the 1- bit half adder is given by,

SUM=A ⊗ B........................  (1)

Cout= AB .........................  (2)



# Schematic

# Output Waveform
# Generetaed Netlist
# Reference
# Acknoledgement
# Author


