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





## Performance Characteristics


### PreLayout Performance Characteristics

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

### PostLayout Performance Charcateristics




<img align="left" width="60" height="50" src=/Images/ng_logo.png>

## About Ngspice 
Ngspice is an open source mixed-signal circuit simulator.

### Installing Ngspice

#### For Ubuntu

Open your terminal and type the following to install Ngspice
```
$  sudo apt-get install -y ngspice
```

## Running the Simulation

To clone the Repository and download the Netlist files for Simulation, enter the following commands in your terminal.

```
$  sudo apt install -y git
$  git clone https://github.com/sherylcorina/BandgapReference
$  cd BandgapReference/Simulation/Ngspice_Simulation/Simulation_Week_4_5
```

*Note: Before running simulation, ensure that the osu018.lib file is in the same directory as the other .cir files. Else you will need to modify the .cir files and add the approporiate path of osu018.lib*

To enter the Ngspice Shell, open the terminal & type:
```
$ ngspice
```
To simulate a netlist, type:
```
ngspice 1 ->  source <filename>.cir
```

You can exit from the Ngspice Shell by typing:
```
ngspice 1 ->  exit
```
 <p align="center"> or </p>
 
```
ngspice 1 ->  quit
```

There are several waveforms that need to be obtained to observe the performance of the Bandgap reference circuit.

*****************************

### To obtain the Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot

Open your terminal and change the working directory to the folder where your netlist file is saved.
Run the netlist file using the following command.
```
$  ngspice temp_variation.cir
```
 <p align="center">
  <img width="800" height="500" src="/Images/s.temp_variation.png">
</p>


### To obtain the Vbgp v/s VDD [ 2V - 4V ] @ RL = 100M ohms plot
Open your terminal and change the working directory to the folder where your netlist file is saved.
Run the netlist file using the following command.
```
$  ngspice supply_variation.cir
```
 <p align="center">
  <img width="800" height="500" src="/Images/s.supply_variation.png">
</p>

### To obtain the Temperature Coefficient of Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot
Open your terminal and change the working directory to the folder where your netlist file is saved.
Run the netlist file using the following command.
```
$  ngspice ppm_variation.cir
```
 <p align="center">
  <img width="800" height="500" src="/Images/s.ppm.png">
</p>

### To obtain the Voltage Coefficent of Vbgp v/s VDD [ 2V - 4V ] @ RL = 100M ohms plot
Open your terminal and change the working directory to the folder where your netlist file is saved.
Run the netlist file using the following command.
```
$  ngspice vc_variation.cir
```
 <p align="center">
  <img width="800" height="500" src="/Images/s.vc_variation.png">
</p>

### To obtain the Start Up Time plot

Open your terminal and change the working directory to the folder where your netlist file is saved.
Run the netlist file using the following command.
```
$  ngspice startup.cir
```
 <p align="center">
  <img width="800" height="500" src="/Images/s.startup.png">
</p>


### To observe the Output Noise Spectral Density plot


Open your terminal and change the working directory to the folder where your netlist file is saved.
Run the netlist file using the following command.
```
$  ngspice noise_analysis.cir
```
 <p align="center">
  <img width="800" height="500" src="/Images/s.noise_analysis.png">
</p>





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

