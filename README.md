# talos-bootstrap

An interactive script for bootstrapping Kubernetes clusters on Talos OS.

![](https://gist.github.com/kvaps/b850a74b678e551b641d585b41e3a428/raw/a0b0af9dde2b562c7f7c9c10054ac1dff6949ca5/627123.gif)

# Installation

Install dependencies:
- `talosctl`
- `dialog`
- `nmap`

Install talos-bootstrap:

```
curl -LO https://github.com/aenix-io/talos-bootstrap/raw/master/talos-bootstrap
chmod +x ./talos-bootstrap
sudo mv ./talos-bootstrap /usr/local/bin/talos-bootstrap
```

# Usage

- Boot your nodes with Talos in maintenance mode
- Create a directory for holding your cluster configuration
- Run `talos-bootstrap` script for every node

# Copyright

Andrei Kvapil <kvapss@gmail.com>  
Licensed under Apache 2.0 License
