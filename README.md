# SPEECH-RECOGNITION-SYSTEM

MENTOR NAME : NEELA SANTHOSH 
DOMAIN : EMBEDDED SYSTEMS 
INTERN ID: CT04DY586

Task Description

The task here is to design and implement a Speech Recognition System using an embedded microcontroller platform along
with a speech recognition module and an LCD for displaying recognized commands. The goal of this project is to allow the
system to listen to human voice inputs, process the audio signals, and translate them into meaningful digital commands
that can either be displayed or used to control other devices. Unlike conventional input systems such as buttons or
keypads, speech recognition provides a hands-free and natural way of interaction between humans and machines.

In this setup, a dedicated speech recognition module (such as an Elechouse Voice Recognition Module or a similar system)
is interfaced with the Arduino. This module captures the user’s spoken commands through a microphone and processes the
audio signals internally to identify predefined keywords. The recognized command is then transmitted to the Arduino in
the form of digital data. The Arduino reads this data and interprets it as a specific instruction.

The processed command is displayed on a 16x2 LCD module (preferably interfaced via I2C to reduce wiring complexity). For
example, if the user says “Light On,” the LCD will display “Command: Light On.” If the user says “Fan Off,” the LCD will
display “Command: Fan Off.” This provides immediate feedback to the user, confirming that the spoken instruction has been
correctly recognized and processed.

This task highlights the integration of speech technology with embedded systems. It combines multiple disciplines: sound
sensing, pattern recognition, signal processing, and digital interfacing. The project is significant because speech
recognition systems are increasingly being used in real-world applications like smart homes, voice-controlled appliances,
robotics, healthcare assistance, and industrial automation.

The system’s design focuses on simplicity and reliability. By pre-training the module with specific commands, the speech
recognition process becomes more accurate for the intended use case. Instead of attempting to recognize an unlimited
vocabulary, the system focuses only on a fixed set of words or phrases, which improves accuracy and reduces computational
requirements. This makes it feasible to implement speech recognition on low-cost microcontrollers like Arduino.

Through this task, learners gain practical experience in working with audio-based sensors, interfacing modules via serial
communication, and programming embedded systems to respond intelligently to voice commands. The project also demonstrates
how user interaction can be enhanced by combining recognition systems with display units, providing both functional
control and visible confirmation.


Working Principle

The working principle of the speech recognition system is based on three fundamental stages: capturing voice signals,
recognizing the speech patterns, and displaying or acting on the recognized command.

1. Voice Capture:
The system starts with a microphone connected to the speech recognition module. When a user speaks a word or phrase, the
microphone converts the sound waves into corresponding electrical signals. These analog signals represent the amplitude
and frequency characteristics of the spoken command.


3. Signal Processing and Recognition:
The speech recognition module is responsible for analyzing the incoming audio signal. It performs filtering,
featureextraction, and pattern matching to determine whether the spoken phrase matches any of the pre-stored commands in
its memory. For example, the module may be trained to recognize commands like “ON,” “OFF,” “START,” or “STOP.” When the
spoken input closely matches one of the stored patterns, the module outputs a unique digital code corresponding to that
command.

This digital code is sent to the Arduino through a serial communication interface (UART). The Arduino receives this code
and interprets it as a specific instruction. For example, code “01” might correspond to “Light On,” while code “02” might
correspond to “Fan Off.”


3. Command Display and Action:
Once the Arduino identifies the command, it sends the corresponding message to the LCD for user feedback. Using the I2C
interface, the LCD displays clear text such as “Command: Light On” or “Command: Fan Off.” This gives immediate
confirmation that the spoken instruction has been recognized correctly. In advanced versions of the project, the Arduino
can also activate or deactivate appliances using relays, making the system not only display the commands but also execute
them.

The system continuously loops through this process, waiting for new voice commands. By updating the LCD in real time, the
user can always see the result of their interaction. The design ensures that even users unfamiliar with technical systems
can operate devices naturally using their voice, making it an accessible and intuitive solution.

In summary, the working principle involves capturing speech as sound, converting it into digital signals, recognizing
predefined patterns, and displaying or executing commands. This project demonstrates the seamless link between human
communication and machine response, making it a strong example of modern embedded applications in human–machine
interaction.
