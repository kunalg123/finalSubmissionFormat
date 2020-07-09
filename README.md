# INCOMPLETE!!!!!

# Bandgap Reference Design 
This project simulates the designed Bandgap Reference circuit to determine its performance characterisitics pre-layout and post-layout. 

*Note: Circuit requires further optimization to improve performance. Design yet to be modified.*


## A Glance at the Bandgap Reference IP

To learn more about Bandgap Reference, its principle of generation, Implementation, Issues & Improvements, consider reading [this](/Documentation/BGR.pdf).

To gain insight into the applications and significance of Bandgap Reference in VLSI, have a look at [this](/Documentation/Applications.pdf).

To review the previous Bandgap Reference Design, read [this](/Documentation/README_old_version.md).

The  Design Specifications of the Bandgap Reference Circuit can be found [here](/Documentation/Specifications.pdf).


## Block Diagram of the Bandgap Reference IP

 <p align="center">
  <img width="800" height="500" src="/Images/New/block.png">
</p>


*Note: Enable functionality has not been implemented. Only Simulations have been performed and verified. Layout with enable functionality will be updated soon.*



## Circuit Diagram of the Bandgap Reference IP

 <p align="center">
  <img width="800" height="500" src="/Images/New/circuit.png">
</p>

## Layout of the Bandgap Reference IP

 <p align="center">
  <img width="800" height="500" src="/Images/New/layout.png">
</p>

**Disclaimer:** 




**1. Layout is incomplete owing to non-availability of Vertical PNP BJT model definition in the Open-Sourced 180nm Technology Files provided by OSU.** 

**2. Layout of the Vertical PNP BJT is still in the development phase and will be updated soon.**








## PreLayout Performance Characteristics

###  Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/New/pre/pre_temp.png">
</p>


###  Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/New/pre/pre_vdd.png">
</p>

###  Temperature Coefficient of Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/New/pre/pre_tc.png">
</p>

###  Voltage Coefficient of Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/New/pre/pre_vc.png">
</p>

###  Start-Up Time of Vbgp @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/New/pre/pre_startup.png">
</p>


###  On-Current of Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/New/pre/pre_current.png">
</p>

## PostLayout Performance Charcateristics

###  Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/New/post/post_temp.png">
</p>


###  Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/New/post/post_vdd.png">
</p>

###  Temperature Coefficient of Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/New/post/post_tc.png">
</p>

###  Voltage Coefficient of Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/New/post/post_vc.png">
</p>



###  On-Current of Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/New/post/post_current.png">
</p>


<img align="left" width="60" height="50" src=/Images/ng_logo.png>







## Author

**Sheryl Serrao** 


## Acknowledgments

- [Spice Model files](https://github.com/kunalg123/flipflop_design)
- [LTspice Reference](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html)
- [Wine Reference](https://help.ubuntu.com/community/Wine)

## Contact Information

- Sheryl Serrao, Undergraduate Student, Mumbai University sherylcorina@gmail.com
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com
- Philipp Gühring, Software Architect, LibreSilicon Assocation pg@futureware.at
- Dr. Gaurav Trivedi Co-Principal Investigator, EICT Academy, IIT Guwahati trivedi@iitg.ac.in

