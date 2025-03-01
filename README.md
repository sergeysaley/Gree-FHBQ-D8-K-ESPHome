# GREE FHBQ-D8-K: HVAC control, ESPHome

## Description

Adaptation of the [https://github.com/kodr5555/gree-fhbq](https://github.com/kodr5555/gree-fhbq) project for Gree FHBQ-D8-K

You can manage the following settings
- on/off
- fan speed
- recuperator operating mode

Example configuration given: 
- written for esp32, but esp8266 is sufficient for this task
- interacts with Home Assistant, but can be used in conjunction with any other home management system that supports MQTT - just add the code for https://esphome.io/components/mqtt.html

## You need:
- ESP32 module
- RS485 - UART TTL module
- DC-DC 12V/5V module
- don't forget to set dip-switch on plate to any appliable address (not 0000, any other)
- change the GPIO assignments for rx_pin and tx_pin in the configuration file to suit your needs and capabilities of your ESP controller
  
## Connection:
- DC-DC 12V side connect to the 12V and ground pins of the COM-BMS connector on the machine board, 5V side - to the 5V pins and ground of the ESP controller. Observe the polarity of course.
- RS485 board - UART TTL connect to ESP (+, gnd, rx, tx) and to A, B pins of the COM-BMS connector
   
Thanks to the [author of https://github.com/kodr5555/gree-fhb](https://github.com/kodr5555), who showed exactly where to connect for control (I spent a lot of time trying to find at least some technical documentation on my ventilation, researching the possibility of control via COM-UNION and COM-MANUAL)
