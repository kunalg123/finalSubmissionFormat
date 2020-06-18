# Bandgap Reference Simulation 
This project simulates the designed Bandgap reference circuit to determine its performance characterisitics. 

*Note: Circuit not designed for optimal performance. Design yet to be modified.*


## A Glance at the Bandgap Reference IP

To learn more about Bandgap Reference, its principle of generation, Implementation, Issues & Improvements, consider reading [this](/BGR.pdf).

To gain insight into the applications and significance of Bandgap Reference in VLSI, have a look at [this](/Applications.pdf).


<div align="center"><b>Bandgap Reference Circuit Diagram</b></div>

<p align="center">
  <img width="500" height="350" src="/Images/bgr_circuit.png">
</p>


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

Download all files from the *Ngspice Simulation* Folder.

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


### To obtain the Vref @  VDD=3.3V & Temp= 27 C over 100ns plot

Open your terminal and change the working directory to the folder where your netlist file is saved.
Run the netlist file using the following command.
```
$  ngspice bandgap.cir
```
 <p align="center">
  <img width="800" height="500" src="/Images/ng_bandgap.png">
</p>


### To obtain the Vref, PTAT & CTAT voltages over -50 C through 200 C
Open your terminal and change the working directory to the folder where your netlist file is saved.
Run the netlist file using the following command.
```
$  ngspice ptat+ctat.cir
```
 <p align="center">
  <img width="800" height="500" src="/Images/ng_PTAT+CTAT.png">
</p>

### To obtain the Vref over -40 C through 140 C
Open your terminal and change the working directory to the folder where your netlist file is saved.
Run the netlist file using the following command.
```
$  ngspice temp_variation.cir
```
 <p align="center">
  <img width="800" height="500" src="/Images/ng_temp_curve.png">
</p>

### To obtain the Vref over supply variation  2V through 4V
Open your terminal and change the working directory to the folder where your netlist file is saved.
Run the netlist file using the following command.
```
$  ngspice supply_variation.cir
```
 <p align="center">
  <img width="800" height="500" src="/Images/ng_supply.png">
</p>

### To observe the Zero Current State

Open your terminal and change the working directory to the folder where your netlist file is saved.
Run the netlist file using the following command.
```
$  ngspice w_o_startup.cir
```
 <p align="center">
  <img width="800" height="500" src="/Images/ng_without_startup.png">
</p>


### To determine the Start-up time

Open your terminal and change the working directory to the folder where your netlist file is saved.
Run the netlist file using the following command.
```
$  ngspice with_startup.cir
```
 <p align="center">
  <img width="800" height="500" src="/Images/ng_startup.png">
</p>



<img align="left" width="45" height="45" src=/Images/ltspice_logo.jpg>

## About LTspice XVII
LTspice XVII is a freeware simulation software developed by Analog Devices.

### Installing and Starting LTspice

#### For Windows

Head on to [Analog Devices](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html), download the lastest version of LTspice for your version of Windows.
 - Run the downloaded LTspice.exe file and go through with the installation.
 - Download the bgr.cir file and the osu018.lib file accompanying it from the *LTspice Simulation* Folder.
 - Open the LTSpice XVII application.
 - ```File -> Open -> Select the bgr.cir file```
 
#### For MacOS 10.9+ 

Head on to [Analog Devices](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html), download the lastest version of LTspice for your Mac.
- Open the downloaded LTspice.dmg file and go through with the installation.
- Download the bgr.cir file and the osu018.lib file accompanying it from the *LTspice Simulation* Folder.
- Copy the absolute path of your osu018.lib file and change the ```.include``` directive in the bgr.cir file to ```.lib your_path/osu018.lib```
- ```Open LTspice -> More Choices -> Open Other Type of File -> Select the bgr.cir file```
- Hit the ```Run``` button.


#### For Ubuntu

LTspice can run under WINE. No Linux version available yet.
Open your terminal and type the following to install LTspice in WINE
```
$  sudo apt-get install wine
$  cd /tmp/
$  wget http://ltspice.analog.com/software/LTspiceXVII.exe
$  wine LTspiceXVII.exe
$  rm LTSpiceXVII.exe
```
- Download the bgr.cir file and the osu018.lib file accompanying it from the *LTspice Simulation* Folder.
- ```Applications -> LTspiceXVII```
- ```File -> Open -> Select the bgr.cir file```



