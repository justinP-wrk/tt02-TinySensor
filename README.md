![](../../workflows/gds/badge.svg) ![](../../workflows/docs/badge.svg)

# What is TinySensor?

TinySensor is an extremely small & basic sensor that aims to use external photodiode hardware as the input. Essentially think about a camera that only has 6 pixels, and each pixel is only 1 bit! A far cry from the multi-Megapixel cameras in all our phones, but still sensitive enough to know light from dark.

## How it works

Inputs 1-6 will be connected to external photodiodes to read either a '0' or '1', inputs will be added together and displayed on the 7-segment display. This is accomplished by adding all of the inputs together, and then using a decoder to display the correct value on the 7 segment display. Additionally, any "good" camera has multiple modes of operation, right? This TinySensor has a "Capture" or a "Streaming" mode. 

## How to test

Dip switches 1-6 can be used instead of external hw to provide inputs, and 7 is used to switch between Capture or Stream sample mode. Throw the switches and the total number should show up on the 7-segment display.
Input pin 7 in the '0' position will require the use of the Step button in order to capture a single "frame" in time. While in position '1' it will use a 12bit counter to update the output continously about 1-2 times per second. without the counter the 10KHz clock would try to update the display far too many times per second. 
