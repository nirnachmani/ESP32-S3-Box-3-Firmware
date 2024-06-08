# ESP32-S3-Box-3-Firmware
ESP32 S3 Box 3 Firmware which combines continuous conversation, dock sensors and media player

I combined [jaymunro](https://github.com/jaymunro/esphome_firmware)'s firmware for continuous conversation and sensors support with [gnumpi](https://github.com/gnumpi/esphome_audio/tree/dev-next)'s implementation of media player. Using the media player seems to solve the low volume problem. The firmware implements the "assist query" and "assist reply" sensors which are not used in gnumpi's implementation. The firmware uses "Hey Jarvis" but you can change it to your needs. I didn't use gnumpi's images as I wanted to maintain the original feel. You will need to adjust the firmware to your own environment (wifi, ap, etc.). I did not test it extensively.

I made a few other changes:
 - I removed the frames around the text (I just like it better like that)
 - I clear the query and reply texts so that the old text doesn't display in a new query before the new one displays
 - The time is taken for Home Assistant

Now also includes wifi information, radar, up-time, temp and humidity, internal temp and more thanks to [Christoph](https://github.com/ChristophCaina/ESP32-S3-Box-3-Firmware) 

Thank you [jaymunro](https://github.com/jaymunro), [gnumpi](https://github.com/gnumpi) and [Christoph](https://github.com/ChristophCaina) for your good work. 
