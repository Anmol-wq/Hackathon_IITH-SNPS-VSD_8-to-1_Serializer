# A Tree Architecture Based 8-to-1 Serializer

This repository presents the design and simulation of A  Serializer, one 
of  the  major  components  of  SerDes which is essentially  a  parallel  in  serial out architecture. 
# Table of Contents
- [Abstract](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer/blob/main/README.md#abstract)
- [Tools Used](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer/blob/main/README.md#tools-used)
- [Serializer](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer/blob/main/README.md#gdi-technique)
- [Reference Circuit](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#reference-circuit)
- [A 2-to-1 Mux](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#mux)
- [A D-Flip Flop](https://github.com/Anmol-wq/Hackathon_IITH-SNPS-VSD_8-to-1_Serializer#f)
- [A Positive Latch](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#gdi-exor-gate)
- [A Negative Latch](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#gdi-exnor-gate)
- [An Inverter](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#gdi-nand-gate)
- [A Frequency Divide by 2 circuit](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#gdi-nor-gate)
- [A 2-to-1 Serializer](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#gdi-and-gate)
- [An 8-to-1 Serializer](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#gdi-mux_2x1)
- [Simulations](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#gdi-half-adder)
- [Netlist](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#gdi-full-adder)
- [Challenges](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#gdi-4-bit-vedic-multiplier)
- [Results](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#simulations)
- [Author](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#netlist)
- [Acknowledgements](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#results)
- [References](https://github.com/Rahesh31/4-bit-Vedic-Multiplier#author)


# Abstract

# Tools Used
- Synopsys Custom Compiler:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.
- Synopsys Primewave:  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.
- Synopsys 28nm PDK:  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# Reference Circuit

  
<p align="center">
  <img src=file:///home/anmol/Downloads/serializer.png![image](https://user-images.githubusercontent.com/73732594/156291568-577162f6-6ef1-4da4-b112-72ccdf73756f.png)> <br>
</p>
<p align="center">
  <b> Basic GDI Cell </b> <br>
</p>
<p align="center">
  <img align="center" src="https://user-images.githubusercontent.com/54439300/155850955-8e8cabae-b10c-4bac-a258-d1dd97dd9223.png"> <br>
</p>
<p align="center">
  <b> Implementation of Boolean circuit using GDI </b> <br>
</p>

# 

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155850962-07d71dcf-ab2a-4508-8cb2-cc3ca481dd86.png"> <br>
</p>
<p align="center">
  <b> Multiplication of two 4-bit numbers using urdhvatiryakbhyam </b> <br>
</p>

# Reference Circuit

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155850973-adea210c-366a-49fc-a0c3-8b65bc75c646.png"> <br>
</p>
<p align="center">
  <b> </b> <br>
</p>

# 

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155852709-d84adc05-ab04-4ac6-9d4c-db89ffa0c5ce.png"> <br>
</p>

# 

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155852802-994e6f5c-641e-43e9-8466-453f7eec0bf1.png"> <br>
</p>

# 

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155852901-1e7bdec3-43c0-4c5e-8379-246b42faf8e3.png"> <br>
</p>

# 

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155853101-47c7d0a2-7861-45f7-8b0a-7c555202501e.png"> <br>
</p>

# 

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155853183-c798b780-860d-4160-914b-f3ddbd10b98d.png"> <br>
</p>

# 

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155853254-f41ef122-ad8b-4059-977f-be24326a076d.png"> <br>
</p>

# 

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155853291-e3d426e3-39fe-4168-872d-1268b60b99aa.png"> <br>
</p>

# 

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155853374-2009ff1f-f84c-4505-8d16-0e4e7e1dab38.png"> <br>
</p>

# 

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155853422-961f5cd0-de33-45aa-9862-e9a826da669d.png"> <br>
</p>

# 

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155854044-d2aff17b-cff7-4dd7-8093-2583e46ca640.png"> <br>
</p>

# Simulations

# Transient Analysis

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155855198-dfea5acb-f505-4889-831c-497f9ab527b7.png"> <br>
</p>
<p align="center">
  <b> Testbench Schematic for Transient Analysis </b> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155855388-14e686b1-172c-4f27-8e12-d356eef5b247.png"> <br>
</p>
<p align="center">
  <b> Transient Analysis Inputs </b> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/54439300/155855369-c4e4eeab-d86e-415d-b1f6-3912029e9a5b.png"> <br>
</p>
<p align="center">
  <b> Transient Analysis Outputs </b> <br>
</p>


# Netlist

Netlist of the Circuit can be found [here]()

# Results



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

[1] [Assaad,  Maher,  “Design  and  modelling  of  clock  and 
data  recovery  integrated  circuit  in  130  nm  CMOS 
technology  for  10  Gb/s  serial  data  communications. 
PhD thesis, University of Glasgow, 2009.](https://theses.gla.ac.uk/707/)
[2] [R. Navid et al., "A 40 Gb/s Serial Link Transceiver in 
28 nm CMOS Technology," in IEEE Journal of Solid-
State Circuits, April 2015.](https://ieeexplore.ieee.org/document/6991609)
[3] [A. A. Suhani S.H., N. Prasad S. and K. S. S. Reddy, "A 
20  Gb/s  Latency  Optimized  SerDes  Transmitter  for 
Data Centre Applications," IEEE CONECCT, 2020.](https://ieeexplore.ieee.org/document/9198598)
[4] [Nivedita Jaiswal, Radheshyam Gamad. "Design of a New Serializer and Deserializer Architecture for On-Chip SerDes Transceivers". Circuits and Systems Vol.06 No.03, 2015](https://www.scirp.org/html/5-7600373_55133.htm)
[5] Synopsys Custom Compiler Tutorial by Sameer Durgoji on the Hackathon Platform.

.

