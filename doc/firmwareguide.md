# Firmware Guide

In this section I will go through the [ZMK Installation Guide](https://zmk.dev/docs/user-setup) in order to clarify and comment on the required steps to setup your keyboard with ZMK firmware. 

I'll also mention a couple of methods to edit the keymap so that you can easily get your desired layout up and running.

# Prerequisites

1. You have an active, working [GitHub](https://github.com) account.
2. You have installed and configured the [git](https://git-scm.com) version control tool.
3. You have locally configured git to access your github account. 

# GitHub Repo

You will first need to create a new GitHub repository to host the config.

1. Navigate to https://github.com/new
2. When prompted for the repo name, enter zmk-config (or zmk-config-corne).
3. The repository can be public or private
4. Do not check any of the options to initialize the repository with a README or other files.
5. Click "Create repository"

# User Config Setup Script

To start the setup process, navigate to the local folder you want to connect to your git repository. Open and run Git Bash here. Then run the following from your command line prompt: 
~~~
bash -c "$(curl -fsSL https://zmk.dev/setup.sh)"
~~~
If you encounter the following or similar error, disabling your antivirus may resolve the issue.
~~~
curl: (35) schannel: next InitializeSecurityContext failed: CRYPT_E_NO_REVOCATION_CHECK (0x80092012) - The revocation function was unable to check revocation for the certificate.
~~~

# Keyboard Selection

When prompted, enter the number for the corresponding keyboard you would like to target:
~~~
Keyboard Selection:
 1) 2% Milk                    21) CRBN Featherlight        41) Leeloo                  61) Redox                           81) Zodiark
 2) A. Dux                     22) eek!                     42) Leeloo v2               62) REVIUNG34                       82) Quit
 3) Advantage 360 Pro          23) Elephant42               43) Leeloo-Micro            63) REVIUNG41
 4) BAT43                      24) Ergodash                 44) Lily58                  64) REVIUNG5
 5) BDN9 Rev2                  25) Eternal Keypad           45) Lotus58                 65) REVIUNG53
 6) BFO-9000                   26) Eternal Keypad Lefty     46) MakerDiary m60          66) Romac Macropad
 7) Boardsource 3x4 Macropad   27) Ferris 0.2               47) Microdox                67) Romac+ Macropad
 8) Boardsource 5x12           28) Fourier Rev. 1           48) Microdox V2             68) S40NC
 9) BT60 V1 Hotswap            29) Glove80                  49) MurphPad                69) SNAP
10) BT60 V1 Soldered           30) Helix                    50) Naked60                 70) Sofle
11) BT60 V2                    31) Hummingbird              51) Nibble                  71) splitkb.com Aurora Corne
12) BT65                       32) Iris                     52) nice!60                 72) splitkb.com Aurora Helix
13) BT75_V1                    33) Jian                     53) nice!view               73) splitkb.com Aurora Lily58
14) Chalice                    34) Jiran                    54) nice!view adapter       74) splitkb.com Aurora Sofle
15) Clog                       35) Jorne                    55) Osprette                75) splitkb.com Aurora Sweep
16) Contra                     36) KBDfans Tofu65 2.0       56) Pancake                 76) Splitreus62
17) Corne                      37) Knob Goblin              57) Planck Rev6             77) TG4x
18) Corneish Zen v1            38) Kyria                    58) Preonic Rev3            78) Tidbit Numpad
19) Corneish Zen v2            39) Kyria Rev2               59) QAZ                     79) Waterfowl
20) Cradio/Sweep               40) Kyria Rev3               60) Quefrency Rev. 1        80) ZMK Uno
         
Pick a keyboard:
~~~
In this version you would select: 17) Corne

# MCU Board Selection

When prompted, enter the number for the corresponding MCU board you would like to target:

~~~
MCU Board Selection:
1) Adafruit KB2040               10) nice!nano v2                       19) Puchi-BLE V1
2) Adafruit QT Py RP2040         11) Nordic nRF52840 DK                 20) QMK Proton-C
3) BlackPill F401CC              12) Nordic nRF5340 DK                  21) Seeeduino XIAO
4) BlackPill F401CE              13) nRF52840 M.2 Module                22) Seeeduino XIAO BLE
5) BlackPill F411CE              14) nRFMicro 1.1 (flipped)             23) Seeeduino XIAO RP2040
6) BlueMicro840 v1               15) nRFMicro 1.1/1.2                   24) SparkFun Pro Micro RP2040
7) BoardSource blok              16) nRFMicro 1.3/1.4                   25) Quit
8) Mikoto 5.20                   17) nRFMicro 1.3/1.4 (nRF52833)
9) nice!nano v1                  18) PillBug

