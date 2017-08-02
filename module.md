
## Inputs

| Name | Description | Default | Required |
|------|-------------|:-----:|:-----:|
| allow_major_version_upgrade | Allow major version upgrade | `false` | no |
| apply_immediately | Specifies whether any database modifications are applied immediately, or during the next maintenance window | `false` | no |
| auto_minor_version_upgrade | Allow automated minor version upgrade | `true` | no |
| backup_retention_period | How long will we retain backups | `0` | no |
| backup_window | When AWS can run snapshot, can't overlap with maintenance window | `22:00-03:00` | no |
| copy_tags_to_snapshot | Copy tags from DB to a snapshot | `true` | no |
| database_name | The name of the database to create | - | yes |
| database_password |  | - | yes |
| database_port |  | - | yes |
| database_user | # Self-explainatory variables | - | yes |
| db_parameter_group | Parameter group, depends on DB engine used | - | yes |
| private_cidr | VPC private addressing, used for a security group | - | yes |
| publicly_accessible | Determines if database can be publicly available (NOT recommended) | `false` | no |
| rds_allocated_storage | The allocated storage in GBs | - | yes |
| rds_engine_type | Database engine type | - | yes |
| rds_engine_version | Database engine version, depends on engine type | - | yes |
| rds_instance_class | Class of RDS instance | - | yes |
| rds_instance_identifier | Custom name of the instance | - | yes |
| rds_is_multi_az | Set to true on production | `false` | no |
| rds_storage_type | One of 'standard' (magnetic), 'gp2' (general purpose SSD), or 'io1' (provisioned IOPS SSD). | `standard` | no |
| rds_vpc_id | VPC to connect to, used for a security group | - | yes |
| skip_final_snapshot | If true (default), no snapshot will be made before deleting DB | `true` | no |
| subnets | List of subnets DB should be available at. It might be one subnet. | - | yes |
| tags | A map of tags to add to all resources | `<map>` | no |

## Outputs

| Name | Description |
|------|-------------|
| rds_instance_address | # Output the address (aka hostname) of the RDS instance |
| rds_instance_endpoint | # Output endpoint (hostname:port) of the RDS instance |
| rds_instance_id | # Output the ID of the RDS instance |
| security_group_id | # Output DB security group ID |
| subnet_group_id | # Output the ID of the Subnet Group |

