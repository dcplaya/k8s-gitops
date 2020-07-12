# velero

Cluster backup solution

* [velero.yaml](velero/velero.yaml)


```
velero restore create RESTORE_NAME --from-backup BACKUP_NAME --include-namespaces ns1,ns2
```

Backup just nzbget
```
velero backup create nzbget --selector "app.kubernetes.io/instance=nzbget" --wait
```
