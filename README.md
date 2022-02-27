# Design-of-two-stage-cmos-operational-amplifier-in-20nm-Technology
This repository presents the design of two stage CMOS operational amplifier implemented using Synopsis Custom Compiler in 20nm Technology.
# Table of Contents
  * [Abstract](#abstract)
  * [Detailed Explanation](#detailed-explanation)
  * [Reference Circuit](#reference-circuit)
          
          [Figure 1]
          [Figure 2]
          [Figure 3]
          
  * [Circuit Design And Console pannel](#circuit-design-and-console-pannel)
  * [Switch Design](#switch-design)
  * [Switch Conections And Console pannel](#switch-conections-and-console-pannel)
  * [Tools Used](#tools-used)
  * [Parameters set for Voltage Source for Input V1](#parameters-set-for-voltage-source-for-input-v1)
  * [Parameters set for Voltage Source for Input V2](#parameters-set-for-voltage-source-for-input-v2)
  * [Parameters set for Voltage Source for Input V3](#parameters-set-for-voltage-source-for-input-v3)
  * [Parameters set for Voltage Source for Input RO](#parameters-set-for-voltage-source-for-input-ro)
  * [Output Waveform](#output-waveform)
  * [Netlist](#netlist)
  * [Conclusion](#conclusion)
  * [Author](#author)
  * [Acknowledgement](#acknowledgement)
  * [References](#references)

## Abstract
Operational amplifier is the
fundamental building block in almost
every analog and mixed signal processing
circuits. This paper presents the design of
a two stage Op-Amp using sub 20 nm
CMOS technology. This design has a
differential amplifier stage and an
additional gain stage, implemented with
minimum number of transistors, so that
the area and power consumption is
optimized. Design and simulation was
done using cadence EDA software tool.
The designed Op-Amp is operating with a
supply voltage of 800 mV and a bias
current of 10µA.The design attains an
open loop gain of 88.74dB with unity gain
bandwidth of 50.7 MHz and a phase
margin of 57.98 degree with load
capacitor of 1 pF.
     
     Keywords- 2 stage CMOS Operationaloperational amplifier, Stability, Frequency
     Compensation, Low power.
     
 ##  Detailed Explanation
Nanometer CMOS technologies play a key role for the improvement of the mixedsignal systems, thanks to the high integration level of analog and digital circuits in the same die area. Even if digital signal processing is replacing some analog operations, the mixed-signal systems require anyway an analog front-end able to manage and convert the external signals. This means that the weak analog performance but also the advantages of the ultra-scaled technologies must be managed. In particular, the scaling-down of physical and electrical parameters leads to improvements for digital circuits on one side, while a lot of design issues for analog circuits on the other side. To cope with market requirements but also the analog design limits, advanced lithography techniques, new material like high-K/metal gate (HKMG), and new devices, as finfet or thinfet, have been introduced.

In this thesis, the main key challenges in ultra-scaled technologies are analysed, and then integrated circuits designed in 20nm CMOS technology are presented. The first chapter focuses on trends in device characteristics and how they influence the performance of nanoscale CMOS technologies circuits. The second chapter shows the design in 20nm CMOS technology of a Fast Tracker Front-End (FTFE) for charge detection, starting from the requirements and the circuital solutions actually employed for ATLAS MDT detectors read-out electronic. The purpose of the project was to implement an efficient system, able to detect consecutive input events, avoiding long dead time e signal losses. The specific architecture is analysed and the resulting performance are shown. In the third chapter a Chopper Instrumentation Amplifier designed in 20nm CMOS technology is presented. It is an amplifier characterized by the use of a modulation technique, called chopper, in order to meet the low offset and low flicker noise requirements, important in sensors and monitoring applications. In particular the three-stage operational amplifier has been designed to work in sub-threshold region, in order to address the scaling problems. After the architecture and the design procedure description, the results of the integrated prototype are shown. At the end some conclusions are drawn.


## Reference Circuit
This paper is organized as follows.
Section 2 presents the two stage
amplifier. Section 3 reviews the 2 stage
CMOS Op amp design with compensation
capacitor. Its specifications are briefly
clarified. Section 4 presents the simulation
results of the proposed op-amp and finally
in Section 5 give my concluding remarks.
Two-stage OP-AMP mainly consists of a
cascade of Voltage to Current and Current
to voltage stages. The first stage consists
of a differential amplifier converting the
differential input voltage to differential
currents. These differential currents are
applied to a current mirror load recovering
the differential voltage. The second stage
consists of common source MOSFET
converting the second stage input voltage
to current. This transistor is loaded by a
current sink load, which converts the
current to voltage at the output.<br/>
          [Figure 1]<br/>
![A general two stage CMOS Op-amp](https://user-images.githubusercontent.com/99643808/155873803-58f3a933-3c0c-4c79-9551-68f02e5ad0d5.png)<br/>
          [Figure 2]<br/>
![wave form in graph ](https://user-images.githubusercontent.com/99643808/155874009-c58a6f31-79c8-45e9-9a7e-d63fc705548a.jpg)<br/>
          [Figure 3]<br/>
![ Topology chosen for this paper](https://user-images.githubusercontent.com/99643808/155874037-7f130957-807d-4351-a1ac-f25a310cb910.png)
## Tools Used

- Synopsys Custom Compiler:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.

![custom_compiler](https://user-images.githubusercontent.com/59500283/155473715-c6a1fd5b-71c7-4655-936a-5fe3befabfd8.png)

- Synopsys Primewave:  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.
- Synopsys 20nm PDK:  The Synopsys 20nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

## Circuit Design And Console pannel

![circuit design](https://user-images.githubusercontent.com/99643808/155874362-a58f55ce-c25a-43ef-abdb-86b301234198.jpeg)

Fig 1. This circuit Consists of a cascode of Voltage to Current and Current to voltage stages. First stage consists of a differential amplifier of NMOS transistor (M1,M2) converting the differential input voltage to differential currents. Which are applied to a current mirror load of PMOS transistor(M3,M4) recovering the voltage.
The second stage consists of common source MOSFET converting the second stage input voltage to current. This transistor is loaded by a current sink load, which converts the current to voltage at the output. CL is the load capacitor and Cc is the compensation capacitor required for stability.

![console of Fif 1.](https://user-images.githubusercontent.com/99643808/155874534-056957da-47d0-4442-82e6-9a0f5a213064.jpeg)

## Switch Design

![CMOS_OP_AMP_NEW_switch](https://user-images.githubusercontent.com/99643808/155874621-62d0c59e-f390-4f25-91d0-156a0ea78524.jpeg)

## Switch Conections And Console pannel

![Switch Conections](https://user-images.githubusercontent.com/99643808/155874768-29aff19e-dce9-445e-9f5d-5502c69980a4.jpeg)


In this section, we present the results obtained for diffrent designs. A 1.2μm CMOS technology with oxide thickness 20nm, NMOS threshold voltage of 0.7V, and PMOS
threshold voltage of -0.9V was used. Common mode input voltage was fixed at half the supply. The output voltage
ranged from 0.5V to 0.5V below the supply . The load
capacitance was held constant at 3pF. Supply voltage was
5V, phase margin was 60
, and gain was  10kV=V.
In the  experiment, we compare the results of cancelling the feedforward zero with the nulling resistor to the
results of cancelling the second dominant pole. 


![Switch Conections Console Pannel](https://user-images.githubusercontent.com/99643808/155874770-c9ab4c9f-0e4c-4bbb-966f-d0f310720db7.jpeg)

Figure 2 shows the console of the switch circuit which denotes there is no error in the circuit below.

## Parameters set for Voltage Source for Input V1
![ Parameters set for Voltage Source for Input V1](https://user-images.githubusercontent.com/99643808/155875254-fd2e4bea-9db1-462a-b4ea-ea143dcac0b5.jpeg)


## Parameters set for Voltage Source for Input V2
![Parameters set for Voltage Source for Input V2](https://user-images.githubusercontent.com/99643808/155875256-55fab6ec-59e8-4645-b1a8-ff232923662c.jpeg)


## Parameters set for Voltage Source for Input V3
![Parameters set for Voltage Source for Input V3](https://user-images.githubusercontent.com/99643808/155875258-ca78ad64-1671-447f-b3b2-d43cfd612eda.jpeg)


## Parameters set for Voltage Source for Input RO
![Parameters set for Voltage Source for Input RO](https://user-images.githubusercontent.com/99643808/155875261-3b45115b-4915-4762-99ff-b2d224e7f6e1.jpeg)

## Output Waveform

![Output-waveform-of-two-stage-CMOS-amplifier-Frequency-Response-of-the](https://user-images.githubusercontent.com/99643808/155875381-340b3284-e9ca-459a-87e1-1d4d968ca5e3.png)

## Netlist


![Image 1](https://user-images.githubusercontent.com/99643808/155875646-baa512f9-635b-4c83-9453-49e2b6d93ee8.jpeg)

![Image 2](https://user-images.githubusercontent.com/99643808/155875648-c5444ba0-f56d-4610-8488-4a201f66a24d.jpeg)

## Conclusion

In this thesis, integrated circuit designs in 20 nm CMOS technology have been presented, with different application fields. The aim of this works was to study and analyse the advantages and especially the limits of the ultra-scaled technologies, as the 20 nm CMOS technology. Supply and threshold voltage ratio reduction, reduced intrinsic gain, worse PVT variations, restrictive layout rules, but also better transition frequency, mismatch variation and radiation hardness, have been described. Improvements for digital circuits on one side, a lot of analog design issues on the other side, characterize the scaled technologies, because of the poor analog performance. Different solutions and approaches have been used to face with the technology issues, circuital and of layout.

## Author

R ROHIT KUMAR, B.Tech(CSE), National Institute of Science And Technology Berhampur,  ODISHA 760005

## Acknowledgement

- [Kunal Ghosh, Co-founder, VSD Corp. Pvt Ltd.](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3B0xcWjpLDThSEo6S9UPO9Tw%3D%3D)
- [Chinmay panda, IIT Hyderabad](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)
- [Synopsis Team/Company](synopsys.com/company/contact-synopsys/office-locations/india/about-synopsys-india.html)
- [IIT Hyderabad](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)
- [Cloud Based Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/')
- [Synopsys India](https://www.synopsys.com/)
- [Sameer Durgoji, NIT Karnataka](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)


## References

[1] P.E. Allen and D.R. Holberg, “CMOS Analog Circuit
Design” Oxford University Press, 2nd edition.<br/>
[2] D. A. Johns and K. Martin, “Analog Integrated Circuit
Design,” New York: John Wiley & Sons, Inc., 1997.<br/>
[3] Google<br/>
[4] B. Razavi, “Design of Analog CMOS Integrated
Circuits,” Tata McGraw-Hill, 2002<br/>
[5] Amana Yadav, “A Review Paper On Design And
Synthesis Of Two stage CMOS Op-amp” ©Ijaet Issn:
2231-1963677 Vol. 2, Issue 1, Pp. 677-688<br/>
[6]	M.Jyothi, L.Ravi Chandra, J.Poornima,k.Rajasekhar , S.Daya Sagar Chowdary, “Design Of Two Stage Operational Amplifier On Zero Cross Detector Using 0.18μm Technology” International Journal Of VLSI & Signal Processing Applications, Vol2, Issue2 , April 2012, ISSN 2231-3133 ( 189- 195)<br/>
[7]	Suparshya Babu Sukhavasi1,susrutha Babu Sukhavasi, Dr.Habibulla Khan, S R Sastry Kalavakolanu,vijaya Bhaskar Madivada, Lakshmi Narayana Thalluri, “Design Of A Low Power Operational Amplifier By Compensating The Input Stage” (IJERA) ISSN: 2248-9622,Vol. 2, Issue 2,mar-apr 2012, Pp.1283-1287<br/>
[8]	Bekkam Satheesh1, N.Dhanalakshmi2, Dr.N.Balaji3, “Design of a Low-Voltage, Low-Power, High-Gain Operational Amplifier for Data Conversion Applications.” (IJERA) ISSN: 2248-9622 , Vol. 2, Issue 3, May-Jun 2012, pp.1030-1036<br/>
[9]	Priyanka Kakoty, “Design of a high frequency low voltage CMOS operational amplifier”, International Journal of VLSI design & Communication Systems (VLSICS) Vol.2,
No.1, March 2011

