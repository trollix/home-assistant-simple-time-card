# Simple Time Card
A text based clock for Homeassistants' Lovelace ui


![](https://img.shields.io/github/v/release/trollix/lovelace-tix-simple-time-card)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg?style=flat)](https://github.com/custom-components/hacs)



![24h clock](resources/screenshot_1256.png)  


## Usage
- Download the files in this folder to your 'www' folder in the hass config directory. The *'www'* folder can be accesed via *'/local/'* in your configuration I've put my custom elements in the sub folder *'elements'* and the js file of this card in the folder *'simple-clock-card'* as an example.

- enable advanced mode and in your lovelace dashboard settings under the resources tab add the following:

![add a resource](https://i.imgur.com/pySUU4V.png)

- or if you use yaml to configure lovelace:
		
		resources:
			- type: module
	        	  url: /local/elements/tix-simple-clock-card/tix-simple-clock-card.js
			  
- add the following lines to a view in '*cards:*' as a *'manual card'* or use your yaml configuration and add:
		
		cards:
			- type: 'custom:tix-simple-time-card'

thats it!
		

## Options
|option| default|description| 
|--|--|--|
|  use_24h| true| When false, shows 12h format clock with AM/ PM, instead of a 24h format clock |
|  show_seconds| true | When false hides the seconds

## Example
- show a 24h clock without seconds:
	
		- type: 'custom:tix-simple-time-card'
		  use_24h: false
		  show_seconds: false
