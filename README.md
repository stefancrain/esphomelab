# Stefan's ESPHomeLab

Currently a WIP, Reuseable config across my ESPHome devices

## Deploying

```shell
cd [projectdir]
esphome --substitution release_id "$(md5sum main.yaml | awk '{print $1}' | cut -b-8 )" run main.yaml --device /dev/xxxx
```
