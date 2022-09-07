# Guía de configuración de bots para CSIRTAmericas

## Introducción
La presente guía trabaja utilizando IntelMQ y el repositorio de bots creado por CERTUNLP (https://github.com/CERTUNLP/intelmq-bots) para el consumo de feeds otorgados por CSIRTAmericas.

## Ejemplo de creación de bots en IntelMQ 

[link](1-example/README.md)

## Parámetros generales de configuración de bots para CSIRTAmericas

[link](2-parameters/README.md)

## Valores de configuración de cada bot según el feed 

| Category      | SubType                        | Provider               | Configuration                                                  |
| :------------ | :----------------------------- | :--------------------- | :------------------------------------------------------------- |
| vulnerability | vulnerable_system              | shodan                 | [link](3-feeds/vulnerability-vulnerable_system-shodan.md)              |
| vulnerability | vulnerable_system              | publicwww              | [link](3-feeds/vulnerability-vulnerable_system-publicwww.md)           |
| vulnerability | virtualization_internet_facing | shodan                 | [link](3-feeds/vulnerability-virtualization_internet_facing-shodan.md) |
| defacement    | compromised_website            | publicwww              | [link](3-feeds/defacement-compromised_website-publicwww.md)            |
| defacement    | compromised_website            | zone-h (published)     | [link](3-feeds/defacement-compromised_website-zoneh_published.md)      |
| defacement    | compromised_website            | zone-h (not published) | [link](3-feeds/defacement-compromised_website-zoneh_not_published.md)  |
| spam          | spam_site                      | publicwww              | [link](3-feeds/spam-spam_site-publicwww.md)                            |
| spam          | spam_relay                     | abusix                 | [link](3-feeds/spam-spam_relay-abusix.md)                              |
| spam          | spam_relay_daily               | abusix                 | [link](3-feeds/spam-spam_relay_daily-abusix.md)                        |
| spam          | spam_account                   | abusix                 | [link](3-feeds/spam-spam_account-abusix.md)                            |
| spam          | spam_account_government        | abusix                 | [link](3-feeds/spam-spam_account_government-abusix.md)                 |
| spam          | spam_account_daily             | abusix                 | [link](3-feeds/spam-spam_account_daily-abusix.md)                      |
| spam          | spam_account_government_daily  | abusix                 | [link](3-feeds/spam-spam_account_government_daily-abusix.md)           |
| cryptojacking | cryptojacking_site             | publicwww              | [link](3-feeds/cryptojacking-cryptojacking_site-publicwww.md)          |
| ics-scada     | ics_scada_internet_facing      | shodan                 | [link](3-feeds/ics-scada-ics_scada_internet_facing-shodan.md)          |
| phishing      | phishing_domains               | phishtank              | [link](3-feeds/phishing-phishing_domains-phishtank.md)                 |
| malware       | infected_connections           | microsoft              | [link](3-feeds/malware-infected_connections-microsoft.md)              |


