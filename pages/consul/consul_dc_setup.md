---
title: Consul Dc setup for server
keywords: consul
#summary: "DHEERAJ POTLURI"
sidebar: consul_sidebar
permalink: consul_dc_setup.html
folder: consul
---
{% include note.html content="Run this to setup DC1 in consul-server" %}

```shell
sudo tee /etc/consul.d/consul-server.json <<EOF
{
  "datacenter": "dc4",
  "server": true,
  "bootstrap_expect": 1
}
EOF
```
{% include tip.html content="We highly discourage single-server production deployments." %}
> Ideal setup whould be 5 server setup so it will be helpfull during failover.   
> Bootstrap_expect should be changed based on number of servers.  

## Where to Next?

To setup vagrant for Consul, joining nodes into a cluster, and
interacting with the agent, check out: [Setting up Dc for consul](consul_dc_setup.html).