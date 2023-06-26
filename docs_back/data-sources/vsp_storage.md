---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "coolbeans_vsp_storage Data Source - terraform-provider-coolbeans"
subcategory: ""
description: |-
  
---

# coolbeans_vsp_storage (Data Source)





<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `serial` (Number)

### Read-Only

- `id` (String) The ID of this resource.
- `info` (List of Object) (see [below for nested schema](#nestedatt--info))

<a id="nestedatt--info"></a>
### Nested Schema for `info`

Read-Only:

- `controller1_ip` (String)
- `controller2_ip` (String)
- `dkc_micro_code_version` (String)
- `free_capacity_in_mb` (Number)
- `management_ip` (String)
- `storage_device_id` (String)
- `storage_device_model` (String)
- `storage_serial_number` (Number)
- `svp_ip` (String)
- `total_capacity_in_mb` (Number)
- `used_capacity_in_mb` (Number)

