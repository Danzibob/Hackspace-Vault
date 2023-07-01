Working on with #Tails 
At-home [[PCB Etching]] project

## V1.0
### Hardware
- ESP-01
- BMP 280
- Toggle switch for record / dump data modes
- Reset switch (convenience)
- 2mm 2 pin JST Battery connector
### Capabilities
- Log altitude, pressure and temperature
- Self-calibrate ground altitude on boot/reset
- 4kb circular buffer
- Data upload to cloud via phone hotspot (hard-coded ssid)
- Works off 1x3.7V LiPo or LIon battery
- (TODO) Write recorded data to flash
- (TODO) Over the air reprogramming
- (???) Live telemetry during flight over wifi?
### Notes
- Minimal I/O left for future expansion
	- (Only builtin-LED pin wasn't connected to something else externally)
	- Could still add an accelerometer to the I2C bus with minimal redesign
- ESP8266 has great RAM and flash capacity for it's size and cost
- Much greater processing power than say Arduino Nano (80MHz CPU)
- Not Bluetooth capable; WiFi only

## Future Plans
- ESP-01 is great for something this tiny, perfect for _very_ simple avionics
- For future designs, ESP-12F board has...
	- More exposed IO (I2C, SPI, UART, ADC)
		- Potential for GPS and radio, along with I2C and analog
		- Hardware support for SD card, so basically infinite storage
			- Appears to support DMA??
		- 2 UARTS (one only has TX) - GPS + Debug 
		- Has _one_ ADC exposed for analog readings
			- Not enough spare GPIO to run a multiplexer if other preipherals are all in use
			- Would be fine if no SD card
		- Has 4 PWMs exposed
	- Still only 16mm wide
	- Can reach double the clock speed (160MHz)
	- Potential for audio output over I2S