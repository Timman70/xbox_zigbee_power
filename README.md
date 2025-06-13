# Xbox Power - Home Assistant Integration

This integration allows you to control Xbox consoles using a Tuya Smart Zigbee IR Remote through Home Assistant. It's ideal if you're running a second or third Xbox in your home setup.

## Installation

1. Extract the `custom_components/xbox_power` directory into your Home Assistant `config/custom_components/` folder.
2. Restart Home Assistant.
3. Go to **Settings → Devices & Services → Add Integration** and search for **Xbox Power**.
4. When prompted, enter the IEEE address of your Tuya Smart Zigbee IR Remote.

## How to Get the IEEE Address

1. Go to **Settings → Devices & Services** in Home Assistant.
2. Click **Devices** and locate your **Tuya Smart Zigbee IR Remote**.
3. Click on the device, then look for the **IEEE address** under device info.
4. Copy that address (formatted like `f8:44:77:ff:fe:93:50:31`) and paste it into the setup form when adding the integration.

## How It Works

This integration:
- Sends Zigbee commands using `zha.issue_zigbee_cluster_command`
- Triggers the IR signal for Xbox power toggle
- Updates the state using a `binary_sensor.xbox_ping` entity

No manual configuration in `configuration.yaml` is required.


---

Created by **TimCloud** (@Timman70)
