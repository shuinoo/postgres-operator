---
title: "pgo_create_schedule"
---
## pgo create schedule

Create a cron-like scheduled task

### Synopsis

Schedule creates a cron-like scheduled task.  For example:

    pgo create schedule --schedule="* * * * *" --schedule-type=pgbackrest --pgbackrest-backup-type=full mycluster

```
pgo create schedule [flags]
```

### Options

```
  -c, --ccp-image-tag string            The CCPImageTag to use for cluster creation. If specified, overrides the pgo.yaml setting.
      --database string                 The database to run the SQL policy against.
  -h, --help                            help for schedule
      --pgbackrest-backup-type string   The type of pgBackRest backup to schedule (full or diff).
      --policy string                   The policy to use for SQL schedules.
      --pvc-name string                 The name of the backup PVC to use (only used in pgbasebackup schedules).
      --schedule string                 The schedule assigned to the cron task.
      --schedule-opts string            The custom options passed to the create schedule API.
      --schedule-type string            The type of schedule to be created (pgbackrest, pgbasebackup or policy).
      --secret string                   The secret name for the username and password of the PostgreSQL role for SQL schedules.
  -s, --selector string                 The selector to use for cluster filtering.
```

### Options inherited from parent commands

```
      --apiserver-url string     The URL for the PostgreSQL Operator apiserver.
      --debug                    Enable debugging when true.
      --namespace string         The namespace to use for pgo requests.
      --pgo-ca-cert string       The CA Certificate file path for authenticating to the PostgreSQL Operator apiserver.
      --pgo-client-cert string   The Client Certificate file path for authenticating to the PostgreSQL Operator apiserver.
      --pgo-client-key string    The Client Key file path for authenticating to the PostgreSQL Operator apiserver.
```

### SEE ALSO

* [pgo create](/cli/pgo_create/)	 - Create a Cluster, PGBouncer, PGPool, Policy, Schedule, or User

###### Auto generated by spf13/cobra on 23-Jul-2019