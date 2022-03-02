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
# Serializer

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156292996-b3db83c6-16c7-46cd-b0c6-b3ff87dc682b.png"> <br>
</p>
<p align="center">
  <b> Serializer Operation </b> <br>
</p>
# Reference Circuit

  
<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156291568-577162f6-6ef1-4da4-b112-72ccdf73756f.png"> <br>
</p>
<p align="center">
  <b> Serializer 8-to-1 </b> <br>
</p>
<p align="center">
  <img align="center" src="https://user-images.githubusercontent.com/73732594/156292110-28235f4f-f37b-4c8c-98e0-3022a8440446.png"> <br>
</p>
<p align="center">
  <b> As Submitted in Literature Survey </b> <br>
</p>

# A 2-to-1 Mux

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156293283-cd78d99a-f466-4e8c-a791-6b10ebd25a64.png")
> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156293438-88739e61-45df-4888-a1af-a00c51fab1b5.png"> <br>
</p>

# A D-Flip Flop

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156293584-c8b7868b-21a9-4d6d-bad8-33840378b954.png"> <br>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/73732594/156293660-f582f77f-6d21-43da-a2e9-e94a04edeace.png"> <br>
</p>

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
  <img src="https://user-images.githubusercontent.com/73732594/156299239-4c238dd3-1605-47fd-bbb6-0f3fe8427793.png"> <br>
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

# Transient Analysis

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
  <img src="https://user-images.githubusercontent.com/73732594/156300095-e8ff8a6c-0d88-4458-989c-1b0ae09bd31a.png"> <br>
</p>
<p align="center">
  <b> Reference successfully reproduced </b> <br>
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

