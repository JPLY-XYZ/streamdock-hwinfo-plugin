# HWiNFO Reader

Alternative to the [hwinfo-streamdeck](https://github.com/shayne/hwinfo-streamdeck) plugin, without requiring the time-limited 'Shared Memory Support' feature.
This plugin takes full advantage of the new 'HWiNFO Gadgets' API and is built using the [Elgato Beta SDK](https://github.com/elgatosf/streamdeck).

It includes a performance-focused rendering system that regenerates SVG graphics only when the sensor value changes, drastically reducing CPU load, data emissions, and communication with the device.

These improvements were made specifically to address a hardware limitation: the device runs over USB 2.0, which can become saturated when more than 5 buttons are active. By reducing unnecessary updates, the plugin ensures smooth, responsive operation even in sensor-heavy setups.




![image](https://github.com/user-attachments/assets/f55791ba-4d38-4e3e-abd3-31e33ea008fa)

## Download

You can download and install the plugin from the [Releases](https://github.com/JPLY-XYZ/streamdock-hwinfo-plugin/releases/) page.
Download the .RAR file, extract its contents, and place the plugin folder into your Stream Dock plugins directory.

![image](https://github.com/user-attachments/assets/6fac7b2f-948f-4442-9268-e2221e68139f)


## Instructions for HWiNFO

![HWiNFO settings](https://i.imgur.com/R3sWtKd.png)

- Open HWiNFO in Sensor Only mode then go into the settings
- Use these recommended settings

![Recommended settings](https://i.imgur.com/26AaLVl.png)

- Start HWiNFO
- On the sensors screen open the settings and choose the HWiNFO Gadget tab
- Enable "enable reporting to Gadget"
- Choose what sensors you would like to monitor by pressing "Report value in Gadget"

(Hint: Two sensors with the same name? [Make sure to rename one of them to avoid conflicts](https://github.com/5e/streamdeck-hwinfo-plugin#known-issue))

![HWiNFO Gadget](https://i.imgur.com/2zBMrJX.png)

- Then the sensors you have enabled will show up in the stream deck plugin

![Quick guide on how to change values from e.g. MB to GB](https://github.com/5e/streamdeck-hwinfo-plugin/issues/25#issuecomment-2184139637)

- It is recommended to set the polling period to 1255 ms to optimize performance and reduce unnecessary updates.

![the polling period to 1255 ms](ttps://github.com/user-attachments/assets/89968638-a981-4353-a74f-2a3798038ac8)



## Known issue

- Enabling HWiNFO gadget on two sensors with the exact same name may cause issues of the Stream Deck plugin showing the wrong value. A fix for this is to rename the sensor name in HWiNFO (right click on sensor and press rename) and then re-select the correct sensor in the settings of the plugin.

