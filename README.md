## INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-
### NAME: KOUSALYA A.
### REG NO: 212222230068
### DEPARTMENT: ARTIFICIAL INTELLIGENCE AND DATA SCIENCE
### DATE: 23.02.2024

**AIM**:  To interface a Analog  input (angular displacement sensor POT) and scale the values up on change in the input.

**COMPONENTS REQUIRED:**
1.	10 KΩPOT
2.	1 KΩ resistor 
3.	Arduino Uno 
4.	USB Interfacing cable 
5.	Connecting wires 
6.	LED of choice 

**THEORY**: 
**Analog signals:**

Analog signals – directly measurable quantities in terms of some other quantity.
Examples:
1. Thermometer – mercury height rises as temperature rises
2. Car Speedometer – Needle moves farther right as you accelerate
3. Stereo – Volume increases as you turn the knob
Reason for conversion of analog to digital quantity is that as the controller or any microprocessor works with digital signals in the form of 0 and 1s, in order to make the signal compatible  most of the analog signals are converted into its equivalent digital level signals using an analog to digital converter .
Quantizing - breaking down analog value is a set of finite states
Encoding - assigning a digital word or number to each state and matching it to the input signal
 There are two ways to best improve accuracy of A/D conversion:
Increasing the resolution which improves the accuracy in measuring the amplitude of the analog signal.
Increasing the sampling rate which increases the maximum frequency that can be measured.
General specifications of analog sensor
	1. Range
	2. Accuracy
	3.Linearity
	4.Compatiblity
	5. signal conversion capability

**Potentiometer**
A potentiometer, informally a pot, is a three-terminal resistor with a sliding or rotating contact that forms an adjustable voltage divider. If only two terminals are used, one end and the wiper, it acts as a variable resistor or rheostat.
Potentiometers are commonly used to control electrical devices such as volume controls on audio equipment. Potentiometers operated by a mechanism can be used as position transducers, for example, in a joystick. Potentiometers are rarely used to directly control significant power (more than a watt), since the power dissipated in the potentiometer would be comparable to the power in the controlled load
CIRCUIT DIAGRAM

**PROCEDURE:**

1.	Connect the circuit as per the circuit diagram 
2.	Connect the board to your computer via the USB cable.
3.	If needed, install the drivers.
4.	Launch the Arduino IDE.
5.	Select your board (If you the board is arduino uno, select accordingly).
6.	Select your serial port, accordingly ( E.g. COM5 )
7.	Open the file of the program  and verify the error , clear if any errors that are existing 
8.	Upload the program and check for the physical working. 
9.	Ensure safety before powering up the device 

**PROGRAM** 
 ```
int pot;
int led=7;
void setup()
{
  pinMode(led,OUTPUT);
  Serial.begin(9600);
}
void loop()
{
  pot=analogRead(A0);
  //Serial.print("Value=");
  Serial.println(pot);
  
  if(pot>900)
  {
  digitalWrite(led, HIGH);
  delay(500); 
  digitalWrite(led, LOW);
  delay(500); 
  }
  else
  {
    digitalWrite(led,LOW);
    delay(500);
  }
}
```
![exp2graph](https://github.com/Kousalya22008930/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/119389108/751d422c-ef7d-4439-9146-d58539ced21b)

## Simulation output:

### ON:
![exp2on](https://github.com/Kousalya22008930/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/119389108/f7f1ccfc-9822-406b-a648-afe805a4df96)
### OFF:
![exp2off](https://github.com/Kousalya22008930/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/119389108/66cd32f8-931d-409a-a9b8-1e81ef0ea9ae)
### Schematic view:
![schview2](https://github.com/Kousalya22008930/EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO-/assets/119389108/e6d12de9-46b1-4958-90d4-dc50d8b27de1)


## RESULT:
Arduino uno analog input functioning is learned and interfaced with digital input switch .
