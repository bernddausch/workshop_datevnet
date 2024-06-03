# DATEVnet Netz

## Funktionen

- Proxys
  - HTTP Proxy 
    - mit und ohne Authentifizierung
  - Socks Proxy
  - FTP Proxy

Beispiel HTTP Proxy ohne Authentifizierung

```
http://win-proxy.services.datevnet.de:8880
```


## HTTP-Proxy

### Konfiguration

- [Brower Konfiguration](https://apps.datev.de/help-center/documents/0904080)
  - Manuell
  - [Proxy Konfiguration mit ProxySetter](https://www.datev.de/web/de/service-und-support/software-bereitstellung/download-bereich/it-loesungen-und-security/datevnet-proxyeinstellungen/)
  - eventuell noch Automatische Konfiguration mit WPAD (wird aktuell von Fachabteilung validiert)
- OS Konfiguration mit netsh
- Konfiguration von .net Anwendungen in den .net Konfigurationsfiles für 32- und 64-Bit Anwendungen
- Anwendungen
  - Anwendungen die Proxyfähig programmiert wurden, haben meist in den Einstellungen die Möglichkeit den Proxy zu hinterlegen (z.B. Firefox)
  - Umgebungsvariablen
  - Startparameter


  