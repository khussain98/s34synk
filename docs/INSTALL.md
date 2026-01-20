**How It Works**

S34Synk retrieves solar system data from the SunSynk API, where it's uploaded via your Sunsynk Data Logger Dongle. This does not directly communicate with your Invetor over LAN.

*Please note that this add-on only provides sensor data, it does not include pre-built home assistant cards to display the information.

**Getting Started**

This add-on publishes sensor values to Home Assistant entities that are retrieved from the SunSynk API.

Add this respository to your Home Assistant add-on store

From the "Settings" menu item in Home Asstant's UI go to "Add-ons". 

In the bottom right-hand corner click "ADD-ON STORE". 

The in the right-hand top corner click the three dots and select "Repositories". 

Paste the following repository link and click add then close 

https://github.com/khussain98/s34synk

Refresh the browser. Right at the bottom you should now see the "S34Synk" add-on. Click it to open the into page, then click the "Install" button.

Provide your SunSynk.net credentials

After installing this add-on make sure you enter all the required information on the configuration page.

In case you are unsure what your Sunsynk inverter's serial number is. Log into the synsynk.net portal and copy the serial number from the "Inverter" menu item. For multiple inverters seperate the inverter serial numbers with a semi colon ; Example 123456;7890123
