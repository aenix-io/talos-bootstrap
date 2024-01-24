# talos-bootstrap

An interactive script for bootstrapping Kubernetes clusters on Talos OS.

*Example: bootstrap full-feature Kubernetes cluster in 5 minutes*:
[![screencast](https://raw.githubusercontent.com/aenix-io/talos-bootstrap/2cc7b82065747e373cd914c87c8cd5c6582c5c6c/images/627123.gif)](https://asciinema.org/a/gwK85Tdr577GsxjXWo7otPFjv)

# Installation

Install dependencies:
- `talosctl` (>=1.6.0)
- `dialog`
- `nmap`

Install talos-bootstrap:

```
curl -LO https://github.com/aenix-io/talos-bootstrap/raw/master/talos-bootstrap
chmod +x ./talos-bootstrap
sudo mv ./talos-bootstrap /usr/local/bin/talos-bootstrap
```

# Usage

- Boot your nodes with Talos in maintenance mode.  
  (booting from [ISO](https://www.talos.dev/v1.5/talos-guides/install/bare-metal-platforms/iso/) or PXE using [matchbox](https://www.talos.dev/latest/talos-guides/install/bare-metal-platforms/matchbox/) is the best option)
- Create a directory for holding your cluster configuration.
- Run `talos-bootstrap` command for every node in your cluster.


# Options

- `-u` option can be used to upgrade or reconfigure nodes on existing cluster

# Customizations

You can specify your customizations in one of the following files:

- `patch.yaml` - common settings used for all nodes.
- `patch-controlplane.yaml` - settings used for controlplane nodes only
- `patch-worker.yaml` - settings used for worker nodes only

Read the [Configuration Patches](https://www.talos.dev/latest/talos-guides/configuration/patching/) documentation for more details.

# Copyright

Andrei Kvapil <kvapss@gmail.com>  
Licensed under Apache 2.0 License
