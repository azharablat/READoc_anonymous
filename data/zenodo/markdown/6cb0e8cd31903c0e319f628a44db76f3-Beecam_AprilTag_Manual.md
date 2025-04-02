![A group of bees on a wood surface

Description automatically generated](data:image/png;base64...)

**BeeCam-AprilTag**

# User Manual

**Version 1.0**

**08/01/2024**

**Table of Contents**

1. Introduction 1

1.1 Overview 1

2. Getting Started 2

2.1 Wi-Fi Adapter Set-up 2

2.2 Set the System Time 5

2.3 Connect Wirelessly and Launch BeecamPreview 5

2.3.1 Queen 5

2.3.2 Workers 9

3. Using the System in the Field 12

3.1 Solar Panel and Battery Installation 12

3.1.1 Supplies 12

3.1.2 Procedure 13

3.2 Wifi Antenna Installation 13

3.3 Collect Data 15

3.4 Video Recording 20

4. Troubleshooting & Support 24

4.1 RPi Unable to Boot 24

4.2 Troubleshooting the Clock 25

4.3 VNC Failing to Connect 27

4.4 Change Desktop Resolution 27

5. Tagging Protocol 30

## Introduction

This manual is a compilation of documents prepared throughout the testing and initial deployment of the Beecam AprilTag system. This manual includes the initial steps necessary to use the Beecam Raspberry Pi system as well as other common procedures during operation. It also includes guides for installing hardware in the field, such as the solar panel power system and the external Wi-Fi adapter.

### Overview

The Beecam AprilTag system is designed to record the foraging trip duration of individual honeybees across multiple colonies in an apiary. The bees are identified individually with the open source fiducial tag, AprilTag. We’ve generated a custom family of circular AprilTags for this system. The custom family contains enough tags to track thousands of individual honey bee foragers but with few enough pixels per tag to be printed at a readable size and resolution. The tags are read at the entrance of the hive. Each hive entrance is monitored by a Raspberry Pi (RPi) computer with a camera module.

The overall goal of this system is to collect large amounts of data over a long period of time in the field, rather than in a lab or observation hive setting. In this document, we will outline how to set up the wireless network for the RPis, install hardware in the field, and operate the system with a remote desktop connection.

## Getting Started

It is important to ensure a functioning system and good wireless connection between each Raspberry Pi indoors before setting up the whole system in the field. We will learn how to connect wirelessly to the Raspberry Pis, create and save remote connections using RealVNC, and manually start the program “BeecamPreview” if it is closed for any reason.

You will need to connect a monitor, keyboard, and mouse to the Queen initially, and the workers will connect automatically once the wireless network is set up.

### Wi-Fi Adapter Set-up

Before deploying outdoors, let’s configure the Wi-Fi adapter to automatically establish the hotspot connection. This will significantly increase the range of the wireless network in the field. Hardware and accessories for installation are shown in the following picture ready for installation.

![A black antenna on a wood surface

Description automatically generated](data:image/jpeg;base64...) ![A black rectangular object with two antennas

Description automatically generated](data:image/jpeg;base64...)

Ensure all holes, especially those around the antenna, are sealed using hot glue. It is highly recommended to insert silica gel packs to prevent any moisture accumulation inside the box.

**Configuration**

1. Connect the dongle to the USB3.0 port on the Queen (it will provide a faster connection).
2. Turn on the Queen Raspberry Pi and click the wireless connection Icon ![A red x on a white background

   Description automatically generated](data:image/png;base64...) on the top right corner of the screen. Then select Advance Options >> Edit Connections.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. Select the network “queen” and click on the gear icon at the bottom to edit its configuration.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. When you select the option “device” you will see two options for wlan1 and one option for wlan0. By default, this connection has the wlan0 ID option pre-selected. Select the second option for wlan1 which corresponds to the new dongle you just connected. Your options will differ from picture below.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. Then click on the “General” tab and make sure the box “Connect automatically with priority” is selected. The options should look like the image below:

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

1. Finally, click “Save"
2. Now Restart the Queen, and make sure the network “queen” shows up automatically and that you can connect to it. The password is “queen1234”

### Set the System Time

In the field, the RPis will keep time with the external clock connected to the Queen. There are two ways to set the external clock’s time. The first, and simplest, is to connect the Queen to wifi. This will accurately update the system time, which can then be written to the external clock with the terminal command

sudo hwclock -w

The second method is to manually set the system time and write it to the external clock instead. To manually set the time, enter the terminal commands

