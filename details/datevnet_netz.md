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

### Allgemein

- Versteht http (Port 80) und https (Port 443)
- SSL Scan möglich. Muss getrennt Freigeschaltet werden
- Proxy mit Anmeldung erfasst Surfverhalten der Mitarbeiter
  - Mitarbeiter kann auf Proxy ohne Authentifizierung Umschalten
- 24/7 Monitoring durch DATEV
  - Eigenes Regelwerk falls im Montioring neue Schadsoftware Varianten erkannt werden
  - im Notfall Stecker ziehen (geschehen bei ['I Love you' Virus](https://en.wikipedia.org/wiki/ILOVEYOU))

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


## Socks Proxy


### Beschreibung
Das SOCKS-Protokoll ist ein Internet-Protokoll, das Client-Server-Anwendungen erlaubt, protokollunabhängig und transparent die Dienste eines Proxyservers zu nutzen. SOCKS ist eine Abkürzung für „SOCKetS“.

Clients hinter einer Firewall, die eine Verbindung zu einem externen Server aufbauen wollen, verbinden sich stattdessen zu einem SOCKS-Proxy. Dieser Proxyserver überprüft die Berechtigung des Clients, den externen Server zu kontaktieren, und leitet die Anfrage an den Server weiter.

...

[Quelle](https://de.wikipedia.org/wiki/SOCKS)

### Addresse Socks Proxy DATEV

```
socks.services.datevnet.de:1080
```