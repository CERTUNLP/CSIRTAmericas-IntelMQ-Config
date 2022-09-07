# ics-scada | ics_scada_internet_facing | shodan

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

`<user>@rsync.csirtamericas.org:<cc>zone/ics_scada/ics_scada_internet_facing/shodan/`

**file:**

`{time[%Y%m%d]}-ics_scada_internet_facing-<CC>.csv`

**name:**

`icsscadainternetfacing`


---
## GenericCsv

**delimiter:**

`,`

**skip_header:**

`true`

**columns:**

`extra.csirtamericas.observation_time,time.source,source.ip,extra.hostnames,extra.domains,extra.service.name,source.port,extra.cve,extra.ics_model,extra.shodan_module,event_description.text,event_description.url,source.asn,source.geolocation.cc,source.geolocation.city,extra.csirtamericas.taxonomy,extra.csirtamericas.provider`


---
## Deduplicator

**filter_keys:**

`time.source,source.ip,source.port,extra.cve,extra.ics_model`

**redis_cache_host:**

`<redis_hostname_or_ip>`