Pick an MCU board:
~~~

In this version you would select: 10) nice!nano v2

The controller I am using in my build is not a 'nice!nano v2' however it is compatible so we can select this option.

# Keymap Customization

At the next prompt, you have an opportunity to decide if you want the stock keymap file copied in for further customization:

~~~
Copy in the stock keymap for customization? [Yn]:
~~~

Hit Enter or type yes/y to accept this. You can edit this file later to add your own custom keymap.

# GitHub Details

In order to have your new configuration automatically pushed, and then built using GitHub Actions, enter some information about your particular GitHub info:

~~~
GitHub Username (leave empty to skip GitHub repo creation): yourusername
GitHub Repo Name: zmk-config
GitHub Repo: https://github.com/yourusername/zmk-config.git
~~~

# Confirming Selections

The setup script will confirm all of your selections one last time, before performing the setup:

~~~
Preparing a user config for:
* MCU Board: corne
* Shield: nice!nano v2
* GitHub Repo To Push (please create this in GH first!): https://github.com/yourusername/zmk-config.git

Continue? [Yn]:
~~~

After hitting Enter or typing y, the script will create an initial config in a directory named after the repo name, update the GitHub Action YAML file, commit the initial version, and then push to your repo.

~~~
> git add .
> git commit -m "initial commit"
> git push
~~~

# References for Keymaps

- Using the default keymap or my custom [keymap](https://github.com/theoriseconcepts/ISRTCorne/blob/main/layout/corne.keymap) as a reference, open the file in an IDE such as VSCode, and edit as desired. You can find all the documentation that you might need at https://zmk.dev/docs.
- If you prefer a more visual approach to key mapping. then I recommend this helpful [keymap editor](https://nickcoutsos.github.io/keymap-editor/) by Nick Coutsos.

# Firmware Edits

- Open [build.yaml](https://github.com/theoriseconcepts/ISRTCorne/blob/main/layout/build.yaml) and to both shield lines, you need to add:

~~~
nice_view_adapter nice_view
~~~

- Now open [corne.conf](https://github.com/theoriseconcepts/ISRTCorne/blob/main/layout/corne.conf) and you can add the optional code:

~~~
# Set deep sleep to 30 minutes
CONFIG_ZMK_SLEEP=y
CONFIG_ZMK_IDLE_SLEEP_TIMEOUT=3600000

# Make Bluetooth stronger
CONFIG_BT_CTLR_TX_PWR_PLUS_8=y

# Change board name (Keep it under 16 characters)
CONFIG_ZMK_KEYBOARD_NAME="Corne View"
~~~

# Installing the Firmware

Once the setup script is complete and the new user config repository has been pushed, GitHub will automatically run the action to build your keyboard firmware files. You can view the actions by clicking on the "Actions" tab on your GitHub repository. Once you have loaded the Actions tab, select the top build from the list. Once you load it, the right side panel will include a link to download the firmware. Once downloaded, extract the zip and you can verify it should contain one or more uf2 files, which will be copied to your keyboard.

# Flashing UF2 Files

To flash the firmware, first put your board into bootloader mode by double clicking the reset button (either on the MCU board itself, or the one that is part of your keyboard). The controller should appear in your OS as a new USB storage device.

Once this happens, copy the correct UF2 file (e.g. left or right), and paste it onto the root of that USB mass storage device. Once the flash is complete, the controller should unmount the USB storage, automatically restart and load your newly flashed firmware. It is recommended that you test your keyboard works over USB first to rule out hardware issues, before trying to connect to it wirelessly.

# Wirelessly Connecting Your Keyboard

You should be able to see your keyboard from the Bluetooth scanning view of your device. ZMK supports multiple BLE “profiles”, which allows you to connect to and switch among multiple devices. If you don't make use of the mentioned behaviours you will have issues pairing your keyboard to other devices.

After flashing each half individually you can connect them together by resetting them at the same time. Within a few seconds of resetting, both halves should automatically connect to each other.