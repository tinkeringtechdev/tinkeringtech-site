---
title: "Xerox Project - Bag Security Device"
pubDate: 2012-03-28
heroImage: "/images/blog/xerox-bag-security-device/1.jpg"
---

![Bag security device 1](/images/blog/xerox-bag-security-device/1.jpg)
![Bag security device 2](/images/blog/xerox-bag-security-device/2.jpg)
![Bag security device 3](/images/blog/xerox-bag-security-device/3.jpg)
![Bag security device 4](/images/blog/xerox-bag-security-device/4.jpg)
![Bag security device 5](/images/blog/xerox-bag-security-device/5.jpg)
![Bag security device 6](/images/blog/xerox-bag-security-device/6.jpg)
![Bag security device 7](/images/blog/xerox-bag-security-device/7.jpg)
![Bag security device 8](/images/blog/xerox-bag-security-device/8.jpg)
![Bag security device 9](/images/blog/xerox-bag-security-device/9.jpg)
![Bag security device 10](/images/blog/xerox-bag-security-device/10.jpg)

A few months ago, some college colleagues and I started work on a prototype for patent number 7,535,358 B2, Method and Apparatus for Electronically Tracking Luggage. This was the Xerox fellowship project that our group had to complete for the semester. Having led the effort and tackling the hardware aspect, I decided to publish a small report on the work that was accomplished along with the design details. All the hardware that was used is open source and cost around $250. Here is a list of the hardware used:

- Arduino UNO
- Sparkfun GSM cellular module with patch antenna
- Adafruit SD logger Shield
- EM-406A GPS module
- 6 AA Rechargeable batteries
- Photocell (light sensor)
- Reed switch
- Medium OtterBox for the enclosure

The device would be placed in a piece of luggage with the photocell and reed switch as the primary triggers. The SD card shield would record an entry onto the SD card every minute, with the Unix timestamp, light sensor and photocell value, latitude and longitude. The time is kept by the RTC on the SD logger shield. If the light sensor or the reed switch thresholds were surpassed, the system would immediately send an SMS through the GSM module to a Twitter account to indicate that the bag had been opened.

Here is the Arduino code for the final device... excuse me for the crappy coding :)

The logged data can be analyzed in the following ways: the owner of the bag could upload the logged data using a simple uploader script to a website that we built. Once uploaded the data is parsed and plotted indicating spikes in the light sensor or reed switch readings along with a Google map showing the locations in the spikes. It is always possible that the GPS module would not have a fix as the bag enters structures that inhibit GPS fixes.

A webpage had also been constructed to scrub the last 10 tweets posted via SMS to the Twitter account. Once scrubbed, the Tweet was parsed for the timestamp and latitude/longitude data. The information was then pushed onto the Google maps API where the location information was pinned. One of the hardest things to do was to fit everything in the Otterbox without shorting/crushing my electronics. It worked out well. The Otterbox is an awesome enclosure btw.

Please contact me with any questions regarding this project. I would be more than happy to assist. Thanks to all the folks at Adafruit for your assistance and awesome documentation. Keep doing what you are doing, you are inspiring budding engineers such as me to try stuff they have never before. Your prompt responses to my forum questions really helped in getting this thing to work. This device is a bit ahead of its time in terms of regulations to be used on an airplane. Once the Feds allow cellphone use on airplanes, this device would be able to fly!

Cheers!!
Lali
