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