sudo date -s 'YYYY-MM-DD HH:MM:SS’

sudo hwclock -w

The external clock module will have some drift, but you can always reset the time manually in the field if need be.

### Connect Wirelessly and Launch BeecamPreview

In this section, we will learn how to connect wirelessly to the RPis, create and save remote connections using RealVNC and manually start the program “BeecamPreview” if it is closed for any reason.

#### Queen

First, turn on the “Queen” and wait for 5 seconds to turn on the rest of the “Workers”.

In your personal computer, go to the WIFI networks and look for the network called “queen”.

Select it, and type the password: **queen1234**

Once the connection has been stablished, open the application RealVNC viewer.

In the top bar type the static IP address for the “Queen” **10.42.0.1** as shown below.



Then, a small window will pop up. There you must type the username **master** and password **1234**.

Check the box “remember password” so the application will connect without asking for these credentials in the future.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

After clicking in “OK” you should be able to see the Queen’s desktop with the camera preview running. Now that you have stablished a secure remote connection to the Queen, go back to the RealVNC window.

Let’s name this remote connection we just created, so in the future we connect automatically by selecting it.

Right click and select properties

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

In the name section type “Queen” and click “OK”.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

Done! You have saved the connection credentials for the “Queen”

![A screenshot of a browser

Description automatically generated](data:image/png;base64...)

Now let’s close the camera preview and re-launch the program.

Double Click in the connection “Queen”

To close the preview, click the camera window, then hit the “esc” key. This is the proper way to close the preview for any reason.

On the desktop, look for the application “BecamPreview” ![A logo of a bee

Description automatically generated](data:image/png;base64...) and double click on it. You will launch the program.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

Click on “Execute”

And you will see the Camera preview displaying the camera view.

That’s it! Now the program is ready to collect data from any tag.

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

#### Workers

Let’s now connect to the Workers. Remember that “Queen” generates a WIFI hotspot which Workers use to connect and share data. Thus, “Queen” must be on to stablish a connection to Workers.

Workers share similar IP addresses. They are differentiated by the last digit, which is their corresponding Worker number:

Worker 01 : 10.42.0.11
Worker 02 : 10.42.0.12
Worker 03 : 10.42.0.13
Worker 04 : 10.42.0.14
Worker 05 : 10.42.0.15

Procedure to connect to Workers is the same as for Queen, having as the only difference the IP addresses and username. We will show the procedure for Worker01. For the rest of the workers just use their corresponding IP addresses.

All workers share the same Username, “**pi**” and password, “**1234**”

For “worker01” type the corresponding IP address and press enter.

![A white stripe on a gray surface

Description automatically generated](data:image/png;base64...)Type the username/password and check box “remember password”

![A screenshot of a computer password

Description automatically generated](data:image/png;base64...)

Click “OK” and you should see the following window

![A screenshot of a computer

Description automatically generated](data:image/png;base64...)

The RPis automatically launch the application “BeecamPreview”. You should see a small window that shows the camera view.

Follow the same procedure for the Queen to name you connection as “Worker01”.

Finally, follow the same procedure to create the connections for the rest of the Workers.

You should get the following connections

![Screens screenshot of a computer

Description automatically generated](data:image/png;base64...)

After naming them correctly:

![Screens screenshot of a computer

Description automatically generated](data:image/png;base64...)

Once all the Raspberry Pis have the application “BecampPreview“ launched, the system is ready to collect data.

Remember that seeing the camera preview on the desktop means the program is running without issues. If not, refer to troubleshooting section.

## Using the System in the Field

### Solar Panel and Battery Installation

![A diagram of a power supply system

Description automatically generated](data:image/png;base64...)

#### Supplies

First, check that all supplies are present. Below is a list of all supplies needed along with a diagram of assembly.

Electronics

* Solar panel
* Solar power controller for Lithium battery
* Lithium battery
* DC to USB-C converter

Connectors and wires

* Solar extension cable
* Battery cable
* Electrical wire
* Switches
* Alligator clamps
* Battery box
* Waterproof container

#### Procedure

The following steps show how to assemble to solar panel and battery power system.

