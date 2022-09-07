# spam | spam_account | abusix

Los valores entre `<>` deben ser reemplazados acorde a sus necesidades, removiendo también los caracteres `<>`.

Para el caso del deduplicator, si su servidor Redis esta en otro host deberá configurar la variable `redis_cache_host` con la IP adecuada, en caso de usar docker-intelmq el valor será `redis`.

## RsyncPowered

**private_key:** `<your_private_key>`

**provider:** `CSIRTAmericas`

**rsync_file_path_formatting:** `true`

**rsync_path:** `<user>@rsync.csirtamericas.org:<cc>zone/spam/spam_account/abusix/`

**file:** `{time[%Y%m%d]}-spam_account-<CC>.csv`

**name:** `spamaccount`


## GenericCsv

**delimiter:** `,`

**skip_header:** `true`

**columns:** `extra.csirtamericas.observation_time,time.source,source.ip,source.asn,source.as_name,source.geolocation.cc,source.registry,source.domain_suffix,source.account,extra.subject,extra.attachment_hashes,extra.attachment_types,extra.email_urls,extra.email_headers,extra.data_origin,extra.csirtamericas.taxonomy,extra.csirtamericas.provider`


## Deduplicator

**filter_keys:** `time.source,source.ip,time.source,source.account,source.domain_suffix`

**redis_cache_host:** `<redis_hostname_or_ip>`
