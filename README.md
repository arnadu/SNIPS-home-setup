#SNIPS setup

Overview of my SNIPS setup to control: 
  - multi-room SONOS system
  - one Television through a BlackBean IR emitter
  
 Hardware:
  <br>Raspberry 3 with 8Gb card, for running SNIPS, with a Respeaker-4 microphone array
  <br>Matrix Voice ESP32 connected via the home wifi network to SNIPS, as a satellite in a separate room
  <br>Broadlink RM 3 Black Bean infrared controller, connected through the home wifi network
  
  <p>Raspberry Install:
  
<br>  Install Raspbian lite with desktop on the Raspberry
<br>  Activate SPI and I2C interfaces
  
<p>  Use SAM on main computer to install SNIPS on raspberry: https://snips.gitbook.io/documentation/ressources/sam_reference
<br>  sam init 
<br>  sam install assistant
<br>  sam install actions 
<br>  assistant is: https://console.snips.ai/assistants/proj_OVGmMe6O1D0G
<br>  skills are:
<br>  https://github.com/arnadu/snips-sonos-skill
<br>  https://github.com/arnadu/snips-tv-skill
  
<p>  Install Respeaker microphone drivers: https://github.com/SeeedDocument/ReSpeaker-4-Mic-Array-for-Raspberry-Pi/blob/master/ReSpeaker-4-Mic-Array-for-Raspberry-Pi.md
  
<p>  Install Respeaker LED control: https://github.com/Psychokiller1888/snipsLedControl

<p> Install snipsWebAdmin on raspberry for easy remote access to SNIPS services: https://github.com/oziee/snipsWebAdmin

<p>  Install Blackbean IR controller: https://github.com/TheGU/rm3_mini_controller
<br>	add empty __init__.py in rm3_mini_controller folder to be able load module broadlink.py

<p> Install matrix voice: https://github.com/Romkabouter/Matrix-Voice-ESP32-MQTT-Audio-Streamer
<br> (note: I used a Ubuntu virtual machine to run Arduino IDE and the install script)
<br>  it looks like there may be a bug in hal library, line 138 of microphone_array.cpp: simply remove the std::round( and leave ::round( 
 
 
 

  
  
  
  
  
  
  
  


