# OC-Workspace

<p align="center">
  <img src=".github/logo.png" alt="OC-Workspace logo" width="128" />
</p>

Scripts for installing and using an OpenStack cloud on Ubuntu.

## Contents

- `openstack-installer/ubuntu.sh` installs and configures OpenStack
  services on a controller node: Keystone, Glance, Nova, Neutron with
  Open vSwitch, Cinder, Swift, Heat, Ceilometer and Trove, plus MySQL,
  RabbitMQ and MongoDB. It creates the service accounts and networks
  and logs to `/root/openstack.log`.
- `openstack-installer/ocf` holds the configuration file templates the
  installer writes, and a Heat template for a single WordPress instance.
- `openstack-scripts/jobs` holds cloud-init user data and scripts for
  launching instances. `openstack-scripts/snippets` holds smaller
  helpers.

## Tech

- Bash and Perl
- OpenStack on Ubuntu

## Usage

Edit the network and host settings at the top of
`openstack-installer/ubuntu.sh`, then run it as root on the controller.

## License

Licensed under the Apache License 2.0. See [LICENSE](LICENSE).