1. First, open the solar power controller and connect the corresponding wires to each output. (As a general note red cables go to the positive terminal and black cables go to the negative terminal)
2. PV input must be connected to the solar panel cable extension.
3. Battery input must be connected to the battery cable (circular terminals go to battery pins)
4. Load input must be connected to the wires that go to the Pis.
5. Once all wires are connected to the solar controller, connect the battery (CAUTION: Battery always must be connected first)
6. The solar controller must be powered now. We need to select the type of battery the controller will charge. Use the button next to the screen to navigate, you will see by default is set Lead-Acid\_GEL. Press the button for 6 seconds until the screen blinks. Then press again until you find the option LiFePO4-4s. This option refers to the type of battery we have (Lithium 12.8V). Keep pressing for 6 seconds to save and exit. Double check the previous selection was done by navigating on the screen and seeing the selection of lithium there.
7. Once the battery is connected and set for the correct type of battery. You can connect the solar panel to the controller using the solar cable extension.
8. Navigate on the screen to see how much power the solar panel is providing. You must see now numbers in the options “CHG Curr” and “CHG Power”.
9. Now you should be able to power all your Raspberry Pi (RPi). Make sure you label each switch with its corresponding RPi. You can double-check if power is being provided to the loads by navigating in the controllers and see what numbers are shown in the options “LoadCurr” and “LoadPower”.

### Wifi Antenna Installation

The following steps show how to connect and position the external Wi-Fi adapter.

1. Install the USB-C adapter as shown in the following picture using the gland cord grip on the left side of the Queen RPi’s junction box. Don’t forget to use tape to ensure it’s tight when attached to the gland grip.

![A white box with a black rectangular object inside

Description automatically generated](data:image/jpeg;base64...) ![A person holding a white object with a black cord

Description automatically generated](data:image/jpeg;base64...)

1. Then, attach the universal clamps to the back side of the black box using Velcro.

![A plastic bag with blue objects on a table

Description automatically generated](data:image/jpeg;base64...) ![A black and blue device with white wheels

Description automatically generated](data:image/jpeg;base64...)

1. Finally, install the WiFi box using a pole around 1.5 to 1.7 meters (4.9 - 5.6 ft) above ground. As shown in the following picture.

![A group of beehives in a yard

Description automatically generated](data:image/jpeg;base64...)![A hook with blue pegs on it

Description automatically generated](data:image/jpeg;base64...)![A black and blue device with blue handles

Description automatically generated](data:image/jpeg;base64...)

### Collect Data

In this section we will show how to access the data and transfer it to your personal computer. The “Queen” RPi collects the data from all the workers and stores it in a file that can be identified by the worker’s name.

If your RPi computers detected a tag they will automatically add that detection to a text file where all of the data is collected. If no tags have been detected, no text file will be generated.

Therefore, in order to test the data sharing, make sure tags have been placed in front of the camera. When tags are detected, the software will sketch a blue frame over the tag displaying the tag ID number and its direction with a green bar. The image below shows tags being detected on the right. The tags on the left are not being detected so no data is being recorded for those tags.



Once you have tags detected, let’s access the folder with the data.

Connect to the “Queen” and open the “File Manager”  that can be found next to the Raspberry Pi icon on the top-left corner.



Select the folder “Documents” and inside select the folder “Data”.

Now you can see the files generated by the “Queen” and ”Workers”



If you open one of the files you can see on each row a tag detection with its corresponding time stamp, ID, position, orientation and CPU temperature.



Now that you made sure you have data. Let’s transfer it to your personal computer.

Close the previous windows.

Then, make a right click on the VNC icon  (on the top-right corner of the screen) and select “File Transfer”



Select the folder where the data is located. Select Documents\, Data\ and the file you want to transfer. If you want to change location where the files will be store in your personal computer on the bottom choose and option for “fetch files to”



### Video Recording

In this section we will show the steps to record the preview window generated by the BeeCam application.

First, make sure the application BeeCam is running, and the entrance preview is displayed.

Then, click on the Raspberry Pi icon ![A red raspberry with green leaves on a white plate

Description automatically generated](data:image/png;base64...) , navigate to the option “Sound & Video” and double-click on “vokoscreenNG”



You will see the following window.



Make sure the option “Window” is selected. Avoid the option “Fullscreen” since it can freeze the screen and you will need to reboot the Raspberry Pi. The rest of the selections must be as shown in the picture above.

Now Let’s program the software to record automatically for a certain period. Make a click in the icon  and check the box “stop recording after”. Then select the number of hours you want.



Do not check the box “Start the timer” unless you want to start recording after certain period.

Now click “Start” and the cursor will change to a “Blue Cross”. Select the window you want to record by making click on the top bar of that window as shown below.



