---
# Copyright (c) 2023 Dell Inc., or its subsidiaries. All Rights Reserved.
#
# Licensed under the Mozilla Public License Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://mozilla.org/MPL/2.0/
#
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

title: "powerscale_smartpool_settings data source"
linkTitle: "powerscale_smartpool_settings"
page_title: "powerscale_smartpool_settings Data Source - terraform-provider-powerscale"
subcategory: ""
description: |-
  This datasource is used to query the SmartPools settings from PowerScale array. The information fetched from this datasource can be used for getting the details / for further processing in resource block. PowerScale SmartPools settings provide the ability to configure SmartPools on the cluster.
---

# powerscale_smartpool_settings (Data Source)

This datasource is used to query the SmartPools settings from PowerScale array. The information fetched from this datasource can be used for getting the details / for further processing in resource block. PowerScale SmartPools settings provide the ability to configure SmartPools on the cluster.



<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `default_transfer_limit_pct` (Number) Applies to all storagepools that fall back on the default transfer limit. Stop moving files to this pool when this limit is met. The value must be between 0 and 100. Only available for PowerScale 9.5 and above.
- `default_transfer_limit_state` (String) How the default transfer limit value is applied.Only available for PowerScale 9.5 and above.

### Read-Only

- `global_namespace_acceleration_enabled` (Boolean) Enable global namespace acceleration.
- `global_namespace_acceleration_state` (String) Whether or not namespace operation optimizations are currently in effect.
- `id` (String) Id of SmartPools settings. Readonly. Fixed value of "smartpools_settings"
- `manage_io_optimization` (Boolean) Manage I/O optimization settings.
- `manage_io_optimization_apply_to_files` (Boolean) Apply to files with manually-managed I/O optimization settings.
- `manage_protection` (Boolean) Manage protection settings.
- `manage_protection_apply_to_files` (Boolean) Apply to files with manually-managed protection.
- `protect_directories_one_level_higher` (Boolean) Increase directory protection to a higher requested protection than its contents.
- `spillover_enabled` (Boolean) Enable global spillover.
- `spillover_target` (Attributes) Spillover data target. (see [below for nested schema](#nestedatt--spillover_target))
- `ssd_l3_cache_default_enabled` (Boolean) Use SSDs as L3 cache by default for new node pools.
- `ssd_qab_mirrors` (String) Controls number of mirrors of QAB blocks to place on SSDs.
- `ssd_system_btree_mirrors` (String) Controls number of mirrors of system B-tree blocks to place on SSDs.
- `ssd_system_delta_mirrors` (String) Controls number of mirrors of system delta blocks to place on SSDs.
- `virtual_hot_spare_deny_writes` (Boolean) Deny data writes to reserved disk space
- `virtual_hot_spare_hide_spare` (Boolean) Subtract the space reserved for the virtual hot spare when calculating available free space
- `virtual_hot_spare_limit_drives` (Number) The number of drives to reserve for the virtual hot spare, from 0-4.
- `virtual_hot_spare_limit_percent` (Number) The percent space to reserve for the virtual hot spare, from 0-20.

<a id="nestedatt--spillover_target"></a>
### Nested Schema for `spillover_target`

Read-Only:

- `id` (Number) Target pool ID if target specified, otherwise null.
- `name` (String) Target pool name if target specified, otherwise null.
- `type` (String) Type of target pool.