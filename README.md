# Stefan's ESPHomeLab

Currently a WIP, Reusable config across my ESPHome devices

## Devices Under Test

- [Indoor Climate](./climate-indoor/)
- [Outdoor Climate](./climate-outdoor/)
- [4 Channel Relay](./relay-4x-channel/)
- [8 Channel Relay](./relay-8x-channel/)

## Using this repo

### Installing ESPHome Manually

I prefer using the [Command Line](https://esphome.io/guides/getting_started_command_line.html)
to build this firmware.

The ESPHome instructions leave out versioning detail required for compatibility.
The included requirements.txt should solve that.

```shell
pip3 install -r requirements.txt
```

### Deploying

```shell
cd [projectdir]

esphome \
  --substitution mac "$(esptool.py chip_id | grep -m1 "MAC:" | cut -d: -f6- | tr -d ':')" \
  --substitution release_id "$(git rev-parse --short=12 HEAD)" \
  run main.yaml \
  --device /dev/cu.xxx
```