After the time you programmed the recording has passed, you will find the video file by clicking the option “Folder”. You can also cancel the recording by clicking on “Stop”.

The process to transfer the video file is the same as for the data files described in the previous section.

## Troubleshooting & Support

This section details known issues and troubleshooting steps for the system.

### RPi Unable to Boot

If you are in a situation where:

* The Pi’s LED lights are on, but you cannot use VNC viewer to connect to the Pi. When you open the waterproof box to inspect the Pi, the red light on the side may be flickering.
* You cannot connect to the Queen and there is no WiFi signal
* You plug in a portable monitor and reboot the Pi, it tries to boot then you get a black screen or no signal on the monitor.

I have found this issue is related to the Pi’s power supply. To fix this:

1. **Check the charge controller**. Ensure the battery is charged.
2. **Connect the affected Pi to another pi’s power cord**. If the Pi and/or WiFi turns back on, the Pi’s power cord was to blame. If the Pi still does not work, there’s probably some other issue with the Pi.
3. Since we know the power cord is faulty, check:
   1. **The entire length of the cord** for cuts or nicks. If any are found, cut them out, and re-connect the wire by (1) stripping the wire with wire strippers, (2) connecting the positive and negative strands with wire nuts, and (3) wrapping the entire new connection with duct tape.



* 1. **The Pi’s power switch in the controller box**. Make sure the metal tabs on the switch are not touching each other causing a short circuit. If they are, there should be clear plastic insulation that you can slide up the red, black, or yellow wires to cover the metal tabs and prevent a short. Also, make sure the blue light on the switch turns on when the switch is in the “on” position.
  2. If you have checked the power cord and switch and found no problems, the culprit is likely the DC voltage converter. Proceed to step 4.

1. **Replacing the voltage converter**. You’ll need a new converter, wire nuts (I use small blue ones), and a wire cutter/stripper.
   1. Cut the power cord at the end of the single black wire (that contains both the black and red wires)



Wire coming from the switch

**Cut out the affected converter here**

* 1. With wire strippers, strip the red and black wires coming out of the new converter, and re-strip the end of the wire coming from the switch.
  2. **The new voltage converter will go inside the waterproof box with the Pi** because now I don’t know how waterproof the converters are. Thread the wire coming from the switch through the cable gland, going into the Pi box.
  3. Now twist together the red wire from the switch to the converter’s red wire, and twist on a wire nut to secure the connection. Repeat with the two black wires.

Plug in the USB-C power cord into the Pi. The tunnel LEDs should be illuminated. Wait a minute or two for the Pi to finish booting. If it’s the queen, the WiFi should be restored, and you should be able to connect to the Pi.

### Troubleshooting the Clock

If your queen is not booting correctly, this may also be due to the clock trying to write garbage data to the system time. Try the following to restore the clock:

1. Check that the wiring from the pi to the clock is correct.

![A diagram of a circuit board

Description automatically generated](data:image/png;base64...)

1. If the wiring is correct, but you still cannot boot properly or read the clock, disconnect the clock from the Queen, remove the battery from the clock, and reboot the Queen without the clock.
   1. The Queen will boot correctly, but the time will be incorrect, and trying to read the clock with the terminal command sudo hwclock -r will return an error that says

hwclock: Cannot access the Hardware Clock via any known method.

1. When the Queen has booted successfully, connect it to wifi. This will automatically update the system time with the correct time.
2. Make sure the Queen will connect to wifi automatically on reboot. This can be done by hovering over the wifi symbol in the top right, selecting “Advanced Options > Edit Connections…” Then, double click on your wifi connection, locate the “General” tab, and make sure the box for “connect automatically with priority” is selected.
3. Connect the clock, without the battery, back to the Queen. Then, perform a soft reboot with the terminal command sudo reboot
4. The Queen should boot correctly, connect to wifi, and now be able to read the clock. Check that the time is correctly read from the clock with sudo hwclock -r in the terminal.
   1. If you get an error that says hwclock: ioctl 1 (RTC\_RD\_TIME) to /dev/rtc to read the time failed: invalid argument, then write the system time to the clock with the command sudo hwclock -w
5. Put the battery back in the clock and try reading the clock again.
   1. If the clock is successfully read, it should be fixed! The following steps are to test that this is true
6. Perform a soft reboot. If the Queen reboots correctly and the clock can be read, navigate back to your wifi connection settings and deselect the “connect automatically with priority” box.
7. Soft reboot again. This time, the Queen will not connect to wifi, but instead will get the correct time from the clock.
   1. It may take a few moments to update the time on the desktop. Reading the clock from the terminal may be faster.
