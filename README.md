# fedex

_Due to [ADR0004](https://github.com/home-assistant/architecture/blob/master/adr/0004-webscraping.md) this integration was removed from [Home Assistant](https://github.com/home-assistant/home-assistant/tree/0.99.0) with version 0.100, and are now republished here._

⚠️ This integration scrapes a website to get the information!
⚠️ There are no one actively maintaining this repository.

The `fedex` platform allows one to track deliveries by [FedEx](http://www.fedex.com/). To use this sensor, you need a [FedEx Delivery Manager](https://www.fedex.com/us/delivery/) account.

## Installation

1. Using the tool of choice open the directory (folder) for your HA configuration (where you find `configuration.yaml`).
2. If you do not have a `custom_components` directory (folder) there, you need to create it.
3. In the `custom_components` directory (folder) create a new folder called `fedex`.
4. Download _all_ the files from the `custom_components/fedex/` directory (folder) in this repository.
5. Place the files you downloaded in the new directory (folder) you created.
6. Restart Home Assistant.
7. Move on to the configuration.

Using your HA configuration directory (folder) as a starting point you should now also have this:

```text
custom_components/fedex/__init__.py
custom_components/fedex/manifest.json
custom_components/fedex/sensor.py
```

## Example configuration.yaml

```yaml
sensor:
  - platform: fedex
    username: YOUR_USERNAME
    password: YOUR_PASSWORD
```

### Configuration options

Key | Type | Required | Description
-- | -- | -- | --
`username` | `string` | `True` | The username to access the FedEx Delivery Manager service.
`password` | `string` | `True` | The password for the given username.
`name` | `string` | `False` | Name the sensor.
`scan_interval` | `list` | `False` | Minimum time interval between updates. Default is 1 hour.

## Contributions are welcome!

If you want to contribute to this please read the [Contribution guidelines](CONTRIBUTING.md)
