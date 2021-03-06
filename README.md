# Overview

This interface supports the integration between Neutron and Neutron API
consumers.

# Usage

No explicit handler is required to consume this interface in charms
that consume this interface.

In addittion to the states automatically set based on relation data by
``charms.reactive.Endpoint``, the interface provides the
``neutron-api.available`` state.

# metadata

To consume this interface in your charm or layer, add the following to `layer.yaml`:

```yaml
includes: ['interface:neutron-api']
```

and add a requires interface of type `neutron-api` to your charm or layers
`metadata.yaml`:

```yaml
requires:
  neutron-api:
    interface: neutron-api
```

# Bugs

Please report bugs on [Launchpad](https://bugs.launchpad.net/openstack-charms/+filebug).

For development questions please refer to the OpenStack [Charm Guide](https://github.com/openstack/charm-guide).
