# Drips and Drops

I made this light installation for Becton Cafe's light display. I wanted to emulate an external space that the viewer is enclosed within, as if they were looking out of a glass enclosure. Seeing how Becton Cafe is primarily used as a relaxed, quiet study space, I wanted to recreate one of my favorite relaxing settings: A rainy day! To further the viewer's sense of safety within the enclosure, I've made the raining liquid flood the entire screen, thus lighting the entire space.

## Install It Yourself!

In order to use this program in your own video displays (though it is important to note that it is optimized for the Becton Cafe light display) you'll need the following:

- A Raspberry Pi (I used the 3B+)
- An HDMI Cable (There is one provided in Becton Cafe)
- A power cable (Either Micro-USB to USB-B or Micro-USB to AC Adapter)

You can either run the program manual once you've downloaded the git repository or you can make it run on boot. Either way you'll need to run this code to make sure you have Processing for pi on your device:
> curl https://processing.org/download/install-arm.sh | sudo sh

Then to make it run on boot, you'll want to make sure that you run

> sudo nano /etc/xdg/lxsession/LXDE-pi/autostart

And add the following lines:

> sleep(50)

> @python PATH_TO_start.py_IN_BECTON_DISPLAY_FOLDER


(the start.py file associated with it is already in the git repository)

Once you do this the program should run automatically once you connect to a source of power.

NOTE: Due to the Raspberry Pi's computing limitations, the program animations actually run much slower than I intended them to when run on the Raspberry Pi. The video linked above shows the program running at its intended speed on my laptop.
