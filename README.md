# Bandgap reference simulation on LTspice XVII
This project simulates the designed Bandgap reference circuit to determine its performance characterisitics. 
*Note: Circuit not designed for optimal performance. Design yet to be modified.*

## About LTspice XVII
LTspice XVII is a freeware simulation software developed by Analog Devices

### Installing and Starting LTspice

#### For Windows

Head on to [Analog Devices](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html), download the lastest version of LTspice for your version of Windows.
 - Run the downloaded LTspice.exe file and go through with the installation.
 - Download the bgr.cir file and the osu018.lib file accompanying it.
 - Open the LTSpice XVII application.
 - File -> Open -> Select the bgr.cir file

#### For MacOS 10.9+

Head on to [Analog Devices](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html), download the lastest version of LTspice for your Mac.
- Open the downloaded LTspice.dmg file and go through with the installation.
- Download the bgr.cir file and the osu018.lib file accompanying it.
- Copy the absolute path of your osu018.lib file and change the .include directive in the bgr.cir file to *.lib your_path/osu018.lib*
- Open LTspice -> More Choices -> Open Other Type of File -> Select the bgr.cir file
- Hit the Run button.


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
- Download the bgr.cir file and the osu018.lib file accompanying it.
- Applications -> LTspiceXVII
- File -> Open -> Select the bgr.cir file

## Running the Simulation

*Note: Before running simulation, ensure that the osu018.lib file is in the same directory as the bgr.cir file. Else you will need to modify the bgr.cir file and add the approporiate path of osu018.lib*

There are several waveforms that need to be obtained to observe the performance of the Bandgap reference circuit.
To obtain the desired waveform, simply uncomment the relevant spice directives and comment the irrelevant ones.
To comment in LTSpice XVII, use the " * " symbol before the text.

### To obtain the Vref @  VDD=3.3V & Temp= 27 C over 100ns plot

Ensure the following directives are present

```
Vdd 1 0 3.3V
.temp 27
.tran 0 100ns
```
- Run it
- Right click on plot -> add traces -> Select V(vref) -> OK

### To obtain the Vref, PTAT & CTAT voltages over -40 C through 200 C

Ensure the following directive is present

```
.step temp -40 200 1
```
- Run it
- Right click on plot -> add traces -> Select V(vref) -> OK
- Right click on plot -> add traces -> Select V(15) -> OK
- Right click on plot -> add traces -> *Add this expression:* V(vref)-V(15) -> OK

### To obtain the Vref over -40 C through 140 C

Ensure the following directive is present

```
.step temp -40 140 1
```
- Run it
- Right click on plot -> add traces -> Select V(vref) -> OK
- Click on the Voltage Label V(vref) at the top of the plot, cursors should now appear. Drag the cursors to determine the voltages at specific points.

### To obtain the Vref over supply variation - 2V through 4V

Ensure the following directives are present

```
Vdd 0 1 3.3V
.dc Vdd 2 4 0.1
```
- Run it
- Right click on plot -> add traces -> Select V(vref) -> OK
- Click on the Voltage Label V(vref) at the top of the plot, cursors should now appear. Drag the cursors to determine the voltages at specific points.

### To observe the Zero Current State

**WARNING! : This method is flawed and yields incorrect results, uploaded only to maintain Log.**
Ensure the following directives are present

```
.ic  V(8)=0V V(9)=0V
.tran 0 50ns
```
*Comment out the start-up ckt*

- Run it
- Right click on plot -> add traces -> Select V(vref) -> OK

### To determine the Start-up time

**WARNING! : This method is flawed and yields incorrect results, uploaded only to maintain Log**

Ensure the following directives are present

```
.ic  V(8)=0V V(9)=0V
.tran 0 50ns
```
*Uncomment the start-up ckt*

- Run it
- Right click on plot -> add traces -> Select V(vref) -> OK
- Click on the Voltage Label V(vref) at the top of the plot, cursors should now appear. Drag the cursors to determine the start-up time.

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

