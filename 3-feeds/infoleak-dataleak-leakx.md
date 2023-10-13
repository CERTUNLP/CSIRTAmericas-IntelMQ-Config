# infoleak | data_leak | intelx

Los valores entre `<>` deben ser reemplazados acorde a sus necesidades, removiendo también los caracteres `<>`.

Para el caso del deduplicator, si su servidor Redis esta en otro host deberá configurar la variable `redis_cache_host` con la IP adecuada, en caso de usar docker-intelmq el valor será `redis`.

---
## RsyncPowered

**private_key:**

`<your_private_key>`

**provider:**

`CSIRTAmericas`

**rsync_file_path_formatting:**

`true`

**sync_path:**

`<user>@rsync.csirtamericas.org:<cc>zone/infoleak/data_leak/intelx/`

**file:**

`{time[%Y%m%d]}-data-leak-credentials-<CC>.csv`

**name:**

`dataleak`


---
## GenericCsv

**delimiter:**

`,`

**skip_header:**

`true`

**columns:**

`extra.csirtamericas.observation_time,time.source,source.account,extra.password,extra.password_type,source.fqdn,extra.leak_source,extra.csirtamericas.taxonomy,extra.provider`


---
## Deduplicator

**filter_keys:**

`time.source,source.account,extra.password`

**redis_cache_host:**

`<redis_hostname_or_ip>`
