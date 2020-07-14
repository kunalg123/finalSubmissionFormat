

# Bandgap Reference Design 
This project simulates the designed Bandgap Reference circuit to determine its performance characterisitics pre-layout and post-layout. 

*Note: Circuit requires further optimization to improve performance. Design yet to be modified.*

**To be updated soon**

## A Glance at the Bandgap Reference IP

To learn more about Bandgap Reference, its principle of generation, Implementation, Issues & Improvements, consider reading [this](/Documentation/BGR.pdf).

To gain insight into the applications and significance of Bandgap Reference in VLSI, have a look at [this](/Documentation/Applications.pdf).

To review the previous Bandgap Reference Design, read [this](/Documentation/README_old_1.0.md).

The  Design Specifications of the Bandgap Reference Circuit can be found [here](/Documentation/Specifications.pdf).


## Block Diagram of the Bandgap Reference IP

 <p align="center">
  <img width="800" height="500" src="/Images/N/block.png">
</p>




## Circuit Diagram of the Bandgap Reference IP

 <p align="center">
  <img width="800" height="500" src="/Images/N/circuit.png">
</p>

## Layout of the Bandgap Reference IP

### Layout of the Complete Bandgap Reference Block with Start-up & Power Down

 <p align="center">
  <img width="800" height="500" src="/Images/N/layout.png">
</p>

### Layout of Vertical Parasitic PNP BJT

 <p align="center">
  <img width="500" height="400" src="/Images/N/bjt.png">
</p>




## Pre-Layout Performance Characteristics

###  Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/PRE/pre_temp.png">
</p>


###  Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/PRE/pre_supply.png">
</p>

###  Temperature Coefficient of Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/PRE/pre_tc.png">
</p>

###  Voltage Coefficient of Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/PRE/pre_vc.png">
</p>

###  Start-Up Time of Vbgp @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/PRE/pre_startup.png">
</p>


###  On-Off-Current of Vbgp wrt Enable @ RL = 100M ohms plot

 <p align="center">
  <img width="1000" height="500" src="/Images/N/PRE/pre_c.png">
</p>

**Not:Current without Inverter for Enable Logic**

## PostLayout Performance Charcateristics

###  Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/POST/post_temp.png">
</p>


###  Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/POST/post_supply.png">
</p>

###  Temperature Coefficient of Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/POST/post_tc.png">
</p>

###  Voltage Coefficient of Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/POST/post_vc.png">
</p>



###  Start-Up Time of Vbgp @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/POST/post_startup.png">
</p>


###  On-Off-Current of Vbgp wrt Enable @ RL = 100M ohms plot

 <p align="center">
  <img width="1100" height="500" src="/Images/N/POST/post_c.png">
</p>

**Not:Current without Inverter for Enable Logic**









## Author

**Sheryl Serrao** 


## Acknowledgments


- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd.
- Philipp Gühring, Software Architect, LibreSilicon Assocation
- Saroj Rout, Associate Professor & Chief Mentor of VLSI Center of Excellence SIT, Bhubaneswar, India
- Santunu Sarangi, Asst. Professor, SIT, Bhubaneswar, India
- Tim Edwards, Senior Vice President of Analog and Design at efabless corporation

## Contact Information

- Sheryl Serrao, Undergraduate Student, Mumbai University sherylcorina@gmail.com
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com
- Philipp Gühring, Software Architect, LibreSilicon Assocation pg@futureware.at
- Dr. Gaurav Trivedi Co-Principal Investigator, EICT Academy, IIT Guwahati trivedi@iitg.ac.in

