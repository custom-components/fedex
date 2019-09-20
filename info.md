# fedex

_Due to [ADR0004](https://github.com/home-assistant/architecture/blob/master/adr/0004-webscraping.md) this integration was removed from [Home Assistant](https://github.com/home-assistant/home-assistant/tree/0.99.0) with version 0.100, and are now republished here._

⚠️ This integration scrapes a website to get the information!
⚠️ There are no one actively maintaining this repository.

The `fedex` platform allows one to track deliveries by [FedEx](http://www.fedex.com/). To use this sensor, you need a [FedEx Delivery Manager](https://www.fedex.com/us/delivery/) account.

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
`scan_inverval` | `list` | `False` | Minimum time interval between updates. Default is 1 hour.