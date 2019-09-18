# Twincat3DimmerHomeAssistant
Twincat 3 1 switch dimmer, with interface for Home Assistant


The dimmer acts like a one switch dimmer. 

Press and hold the pushbutton for up and down dimming.
Press one time the pushbutton for dimming on and off.

Besides this, there are two IO fields for an ads light entity:
  - dim value as UINT
  - light switch as BOOL
  
When dimming on and off with a real pushbutton, the dim value is tracked by the HA interface.


Twincat call:

fbDimmer(
	bOn:= ,         //On rising edge, the output value will dim to the previous value, or to max when not availble
	bOff:= ,        //On rising edge, the output value will dim to zero
	tTimeDimOn:= ,  //Wanted time to dim up
	tTimeDomOff:= , //Wanted time to dim down
	minValue:= ,    //Min light level to avoid flickering
	maxValue:= ,    //Max level -> 512
	bPb:= ,         //Pushbutton
	nIgnition:= ,   //Ignition value of the LED to increase the dimmer curve performance
	nOut=> ,        //Output value
	bLight=> ,      //Pushbutton pilot light
	nOutDmx=> ,     //Dmx output in byte
	nOutPercentage=> , //Percentage output in UINT
	nHaValue:= ,    //Connect to Home Assistant Light ADS Light brightness 
	bHaSwitch:= );  //Connect to Home Assistant Light ADS switch
 
 
 
 



