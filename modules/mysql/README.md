# terraform-google-sql for MySQL

[^]: (autogen_docs_start)

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| activation\_policy | The activation policy for the master instance. Can be either `ALWAYS`, `NEVER` or `ON\_DEMAND`. | string | `"ALWAYS"` | no |
| additional\_databases | A list of databases to be created in your cluster | list | `<list>` | no |
| additional\_users | A list of users to be created in your cluster | list | `<list>` | no |
| authorized\_gae\_applications | The list of authorized App Engine project names | list | `<list>` | no |
| backup\_configuration | The backup configuration block of the Cloud SQL resources This argument will be passed through the master instance directrly.<br><br>See \[more details\]\(https://www.terraform.io/docs/providers/google/r/sql\_database\_instance.html\). | map | `<map>` | no |
| create\_timeout | The optional timout that is applied to limit long database creates. | string | `"10m"` | no |
| database\_flags | The database flags for the master instance. See \[more details\]\(https://cloud.google.com/sql/docs/mysql/flags\) | list | `<list>` | no |
| database\_version | The database version to use | string | n/a | yes |
| db\_charset | The charset for the default database | string | `""` | no |
| db\_collation | The collation for the default database. Example: 'utf8\_general\_ci' | string | `""` | no |
| db\_name | The name of the default database to create | string | `"default"` | no |
| delete\_timeout | The optional timout that is applied to limit long database deletes. | string | `"10m"` | no |
| disk\_autoresize | Configuration to increase storage size | string | `"true"` | no |
| disk\_size | The disk size for the master instance | string | `"10"` | no |
| disk\_type | The disk type for the master instance. | string | `"PD_SSD"` | no |
| failover\_replica | Specify true if the failover instance is required | string | `"false"` | no |
| failover\_replica\_activation\_policy | The activation policy for the failover replica instance. Can be either `ALWAYS`, `NEVER` or `ON\_DEMAND`. | string | `"ALWAYS"` | no |
| failover\_replica\_configuration | The replica configuration for the failover replica instance. In order to create a failover instance, need to specify this argument. | map | `<map>` | no |
| failover\_replica\_crash\_safe\_replication | The crash safe replication is to indicates when crash-safe replication flags are enabled. | string | `"true"` | no |
| failover\_replica\_database\_flags | The database flags for the failover replica instance. See \[more details\]\(https://cloud.google.com/sql/docs/mysql/flags\) | list | `<list>` | no |
| failover\_replica\_disk\_autoresize | Configuration to increase storage size. | string | `"true"` | no |
| failover\_replica\_disk\_size | The disk size for the failover replica instance. | string | `"10"` | no |
| failover\_replica\_disk\_type | The disk type for the failover replica instance. | string | `"PD_SSD"` | no |
| failover\_replica\_ip\_configuration | The ip configuration for the failover replica instances. | map | `<map>` | no |
| failover\_replica\_maintenance\_window\_day | The day of week \(1-7\) for the failover replica instance maintenance. | string | `"1"` | no |
| failover\_replica\_maintenance\_window\_hour | The hour of day \(0-23\) maintenance window for the failover replica instance maintenance. | string | `"23"` | no |
| failover\_replica\_maintenance\_window\_update\_track | The update track of maintenance window for the failover replica instance maintenance. Can be either `canary` or `stable`. | string | `"canary"` | no |
| failover\_replica\_name\_suffix | The optional suffix to add to the failover instance name | string | `""` | no |
| failover\_replica\_pricing\_plan | The pricing plan for the failover replica instance. | string | `"PER_USE"` | no |
| failover\_replica\_replication\_type | The replication type for the failover replica instance. Can be one of ASYNCHRONOUS or SYNCHRONOUS. | string | `"SYNCHRONOUS"` | no |
| failover\_replica\_tier | The tier for the failover replica instance. | string | `""` | no |
| failover\_replica\_user\_labels | The key/value labels for the failover replica instance. | map | `<map>` | no |
| failover\_replica\_zone | The zone for the failover replica instance, it should be something like: `a`, `c`. | string | `""` | no |
| ip\_configuration | The ip configuration for the master instance. | map | `<map>` | no |
| maintenance\_window\_day | The day of week \(1-7\) for the master instance maintenance. | string | `"1"` | no |
| maintenance\_window\_hour | The hour of day \(0-23\) maintenance window for the master instance maintenance. | string | `"23"` | no |
| maintenance\_window\_update\_track | The update track of maintenance window for the master instance maintenance. Can be either `canary` or `stable`. | string | `"canary"` | no |
| name | The name of the Cloud SQL resources | string | n/a | yes |
| pricing\_plan | The pricing plan for the master instance. | string | `"PER_USE"` | no |
| project\_id | The project ID to manage the Cloud SQL resources | string | n/a | yes |
| read\_replica\_activation\_policy | The activation policy for the read replica instances. Can be either `ALWAYS`, `NEVER` or `ON\_DEMAND`. | string | `"ALWAYS"` | no |
| read\_replica\_configuration | The replica configuration for use in all read replica instances. | map | `<map>` | no |
| read\_replica\_crash\_safe\_replication | The crash safe replication is to indicates when crash-safe replication flags are enabled. | string | `"true"` | no |
| read\_replica\_database\_flags | The database flags for the read replica instances. See \[more details\]\(https://cloud.google.com/sql/docs/mysql/flags\) | list | `<list>` | no |
| read\_replica\_disk\_autoresize | Configuration to increase storage size. | string | `"true"` | no |
| read\_replica\_disk\_size | The disk size for the read replica instances. | string | `"10"` | no |
| read\_replica\_disk\_type | The disk type for the read replica instances. | string | `"PD_SSD"` | no |
| read\_replica\_ip\_configuration | The ip configuration for the read replica instances. | map | `<map>` | no |
| read\_replica\_maintenance\_window\_day | The day of week \(1-7\) for the read replica instances maintenance. | string | `"1"` | no |
| read\_replica\_maintenance\_window\_hour | The hour of day \(0-23\) maintenance window for the read replica instances maintenance. | string | `"23"` | no |
| read\_replica\_maintenance\_window\_update\_track | The update track of maintenance window for the read replica instances maintenance. Can be either `canary` or `stable`. | string | `"canary"` | no |
| read\_replica\_name\_suffix | The optional suffix to add to the read instance name | string | `""` | no |
| read\_replica\_pricing\_plan | The pricing plan for the read replica instances. | string | `"PER_USE"` | no |
| read\_replica\_replication\_type | The replication type for read replica instances. Can be one of ASYNCHRONOUS or SYNCHRONOUS. | string | `"SYNCHRONOUS"` | no |
| read\_replica\_size | The size of read replicas | string | `"0"` | no |
| read\_replica\_tier | The tier for the read replica instances. | string | `""` | no |
| read\_replica\_user\_labels | The key/value labels for the read replica instances. | map | `<map>` | no |
| read\_replica\_zones | The zones for the read replica instancess, it should be something like: `a,b,c`. Given zones are used rotationally for creating read replicas. | string | `""` | no |
| region | The region of the Cloud SQL resources | string | `"us-central1"` | no |
| tier | The tier for the master instance. | string | `"db-n1-standard-1"` | no |
| update\_timeout | The optional timout that is applied to limit long database updates. | string | `"10m"` | no |
| user\_host | The host for the default user | string | `"%"` | no |
| user\_labels | The key/value labels for the master instances. | map | `<map>` | no |
| user\_name | The name of the default user | string | `"default"` | no |
| user\_password | The password for the default user. If not set, a random one will be generated and available in the generated\_user\_password output variable. | string | `""` | no |
| zone | The zone for the master instance, it should be something like: `a`, `c`. | string | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| failover-replica\_instance\_connection\_name | The connection name of the failover-replica instance to be used in connection strings |
| failover-replica\_instance\_first\_ip\_address | The first IPv4 address of the addesses assigned for the failover-replica instance |
| failover-replica\_instance\_name | The instance name for the failover replica instance |
| failover-replica\_instance\_self\_link | The URI of the failover-replica instance |
| failover-replica\_instance\_server\_ca\_cert | The CA certificate information used to connect to the failover-replica instance via SSL |
| failover-replica\_instance\_service\_account\_email\_address | The service account email addresses assigned to the failover-replica instance |
| generated\_user\_password | The auto generated default user password if not input password was provided |
| instance\_connection\_name | The connection name of the master instance to be used in connection strings |
| instance\_first\_ip\_address | The first IPv4 address of the addresses assigned for the master instance. |
| instance\_ip\_address | The IPv4 address assigned for the master instance |
| instance\_name | The instance name for the master instance |
| instance\_self\_link | The URI of the master instance |
| instance\_server\_ca\_cert | The CA certificate information used to connect to the SQL instance via SSL |
| instance\_service\_account\_email\_address | The service account email address assigned to the master instance |
| private\_address | The private IP address assigned for the master instance |
| read\_replica\_instance\_names | The instance names for the read replica instances |
| replicas\_instance\_connection\_names | The connection names of the replica instances to be used in connection strings |
| replicas\_instance\_first\_ip\_addresses | The first IPv4 addresses of the addresses assigned for the replica instances |
| replicas\_instance\_self\_links | The URIs of the replica instances |
| replicas\_instance\_server\_ca\_certs | The CA certificates information used to connect to the replica instances via SSL |
| replicas\_instance\_service\_account\_email\_addresses | The service account email addresses assigned to the replica instances |

[^]: (autogen_docs_end)