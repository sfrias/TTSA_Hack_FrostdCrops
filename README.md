# TTSA_Hack_FrostdCrops
Enjoy considering, assembling and evolving a crop ice forecasting model

Almost Two points to collect data. Higher position and lower position: 

## Analysis and understanding of the problem


Heat is preferably transmitted through three mechanisms: conduction, convection, and radiation. Temperature is an indicator that, depending on the mechanism, will generate an output:

- In the case of conduction, it is the ability of the air to cool the crops to dangerous levels. At the same time, this capacity will depend on the density of the air (in turn it depends on the temperature), the exchange rate (it depends on gravity for convection between zones of different temperatures, and on the speed of the air fluid and its variations, which, in turn, depends on the topology of the terrain and the climatic conditions related to the wind.).

- In the case of convection, the average speed of the drop in temperature of the culture will depends first of temperature differences between the air and the crop, in turn on the density of air and crop, and heat exchange capacity (an equivalent to a fraction of the behavior of a black body can be established) marks temperature change speed into a crop. This means that after a period of time, with certain conditions of temperature, air density, fluid air circulation, the crop will have a certain temperature change.

- Radiation: at low temperatures, is not a significant factor of heat transfer, but it is a good indicator of the temperature of the crop, if we know the average emissivity of its surface.

## Measurements:


Magnitudes that could be measured would be: air temperature, air speed (cooling capacity), air humidity level (affects the transport of energy, and its exchange in the change of state of the contained water), and additionally it can be propose to measure the level of infrared radiation of the environment to correlate the measured values with the current state of temperature of the culture.


## Points of measurement: 


- Higher point is paramount to measure temperature, humidity, wind speed average modulus and connect with LoRaWAN plattform to send values and warnings.

- Lower point/wind speed stream point: paramount to measure colder and with higher density/humidity. most challenged with select a low power device to measure IR stereo radiation 360º on approx. 32 fractions measurement on crop environment. On research.

## Hardware decisions

Hardware try: two comm shots developed in parallel, for two units LoRA capable the common part is Raspberry connected with Sx Standard transceiver, and with an alternative module, that connects sensor module swarm. Each sensor module can be equipped with temperature-humidity sensor, IR sensor, optionally atmosferic pressure sensor.

First shot: alternative module based on nrF24L(~12mA on TX) module, whith Enhanced Shockburst Protocol (ESB) at 2.4Ghz ISM band, combined with MCU Atmel ATtiny44A, both on ultra-low Idle(32uA) and Powerdown(1.8uA) power state.

Second Shot: alternative module based on ESP8266, with ESP-Now protocol at 2.4Ghz ISM band, ultra low power for sleep state.

Sensors:
- temperature-humidity: some standard as DHT, for example DHT11.
- IR sensor: really a challenge for low power and reliability, also picked nearest available. Some of MIL chips as afc7103a17, commercial specialized version is MLX90614ESF, with i2c bus comms (-40ºC to +125ºC environment, -70ºC to 380ºC, tolerance MIL 0.2ºC, COMM 0.5ºC), C-Gradient compensated.
- atmosferic sensor: BMP180
