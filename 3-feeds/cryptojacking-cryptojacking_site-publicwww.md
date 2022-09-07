# cryptojacking | cryptojacking_site | publicwww

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

`<user>@rsync.csirtamericas.org:<cc>zone/cryptojacking/cryptojacking_site/publicwww/`

**file:**

`{time[%Y%m%d]}-cryptojacking_site-<CC>.csv`

**name:**

`cryptojackingsite`

---
## GenericCsv

**delimiter:**

`,`

**skip_header:**

`true`

**columns:**

`time.source,source.url,source.ip,source.fqdn,extra.source_code,extra.alexa_ranking,extra.publicwww_query,extra.csirtamericas.taxonomy`

---
## Deduplicator

**filter_keys:**

`time.source,source.url,source.ip`

**redis_cache_host:**

`<redis_hostname_or_ip>`