## LTspice XVII Window


<p align="center">
  <img width="810" height="500" src="/Images/ltspice_window_1.png">
</p>

<p align="center">
  <img width="800" height="500" src="/Images/ltspice_window_2.png">
</p>

## Running the Simulation

*Note: Before running simulation, ensure that the osu018.lib file is in the same directory as the bgr.cir file. Else you will need to modify the bgr.cir file and add the approporiate path of osu018.lib*

There are several waveforms that need to be obtained to observe the performance of the Bandgap reference circuit.
To obtain the desired waveform, simply uncomment the relevant spice directives and comment the irrelevant ones.

To comment in LTSpice XVII, use the " * " symbol before the text.

### To obtain the Vref @  VDD=3.3V & Temp= 27 C over 100ns plot
<img align="right" width="260" height="200" src=/Images/1.1.png>

Ensure the following directives are present

```
Vdd 1 0 3.3V
.temp 27
.tran 0 100ns
```
- ```Run it```
- ```Right click on plot plane -> add traces -> Select V(vref) -> OK```
 <p align="center">
  <img width="800" height="500" src="/Images/reference.png">
</p>


### To obtain the Vref, PTAT & CTAT voltages over -40 C through 200 C
<img align="right" width="260" height="200" src=/Images/2.1.png>

Ensure the following directive is present

```
.step temp -40 200 1
```
- ```Run it```
- ```Right click on plot plane -> add traces -> Select V(vref) -> OK```
- ```Right click on plot plane -> add traces -> Select V(15) -> OK```
- ```Right click on plot plane -> add traces -> *Add this expression:* V(vref)-V(15) -> OK```
 <p align="center">
  <img width="800" height="500" src="/Images/PTAT+CTAT.png">
</p>

### To obtain the Vref over -40 C through 140 C
<img align="right" width="180" height="200" src=/Images/3.2.png>

<img align="right" width="230" height="200" src=/Images/1.1.png>

Ensure the following directive is present

```
.step temp -40 140 1
```
- ```Run it```
- ```Right click on plot plane -> add traces -> Select V(vref) -> OK```
- ```Click on the Voltage Trace Label V(vref) at the top of the plot plane, cursors should now appear. Drag the cursors to determine the voltages at specific points.```

<p align="center">
  <img width="800" height="500" src="/Images/temp_variation.png">
</p>

### To obtain the Vref over supply variation  2V through 4V
<img align="right" width="180" height="200" src=/Images/4.2.png>

<img align="right" width="230" height="200" src=/Images/1.1.png>
Ensure the following directives are present

```
Vdd 0 1 3.3V
.dc Vdd 2 4 0.1
```
- ```Run it```
- ```Right click on plot plane -> add traces -> Select V(vref) -> OK```
- ```Click on the Voltage Trace Label V(vref) at the top of the plot plane, cursors should now appear. Drag the cursors to determine the voltages at specific points.```
<p align="center">
  <img width="800" height="500" src="/Images/supply_variation.png">
</p>


### To observe the Zero Current State

**WARNING! : This method is flawed and yields incorrect results, uploaded only to maintain Log.**
<img align="right" width="260" height="200" src=/Images/1.1.png>

Ensure the following directives are present

```
.ic  V(8)=0V V(9)=0V
.tran 0 50ns
```
*Comment out the start-up ckt*

- ```Run it```
- ```Right click on plot plane -> add traces -> Select V(vref) -> OK```

<p align="center">
  <img width="800" height="500" src="/Images/without_startup.png">
</p>


### To determine the Start-up time

**WARNING! : This method is flawed and yields incorrect results, uploaded only to maintain Log**
<img align="right" width="180" height="200" src=/Images/6.2.png>

<img align="right" width="230" height="200" src=/Images/1.1.png>
Ensure the following directives are present

```
.ic  V(8)=0V V(9)=0V
.tran 0 50ns
```
*Uncomment the start-up ckt*

- ```Run it```
- ```Right click on plot plane-> add traces -> Select V(vref) -> OK```
- ```Click on the Voltage Trace Label V(vref) at the top of the plot plane, cursors should now appear. Drag the cursors to determine the start-up time.```

<p align="center">
  <img width="800" height="500" src="/Images/bgr_startup.png">
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

