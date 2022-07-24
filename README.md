# Stefan's ESPHomeLab

Currently a WIP, Reusable config across my ESPHome devices

## Deploying

```shell
cd [projectdir]

esphome \
  --substitution mac "$(esptool.py chip_id | grep -m1 "MAC:" | cut -d: -f6- | tr -d ':')" \
  --substitution release_id "$(git rev-parse --short=12 HEAD)" \
  run main.yaml \
  --device /dev/cu.xxx

```
