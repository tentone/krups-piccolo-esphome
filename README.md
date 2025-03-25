# KRUPS Piccolo ESPHome
 - ESPHome based controller for dolce gusto (krups) piccolo coffer machine
 - Control coffe machine remotely
   - Turn on/off
   - Keep track of the machine state
   - Start maitenance procedure
   - Start and stop coffe automatically
     - Short press for expresso
     - Long press for large coffe

```mermaid
  graph TD;
      HEATING_UP-->WAITING;
      WAITING-->COFFE;
      COFFE-->HEATING_UP;
      HEATING_UP-->MAITENANCE
```

## Card

 - Use `card.yaml` template to create card
 - Configure webservice to serve the files.
 - Replace the URL to acess image files
 - <img src="readme/card.png" width=300>

## Material
 - Two relays (board)
   - Control pump
   - Turn on/off
 - Optocoupler PC817 board (2 inputs)
   - Status LED's
 - ESP board (code uses NodeMCU board w/ ESP8266)
 - Button (any small button will do)
   - Preferably one that can be easily attached to the machine shell

## Diagram


## Control board
 - The control board of the machine is well labeled
 - NCT (temperature sensor)
   - Not Used for this project
 - MMI (Button and Leds)
   - Red LED (GND)
   - On/Off Button (Activated w/ 5V) 
   - 5V
   - Green LED (GND)
 - V. Det
   - Cold (Activated /w 5V)
   - 5V
   - Hot (Activated /w 5V)
 - Hold
   - Enabled/disable the pump
   - Actived with a magnetic sensor when the lid closes
   - Can be shunted for this project

<img src="readme/board.png" width=300>

## Installation 
 - Install ESPHome Builder in HAOS
 - Setup ESP8266 or ESP32 board and take note of the encryption and OTA keys
 - Copy the `coffe.yaml` code to your file.
   - Replace keys
 - Compile and install.
