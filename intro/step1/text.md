
Gatekeeper uses the OPA Constraint Framework to describe and enforce policy.

https://github.com/open-policy-agent/gatekeeper

## Install OPA Gatekeeper
```plain
k -f /root/gatekeeper.yaml apply
```{{exec}}

<br>

## Create OPA Template
```plain
k -f /root/opa_template.yaml apply
```{{exec}}

```
k get constrainttemplates
```{{exec}}

<br>

## Create OPA Constraint
```plain
k -f /root/opa_constraint.yaml apply
```{{exec}}

```
k get k8srequiredlabels
```{{exec}}

<br>

## Test
Creating a new *Namespace* will fail because labels are required:
```plain
k create ns test
```{{exec}}