8. Perform a hard reboot (shutdown, disconnect power, wait a few seconds, power back on).
   1. If the Queen boots up again with the correct time and the clock can be read via the terminal, you’re all set!

### VNC Failing to Connect

If you get “timed out waiting for a response” error from VNC when trying to connect, try the following:

* If you just turned on the Pi, try to reconnect in a minute or two. It can take a minute for the workers to connect to the queen’s hotspot.
* If you didn’t just turn on the Pi, reboot it (turn its switch off and on again). That will force it to connect to wifi again. (I’ve noticed that sometimes they fail to connect to wifi on the first attempt)

If the error persists the Pi may be too far away from the Queen to establish a reliable WiFi connection. Detach the Pis from the hives and move them closer together so the queen and worker can establish a connection.

### Change Desktop Resolution

In case the screen resolution is too small to display the camera preview. You need to change the Raspberry Pi resolution following these steps.

Open a new terminal window  by clicking on the terminal icon on the top-left corner.

Then type the command **sudo nano /boot/config.txt**



Press enter and scroll down (use the arrow keys) until you find the sections for HDMI.

Make sure that **hdmi\_group = 2** and **hdmi\_mode = 28**



Once you modify it, press Control + X, then press “Y” and finally press “Enter”.

To save the modifications you need to restart the computer. Click on the Raspberry icon , select “LogOut” and then select “Reboot”

 

Now the Raspberry Pi resolution must fit the entire camera preview

## Bee Tagging Protocol

We tag bees when they have newly emerged from their cells as young workers. Newly-emerged workers are far more docile than mature workers and nearly unable to sting. Mature workers must be sedated with ice or CO2 in order to be tagged. This puts a lot of stress on their bodies, and they don’t always recover. Thus, tagging newly emerged bees is safer, faster, and requires fewer materials.

**Materials**:

1. Shellac-based glue
2. Tooth Picks
3. Tweezers
4. **Procedure**:
5. **1.** Remove brood frames from hive

| A group of people working on a beehive  Description automatically generated |
| --- |
| Figure 1. Tagging station with brood frames removed from the hive and set up for tagging newly-emerged bees |

**2.** Find and remove a newly-emerged bee. They can be identified by their lighter color and fuzzier thorax and head.

| A person holding a bee  Description automatically generated | A person wearing blue gloves holding a bee  Description automatically generated |
| --- | --- |
| (a) | (b) |
| A person holding a bug  Description automatically generated | A person holding a bee  Description automatically generated |
| (c) | (d) |
| Figure 2. Examples of newly-emerged honey bees. They are most distinct by the fuzz around their eyes like in (a), (b), and (c). | |

**3.** Use a toothpick to carefully place a small bead of glue on the thorax of the bee. Only a small amount is needed to secure the tag. Be careful to avoid gluing the wings or head.

| A person holding a stick with a bug  Description automatically generated |
| --- |
| Figure 3. Toothpick dipped in glue applied to bee’s thorax. |

**4.** Grab a tag with tweezers and place it on the bee’s thorax. Ensure the tag is correctly oriented before gently pressing it down to adhere it securely.

The “top” of the tag will correspond with the “forward” direction for the bee, so the tag must be placed with the “top” side facing the bee’s head. The tags can be printed with yellow instead of white on this side to make visual alignment much easier.

| A person holding a pair of tweezers  Description automatically generated | A person wearing blue gloves holding tweezers to a finger  Description automatically generated |
| --- | --- |
| (a) | (b) |
| A person holding a bug  Description automatically generated | |
| (c) | |
| Figure 4. Tag carefully (a) placed with tweezers and (b) pressed down to securely adhere too the thorax. The yellow line (c) allows for visual alignment with the bee’s head. | |

**5.** Once the tag is secure place the bee back on the frame.

| A group of bees on a wooden frame  Description automatically generated |
| --- |
| Figure 5. Wooden frame with several tagged bees placed back inside |

**6.** Repeat for a total of 100 bees, then return frames to the colony.

Note: Sometimes a colony will not have a large enough population of newly-emerged bees to tag. In this case, we tag bees from a different colony (one not involved in the tagging experiment), and, with lots of smoke, add them one-by-one to the experimental hive. This is established practice as newly emerged bees are readily accepted into other colonies.