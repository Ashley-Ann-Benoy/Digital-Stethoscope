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
- We then flashed the code on the IC and  made the LCD TFT screen connections .
- We took measurements of the assembled setup and designed a compact enclosure with a lid, featuring cutouts for the acoustic sensor and a battery slot.

## Simulation Results
![WhatsApp Image 2025-05-11 at 23 04 28](https://github.com/user-attachments/assets/676283ac-7c9b-4407-b349-a52547164ac3)

## Schematic
![Screenshot 2025-04-01 205124](https://github.com/user-attachments/assets/3de2b7ae-8619-4d17-8622-c52183fbfa94)
## PCB Layout and 3D view
![Screenshot 2025-04-01 205035](https://github.com/user-attachments/assets/310cc9ef-4899-44aa-a6ba-efcdcc17590b)
![Screenshot 2025-04-01 205024](https://github.com/user-attachments/assets/aa3de4de-1c26-4c6c-9281-6d6657d3f451)

##  Hardware Set up 
## Enclosure Box Design
![image](https://github.com/user-attachments/assets/de61e62d-4c9b-4e15-9bb9-6538a19e1dd1)
![image](https://github.com/user-attachments/assets/bbd7c41b-e042-41ba-9591-9a6e976e3755)


## Code logic explanation
## Challenges Faced
- Screen glitching and lag
- White screen
- Custom Acoustic sensor is weak
  
## Further Improvements

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
