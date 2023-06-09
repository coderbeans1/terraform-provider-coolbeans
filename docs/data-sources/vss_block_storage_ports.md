---
# generated by https://github.com/fbreckle/terraform-plugin-docs
page_title: "hitachi_vss_block_storage_ports Data Source - terraform-provider-hitachi"
subcategory: "VSS Block Storage Port"
description: |-
  Obtains a list of storage ports information.
---

# hitachi_vss_block_storage_ports (Data Source)

Obtains a list of storage ports information.

## Example Usage

```terraform
data "hitachi_vss_block_storage_ports" "storagePorts" {
  vss_block_address = ""
  #port_id = "5f07176a-e10d-47b7-99b4-57b93806048b"
}

output "storagePorts" {
  value = data.hitachi_vss_block_storage_ports.storagePorts
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `vss_block_address` (String) The host name or the IP address (IPv4) of the REST API server on Virtual Storage Software block.

### Optional

- `port_id` (String) Port id of the storage device

### Read-Only

- `id` (String) The ID of this resource.
- `info` (Block List) This is output schema (see [below for nested schema](#nestedblock--info))

<a id="nestedblock--info"></a>
### Nested Schema for `info`

Read-Only:

- `configured_port_speed` (String) Configured port speed of port
- `fc_information` (Block List) FC information of port (see [below for nested schema](#nestedblock--info--fc_information))
- `interface_name` (String) Interface name of port
- `iscsi_information` (Block List) Iscsi information of port (see [below for nested schema](#nestedblock--info--iscsi_information))
- `name` (String) Name of port
- `nickname` (String) Nickname of port
- `por_speed_duplex` (String) Por speed duplex of port
- `port_auth_settings` (Block List) Port auth settings information (see [below for nested schema](#nestedblock--info--port_auth_settings))
- `port_speed` (String) Port speed of port
- `protection_domain_id` (String) Protection domain id of port
- `protocol` (String) Protocol of port
- `status` (String) Status of port
- `status_summary` (String) status summary of port
- `storage_node_id` (String) Storage node id of port
- `type` (String) Type of port

<a id="nestedblock--info--fc_information"></a>
### Nested Schema for `info.fc_information`

Read-Only:

- `connection_type` (String) Connection type of FC port
- `physical_wwn` (String) Wwn of port
- `sfp_data_transfer_rate` (String) Data transfer rate of FC port


<a id="nestedblock--info--iscsi_information"></a>
### Nested Schema for `info.iscsi_information`

Read-Only:

- `delayed_ack` (Boolean) Delayed ack of Iscsi port
- `ip_mode` (String) Ip mode of Iscsi port
- `ipv4_information` (Block List) Ipv4 information (see [below for nested schema](#nestedblock--info--iscsi_information--ipv4_information))
- `ipv6_information` (Block List) Ipv6 information (see [below for nested schema](#nestedblock--info--iscsi_information--ipv6_information))
- `is_isns_client_enabled` (Boolean) Checks if is isns client enabled of Iscsi port
- `isns_servers` (Block List) Isns servers information (see [below for nested schema](#nestedblock--info--iscsi_information--isns_servers))
- `mac_address` (String) Mac address of Iscsi port
- `mtu_size` (Number) Mtu size of Iscsi port

<a id="nestedblock--info--iscsi_information--ipv4_information"></a>
### Nested Schema for `info.iscsi_information.ipv4_information`

Read-Only:

- `address` (String) Address of ipv4 information
- `default_gateway` (String) Default gateway of ipv4 information
- `subnet_mask` (String) Subnet mask of ipv4 information


<a id="nestedblock--info--iscsi_information--ipv6_information"></a>
### Nested Schema for `info.iscsi_information.ipv6_information`

Read-Only:

- `default_gateway` (String) Default gateway of ipv6 information
- `global_address_1` (String) Global address of ipv6 information
- `global_address_mode` (String) Global address mode of ipv6 information
- `linklocal_address` (String) Linklocal address of ipv6 information
- `linklocal_address_mode` (String) Linklocal address mode of ipv6 information
- `subnet_prefix_length_1` (Number) Subnet prefix length of ipv6 information


<a id="nestedblock--info--iscsi_information--isns_servers"></a>
### Nested Schema for `info.iscsi_information.isns_servers`

Read-Only:

- `index` (Number) Index of isns server
- `port` (Number) Port of isns server
- `server_name` (String) Server name of isns server



<a id="nestedblock--info--port_auth_settings"></a>
### Nested Schema for `info.port_auth_settings`

Read-Only:

- `auth_mode` (String) Auth mode of Port
- `is_discovery_chap_auth` (Boolean) Is discovery chap auth of Port
- `is_mutual_chap_auth` (Boolean) Is mutual chap of Port


