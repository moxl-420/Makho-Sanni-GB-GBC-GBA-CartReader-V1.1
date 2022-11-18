# Currently this is still a WIP as I'm still building and waiting for parts, this should get you on your way however.

## First I want to state that I create nothing but the 3d files for the case!
See this as a buildguide for myself in the future in case I want to recreate it.

## Links:
Stl files for the case:

https://www.thingiverse.com/thing:5638408

https://www.printables.com/model/319780-gb-gbc-gba-makho-sanni-cart-reader-case

Since this is based on the Sanni V3 here are the links to their info:

Sanni V3 software:

https://github.com/sanni/cartreader/releases

Sanni V3 user guide:

https://github.com/sanni/cartreader/wiki/User-Guide

Makho's Instructional video how he created this: (All links below for Makho can be found in the description of the video)
https://www.youtube.com/watch?v=kCagzAQVYlU (I recommend using sockets for everything if you're going to follow the video so that it will fit the case)

Makho's Buildpics:
https://imgur.com/a/HU23kEP

Makho's list of materials needed:
(For Female sockets I've used standard rows which I cut to length, detailed later)
https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbGg4NzhpQ1lQLWtycWJqbnNNSXRtSXpWUGFDQXxBQ3Jtc0tsRTVGdnRPRFRHQ0dtNGgyVURKVGdBclhFUVFEOXQ3SUU5a015RG94b25sNFFQcFpvQ3ZEQTkzN215UE9YZ2p6ZFJjS3gwU2xfLVQwZjNBV1NrVlV5ZFg4ejZMWXJ4ZkhuQVZmV2JEaVg1VGdYSXBjOA&q=https%3A%2F%2Fwww.dropbox.com%2Fs%2Fdc057hifxfi4ps4%2Fbom.xls%3Fdl%3D1&v=kCagzAQVYlU

Makho's Gerber Files:
https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa2JCWmNkeE10TTNpS3pfWkhzT2ZWekdOV2hhQXxBQ3Jtc0trSFZnNTQ5UFhYbTBGbnhfZTN3RE56TFJidU5ic0ttNEkxNk1xNGxGZzBaLWUyaTRFODB1VkVPSm9rZ3hHckNaeXBySTlpMjFPeEp4ZWpYT2J0d1hrRktxakt5eWhVUk5NSHN0WGNSN0l4OHg2SFlSSQ&q=https%3A%2F%2Fwww.dropbox.com%2Fs%2F90a4kdka3ctof63%2Fsanni_gba_v1.1.zip%3Fdl%3D1&v=kCagzAQVYlU

The Gerber files should be 1.6mm. I payed 12.3€ incl shipping to Europe for 5. 

![This is an image](https://i.imgur.com/FQWu6kX.jpg)

## Once everything is arrived from the list it's time to start building. 
### Soldering the underside.
The first thing you should do is attach the resistors or the buttons won't work. 
10k ohm resistor with code 103.

![This is an image](https://i.imgur.com/OmdcHLY.jpg)

Because afterwards it can get crowded:

![This is an image](https://imgur.com/mURZnYB.jpeg)

For the oled screen you must set the jumpers depending on your model.
My screen was GND-VCC-SCL-SDA

![This is an image](https://imgur.com/F35PndN.jpeg)

JP2 should be set to GND and JP1 to VCC as show below. If yours is switched, you should switch the bridging:

![This is an image](https://imgur.com/lCxJEP9.jpeg)

- Start with the voltage regulator in red.
- The USB C charging port (which is missing because I forgot to order it)


![This is an image](https://imgur.com/e7E3ECT.jpeg)

For all sockets I've cut them to length and used coarse (80grit) sandpaper to have flush ends.

- The sockets for the sd card depending on your model, I have a MicroSD
- The sockets for the Arduino (If you're not gonna use sockets, this is the time for the buttons else can be done later)
- The buttons (check orientation in able to fit the case)
- The battery terminals
It should look something like this:

![This is an image](https://imgur.com/EcQOmzu.jpeg)


The 5V to 3.3V step-down converter should be installed like this:
5v   in
3.3v out

![This is an image](https://imgur.com/NCOpwEl.jpeg)

For the sd cardreader I've chosen to not bend the pins but to solder straight pins in:

![This is an image](https://i.imgur.com/4MJYfZs.jpeg)

### Soldering the top
If you haven't soldered in the buttons yet, now is the time.
There are multiple choices for buttons, I went with what I had laying around. Ajazz Bananas in this case.
Solder the following components:
- 4-pin socket for the Oled screen
- The Led (The longest lead goes through the hole marked VCC)
- The GB cart slot
If you're finished it should look something like:

![This is an image](https://imgur.com/Huo3bZH.jpeg)

### Populating the board.

I put the pins in the sockets of the Arduino and afterwards put the arduino in it to solder the pins, using the motherboard as a jig.
When done it should look something like this:

![This is an image](https://imgur.com/GKp9fzA.jpeg)

![This is an image](https://imgur.com/ZPWdfm6.jpeg)


## Printing the case:
### This is not on Makho's list of items needed as he didn't create the case.
You'll need 3x M3 5-8mm thread screws 
(in these pictures V2 of the case is shown, in the links below you'll find later versions.)

You can choose either links:

https://www.printables.com/model/319780-gb-gbc-gba-makho-sanni-cart-reader-case

https://www.thingiverse.com/thing:5638408


Place the pcb in the bottom parts with the 2 switches first.

![This is an image](https://imgur.com/8PbXPuj.jpeg)

With the top part on:

![This is an image](https://imgur.com/uNFuw9j.jpeg)


# Flashing the Arduino

You can follow the Sanni Guidelines:
https://github.com/sanni/cartreader/wiki/User-Guide

The only thing you have to keep in mind is that you have to define the HW model as HW3
and that you can comment most other systems as it can only read GBx games.
![This is an image](https://i.imgur.com/AuONNzz.png)

# Using the device

In the guidelines of Sanni you can find the full behaviour of the buttons:
https://github.com/sanni/cartreader/wiki/User-Guide 

Below is a snippet of their info:

♻️ Button 1

    Press once to move the selection down.
    Double-click to move the selection up.
    Hold longer to execute current selection.
    While inside the filebrowser you can go to the next page by moving the selection down once more after you reached the last item on the current page.
    In a similar fashion you can go back one page by double-clicking while the first item is selected.
    You can enter a folder by holding button 1 pressed longer.
    You can go back to the SD's root folder by double-clicking until you reach the first selection of the first page and then double-clicking once more.

🔴 Button 2

    Press to execute current selection.
    When in filebrowser mode enters a directory.
