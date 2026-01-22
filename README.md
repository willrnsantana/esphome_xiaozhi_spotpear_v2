A W.I.P yaml for replacing the original sporpear firmware with a esphome compatible one.

This is a "fork" from the original file from:
https://github.com/RealDeco/xiaozhi-esphome/tree/main/devices/Spotpear%20Balls

All the warnings listed on the original applies

What it changes:

1 - Adds controls for auto dim (turn on/off) the screen. It lights up upon wake word and dims after N seconds to configurable brightness settings
2 - Adds controls for wake light, using the embeded RGB Led (but separate settings) so it lights up on wake word, fast blinks on "thinking" and 
    slow blinks during response. It just mimics the echo devices behavior for a more polished interaction. The embedded LED goes back to it's 
    previous setting after the interaction
3 - Leas but not last, it integrates the media_player component for future uses as a output speaker for Music Assistant for example. It 
    **DO NOT WORK** currently, but I'm working with @meconiotech in his absolute amazing full duplex i2s audio driver (https://github.com/n-IA-hane/intercom-api), 
    so even simple devices like the spotpears in wich mic and speaker share a single i2s bus can have full duplex audio (so the wake word can be 
    always on even with music playing or to interrupt responses. In the future, using his intercon project maybe even drop-in style intercom should
    be possible.
