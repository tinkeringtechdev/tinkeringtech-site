---
title: "Sparkfun Cellular Shield"
pubDate: 2011-12-28
heroImage: "/images/blog/sparkfun-cellular-shield/1.jpg"
---

![Sparkfun Cellular Shield 1](/images/blog/sparkfun-cellular-shield/1.jpg)
![Sparkfun Cellular Shield 2](/images/blog/sparkfun-cellular-shield/2.jpg)
![Sparkfun Cellular Shield 3](/images/blog/sparkfun-cellular-shield/3.jpg)

I bought the Sparkfun Cellular Shield SM5100B with an Arduino UNO, and Quad-band Wired Cellular Antenna SMA antenna. Hope to use it for an upcoming project. Here's how I set it up. I followed the instructions at [tronixstuff.wordpress.com](http://tronixstuff.wordpress.com/2011/01/19/tutorial-arduino-and-gsm-cellular-part-one/) to get the cell module working. Everything went well till I got to the part for setting up the band for the US. I was using a T-mobile post paid SIM card. T-mobile is on the GSM850&PCS1900 i.e AT+SBAND=7. This was the message on startup:

```
+SIND: 1
+SIND: 10,'SM',1,'FD',1,'LD',1,'MC',1,'RC',1,'ME',1
+SIND: 3
+SIND: 4
+SIND: 8 (loss of signal)
```

I eventually figured out that the band setting for the US was not set correctly on the module. I did that by using ZedLeps code modification at sparkfun.com/products/9607, uploading the sketch to the board, and then entering `AT+SBAND=7` in the arduino serial monitor. This did the trick. I also had to hit the reset button on the UNO using a piece of plastic to reach under the shield once I made the change. This time around, success! Got `+SIND: 11`. Eventually managed to send text messages and receive a call.
