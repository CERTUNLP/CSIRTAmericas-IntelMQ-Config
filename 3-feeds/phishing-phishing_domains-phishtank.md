# phishing | phishing_domains | phishtank

Los valores entre `<>` deben ser reemplazados acorde a sus necesidades, removiendo también los caracteres `<>`.

Para el caso del deduplicator, si su servidor Redis esta en otro host deberá configurar la variable `redis_cache_host` con la IP adecuada, en caso de usar docker-intelmq el valor será `redis`.

## RsyncPowered

**private_key:** `<your_private_key>`

**provider:** `CSIRTAmericas`

**rsync_file_path_formatting:** `true`

**sync_path:** `<user>@rsync.csirtamericas.org:<cc>zone/phishing/phishing_domains/phishtank/`

**file:** `{time[%Y%m%d]}-phishing_domains-<CC>.csv`

**name:** `phishingdomains`


## GenericCsv

**delimiter:** `,`

**skip_header:** `true`

**columns:** `extra.csirtamericas.observation_time,time.source,source.fqdn,source.url,source.ip,source.asn,source.as_name,extra.phishing_target,event_description.url,extra.csirtamericas.taxonomy,extra.csirtamericas.provider`


## Deduplicator

**filter_keys:** `time.source,source.fqdn,source.url,extra.phishing_target,event_description.url`

**redis_cache_host:** `<redis_hostname_or_ip>`
