---
title: "How to Make a Peace Pendant"
pubDate: 2016-03-22
heroImage: "/images/blog/peace-pendant-how-to/9.png"
---

## Rechargeable Sound Reactive LED Peace Pendant — Overview

With all the madness going on in the world right now, a LED sound reactive peace pendant would help radiate some love. Below are instructions on how you can make this cool project.

The circuitry for this wearable project isn't that complex, and the 3D printed enclosure will provide a nice pendant that you can wear to your next party or event.

**Features:**
- Sound reactive
- Rechargeable
- On/Off switch
- Programmable

## Parts

Most of the parts available through Adafruit. Their Weekly shows have 10% off coupons which are a great deal to pick up these parts.

- Arduino or Adafruit Gemma
- NeoPixel Ring (12 LEDs)
- Switch
- #4 3/8 inch Screws (x2) or similar
- Li-Po battery 3.7V 150mAh
- Lipoly battery charger
- Mic Amp
- Necklace and ring
- Micro USB cable for programming/charging
- 22 AWG hook-up wire or any other suitable wire

**Tools and Supplies:**
- 3D printer with filament
- Soldering Iron with solder
- Wire Strippers and pliers
- Hot glue gun and super glue

## Circuit Diagram

![Circuit diagram](/images/blog/peace-pendant-how-to/9.png)

## 3D Printing

Please download the .stl from Thingiverse (thing:1134027) and print out the enclosure and lid. Some support material is required, but nothing intense. Printed in 1.75mm PLA on a PrintrBot Simple Metal at about 220°C. Repetier Host was the 3D printing software using Slic3r. The enclosure was designed in Tinkercad, on a PRINTinZ Zebra plate.

![Print 1](/images/blog/peace-pendant-how-to/1.jpg)
![Print 2](/images/blog/peace-pendant-how-to/2.jpg)

## Assembly

The pendant assembly isn't that complicated. The enclosure was designed to comfortably hold the above-mentioned parts without much hassle. Please see the video for the assembly summary.

1. Start by soldering short lengths of hook-up wire to the LED ring. The front face of the enclosure was designed with holes aligned to the LED ring wire solder points. Mount the ring onto the face of the enclosure and slide the wires into the enclosure. You could use some adhesive to anchor the ring, but this isn't required since the fit is tight enough to hold it in place.

2. Solder a short piece of wire to one of the far-end pins on the slide switch, and connect that to the BAT of the LiPo charger. Solder the RED lead of the JST-PH lead onto the middle pin of the slide switch. Please see the circuit diagram above for an illustration.

3. Push the slide switch into the opening on the side of the enclosure. You could use a small amount of super glue to the edges — be careful not to encircle the entire switch with glue or the switch won't work! You could also use hot glue on the inside to hold the switch in place.

![Assembly step](/images/blog/peace-pendant-how-to/3.jpg)

4. Solder the Black GND lead of the JST-PH lead to the GND on the LiPo charger. Ensure the wires soldered to the LiPo charger are attached to the TOP side of the charger so it sits flush when inserted into the enclosure.

5. Solder short lengths of hook-up wire to the MIC amp. The connections are shown in the circuit picture above.

6. Solder the LED ring wires to the Arduino Gemma according to the circuit diagram.

7. Insert the battery lead into the LiPo charger and seat the charger in the enclosure. Use some hot glue to secure the charger on the enclosure — this matters since the USB cable will constantly be attached and detached for charging.

![Assembly step](/images/blog/peace-pendant-how-to/4.jpg)

8. At this point, the soldering is complete. Let's program the Arduino before final assembly. You will need the Adafruit NeoPixel library for the sketch. Download the Arduino sketch from GitHub and load it onto the Gemma. Once the sketch is loaded, test the flashing of the LEDs by tapping the mic. The LEDs should react to the sound. If it does not work, check your wiring and ensure your Arduino sketch is loaded correctly.

9. Once the circuit is verified to be working, button-up your project by putting the LiPo battery in the enclosure and pass the JST lead under the charger partition built into the enclosure.

![Assembly step](/images/blog/peace-pendant-how-to/5.jpg)

10. If you want to insert a ring to hang the enclosure on a lanyard, now would be the time before final assembly. I used a keyring and slid that on the enclosure.

![Assembly step](/images/blog/peace-pendant-how-to/6.jpg)

11. Let's do the final assembly by inserting the battery first, then the Arduino Gemma. Insert a small plastic spacer before putting in the MIC to prevent any short circuits. Close the enclosure using 2 x #4 3/8 inch screws with the 3D printed lid. Ensure the USB charging port lines up with the opening. Attach a lanyard, beaded necklace, or whatever you like.

## How to Use

![In use](/images/blog/peace-pendant-how-to/7.jpg)

Turn on the pendant by sliding on the switch. Test it by snapping your fingers or clapping. You can adjust the sensitivity of the pendant by playing around with the gain of the MIC (pot on the back of the MIC amp); you can also adjust the sensitivity in the Arduino sketch.

In order to charge the pendant, simply attach a micro USB cable to the LiPo charger.

Now go forth and spread the PEACE!!! :)
Happy Making!
