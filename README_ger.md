# Konfiguration von Marlin für einen eigenen Core XY Drucker
Dieser Durcker basiert auf dem [D-Bot](https://www.thingiverse.com/thing:1001065) von spauda01@thingiverse.

Dieses Projekt wurde von der ursprünglichen Marlin Firmware geforkt.

## Voraussetzungen
Das Hochladen der Firmware funktioniert am besten mit PlatformIO für Visual Studio Code und der Auto Build Marlin Erweiterung.

### Installieren von Visua Studio Code
Gehe als erstes auf die [offizielle Seite von VS Code](https://code.visualstudio.com/) und installiere die neueste Version für dein Betriebssystem.

### Benötigte Erweiterungen installieren
Nachdem VS Code installiert wurde, müssen Erweiterungen installiert werden, um die Firmware zu kompilieren und hochzuladen.

Um dies zu tun, öffne VS Code und wähle die Erweiterungen auf der linken Seite aus.

![extension section](https://github.com/nipfuh/D-Bot-Marlin/blob/2.0.x/compile_doc/extension_section.png?raw=true)

In der Suchzeile, suche nach "auto build marlin" und wähle die Erweiterung `Auto Build Marlin` von `Marlin Firmware` aus.

Klicke auf `Install`.

![Auto Build Marlin install](https://github.com/nipfuh/D-Bot-Marlin/blob/2.0.x/compile_doc/auto_build_marlin.png?raw=true)

VS Code installiert dann alle benötigten Erweiterungen, inklusive PlatformIO.

_Achtung: Es kann sein, dass du das Paket python3-venv installieren musst, wenn du Ubuntu verwendest. VS Code wird während der Installation danach fragen, falls es nötig ist_

## Die Firmware

### Herunterladen und Öffnen

Auf dieser Webseite findest du auf der rechten Seite den Abschnitt releases. Wähle dort die neueste Version aus und lade die angefügte .zip-Datei herunter.
Entpacke diese anschließend mit einem Programm deiner Wahl.


Öffne als nächstes VS Code. Wähle auf der linken Seite PlatformIO aus und klicke auf `Open`.

![opening the project](https://github.com/nipfuh/D-Bot-Marlin/blob/2.0.x/compile_doc/platformio_open.png?raw=true)

In dem Tab, der sich öffnet, wähle `Open Project` und wähle den Ordner aus, den du gerade entpackt hast.

Wenn VS Code fragt, ob du dem Ordner vertraust, bestätige, dass du das tust.

_Achtung: Du musst das Elternverzeichnis des Repositorys öffnen, d.h. den Ordner, der den Ordner `Marlin`_ enthält.


### Kompilieren und Hochladen

Wenn das Projekt geöffnet ist, kannst du es kompilieren und auf den Drucker hochladen. Wähle in der unteren Leiste `build`.

![building the project](https://github.com/nipfuh/D-Bot-Marlin/blob/2.0.x/compile_doc/platformio_build.png?raw=true)

PlatformIO wird nun versuchen, Marlin zu komoilieren und dabei alle benötigten Abhängigkeiten herunterladen.

_Achtung: Es kann sein, dass der erste Build fehlschlägt. Klicke noch einmal auf build, dann sollte alles funktionieren._

Wenn Marlin fertig kompiliert ist, kannst du es auf den Drucker hochladen. Um das zu tun, klicke `upload` in der unteren Leiste.

![uploading the project](https://github.com/nipfuh/D-Bot-Marlin/blob/2.0.x/compile_doc/platformio_upload.png?raw=true)

PlatformIO sollte deinen angeschlossenen Arduino automatisch erkennen und die Firmware hochladen.

Wenn der Prozess ohne Fehler durchläuft, ist Marlin nun auf deinem Arduino und du kannst loslegen :)

## Kofiguration & Einstellungen

Wenn du den Namen deines Druckers oder andere Einstellungen ändern willst, musst du die Datei `Marlin/Configuration.h` öffnen (wähle sie im Dateiexplorer auf der linken Seite aus).

### Den Namen des Druckers ändern

Um den Namen zu ändern, gehe in der gerade geöffneten Configuration.h zu Zeile 146 und ändere den Namen, der dort eingetragen ist.
Beachte, dass du nichts in dieser Zeile ändern darfst bis auf den Namen __zwischen__ den Anführungszeichen.