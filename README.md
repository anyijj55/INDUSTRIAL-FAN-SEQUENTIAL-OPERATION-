INDUSTRIAL FAN SEQUENTIAL OPERATION 

Sequential Operation of Industrial Fans with 5-Minute Delay 

Objective: 

To control three industrial fans (Fan 1, Fan 2, Fan 3) such that: 

Fan 1 starts immediately when the system is turned on. 

Fan 2 starts 5 seconds after Fan 1. 

Fan 3 starts 5 seconds after Fan 2. 

Components Required: 

PLC: To control the sequential operation. 

On-Delay Timers (TON): To introduce the 5-minute delay between fan operations. 

Start/Stop Buttons: To control the system. 

Output Coils: To control the fans (Fan 1, Fan 2, Fan 3). 

Explanation of Operation: 

System Activation: 

When the Start Button is pressed, the System ON Coil is energized, activating the system. 

Fan 1 Operation: 

Fan 1 starts immediately as the System ON Coil is true. 

Fan 2 Operation: 

Timer 1 starts counting as soon as the system is activated. 

After 5 seconds, Timer 1's Done Bit (DN) becomes true, energizing the Fan 2 Coil. 

Fan 3 Operation: 

Timer 2 starts counting when Timer 1's Done Bit (DN) becomes true. 

After another 5 seconds, Timer 2's Done Bit (DN) becomes true, energizing the Fan 3 Coil. 

System Deactivation: 

When the Stop Button is pressed, the System ON Coil is de-energized, turning off all fans and resetting the timers. 

 
