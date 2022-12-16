---
page_title: "morpheus_backup_setting Resource - terraform-provider-morpheus"
subcategory: ""
description: |-
  Provides a Morpheus backup setting resource.
---

# morpheus_backup_setting

Provides a Morpheus backup setting resource.

## Example Usage

```terraform
resource "morpheus_backup_setting" "tf_example_backup_setting" {
  scheduled_backups                = true
  create_backups                   = true
  backup_appliance                 = false
  default_backup_storage_bucket_id = 17
  default_backup_schedule_id       = 3
  retention_days                   = 21
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `backup_appliance` (Boolean) Whether a backup will be created for the Morpheus appliance database
- `create_backups` (Boolean) Whether morpheus will automatically configure instances for manual or scheduled backups
- `default_backup_schedule_id` (Number) The ID of the execution schedule used as the default backup schedule
- `default_backup_storage_bucket_id` (Number) The ID of the storage bucket to set as the default for backups
- `retention_days` (Number) The number of days to retain backups
- `scheduled_backups` (Boolean) Whether automatic backups will be scheduled for provisioned instances

### Read-Only

- `id` (String) The ID of the backup settings

## Import

Import is supported using the following syntax:

```shell
terraform import morpheus_backup_setting.tf_example_backup_config 1
```