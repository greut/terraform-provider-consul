---
layout: "consul"
page_title: "Consul: consul_acl_auth_method"
sidebar_current: "docs-consul-data-source-acl-auth-method"
description: |-
  Provides information about a Consul ACL Auth Method.
---

# consul_acl_auth_method

The `consul_acl_auth_method` data source returns the information related to a
[Consul Auth Method](https://www.consul.io/docs/acl/acl-auth-methods.html).

## Example Usage

```hcl
data "consul_acl_auth_method" "test" {
  name = "minikube"
}

output "consul_acl_auth_method" {
  value = data.consul_acl_auth_method.test.config
}
```


## Argument Reference

The following arguments are supported:

* `name` - (Required) The name of the ACL Auth Method.

## Attributes Reference

The following attributes are exported:

* `description` - The description of the ACL Auth Method.
* `type` - The type of the ACL Auth Method.
* `config` - The configuration options of the ACL Auth Method.
