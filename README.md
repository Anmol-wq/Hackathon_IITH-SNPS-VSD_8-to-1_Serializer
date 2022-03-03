# A Tree Architecture Based 8-to-1 Serializer

This repository presents the design and simulation of A  Serializer, one 
of  the  major  components  of  SerDes which is essentially  a  parallel  in  serial out architecture. 

# Table of Contents
- [Abstract](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer/blob/main/README.md#abstract)
- [Tools Used](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer/blob/main/README.md#tools-used)
- [Serializer](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer/blob/main/README.md#serializer)
- [Reference Circuit](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#reference-circuit)
- [A 2-to-1 Mux](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#mux2-to-1)
- [A D-Flip Flop](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#f-f)
- [A Positive Latch](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#p-latch)
- [A Negative Latch](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#n-latch)
- [An Inverter](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#inv-erter)
- [A Frequency Divide by 2 circuit](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#f-by-2)
- [A 2-to-1 Serializer](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#ser-2)
- [An 8-to-1 Serializer](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#ser-8)
- [Simulations](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#simula-tions)
- [Netlist](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#net-list)
- [Challenges](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#chall-enges)
- [Results](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#res-ults)
- [Author](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#auth-or)
- [Acknowledgements](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#acknowledge-ments)
- [References](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#ref-s)


# Abstract
Based on the 2-to-1 Serializer developed, one can use this architecture to implement a multiplexer with a larger number of input channels. Most of them are based on the topology of tree structure. As illustrated in the figure, the tree structure is a natural extension of the 2-to-1 unit, the idea is to group the input channels in pairs and multiplex each pair, reducing the number by a factor of two after each rank. In this architecture, the flip-flop is driven by a clock frequency fck, the serializer in rank 3 is driven by a clock frequency fck/2, in rank 2 are driven by a clock frequency fck/4, and those in the rank1 are driven by a clock frequency fck/8.


# Tools Used
- Synopsys Custom Compiler:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis. This tool was used to design the circuit on a transistor level. Steps were followed from the provided doc at Hackathon platform to setup defs file at the following location.

- Synopsys Primewave:  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.
- Synopsys 32-28nm SAED_PDK:  SAED 32-28nm was used for model library files, and at Typical corner for both p and nMOS (TT).

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156302649-dbdff5e0-b03f-440e-9207-402197de8c0a.png"> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156302916-c55971e2-ac80-423e-879c-7c30fe8d621f.png"> <br>
</p>


# Serializer

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156292996-b3db83c6-16c7-46cd-b0c6-b3ff87dc682b.png"> <br>
</p>
<p align="center">
  <b> Serializer Operation </b> <br>
</p>

- This figure explains the working of a 2-to-1 serializer, 7 of which are used further ahead for creating the 8-to-1 serializer here.

# Reference Circuit
 
<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156291568-577162f6-6ef1-4da4-b112-72ccdf73756f.png"> <br>
</p>
<p align="center">
  <b> Serializer 8-to-1 </b> <br>
</p>

- The pin ordering here is utilized to obtain the serial data in format D1-D2-D3-...-D8. Also, the clock pins are being taken independently, which is made a note of.
- The above two facets facilitated the final implementation. 

<p align="center">
  <img align="center" src="https://user-images.githubusercontent.com/73732594/156292110-28235f4f-f37b-4c8c-98e0-3022a8440446.png"> <br>
</p>
<p align="center">
  <b> As Submitted in Literature Survey </b> <br>
</p>

- The overall structure here is replicated in the final implementation,but making use of pin-orderings and clock facilitation at each rank as per the figure before it.
 

# A 2-to-1 Mux

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156293283-cd78d99a-f466-4e8c-a791-6b10ebd25a64.png")
> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156293438-88739e61-45df-4888-a1af-a00c51fab1b5.png"> <br>
</p>

This is a transmission-gate based 2:1 mux as seen in "Digital Integrated Circuits" by Prof. Jan Rabaey.

# A D-Flip Flop

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156293584-c8b7868b-21a9-4d6d-bad8-33840378b954.png"> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156293660-f582f77f-6d21-43da-a2e9-e94a04edeace.png"> <br>
</p>

The D-flip flop implementation as a circuit contains a positive and a negative latch, along with inverters and muxes. And thus, consists of sub-circuits which are to be utilized for this design.

# A Positive Latch

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156293845-a7e11e28-2517-4185-bd66-197b4c9136d4.png"> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156293968-b9bee395-5ee9-45fe-b7ad-9fac507b4612.png"> <br>
</p>

# A Negative Latch
<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156294116-df13dde8-b790-4e1b-88f9-1abb0aa6a997.png"> <br>
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156294170-242b43ee-5176-49ff-b46b-61e907e611a5.png"> <br>
</p>


# An Inverter

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156294302-9d189706-72e9-4302-a35a-da8a59ded70d.png"> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156294373-b61434d4-6376-42b7-a76b-52d5ab2b90aa.png"> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156294643-4b98e8eb-c078-4a48-a7c3-7afdcf70f1d8.png"> <br>
</p>

# A Frequency Divide by 2 circuit

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156298051-4148376e-6856-41b2-ba0f-afca57ccf157.png"> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156298569-974a956a-0c4f-4ffe-b09b-fa1f7fff2284.png"> <br>
</p>

# A 2-to-1 Serializer

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156298758-a266297f-76c3-437a-b7a9-b83b084d8009.png"> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156298940-92a003e8-9311-4d0f-8668-97cfb9d0d844.png"> <br>
</p>

# An 8-to-1 Serializer
<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156299239-4c238dd3-1605-47fd-bbb6-0f3fe8427793.png"> <br>
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156300836-4426c15c-76a7-4db6-a012-3eb0d0d11b8f.png"> <br>
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156299345-3c217c79-c94e-4ed0-bba8-015cb680d163.png"> <br>
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156299481-8639a2a3-7ddd-4a0f-b262-4a20b2deea03.png"> <br>
</p>
<p align="center">
  <img src="file:///home/anmol/Pictures/Screenshot%20from%202022-03-01%2023-25-35.png![image](https://user-images.githubusercontent.com/73732594/156299644-32f4143a-13ac-4d32-909d-6a0b881893b8.png)
"> <br>
</p>

# Simulations

## Transient Analysis

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156299815-46508a6d-ea9a-4a2f-a317-a9c510e3abb5.png"> <br>
</p>


<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156299930-5c2a4d11-6a1e-472b-924e-9acccabc7979.png"> <br>
</p>
<p align="center">
  <b> Transient Analysis </b> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156374501-e69d14e3-3c09-4852-a765-5e26d1fd97d3.png"> <br>
</p>
<p align="center">
  <b> Reference successfully reproduced </b> <br>
</p>

Here, we can see from net1 to the net2 how the data is being serialized out, since the pattern repeats, it has been shown only till 10us.

# Netlist

```
*  Generated for: PrimeSim
*  Design library name: Proposed_ckt
*  Design cell name: as_8to1
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Tue Mar  1 18:15:02 2022

.global gnd!
********************************************************************************
* Library          : Proposed_ckt
* Cell             : as_2to1_serializer
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt as_2to1_serializer clk out din1 din2
xm54 net24 clk net25 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm53 net25 clkb net10 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm52 net9 net25 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm51 net10 net9 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm46 net12 clk net14 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm41 net14 clkb net8 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm42 net7 net14 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm45 net8 net7 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm38 net6 net5 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm37 net5 net12 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm36 net12 clk net6 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm35 din1 clkb net12 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm30 net4 net3 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm29 net3 net24 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm28 net24 clk net4 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm8 din2 clkb net24 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm27 net2 net1 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm24 net1 net17 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm22 net17 clk net2 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm20 net14 clkb net17 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm9 clkb clk vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm1 out clk net25 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm0 out clkb net17 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm50 net24 clkb net25 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm49 net25 clk net10 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm48 net9 net25 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm47 net10 net9 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm39 net12 clkb net14 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm40 net14 clk net8 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm43 net7 net14 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm44 net8 net7 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm34 net6 net5 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm33 net5 net12 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm32 net12 clkb net6 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm31 din1 clk net12 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm7 net4 net3 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm6 net3 net24 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm5 net24 clkb net4 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm2 din2 clk net24 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm26 net2 net1 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm25 net1 net17 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm23 net17 clkb net2 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm21 net14 clk net17 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm3 out clk net17 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm4 out clkb net25 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm10 clkb clk gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
v12 vdd gnd! dc=1.8
.ends as_2to1_serializer

********************************************************************************
* Library          : Proposed_ckt
* Cell             : as_dff_new
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt as_dff_new clk q din
xm26 net98 q gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm25 q net90 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm23 net90 clkb net98 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm21 net103 clk net90 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm18 net64 net103 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm17 net103 net56 gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm14 net56 clk net64 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm12 din clkb net56 gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm5 clkb clk gnd! gnd! n105 w=0.1u l=0.04u nf=1 m=1
xm27 net98 q vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm24 q net90 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm22 net90 clk net98 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm20 net103 clkb net90 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm19 net64 net103 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm16 net103 net56 vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
xm15 net56 clkb net64 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm11 din clk net56 vdd p105 w=0.15u l=0.04u nf=1 m=1
xm4 clkb clk vdd vdd p105 w=0.15u l=0.04u nf=1 m=1
v8 vdd gnd! dc=1.8
.ends as_dff_new

********************************************************************************
* Library          : Proposed_ckt
* Cell             : as_8to1_symbol
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt as_8to1_symbol clk clk1 clk2 clk3 out din1 din2 din3 din4 din5 din6 din7
+  din8
xi6 clk1 g e f as_2to1_serializer
xi5 clk2 f c d as_2to1_serializer
xi4 clk2 e a b as_2to1_serializer
xi3 clk3 d din8 din4 as_2to1_serializer
xi2 clk3 c din6 din2 as_2to1_serializer
xi1 clk3 b din7 din3 as_2to1_serializer
xi0 clk3 a din5 din1 as_2to1_serializer
xi7 clk out g as_dff_new
.ends as_8to1_symbol

********************************************************************************
* Library          : Proposed_ckt
* Cell             : as_8to1
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xi0 0_1 1 2 3 out din1 din2 din3 din4 din5 din6 din7 din8 as_8to1_symbol
v42 din3 gnd! dc=0 pulse ( 0 1.8 7n 0.2n 0.2n 16n 32n )
v44 din5 gnd! dc=0 pulse ( 0 1.8 2n 0.2n 0.2n 16n 32n )
v46 din7 gnd! dc=0 pulse ( 0 1.8 8n 0.2n 0.2n 16n 32n )
v47 din8 gnd! dc=0 pulse ( 0 1.8 8n 0.2n 0.2n 32n 64n )
v43 din4 gnd! dc=0 pulse ( 0 1.8 7n 0.2n 0.2n 32n 64n )
v45 din6 gnd! dc=0 pulse ( 0 1.8 2n 0.2n 0.2n 32n 64n )
v33 din1 gnd! dc=0 pulse ( 0 1.8 3n 0.2n 0.2n 16n 32n )
v41 din2 gnd! dc=0 pulse ( 0 1.8 3n 0.2n 0.2n 32n 64n )
v32 3 gnd! dc=0 pulse ( 0 1.8 0 0.2n 0.2n 8n 16n )
v31 2 gnd! dc=0 pulse ( 0 1.8 0 0.2n 0.2n 4n 8n )
v30 1 gnd! dc=0 pulse ( 0 1.8 0 0.2n 0.2n 2n 4n )
v27 0_1 gnd! dc=0 pulse ( 0 1.8 0 0.2n 0.2n 1n 2n )








.tran '0.1n' '100n' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(0_1) v(1) v(2) v(3) v(out) v(din1) v(din2) v(din3) v(din4) v(din5)
+ v(din6) v(din7) v(din8)

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end


```
As we can see the (W/L)pMOS=(0.15u/0.04u), and (W/L)nMOS=(0.15u/0.04u) is used consistently throughout the design.

# Challenges

- Initially, instead of symbols, the whole circuit consisted of actual schematics instead of their generated symbols. This led to visibility issue as circuit is big. Appropriate symbols were created to facilitate better maneuverablity. 
- The frequency divider circuit is yielding latency issues, so as per literature survey, it was concluded that a PLL may be assumed to provide the required clocks at the three ranks respectively, at the same time.

# Results

The circuit has been simulated successfully at clock frequency of 500 MHz, and the voltage signal is maintained at 1.8 V throughout, with data input lines transmitting data at 62.5 MHz.

# Author

- [Anmol Saxena, M.Tech ICT, DA-IICT](https://www.linkedin.com/in/anmol-saxena-ee/)

# Acknowledgements

- [Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/)
- [Synopsys Inc](https://www.synopsys.com/)
- [IIT Hyderabad](https://iith.ac.in/)
- [Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)
- [Sameer Durgoji, NIT Karnataka](https://www.linkedin.com/in/sameer-s-durgoji-340b26180/)
- [Chinmay Panda, IIT Hyderabad](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)

# References

- [Assaad,  Maher,  “Design  and  modelling  of  clock  and 
data  recovery  integrated  circuit  in  130  nm  CMOS 
technology  for  10  Gb/s  serial  data  communications. 
PhD thesis, University of Glasgow, 2009.](https://theses.gla.ac.uk/707/)
- [R. Navid et al., "A 40 Gb/s Serial Link Transceiver in 
28 nm CMOS Technology," in IEEE Journal of Solid-
State Circuits, April 2015.](https://ieeexplore.ieee.org/document/6991609)
- [A. A. Suhani S.H., N. Prasad S. and K. S. S. Reddy, "A 
20  Gb/s  Latency  Optimized  SerDes  Transmitter  for 
Data Centre Applications," IEEE CONECCT, 2020.](https://ieeexplore.ieee.org/document/9198598)
- [Nivedita Jaiswal, Radheshyam Gamad. "Design of a New Serializer and Deserializer Architecture for On-Chip SerDes Transceivers". Circuits and Systems Vol.06 No.03, 2015](https://www.scirp.org/html/5-7600373_55133.htm)
- Synopsys Custom Compiler Tutorial by Sameer Durgoji on the Hackathon Platform.

.

