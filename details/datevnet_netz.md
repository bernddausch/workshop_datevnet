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
- Nutzt Blacklists zum Blockieren bekannter **böser** URLs

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

Dadurch muss der Proxy das Protokoll/die Anwendung nicht verstehen. 

### Anwendung

Hiermit können Anwendungen z.B. ssh eine Verbindung über den Proxy aufbauen. Nachteil ist hier wie bei HTTPS ohne Scan, das die Daten NICHT auf Viren geprüft werden können. Auch der Abfluss von Dokumenten kann hier nicht verhindert werden.

### Addresse Socks Proxy DATEV

```
socks.services.datevnet.de:1080
```

## FTP Proxy

Servername und Credentials werden im Benutzernamen und Kennwort "kodiert" und an den FTP Proxy übergeben.

Nicht mehr Empfohlen da die Daten Unverschlüsselt übertragen werden und an jeden Punkt den die Daten passieren ausgelesen werden können.

[DATEV Hilfe](https://apps.datev.de/help-center/documents/0903258)