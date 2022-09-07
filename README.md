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
| vulnerability | vulnerable_system              | shodan                 | [link](vulnerability-vulnerable_system-shodan.md)              |
| vulnerability | vulnerable_system              | publicwww              | [link](vulnerability-vulnerable_system-publicwww.md)           |
| vulnerability | virtualization_internet_facing | shodan                 | [link](vulnerability-virtualization_internet_facing-shodan.md) |
| defacement    | compromised_website            | publicwww              | [link](defacement-compromised_website-publicwww.md)            |
| defacement    | compromised_website            | zone-h (published)     | [link](defacement-compromised_website-zoneh_published.md)      |
| defacement    | compromised_website            | zone-h (not published) | [link](defacement-compromised_website-zoneh_not_published.md)  |
| spam          | spam_site                      | publicwww              | [link](spam-spam_site-publicwww.md)                            |
| spam          | spam_relay                     | abusix                 | [link](spam-spam_relay-abusix.md)                              |
| spam          | spam_relay_daily               | abusix                 | [link](spam-spam_relay_daily-abusix.md)                        |
| spam          | spam_account                   | abusix                 | [link](spam-spam_account-abusix.md)                            |
| spam          | spam_account_government        | abusix                 | [link](spam-spam_account_government-abusix.md)                 |
| spam          | spam_account_daily             | abusix                 | [link](spam-spam_account_daily-abusix.md)                      |
| spam          | spam_account_government_daily  | abusix                 | [link](spam-spam_account_government_daily-abusix.md)           |
| cryptojacking | cryptojacking_site             | publicwww              | [link](cryptojacking-cryptojacking_site-publicwww.md)          |
| ics-scada     | ics_scada_internet_facing      | shodan                 | [link](ics-scada-ics_scada_internet_facing-shodan.md)          |
| phishing      | phishing_domains               | phishtank              | [link](phishing-phishing_domains-phishtank.md)                 |
| malware       | infected_connections           | microsoft              | [link](malware-infected_connections-microsoft.md)              |


