# TryLater-Anwendung
Die **TryLater-Anwendung** stellt die vollständige TryLater-App bereit:
Sie verwaltet Nutzerdaten, Geschäftslogik und liefert gleichzeitig das Frontend an die Benutzer aus.

---

## 🔗 Projekt-Links
- **[Projekt-Wiki](https://github.com/SpaghettiCodeGang/TryLater-Server/wiki)**
- **[Projekt-Board](https://github.com/orgs/SpaghettiCodeGang/projects/1)**
- **[TryLater-Server-Repo](https://github.com/SpaghettiCodeGang/TryLater-Server)**
- **[TryLater-Client-Repo](https://github.com/SpaghettiCodeGang/TryLater-Client)**
- **[Live-Demo “TryLater”](https://www.trylater.de)**

---

## 🧰 Voraussetzungen

- Docker und Docker Compose müssen installiert sein
- **Linux:** Docker einfach über den Paketmanager installieren (`apt`, `pacman`, `dnf`, etc.)
- **macOS & Windows:** [Docker Desktop](https://www.docker.com/products/docker-desktop/) installieren und vor dem Start des Projekts öffnen

> 💡 **Hinweis:** Die Anwendung muss zwingend über Docker Compose gestartet werden, da die Datenbank als eigener Container bereitgestellt wird.

---

## ⚙️ Setup

- `.env` Datei mit Dummy-Daten liegt bereits im Projekt bei
- Keine weitere Konfiguration notwendig

### Starten

```bash
docker-compose up -d
```

- Anwendung läuft anschließend unter: [http://localhost:8080](http://localhost:8080)

---

## 🗂️ Projektstruktur

| Pfad                    | Beschreibung                                  |
|:------------------------|:----------------------------------------------|
| `/trylater.jar`         | Kompilierte TryLater Anwendung (Spring Boot)  |
| `/docker-compose.yml`   | Startet PostgreSQL und die TryLater Anwendung |
| `/images/`              | Ordner für hochgeladene Benutzerbilder        |
| Docker Volume `db_data` | Persistente Daten der Datenbank               |

---

## 🌐 Anwendung

Nach dem Start über Docker stellt die Anwendung bereit:

- **Frontend**  
  → erreichbar über: [http://localhost:8080](http://localhost:8080)

- **API**  
  → erreichbar über: [http://localhost:8080/api/...](http://localhost:8080/api/...)

Eine vollständige Übersicht der API-Endpunkte findet sich im [TryLater-Server Wiki](https://github.com/SpaghettiCodeGang/TryLater-Server/wiki/API‐Schnittstellenübersicht).

---

## 📱 Optimierung für mobile Geräte

Die TryLater-App wurde primär für die Nutzung auf Smartphones entwickelt und optimiert.  
Die Benutzeroberfläche sowie das Layout sind für kleinere Bildschirme ausgelegt.

> 💡 Hinweis: Auf Desktop-Browsern kann die Darstellung aufgrund des Mobile-First-Ansatzes vergleichsweise luftig oder schlicht wirken.

---

## 🧪 Testzugang

> ❗️ Es sind keine Testbenutzer hinterlegt.
> ➡️ Bitte registrieren Sie selbst einen oder mehrere Accounts, um Funktionen wie Empfehlungen zu testen.

---

## 📄 Beispiel `.env` Datei

```dotenv
SPRING_DATASOURCE_USERNAME=trylater_user
SPRING_DATASOURCE_PASSWORD=trylater_password
JWT_SECRET=R4eeA63VK5KsoqiAaWhn1E5LECxF2w4d0llKcQxkkBExVOdYUcUwB24LuJMouBrsU93vDcTiifC8pVGib23kpXVQAVwlUPiYWhbE
```

> 💡 Hinweis: Diese Dummy-Daten sind für die Testumgebung vorgesehen und enthalten keine sicherheitsrelevanten Informationen.

---

## 🧃 Viel Spaß beim Testen!

