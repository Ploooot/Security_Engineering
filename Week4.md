### Week 4

## Task 1 : Side-channels

<b> Brief explanation of what side-channel the attack uses and how</b>

A side-channel attack is a form of security breach that focuses on exploiting data revealed by accident  by a system's physical characteristics, such as its power usage, electromagnetic emissions, timing, or other unintended channels. These attacks use the fact that a system's physical implementation often unintentionally discloses information about the data it is handling.
The essence of side-channel attacks lies in their capacity to exploit unintentional data leaks stemming from the physical implementation of a system. To protect themselves, companies take preventive measures, including the use of constant-time algorithms, hardware safeguards, and techniques like introducing noise, all aimed at minimizing the exposure of sensitive information through side-channels.

<b> What systems does it affect?</b>

This kind of attack can affects Cryptographic Sys, Smart Cards, Embedded Sys, Hardware Security Modules, Mobile Devices, Cloud Servers, Banking Sys, Defense Sys, High-Performance Computing Sys and Automotive Electronics.

<b>What information is leaked via the side channel?</b>

Cryptographic Keys can be leaked via Power Consumption or Electromagnetic Radiation by analyzing variations in power consumption during cryptographic operations for example. You can also know keyboard input by capture and analyzing sound patterns to infer keystrokes or data input on a keyboard.

<b>Is there a documented case of it being used in a real life attack?</b>

Computer scientists have devised an attack that reliably extracts secret cryptographic keys by capturing the high-pitched sounds coming from a computer while it displays an encrypted message.
They demonstrated “the attack on various targets and by various methods, including the internal microphone of a plain mobile phone placed next to the computer and using a sensitive microphone from a distance of four meters”.

https://arstechnica.com/information-technology/2013/12/new-attack-steals-e-mail-decryption-keys-by-capturing-computer-sounds/

<b>Has it been fixed? If yes, how it was fixed?</b>

“The technique has its limitations. Most obviously, the attackers must have a smartphone, bug, or other microphone-enabled device in close proximity to a computer at the precise moment it's decrypting a message that was sent by, or otherwise known to, the attackers. Still, the technique represents a solid advance in the field of cryptanalytic side-channel attacks, which target cryptographic implementations that leak secret information through power consumption, electromagnetic emanations, timing differences, or other indirect channels.”

https://arstechnica.com/information-technology/2013/12/new-attack-steals-e-mail-decryption-keys-by-capturing-computer-sounds/
