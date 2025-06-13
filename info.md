# Custom Gree climate integration. Controls AC's supporting the Gree protocol.

## UI Configuration
You can add the integration from the Home Assistant UI.
Navigate to **Settings** > **Devices & Services** and search for **Gree Climate**.

## Component configuration
To configure this component manually, add the following configuration to your configuration.yaml (replacing the placeholders).

```
 climate:
   - platform: gree
     name: First AC
     host: <ip of your first AC>
     port: 7000
     mac: '<mac address of your first AC>'
     target_temp_step: 1
     encryption_key: <OPTIONAL: custom encryption key if wifi already configured>
     uid: <some kind of device identifier. NOTE: for some devices this is optional>
     temp_sensor: <entity id of the temperature sensor. For example: sensor.bedroom_temperature>
     lights: <OPTIONAL: input_boolean to switch AC lights mode on/off. For example: input_boolean.first_ac_lights>
     xfan: <OPTIONAL: input_boolean to switch AC xfan mode on/off. For example: input_boolean.first_ac_xfan>
     health: <OPTIONAL: input_boolean used to switch the Health option on/off of your first AC. For example: input_boolean.first_ac_health>
     sleep: <OPTIONAL: input_boolean to switch AC sleep mode on/off. For example: input_boolean.first_ac_sleep>
     powersave: <OPTIONAL: input_boolean to switch AC powersave mode on/off. For example: input_boolean.first_ac_powersave>
   
   - platform: gree
     name: Second AC
     host: <ip of your second AC>
     port: 7000
     mac: '<mac address of your second AC>'
     target_temp_step: 1
```
