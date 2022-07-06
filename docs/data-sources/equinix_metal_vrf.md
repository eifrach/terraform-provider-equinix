---
subcategory: "Metal"
---

# equinix_metal_virtual_circuit (Data Source)

Use this data source to retrieve a VRF resource.

~> VRF features are not generally available. The interfaces related to VRF resources may change ahead of general availability.

## Example Usage

```hcl
data "equinix_metal_vrf" "example_vrf" {
  vrf_id = "48630899-9ff2-4ce6-a93f-50ff4ebcdf6e"
}
```

## Argument Reference

The following arguments are supported:

* `vrf_id` - (Required) ID of the VRF resource

## Attributes Reference

In addition to all arguments above, the following attributes are exported:

* `name` - User-supplied name of the VRF, unique to the project
* `metro` - Metro ID or Code where the VRF will be deployed.
* `project_id` - Project ID where the VRF will be deployed.
* `description` - Description of the VRF.
* `local_asn` - The 4-byte ASN set on the VRF.
* `ip_ranges` - All IPv4 and IPv6 Ranges that will be available to BGP Peers. IPv4 addresses must be /8 or smaller with a minimum size of /29. IPv6 must be /56 or smaller with a minimum size of /64. Ranges must not overlap other ranges within the VRF.