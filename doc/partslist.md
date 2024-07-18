# Corne Parts List and Buying Guide

The parts list compiled here is based on the factors of affordability, convenience, and functionality. An attempt was made to keep the costs low while also ensuring that the components are of decent quality. Availability of UK suppliers was limited, so hopefully my recommendations prove useful.

If you are aware of alternatives or improvements to my suggestions, please let me know.

# The PCB

Do you want to keep the costs to a minimum? Are you confident in your ability to source parts such as pcb screws, diodes, hotswap sockets, etc? Then I'd recommend using jlcpcb.com to print the corne pcb. Just upload the latest "gerbers" from [foostan/crkbd](https://github.com/foostan/crkbd/releases) onto the frontpage of jlcpcb and either stick with the default options or upgrade to lead free HASL for +1 usd. You can also consider a different colour to the default green if you prefer.

However, if you prefer the convenience of a partial kit to help you get started, then I recommend using [42Keebs](https://42keebs.eu/shop/kits/pro-micro-based/corne-cherry-v3-hotswap-split-ergo-40-kit/?attribute_plate-type=FR4%20(PCB%20material)&attribute_pa_colour=black). This site will provide you with most of the parts needed to build this keyboard, and they also have a soldering service. For my build, I opted to buy the base kit from here with the Controller Sockets/Pins/Headers addon. You can easily find the other components cheaper elsewhere, and do the soldering yourself. 

![42KEEBS](https://github.com/theoriseconcepts/ISRTCorne/blob/main/doc/images/42Keebs.png)

Base FR4 Kit includes: 
- 2x main PCB
- 44x SMD diode (42 + 2 spare)
- 42x Kailh hotswap socket
- 2x TRRS socket
- 2x SMD power switch
- 2x Reset switch
- Brass standoffs and screws
- 2x FR4 switch plate
- 2x bottom plate made from PCB material (FR4)
- 2x clear acrylic covers

# The Components

![COMPONENTS](https://github.com/theoriseconcepts/ISRTCorne/blob/main/doc/images/components.jpg)

The main items you'll require not in the kit are switches, keycaps, and controllers. There are also many other extras I'd recommend to upgrade the look and design of the keyboard. Components such as the case and build tools are also important, so I shall share my recommendations for those as well. 

Many of the items for this build were acquired from AliExpress, so while I shall share links to the stores I used, make sure that you do your own due diligence to avoid purchasing from any suspicious places. I've had good experiences with the "Choice" options, where you get free shipping on orders > 10 usd, taking around 7-10 days to arrive in the UK.

|Part|Quantity|Notes|Price (£)|Link|
|:-----:|:-----:|:-----:|:-----:|:-----:|
|Promicro NRF52840|2|Cheap alternative to nice!nano V2 Wireless Controller. Uses the same ZMK firmware.|4.95/unit|https://www.aliexpress.com/item/1005006371175315.html|
|Lithium Polymer Battery|2|You might be able to find it cheaper elsewhere if it's in stock. Anything similar to 90mAh 301228 will fit.|7.39/unit|https://www.ebay.co.uk/itm/265318798148|
|Display Module|2|For ease of installation and software support choose the nice!view LCD Display. If you're comfortable troubleshooting display issues, then the aliexpress option is an okay alternative.|20.28/unit (1.20/unit)|https://42keebs.eu/shop/parts/niceview-power-efficient-lcd-display/ (https://www.aliexpress.com/item/1005005281308478.html)|
|5 Pin Linear Switches|42 x Switches|5 pins is a must have, but otherwise, choose your favourite style of switch. I'm liking the sound and feel of the Outemu silent cream switches.|3.74/50 PCS|https://www.aliexpress.com/item/1005006270820565.html|
|DSA Blank Keycaps|40 x 1u Keycaps, 2 x 1.5u Keycaps|Keycaps are something that you can spend a lot of time and money on. If you're looking for blank DSA keycaps like I was, then this is the best option I could find.|30/set|https://mechboards.co.uk/products/split-keyboard-dsa-blank-keycaps|

Once you've acquired the above components, you're ready to build a functioning keyboard. There are however a few more components I'd recommend that can take your keyboard to the next level. 

|Part|Quantity|Notes|Price (£)|Link|
|:-----:|:-----:|:-----:|:-----:|:-----:|
|Corne Keyboard Case|1 (Left and Right)|There are many options available for corne keyboard cases. Most likely you'll need to find and order a 3D print model that you like.|37.52|https://www.printables.com/model/347524-corne-keyboard-case-5-and-6-columns (https://www.fiverr.com/harvey_cad/3d-print-anything-and-deliver-it-to-you-in-the-uk)|
|M5 Hex Socket Head Cap Screws|8 (Various Lengths)|If you opt for a 3D printed case like mine, then there is the option to use these screws as tenting legs.|9.99/150 PCS|https://www.amazon.co.uk/dp/B0BVFXF5HW|
|Silicone Rubber Round End Caps|8|Can be used to cover screw ends. Depending on screw orientation, this will either act as a desk support or aesthetically cover the screw legs.|1.20/10 PCS|https://www.aliexpress.com/item/1005002270601725.html|
|Magnetic USB to USB-C cable|2|Make sure it's not charging only. The usb port of the mcu will wear out quickly if these are not used. I like the 2m cable. Cheap alternative from aliexpress that wasn't available at time of building.|11.90/3 PCS|https://www.amazon.co.uk/dp/B07QKDG4HY (https://www.aliexpress.com/item/1005003776565766.html)|
|3.5mm 4 Pole Stereo Audio Cable|1|Useful to ensure that you have a wired option if required.|7.99|https://www.amazon.co.uk/dp/B09WCF8JZC|

# Tools

You will need the following tools:
- Soldering iron
- Solder
- Solder wick
- Cleaning ball
- Screwdriver
- Tweezers
- Pliers

A great cheap solder kit to get you started: https://www.amazon.co.uk/dp/B07Q4T12PH - £13.99 and https://www.amazon.co.uk/dp/B09VP79Y32 - £11.99

It's also nice to have:
- Safety goggles - https://www.aliexpress.com/item/1005005908055909.html - £1.82
- Helping hands - https://www.aliexpress.com/item/1005005615276375.html - £15.66
- Silicone Heat Mat - https://www.amazon.co.uk/dp/B0C6JPV1LY - £9.99
- Heat resistant tape - https://www.amazon.co.uk/dp/B07FBGPB96 - £4.99
- Keycap Removal Tool - https://www.amazon.co.uk/dp/B09838V6Q9 - £2.29