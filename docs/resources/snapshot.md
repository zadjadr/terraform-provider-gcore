---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "gcore_snapshot Resource - terraform-provider-gcore"
subcategory: ""
description: |-
  
---

# gcore_snapshot (Resource)



## Example Usage

```terraform
provider gcore {
  permanent_api_token = "251$d3361.............1b35f26d8"
}

resource "gcore_snapshot" "snapshot" {
  project_id  = 1
  region_id   = 1
  name        = "snapshot example"
  volume_id   = "28e9edcb-1593-41fe-971b-da729c6ec301"
  description = "snapshot example description"
  metadata    = {
    env = "test"
  }
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **name** (String)
- **volume_id** (String)

### Optional

- **description** (String)
- **id** (String) The ID of this resource.
- **last_updated** (String)
- **metadata** (Map of String)
- **project_id** (Number)
- **project_name** (String)
- **region_id** (Number)
- **region_name** (String)

### Read-Only

- **size** (Number)
- **status** (String)

## Import

Import is supported using the following syntax:

```shell
# import using <project_id>:<region_id>:<snapshot_id> format
terraform import gcore_snapshot.snapshot1 1:6:447d2959-8ae0-4ca0-8d47-9f050a3637d7
```