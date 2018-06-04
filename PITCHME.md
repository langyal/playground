
---
## Campus 2018Q2, Zagreb
laszlo.angyal@pan-net.eu

---
- Beryllium development
- Openstack Summit 2018 May, Vancouver
- AT&T v. Pan-Net

---
## Beryllium: Design, Build, Operate

<span style="font-size:0.6em">
https://gitlab.tools.in.pan-net.eu/groups/cid/-/milestones/28
</span>

this milestone is used as a summary of activities; examples:
```
- versions to be used
- Li-Be differences highlights
- generic code: deployment
- environment manifest: environments.yaml
- environment specific code: environments
- feature requests
- online documentation
```

---
## beryllium project

<span style="font-size:0.6em">
https://gitlab.tools.in.pan-net.eu/cid/beryllium
</span>

we use three project milstones:
```
- beryllium/design (Day 0)
- beryllium/build (Day 1)
- beryllium/operate (Day 2)
```

---
#### Be design highlights: versions

Lithium -> Beryllium
```
- Ubuntu version: trusty/14.04 -> xenial/16.04
- Kernel version: 4.x
- Contrail version: 3.2.x -> 4.1.x
- Openstack version: Mitaka -> Ocata
- CEPH version: Jewel/10.2.x 
- infra units: trusty/14.04 -> xenial/16.04
- maas: 2.x
- juju: 2.x
- openstack-charms: 16.04 ->latest
```

---
#### Be design highlights: rack->server

Lithium: rack-role-driven design
```
- rack-role-driven design
- storage rack
- compute rack
- management rack
```

Beryllium: server-role-driven design
```
- unified rack
- server role defines config
- no special mgmt rack design
```

---
#### Be design highlights: management cluster design

Lithium:
```
- separated mgmt rack(s)
- L2 networks
```

Beryllium:
```
- we still have to use L2
- experimental: DNS based
- goal: switch to L3 technology
- currently, scaling at the mgmt plane is not an issue
```

---
#### Be design highlights: Infrastructure as Code

stages:
```
[greenfield]: even the network is unconfigured
[ready-for-foundation]: 3 infra nodes + network is configured
[ready-for-cloud]: foundation is deployed
[ready-for-postdeployment]: cloud is deployed
[ready]: post-deployment applied also
```

Lithium:
```
- gitlab pipeline can be run from stage [ready-for-cloud]
```

Beryllium:
```
- gitlab pipeline can be run from stage [ready-for-foundation]
- gitlab integrated development
- documentation as code (gitlab pages)
- code review: next challenge
```

---
#### Be design highlights: logical networks
![ic-network-design.001.png](ic-network-design.001.png)

---
#### Be design highlights: multi-site

Lithium: not considered

Beryllium: considered
```
- ip anycast
- object storage replication
- global health check
```

---
## Openstack Summit 2018 May, Vancouver

- building the cloud
- using the cloud
- general topics

---
#### Openstack Summit: building the cloud #1

- openstack-helm
  - build openstack via helm charts: https://github.com/openstack/openstack-helm-infra

- kolla
  - kolla-ansible (docker): https://docs.openstack.org/kolla-ansible/latest/
  - kolla-kubernetes: https://docs.openstack.org/kolla-kubernetes/latest/

---
#### Openstack Summit: building the cloud #2

Airship: http://www.airshipit.org
- AT&T: Rodolfo Pacheco, Alan Meadows
- basically, openstack-helm _extra_
- https://www.youtube.com/watch?reload=9&v=ckcLnBqGQrQ


---
## AT&T v. Pan-Net


