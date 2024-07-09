# Build Guide

Welcome to my build guide for the corne keyboard! In this guide I will outline the steps required to build your own custom keyboard. I've tried to make it as budget friendly as possible, however it turns out that building your own keyboard is a lengthy and pricey task. If you're a beginner looking to enter the world of ergonomically split mechanical keyboards, then I'd 100% recommend diving in and giving it a go. 

Firstly, read the [parts list](https://github.com/theoriseconcepts/ISRTCorne/blob/main/doc/partslist.md) and make sure that you have the necessary parts and tools.

There are lots of helpful build guides on GitHub and YouTube, so if you need more information to help you than I provide, don't hesitate to explore elsewhere and let me know what I'm missing.

# Steps

This process can be long and involve a lot of small, precise work. Make sure you're setup in a comfortable, well-ventilated area with lots of light. The method I found to work best for me is to start with the smallest component and work your way up.

# Step 1: Diodes

I like to start by soldering the diodes to the bottom of the pcb. Take your soldering iron and heat up one of the pads. Then feed a small amount of solder onto the pad. It's important that the diodes are installed in the correct orientation with the line on the diode matching the line on the pcb. Use tweezers to pick up the diode and then heat the pad that has the solder. While the solder is melted you can place the diode onto the board. Once the diode is positioned correctly, you can rotate the pcb and solder the other diode leg. Repeat this process for the remaining diodes.

![DIODES](https://github.com/theoriseconcepts/ISRTCorne/blob/main/doc/images/diodes.jpg)

# Step 2: Hotswap Sockets

Similarly for the hotswap sockets, heat up one of the pads and apply a small amount of solder to cover the pad. Using tweezers, pick up a hotswap socket, ensuring that it is orientated correctly. Heat the pad with the solder and slot the hotswap socket into place, pressing down on the back with the tweezers to make sure it's flush with the board. Once the hotswap socket is positioned correctly, you can rotate the pcb and solder the other hotswap socket leg. Repeat this process for the remaining hotswap sockets.

![HOTSWAP SOCKETS](https://github.com/theoriseconcepts/ISRTCorne/blob/main/doc/images/hotswapsockets.jpg)

# Step 3: TRRS Socket, Reset Switch, Power Switch

Now, flip the board over and locate the TRRS slot. Place the TRRS socket into position and get some heat resistant tape to hold it in place. Carefully flip the board again making sure that the TRRS socket isn't loose, then solder one of the legs. If you're satisfied that the TRRS socket is correctly positioned, solder the other legs, otherwise adjust as needed. Next, do the same process for the reset switch. For the power switch, you need to flip the pcb board and use the same soldering method that we used for the diodes. Repeat this process for the other pcb board.

# Step 4: MCU

For the microcontroller, you can use the pin headers that come with it to solder directly to the pcb, however, I'd recommend using a hotswap socket header. Insert the pin headers into the pcb slot. If the fit is quite tight like mine was, you may need to use a little extra force. You can also take a single pin header and wiggle it in the holes to loosen them up. Once the pin header is in position, secure it with heat resistant tape and check that it's straight. Solder the legs on the bottom of the pcb. Do the same for the other row and board. Then I found it easiest to use a small pair of pliers to pick up the mill max pins and insert them one at a time into the header holes. You should hear each pin click into place. Once done, take your micro controller and place it on top with the logo facing up, and any unused holes will be towards the usb-c end of the board. With the controller correctly placed, you can solder it to the mill max pins. 

# Step 5: Display Module

Display installation will vary depending on the type of screen you choose. The board I'm using has slots for OLED screens and the nice!view. For the nice!view, start by soldering over the OLED holes on the top of the pcb so there are no open connections. Then, insert the nice!view header into the labelled slot and solder the legs in place. Next, insert the socket header and place the nice!view screen on top. Solder one of the joint, then adjust until the screen is horizontal, and solder the rest of the joints. Repeat for the other board. 

# Step 6: Battery

To install the battery, you will need to remove the display. If you used a long header for the mcu, you will need to remove the micro controller so the battery can sit underneath. If like me you used a short header, then you can leave the mcu in place and the battery will sit on top, and under the display. The pcb has two holes at the edge labelled B+ and B- for the battery wires. I decided to solder the wires directly to the pcb, passing the wire ends through the holes on top, (red to B+ and black to B-), then applying solder to the bottom of the board. Do this for both pcbs. Let the battery rest on top of the mcu and secure it in place with some heat resistant tape.

![DISPLAY](https://github.com/theoriseconcepts/ISRTCorne/blob/main/doc/images/display.jpg)

# Step 7: Switches and Keycaps

Now grab the plate and take one switch. Align it in the plate next to the mcu and push it into the respective socket. It should click into place. Now take another switch and place it in the opposite corner. You will need to carefully pull the plate up to ensure that the switches click into place. Repeat this for the other switches. You can now take the keycaps and press those onto the switches, however, first you will want to install the board in a case. 

![SWITCHES](https://github.com/theoriseconcepts/ISRTCorne/blob/main/doc/images/switches.jpg)

# Step 8: Case

(Optional: I needed to sand down the hole for the mcu usb-c port in order to fit the connector for the magnetic cable. I also spray painted the case white.)

Now that the board is fully assembled we can insert it into a case. Start by taking the screws and brass standoffs. Attach these to the base of the case. Then align the standoff holes on the pcb with the standoffs. Don't screw them too tightly as they can be a pain to unscrew if you need to. Next, insert the screw legs to adjust the height and tilt of the case as desired. Finally, add the rubber caps to complete the case. 

![CASE](https://github.com/theoriseconcepts/ISRTCorne/blob/main/doc/images/case.jpg)

# Firmware

Well done, you have successfully built your own custom keyboard!

See the [firmware guide](https://github.com/theoriseconcepts/ISRTCorne/blob/main/doc/firmwareguide.md) for how to install and edit the keyboard firmware.