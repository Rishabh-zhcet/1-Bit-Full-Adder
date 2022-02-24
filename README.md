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

As we know that the implementation of universal gates like **NAND** & **NOR** gates require less number of mosfets in comparision with **AND/OR** gates. Hence to reduce the design complexity, we can replace the **AND-AND-OR** logic of the carry with the **NAND-NAND-NAND** logic. The design can be modified as follows:

<p align="center" width="100%">
  
<img width="100%" src="https://user-images.githubusercontent.com/65393666/155504379-6c1d957c-64bf-4c72-b28a-f4d97a920c2b.png">

</p>

<p align="center">
<b>Fig:3 Modified Full Adder Circuit</b></br>
</p>

# Schematic

![Schematic](https://user-images.githubusercontent.com/65393666/155510454-e96140b9-5f59-4eb3-8a88-e929ac95ce81.png)

# Output Waveform

![Output Waveform](https://user-images.githubusercontent.com/65393666/155509859-42d1d695-8467-4640-ab19-993fb5950ab9.png)

# Generetaed Netlist

```
*  Generated for: PrimeSim
*  Design library name: cp_lib
*  Design cell name: 1_Bit_Full_Adder_tb
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Thu Feb 24 10:29:51 2022

.global gnd! vdd!
********************************************************************************
* Library          : cp_lib
* Cell             : 1_Bit_Full_Adder
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt _1_bit_full_adder a b cin cout gnd_1 sum vdd vt_bulk_n_gnd!
+ vt_bulk_p_vdd!
xm46 net152 net156 gnd_1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm44 cout net160 net152 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm43 net146 cin gnd_1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm42 net156 net145 net146 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm41 net140 b gnd_1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm40 net160 a net140 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm36 net125 net119 gnd_1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm35 net122 cin gnd_1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm34 net119 cin gnd_1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm33 net116 net101 gnd_1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm31 net110 b gnd_1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm57 net98 a gnd_1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm28 net101 b gnd_1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm58 net128 net145 gnd_1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm53 sum net128 net125 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm54 sum net145 net122 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm55 net145 net98 net116 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm56 net145 a net110 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm47 sum cin net134 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm48 sum net119 net131 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm50 net145 b net107 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm51 net145 net101 net104 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm26 cout net160 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm25 cout net156 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm24 net156 net145 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm23 net156 cin vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm22 net160 a vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm21 net160 b vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm11 net104 a vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm9 net98 a vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm12 net107 net98 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm17 net131 net145 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm16 net119 cin vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm15 net128 net145 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm10 net101 b vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm18 net134 net128 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
.ends _1_bit_full_adder

********************************************************************************
* Library          : cp_lib
* Cell             : 1_Bit_Full_Adder_tb
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xi19 a b cin cout gnd! sum net8 gnd! vdd! _1_bit_full_adder
v1 net8 gnd! dc=1.8
v4 cin gnd! dc=0 pulse ( 0 1.8 5u 20p 20p 5u 10u )
v3 b gnd! dc=0 pulse ( 0 1.8 10u 20p 20p 10u 20u )
v2 a gnd! dc=0 pulse ( 0 1.8 20u 20p 20p 20u 40u )
c6 cout gnd! c=1p
c5 sum gnd! c=1p








.tran '1us' '40us' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(a) v(b) v(C) v(cout) v(sum)

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end
```


# Reference
# Acknoledgement
# Author


