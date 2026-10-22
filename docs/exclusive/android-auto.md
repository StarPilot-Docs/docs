---
title: Android Auto — Setup & Troubleshooting
description: Show the StarPilot driving view on your car's screen with Android Auto, and fix common connection problems.
---

# Android Auto

Android Auto shows the StarPilot driving view on your car's screen. Set it up while parked in [Galaxy](../usage/galaxy.md), StarPilot's web interface, using your phone or computer. Controls in this guide are on Galaxy's **Android Auto** page unless the car's screen or settings are named.

It is designed for cars with built-in **wireless Android Auto**. A wireless adapter may work in a wired-only car; a direct USB connection is also available but has been tested on fewer cars.

## Set up

1. In Galaxy, open **Android Auto**. Under **Android Auto Support**, turn it on and follow **Install support**. If Bluetooth is off, accept Galaxy’s prompt to turn it on too. You can also turn it on separately from Galaxy’s **Bluetooth** page under **Tools**. Download a current stable Android Auto package by Google LLC, then upload the downloaded file without unzipping it. Step 1 should show **Ready**.
2. On the car's screen, open its phone pairing menu. In Galaxy step 2, **Pair Your Car**, tap **Find car**, choose the car, and confirm the pairing code in Galaxy and on the car's screen. Turn on wireless Android Auto in the car's settings if needed; it may be called *smartphone connection* or *phone projection*.
3. In Galaxy step 3, **Connect & Drive**, tap **Connect**. Keep the car's screen awake. The first picture can take about 30 seconds. Turn on **Automatic Connection** if you want StarPilot to connect when you start driving.

For a direct cable connection, turn on **Wired USB Connection** on the Galaxy Android Auto page and connect the car's data USB port to the comma's USB-C port with a data-capable cable. Bluetooth pairing is not required for this mode.

## Connection problems

If tapping **Connect** in Galaxy step 3 does not start a connection, check that Galaxy step 1 says **Ready**, step 2 shows the selected car, the car is on, Bluetooth is enabled on Galaxy’s **Bluetooth** page under **Tools**, and wireless Android Auto is enabled in the car. Other paired phones may take the screen first.

The status below **Connect** in Galaxy step 3 shows where to look:

| Status | What to check |
| --- | --- |
| **Connecting to car** or **Finding Android Auto** | The car is on and paired in step 2. |
| **Starting wireless setup** or **Waiting for car** | Wireless Android Auto is enabled and a phone is not using it. |
| **Getting car Wi-Fi** or **Joining car Wi-Fi** | Restart the car if this repeatedly fails. |
| **Authenticating** | Update the Android Auto package in step 1 if authentication fails. |
| **Projecting** | The connection is working. |
| **Car showing its own screen** | Select Android Auto on the car's screen. |
| **Retrying** | Wait for the automatic reconnect. |

If the car screen stays black after 30 seconds or freezes, tap **Disconnect** in Galaxy step 3, wait a few seconds, then tap **Connect** there again. If that fails, turn the car off, wait for its screen to go dark, and start it again. Frequent drops may mean a paired phone is taking the screen back. Download **Connection Logs** from Galaxy's Android Auto page when asking for help.

### Other phones and audio

Most cars run Android Auto on one device at a time. Set the comma as the car's preferred device if that option exists. You can also disable wireless Android Auto for that car on other phones, or remove old Bluetooth pairings if the car has reached its device limit. For a wireless adapter, select the comma as its main device in the adapter's app.

The comma does not handle phone calls or music. Some cars can keep your phone connected for **media audio** while the comma uses Android Auto. Selecting your phone for calls may move Android Auto to the phone and disconnect the comma; switch back to the comma afterward.

### Wireless adapters

Pair the comma with **both** the adapter and the car. In Galaxy's Android Auto step 2, select the adapter as the receiver and leave it selected. Then open Galaxy's **Bluetooth** page, pair the comma with the car's Bluetooth entry, and tap **Connect** there. Return to Galaxy's Android Auto page and tap **Connect** in step 3. The car's Bluetooth connection lets StarPilot recognize which car you are driving.

## Settings and upkeep

- **Automatic Connection** tries again each time you start driving. Disconnecting pauses it for the rest of that drive.
- Pair another car in Galaxy step 2 with **Pair another**. Disconnect first, then tap **Use** next to the car you want.
- Pairing, switching cars, and changing settings require Park or offroad mode. Connect, Disconnect, and package updates are available while driving.
- When wireless Android Auto connects, the comma uses its Wi-Fi for the car instead of its usual network. Use the Galaxy hotspot for local access. Remote Galaxy needs another Internet connection on the comma.
- If Galaxy step 1 says the certificate expires soon or has expired, use **Update** or **Reinstall** there. Your paired cars and settings remain saved.
- The extracted Android Auto identity stays on the comma. The uploaded package is deleted after import. Full connection logs stay there until downloaded; StarPilot may send connection errors while parked and disconnected.

## Start over

1. In Galaxy's **Bluetooth** page, forget the car; delete the comma from the car's Bluetooth list.
2. Restart the car, or unplug a wireless adapter for five seconds.
3. Open the car's pairing screen and pair again in Galaxy's Android Auto step 2.
