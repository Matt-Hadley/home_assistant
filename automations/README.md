## Zigbee2MQTT OTA Updater

This automation handles Over-The-Air (OTA) updates for Zigbee devices that:

- Support OTA updates.
- Match a configured list of allowed device models.

It performs the following steps:

1. Requests the device list from Zigbee2MQTT.
2. Filters devices eligible for OTA updates.
3. Checks for available updates per device.
4. Initiates OTA updates and waits for completion.
5. Logs all key events and errors to Home Assistant’s logbook.

### Configuration

Adjust the following in the automation YAML inside `automations/`:

- `allowed_model_ids`: List of Zigbee device model IDs to update.
- MQTT topics (defaulted for Zigbee2MQTT bridge topics).

### Usage

- Trigger manually or via schedules as needed.
- Monitor progress and errors in Home Assistant’s logbook.