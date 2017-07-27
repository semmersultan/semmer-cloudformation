# RDS stack
Creates a RDS Database, Role and Alarms

## RDS

### Parameters

| Name | Description | Default | Required |
|------|-------------|:-----:|:-----:|
| VpcID | VPC ID |  | yes |
| VpcCIDR | VPC Cidr Range |  | yes |
| DBUsername | Master Username |  | yes |
| DBInstanceType | RDS Capacity | db.t2.medium | yes |
| DBStorageSize | Storage to allocate to DB | 200 | yes |
| BackupRetention | Number of days to retain snapshot | 1 | yes |
| InternalZone | Route53 DNS Internal Zone | none | yes |
| ExternalZone | Route53 DNS External Zone | none | yes |
| UseProdConfig | Create a Multi AZ DB with Encryption on SE | false | no |


### Encrypt DB password
    shush encrypt alias/db_rds_pass Password1234!
And add to Makefile
