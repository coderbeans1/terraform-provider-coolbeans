---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "hitachi_vss_block_iscsi_chap_user Resource - terraform-provider-hitachi"
subcategory: "ISCIS Chap User"
description: |-
  The following request sets the CHAP user.
---

# hitachi_vss_block_iscsi_chap_user (Resource)

The following request sets the CHAP user.

## Example Usage

```terraform
resource "hitachi_vss_block_iscsi_chap_user" "my_chap_user2" {
  vss_block_address       = ""
  target_chap_user_name   = "rahul112"
  target_chap_user_secret = "rahul8010111211"
  #initiator_chap_user_name = "rahul111"
  #initiator_chap_user_secret = "rahul8910111222"
}

output "chap_user_output" {
  value = resource.hitachi_vss_block_iscsi_chap_user.my_chap_user2
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `target_chap_user_name` (String) CHAP user name used for CHAP authentication on the compute port (i.e., target side).
		(1 to 223 chars) , must match /^[a-zA-Z0-9\.:@_\-\+=\[\]~ ]{1,223}$/
- `target_chap_user_secret` (String) CHAP secret used for CHAP authentication on the compute port (i.e., target side).
		(12 to 32 chars) , must match /^[a-zA-Z0-9\.:@_\-\+=\/\[\]~ ]{12,32}$/
- `vss_block_address` (String) The host name or the IP address (IPv4) of the REST API server on Virtual Storage Software block.

### Optional

- `chap_user_id` (String) The ID of the CHAP user.
- `initiator_chap_user_name` (String) CHAP user name used for CHAP authentication on the initiator port of the compute node in mutual CHAP authentication.
		(1 to 223 chars) , must match /^[a-zA-Z0-9\.:@_\-\+=\[\]~ ]{1,223}$/
- `initiator_chap_user_secret` (String) CHAP secret used for CHAP authentication on the initiator port of the compute node in mutual CHAP authentication.
		(12 to 32 chars) , must match /^[a-zA-Z0-9\.:@_\-\+=\/\[\]~ ]{12,32}$/

### Read-Only

- `id` (String) The ID of this resource.
- `info` (List of Object) This is output schema (see [below for nested schema](#nestedatt--info))

<a id="nestedatt--info"></a>
### Nested Schema for `info`

Read-Only:

- `chap_user_id` (String)
- `initiator_chap_user_name` (String)
- `target_chap_user_name` (String)