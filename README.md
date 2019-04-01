# esx_taximeter

![ESX TaxiMeter](https://i.imgur.com/1Q2ralm.jpg "ESX TaxiMeter")

ESX Taxi Meter is a plugin that adds a fare meter to your server. Great for those who work as an Uber, Taxi, Limo, Tow, Aircraft Ferry or any other job that might charge per mile of travel.

Right now it supports two types of fares. A "Flat Rate" fare which is simple enough and a "distance" fare which shows a fare total based upon the distance traveled. The driver is the "owner" of the meter and any passengers in the car will be able to see the meter if it is active.

In the configuration file, you can set restrictions on which vehicles and which ESX jobs can use the meter. You can also configure the meter to use either imperial or metric measurements.

The meter menu can be launched by using LEFTCTRL + G

## Requirements

- [es_extended](https://github.com/ESX-Org/es_extended)
- [esx_taxijob](https://github.com/ESX-Org/esx_taxijob) (optional)

## Installation

Run this command inside of your server-data/resources folder:

``` sh
git clone https://github.com/michaelhodgejr/esx_taximeter.git [esx]/esx_taximeter
```

Inside \[esx\]/esx_taximeter, create your config.lua file from the default, and edit it as desired.

``` sh
cp config.default config.lua
```

Add this to your server.cfg file:

``` sh
start esx_taximeter
```

## Known Issues

If you are unable to open the menu with Ctrl + G, it's probably because you are not currently employed as a taxi driver! You either need to install esx_taxijob and change your job, or add your current job to config.lua, or modify config.lua to allow everyone to use the taxi meter:

``` lua
Config.RestrictToCertainESXJobs = false
```

When a passenger gets in the vehicle, the driver will need to toggle the taxi meter off and on to make it appear on the passenger's screen.

## Upgrading
