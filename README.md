# Forgejo

[Forgejo](https://forgejo.org/) ist eine leichtgewichtige, selbstgehostete Software-Forgelösung. Sie ist einfach zu installieren, pflegeleicht und bietet eine vollständige Plattform für das Hosting von Git-Repositories.

## Unterstützte Versionen

Du kannst die zu installierende Version über die `Version`-Variable festlegen. Die folgenden Werte sind möglich:

- `latest`  – neueste stabile Version (Standard)
- `nightly` – aktuelle Nightly-Build
- `x.y.z`   – spezifische Forgejo-Version (z. B. `1.20.4`)

## Server-Ports

Folgende Ports werden standardmäßig vom Server verwendet:

| Port | Standardwert |
|------|--------------|
| App  | 3000         |
| SSH  | 20815        |

## Startparameter

Der Server wird mit folgendem Befehl gestartet:

```bash
./forgejo web -p {{SERVER_PORT}} -c ./app.ini
```

## Konfiguration

Die Konfiguration erfolgt über die Datei `custom/app.ini`, die bei der ersten Installation automatisch erzeugt wird, falls sie noch nicht vorhanden ist.

### Wichtige Konfigurationswerte:

- `LOCAL_ROOT_URL` – Basis-URL für die Instanz
- `DOMAIN` – Domain/IP-Adresse des Servers
- `DISABLE_SSH` – SSH deaktivieren (true/false)
- `SSH_PORT` – Port für Git+SSH-Zugriffe

## Installation (Pterodactyl Egg)

Das Installationsskript ermittelt automatisch die neueste Version und die passende Architektur (`amd64` oder `arm64`) und installiert Forgejo in der Serverumgebung. Weitere Details zum Installationsprozess findest du im Egg.

## Lizenz

Forgejo steht unter der [MIT-Lizenz](https://forgejo.org/#license).

---

> **Hinweis:** Dieses Projekt verwendet ein automatisch generiertes [Pterodactyl](https://pterodactyl.io/)-Egg. Alle Details zur Software findest du auf der offiziellen Website: [forgejo.org](https://forgejo.org/)
