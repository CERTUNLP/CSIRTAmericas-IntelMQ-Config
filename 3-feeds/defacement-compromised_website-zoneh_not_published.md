# defacement | compromised_website | zone-h (not published)

Los valores entre `<>` deben ser reemplazados acorde a sus necesidades, removiendo también los caracteres `<>`.

Para el caso del deduplicator, si su servidor Redis esta en otro host deberá configurar la variable `redis_cache_host` con la IP adecuada, en caso de usar docker-intelmq el valor será `redis`.

## RsyncPowered

**private_key:** `<your_private_key>`

**provider:** `CSIRTAmericas`

**rsync_file_path_formatting:** `true`

**sync_path:**
 `<user>@rsync.csirtamericas.org:<cc>zone/defacement/compromised_website/zoneh/`

**file:** `{time[%Y%m%d]}-compromised_website-not_published-<CC>.csv`

**name:** `compromisedwebsite`


## GenericCsv

**delimiter:** `,`

**skip_header:** `true`

**columns:** `extra.csirtamericas.observation_time,time.source,extra.zoneh_accepted_date,extra.actor,source.fqdn,source.url,source.ip,source.asn,source.as_name,extra.os.name,extra.http_target,extra.reason,extra.compromise_method,extra.mirror,extra.type,extra.redefacement,extra.publication,extra.def_grade,extra.zoneh_report_id,extra.csirtamericas.taxonomy,extra.csirtamericas.provider`


## Deduplicator

**filter_keys:** `extra.zoneh_report_id`

**redis_cache_host:** `<redis_hostname_or_ip>`
