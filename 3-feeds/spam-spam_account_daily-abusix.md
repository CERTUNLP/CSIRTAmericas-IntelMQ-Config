# spam | spam_account_daily | abusix

Los valores entre `<>` deben ser reemplazados acorde a sus necesidades, removiendo también los caracteres `<>`.

Para el caso del deduplicator, si su servidor Redis esta en otro host deberá configurar la variable `redis_cache_host` con la IP adecuada, en caso de usar docker-intelmq el valor será `redis`.

## RsyncPowered

**private_key:** `<your_private_key>`

**provider:** `CSIRTAmericas`

**rsync_file_path_formatting:** `true`

**rsync_path:** `<user>@rsync.csirtamericas.org:<cc>zone/spam/spam_account/abusix/`

**file:** `{time[%Y%m%d]}-spam_account_daily-<CC>.csv`

**name:** `spamaccountdaily`


## GenericCsv

**delimiter:** `,`

**skip_header:** `true`

**columns:** `extra.csirtamericas.observation_time,source.domain_suffix,source.ip,source.asn,source.as_name,extra.email_count,extra.csirtamericas.taxonomy,extra.csirtamericas.provider`


## Deduplicator

**filter_keys:** `extra.csirtamericas.observation_time,source.domain_suffix,source.ip`

**redis_cache_host:** `<redis_hostname_or_ip>`
