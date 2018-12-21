Nudnik examples
===============

Goals
-----

Quoted from [nudnik's repo](https://github.com/salosh/nudnik):
>Allow easy testing of load-balancing and failures in gRPC and REST based service-mesh

Features
--------

* Rate limiting
* Fake IO load from either client or server side
* Export timing metrics to a file or InfluxDB with any custom formatting
* Introduce Chaos factor - which randomly braeks things (very useful when your planning to fail ...)

Exmaples structure
------------------

Exmaples are devided based on solution:
* `baremetal` - introduce baremetal (non-containerized) solutions (comes in handy when you want to `stress-test`, `load` etc on the HW level)
* `docker` - introcude use-cases running `nudnik-client` and `nudnik-server` { same binary different configuration }, 
* `docker/compose` - a full solution running `nudnik-client` and `nudnik-server` reporting to `influxdb` and graphong via `grafana` -> more on that in `docker/compose/README.md`
* `docker/kubernetes-manifests` -> Kubernetes standard deployment manifests
* `docker/kubernetes-helm/nudnik-charts` -> our helm charts (github-based) repository