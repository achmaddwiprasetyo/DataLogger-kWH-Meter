# DataLogger-kWH-Meter
A module for Node-RED that you can use to get data from wifi power meter of Pilot SPM91, SPM93

* [node\-red\-contrib\-iammeter](#node-red-contrib-iammeter)
  * [Installation](#installation)
  * [Local Output: Single\-phase electric energy meter (SPM91)](#local-output-single-phase-electric-energy-meter-SPM91)
  * [Local Output: three\-phase electric energy meter(SPM93)](#local-output-three-phase-electric-energy-meter-SPM93)
* [Monitor your solar PV system in Node\-Red](#monitor-your-solar-pv-system-in-node-red)
  * [Effect &amp;&amp; Demo](#effect--demo)
  * [Tutorial](#tutorial)
* [About ZHPILOT](#about-zhpilot)

# node-red-contrib-zhpilot

This is a node introduction for the [ZHPILOT](www.zhpilot.com/)

ZHPILOT provides both a single-phase and three-phase energy meter. They are all bi-directional, din rail.
You can use them to meter the energy consumption.

[SPM91: Single Phase Energy Meter](https://www.zhpilot.com/din-rail-ac-single-phase-energy-meter-spm91-230v-63a-with-modbus-product/)

[SPM93: Three Phase Multifunction Energy Meter](https://www.zhpilot.com/din-rail-ac-three-phase-multifunction-energy-meter-spm93-for-measure-kwh-7-1-digits-lcd-display-with-modbus-protocol-product/)


## Installation

Install in Node-RED via the Manage Palette menu.

May also be installed via npm:

`npm install node-red-contrib-iammeter`

## Local Output: Single-phase electric energy meter (SPM91)


```json
   [0,0,22292,0,0,0,0,0,0,0,0,5001,1000,0,0,0,0,0,0,0,0,0,0,0,0]
```
[voltage, current, power,import energy, export energy]

unit: voltage [V], current [A], power [W],import energy [kWh], export energy [kWh]




## Local Output: three-phase electric energy meter (SPM93)


```json
 [
   [234.7,9.99,1068,21.063,20.667,49.99,1],
   [220,9.99,1100,21.063,20.667,49.99,0.5],
   [220,9.99,1213,21.063,20.667,49.99,0.55],
   [224.9,0,3381,26.329,25.834,49.99,0.55]
 ]
```
 [ voltageA, currentA, powerA,import energyA, export energyA], [ voltageB, currentB, powerB,import energyB, export energyB], [ voltageC, currentC, powerC,import energyC, export energyC]

unit: voltage [V], current [A], power [W],import energy [kWh], export energy [kWh]



# Monitor your solar PV system in Node-Red 

You can use the Energy monitor node of IAMMETER to monitor your solar PV system in Node-Red.

## Effect && Demo

Node-RED UI: http://ha.iammeter.com:11880/ui

Node-RED flow: http://ha.iammeter.com:11880/#flow/5fb9966c8a33b771

Node-RED in Homeassistant:  [http://ha.iammeter.com:18123/nodered  ](http://ha.iammeter.com:18123/nodered)

**user/password: iammeter/iammeter**

![iammeter_node-red-solar-pv-system_daily](https://iammeterglobal.oss-ap-southeast-1.aliyuncs.com/miwyf/img/iammeter_node-red-solar-pv-system_daily.png)

## Tutorial

[How to monitor your solar PV system in NodeRed](https://imeter.club/topic/129)



# About ZHPILOT

[Monitor your energy consumption in IAMMETER-Cloud](https://www.iammeter.com/applications)

[Integrate IAMMETER energy meter to third-party platforms](https://www.iammeter.com/docs/homeassistant#5-integrate-iammeter-energy-meter-to-third-party-platforms-other-than-home-assistant)

