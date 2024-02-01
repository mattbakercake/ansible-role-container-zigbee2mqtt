# Ansible role to install Zigbee2Mqtt container

Install latest stable zigbee2mqtt container onto host

# Notes

The container will fail to start properly until a zigbee coordinator is plugged in and
the correct location is added to the config (`zigbee_serial_device_port`).  see docs to for a
guide on how to ascertain this https://www.zigbee2mqtt.io/guide/getting-started/#installation

# Variables

see `defaults\main.yaml`

* `timezone` - instance timezone
* `docker_dir` - docker dir
* `docker_compose_dir` - docker compose dir
* `mqtt_host` - mqtt host name/ip
* `mqtt_port` - mqtt service port 1883 / 8883 (TLS)
* `cert_dir` - ssl certificates dir (required if using TLS port 8883)
* `ca_cert` - name of CA certificate (required if using TLS port 8883)
* `mqtt_user` - mqtt user (required if using port 1883)
* `mqtt_password` - mqtt password (required if using port 1883)
* `zigbee_serial_device_port` - the device port that serial zigbee coordinator is plagged into e.g. /dev/ttyACM0