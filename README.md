# Home Assistant Config

Home Assistant configuration and helper packages for my smart home
(Zigbee2MQTT, Shelly, Broadlink IR, TCL Google TV).

## Scripts / Packages

| File | Description |
| --- | --- |
| [`tv_audio_output.yaml`](packages/tv_audio_output.yaml) | Switches a TCL Google TV's audio output between HDMI ARC/eARC and a Bluetooth speaker by writing the `tcl_device_out_type` setting via ADB. Adds a dashboard switch, a live output sensor, a Bluetooth-connected sensor, and automations that follow the speaker automatically (connect → Bluetooth, disconnect → HDMI). Requires the Android Debug Bridge integration. |

## Install

Drop a package file into `<config>/packages/` and enable packages in
`configuration.yaml`:

```yaml
homeassistant:
  packages: !include_dir_named packages
```

Then check the configuration and restart Home Assistant. Per-file requirements
and customization notes are documented in each file's header.
