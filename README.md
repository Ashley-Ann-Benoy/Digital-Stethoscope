# Digital Stethoscope  
A **digital stethoscope** that amplifies, filters, and digitally processes heart sounds for enhanced diagnostics and remote monitoring.  
## Project Outline
We intend on developing a digital stethoscope system which includes an acoustic sensor that is attached to the processing unit, which will catch the signal, amplify it using an amplifier circuit using an op amp TL082.
The amplified signal is then sent to the ATMEGA328-P, which then converts the analog signal to a digital one, which is then displayed as a waveform on the LCD TFT screen. We also have a flash memory IC for storing waveforms and retrieving them later.  The entire step will be placed in a 3D-printed enclosure, which will offer mechanical support and keep the enclosure compact.
## Working
The custom acoustic sensor is positioned on a pulse point of the body.
The sound is transmitted to an amplifier circuit via a condenser microphone. 
The amplified signal is then sent to the A0 ADC pin of the  ATmega328P microcontroller, where it is processed and displayed on the LCD screen.
On the LCD screen, we display to waveform as well as the calculated BPM rate.
## Approach and Execution Flow
We took a step-by-step approach.
- We started by simulating an amplifier circuit using LT Spice and tweaking the values to meet our requirements.
- We then put together the circuit on a breadboard to confirm our results.
- We then went ahead with schematic building on KiCAD 8.0. After which, we ran an ERC to check if everything was connected properly. This was followed by PCB layout and routing.
- While doing the PCB Layout, we kept in mind to keep the analog and digital paths separate to minimize noise interference and preserve signal integrity.
- We then flashed the code on the IC and  made the LCD TFT screen connections.
- We took measurements of the assembled setup and designed a compact enclosure with a lid, featuring cutouts for the acoustic sensor and a battery slot.

## Simulation Results
![WhatsApp Image 2025-05-11 at 23 04 28](https://github.com/user-attachments/assets/676283ac-7c9b-4407-b349-a52547164ac3)

## Schematic
![Screenshot 2025-04-01 205124](https://github.com/user-attachments/assets/3de2b7ae-8619-4d17-8622-c52183fbfa94)
## PCB Layout and 3D view
![Screenshot 2025-04-01 205035](https://github.com/user-attachments/assets/310cc9ef-4899-44aa-a6ba-efcdcc17590b)
![Screenshot 2025-04-01 205024](https://github.com/user-attachments/assets/aa3de4de-1c26-4c6c-9281-6d6657d3f451)

## Set up
![image](https://github.com/user-attachments/assets/53ad252c-7bdd-4381-a44e-74cb9b514ec9)
![hr_120](https://github.com/user-attachments/assets/9d0b57e3-d23f-4155-bbf6-cad080be3cab)
![hr_72](https://github.com/user-attachments/assets/98b5fd62-e0f1-4946-81f1-a8f5e208d4f0)

## Enclosure Box Design
**Lid**
![image](https://github.com/user-attachments/assets/de61e62d-4c9b-4e15-9bb9-6538a19e1dd1)
**Box**
![image](https://github.com/user-attachments/assets/bbd7c41b-e042-41ba-9591-9a6e976e3755)


## Challenges Faced
We encountered a few challenges, which we debugged and  tried to resolve through troubleshooting and testing.
- Pin Header Size Mismatch: The pin headers on the PCB were smaller than expected and didn't fit the LCD TFT pins directly. We solved this by soldering the wires and using a perforated board.
- White screen: Caused due to too much power supply (5V) to the LED pin of the LCD screen, we resolved this by creating a separate path which had to 5V to 3.3V step down using a voltage regulator to the LED pin of the LCD screen.
- Screen glitching and lag:   Changed the delay value and flashed the code again and ensured the power supply was proper, and even tightened the LCD connections.
- Custom Acoustic sensor is picking up weak signals: Making the Tube shorter and trying to seal the gaps between the opening of the tube and the condenser microphone.
  
## Further Improvements
We could perhaps implement a model to detect anomalies and irregularities, which would capture abnormal behavior and send alerts, which would give us a  more accurate and timely diagnosis.

##  Team Members  
- **Ashley Ann Benoy** - EE23BTECH11204  
- **Avani Chouhan** - EE23BTECH11205  
- **Abburi Tanusha** - EE23BTECH11201  
- **Manugunta Meghana Sai** - EE23BTECH11212  
- **Muthyala Nikhitha Sri** - EE23BTECH11213



## References
https://circuitdigest.com/microcontroller-projects/diy-wireless-digital-stethoscope

https://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/s2012/myw9_gdd9/myw9_gdd9/

https://circuitdigest.com/fullimage?i=circuitdiagram_mic/Wireless-Stethoscope-Circuit.png

https://www.youtube.com/watch?v=w6MbM_f_7Uo

https://www.youtube.com/watch?v=QSXJG3opua8&t=3s
