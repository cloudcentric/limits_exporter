# Openstack Limits Exporter
Prometheus exporter for openstack limits of specified projects

## Installation
```
pip install limits-exporter
```
In the examples folder exists a sample systemd unit file template.

## Usage
The exporter needs a `clouds.yaml` file, which is located at:
- `/etc/openstack/clouds.yaml`
- `~/.config/openstack/clouds.yaml`
- `./clouds.yaml`
- or at a custom location set with `export OS_CLIENT_CONFIG_FILE=/path/to/clouds.yaml`

For running the exporter you need to specify the `--clouds cloud1,cloud2,...` argument,
which is a comma seperated list of the cloud names in your `clouds.yaml`

Other optional arguments are:
- `--interval` the scrape interval in seconds
- `--port` the port on which the server runs

## More Information
- https://docs.openstack.org/python-openstackclient/latest/configuration/index.html


