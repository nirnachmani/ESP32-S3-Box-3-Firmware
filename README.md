# ESP32-S3-Box-3-Firmware
ESP32 S3 Box 3 Firmware which combines continuous conversation, dock sensors and media player

I combined [jaymunro](https://github.com/jaymunro/esphome_firmware)'s firmware for continuous conversation and sensors support with [gnumpi](https://github.com/gnumpi/esphome_audio/tree/dev-next)'s implementation of media player. Using the media player seems to solve the low volume problem. The firmware implements the "assist query" and "assist reply" sensors which are not used in gnumpi's implementation. The firmware uses "Hey Jarvis" but you can change it to your needs. I didn't use gnumpi's images as I wanted to maintain the original feel. You will need to adjust the firmware to your own environment (wifi, ap, etc.). I did not test it extensively.

I made a few other changes:
 - I removed the frames around the text (I just like it better like that)
 - I clear the query and reply texts so that the old text doesn't display in a new query before the new one displays
 - The time is taken from Home Assistant
 - Added volume information in the right corner, visual feedback when pressing to change the volume on the touchscreen and startup volume configuration setting to set a default volume when starting
 - Muting microphone can now be done by tapping on left top corner of the screen. When microphone is mute, an icon appears in the left top corner, instead of wake word.
 - Muting speaker can be done by tapping on right top corner of the screen. When speaker is mute, an icon appears in the right top corner, instead of volume.
 - Timers shows instead of the main picture on idle and touching the middle of the screen stops the timer's ringing
    
Known bug - when muting and then un-muting with physical mute button, microphone/wake word detection stops working until reboot. I am unable to find the cause of that.

Now also includes wifi information, radar, up-time, temp and humidity, internal temp and more thanks to [Christoph](https://github.com/ChristophCaina/ESP32-S3-Box-3-Firmware) 

Thank you [jaymunro](https://github.com/jaymunro), [gnumpi](https://github.com/gnumpi) and [Christoph](https://github.com/ChristophCaina) for your good work. 
