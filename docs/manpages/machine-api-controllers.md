NAME
====

machine-api-controllers (Deployment)

DESCRIPTION
====

The machine-api-controllers deployment consists of several containers which
manage and maintain the custom resources and platform interactions associated
with the Machine API.

The following comprise the Machine API controllers:

- MachineSet Controller

Ensures presence of expected number of replicas and a given provider config
for a set of machines.

- Machine Controller

  - cluster-api-provider-aws [0]

  - cluster-api-provider-gcp [1]

  - cluster-api-provider-azure [2]

  - cluster-api-provider-libvirt [3]

  - cluster-api-provider-openstack [4]

  - cluster-api-provider-baremetal [5]

  - cluster-api-provider-ovirt [6]

Ensures that a provider instance is created for a Machine object in a given
provider.

- Node link Controller

Ensures machines have a nodeRef based on IPs or providerID matching.
Annotates nodes with a label containing the machine name.

- Machine healthcheck controller

Ensures machines targeted by MachineHealthCheck objects satisfy a healthiness
criteria or are remediated otherwise.

SEE ALSO
====

* machine-api-operator
* openshift-machine-api

[0]: https://github.com/openshift/cluster-api-provider-aws
[1]: https://github.com/openshift/cluster-api-provider-gcp
[2]: https://github.com/openshift/cluster-api-provider-azure
[3]: https://github.com/openshift/cluster-api-provider-libvirt
[4]: https://github.com/openshift/cluster-api-provider-openstack
[5]: https://github.com/openshift/cluster-api-provider-baremetal
[6]: https://github.com/openshift/cluster-api-provider-ovirt

BUGS
====

https://github.com/openshift/machine-api-operator
