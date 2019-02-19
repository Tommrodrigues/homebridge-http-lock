# homebridge-http-lock-mechanism

#### Homebridge plugin to control a web-based lock

## Installation

1. Install [homebridge](https://github.com/nfarina/homebridge#installation-details)
2. Install this plugin: `sudo npm install -g homebridge-http-lock`
3. Update your `config.json` file (See below).

## Configuration example

```json
"accessories": [
     {
       "accessory": "HTTPLock",
       "name": "Lock",
       "openURL": "http://myurl.com/open",
       "closeURL": "http://myurl.com/close"
     }
]
```

### Structure

| Key | Description |
| --- | --- |
| `accessory` | Must be `GarageDoorOpener` |
| `name` | Name to appear in the Home app |
| `openURL` | URL to trigger the opening of your garage |
| `closeURL` | URL to trigger the closing of your garage |
| `autoLock` _(optional)_ | Whether your lock should re-lock after being opened (default `false`) |
| `autoLockDelay` _(optional)_ | Time (in seconds) until your lock will auto lock if enabled (default is `10`) |
| `timeout` _(optional)_ | Time (in milliseconds) until the accessory will be marked as "Not Responding" if it is unreachable (`5000` is default) |
| `http_method` _(optional)_ | The HTTP method used to communicate with the thermostat (`GET` is default) |
| `username` _(optional)_ | Username if HTTP authentication is enabled |
| `password` _(optional)_ | Password if HTTP authentication is enabled |
| `model` _(optional)_ | Appears under "Model" for your accessory in the Home app |
| `serial` _(optional)_ | Appears under "Serial" for your accessory in the Home app |
| `manufacturer` _(optional)_ | Appears under "Manufacturer" for your accessory in the Home app |

## Removal

```
sudo npm uninstall -g homebridge-http-lock-mechanism
```
