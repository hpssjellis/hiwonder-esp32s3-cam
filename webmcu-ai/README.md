

This si a quick port of the hiwonder esp32s3 cam vision ML to my webmcu-ai on-device ML full stack.

Since the hiwonder does not come with an sd card, I can't do the entire process, but I can 
train on a webpage, create the myWeights.h include file and transfer that file to the arduino build 
and then the model can run inference by choosing menu item #5.

Lots of I2C errors on load, but yes it does seem to work, just at the moment not very well.


webmcu-AI at  https://github.com/webmcu-ai

The active ML training webpage is at   https://webmcu-ai.github.io/webmcu-vision-web/index.html





