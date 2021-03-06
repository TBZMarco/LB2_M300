# LB2_M300 :mortar_board: 

Diese Dokumentation beschreibt das vorgehen in der LB2 im Modul 300 an der TBZ. Auch wird erläutert um was es im Auftrag geht.

## Einleitung :shipit: 

Wir wollen einen Apache Webserver und eine MySQL Datenbank in 2 Verschiednenen Container erstellen. Für die Maschienen verwnden wir Docker und für die Dokumentation GitHub. Das Ziel ist das diese beiden Contaiener voll funktionsfähig laufen und ihre Aufgabe erfüllen. Das ganze wollen wir in Form einer Dockerumgebung machen, bei der wir selber Images erstelen und ausführen. Nachfolgen wird Docker auch noch ein bisschen erklärt.

# Einführung Docker:
Docker ist eine kostenlose Software, die Anwendungen mithilfe von Containervirtualisierung isoliert. Docker vereinfacht das Deployment von Anwendungen, da Container, die alle notwendigen Pakete enthalten, einfach als Dateien übertragen und installiert werden können. Container sorgen für die Trennung und Verwaltung von Ressourcen, die auf einem Computer verwendet werden. Dazu gehören: Code, Laufzeitmodule, Systemtools, Systembibliotheken.
![grafik](https://user-images.githubusercontent.com/89446114/178372813-d1caa1b6-31bd-473e-ac6f-02008f56c16e.png)

### Probleme 

Leider hatten wir schon von Beginn an Probleme, da Frau Falco in der ersten Woche Krank war und bei Herr Neuschwander trotz mehfachem Installieren das Wireguard nicht Funktionierte. Da aber normalerweise Frau Falco mehr den Technischen Part übernimmt, wollten wir das in diesem Modul mal anderst machen und uns abwechseln. Aber leider wurde daraus nichts, da Herr Neuschwander das WireGuard nicht zum laufen gebracht hat. 

## Inhalt :floppy_disk:


#### [Dokumentation erster Container Dienst](Dokumenation/1Container.md "Dokumentation erster Container Dienst")

#### [Dokumentation ergänzender Container Dienst](Dokumenation/2Container.md "Dokumentation ergänzender Container Dienst")

#### [Quellen](Dokumenation/Quellen.md "Quellen")

## Fazit :balloon:
Wir haben am Anfang den Apache-Server ohne Probleme aufsetzen können, allerdings hatten wir beim Datenbankserver ein paar Probleme die leider den Erfolg behindert haben. Allerdings konnetn wir sehr lehrreiche Erfahrungen aus dem Ganzen ziehen. Der Umfang des Projektes war sehr klein, aber die fehlende Erfahrung hat es zu einer echten Herausforderung gemacht. Diese konnten wir dan auch zum Teil schaffen aber eben leider nicht alles. Dennoch konnten wir grosse Fortschritte im umgang mit Docker machen. Alles in Allem ist das gesamte Projekt gut verlaufen.

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/ch/"><img alt="Creative Commons Lizenzvertrag" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/3.0/ch/88x31.png" /></a><br />Dieses Werk ist lizenziert unter einer <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/ch/">Creative Commons Namensnennung - Nicht-kommerziell - Weitergabe unter gleichen Bedingungen 3.0 Schweiz Lizenz</a>
