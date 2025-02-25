---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "gcore_network Data Source - terraform-provider-gcorelabs"
subcategory: ""
description: |-
  Represent network. A network is a software-defined network in a cloud computing infrastructure
---

# gcore_network (Data Source)

Represent network. A network is a software-defined network in a cloud computing infrastructure

## Example Usage

```terraform
provider gcore {
  permanent_api_token = "251$d3361.............1b35f26d8"
}

data "gcore_project" "pr" {
  name = "test"
}

data "gcore_region" "rg" {
  name = "ED-10 Preprod"
}

data "gcore_network" "tnw" {
  name       = "example"
  region_id  = data.gcore_region.rg.id
  project_id = data.gcore_project.pr.id
}

output "view" {
  value = data.gcore_network.tnw
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String)

### Optional

- `project_id` (Number)
- `project_name` (String)
- `region_id` (Number)
- `region_name` (String)

### Read-Only

- `external` (Boolean)
- `id` (String) The ID of this resource.
- `mtu` (Number)
- `shared` (Boolean)
- `type` (String) 'vlan' or 'vxlan' network type is allowed. Default value is 'vxlan'


