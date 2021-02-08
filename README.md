# Heatview

Dieses Projekt visualisiert Rad-Unfälle und im Kontext dieser relevante Zusatzinformation, soweit diese als offene Daten bereitgestellt werden.

![Heatview Visualisierung Unfallorte](https://raw.githubusercontent.com/mfdz/heatview-website/main/site/img/card.png)

Es baut auf dem Datenvisualisierungs-Werkzeug kepler.gl der Firma Uber auf und nutzt derzeit die folgenden Datensätze:

* Daten des [Unfallatlas](https://qri.cloud/mfdz/destatis_unfalldaten) von destatis, unter de-dl/by-2-0, © Statistische Ämter des Bundes und der Länder. Details siehe unten.
* [Geschwindigkeiten der Radfahrenden (2020)](https://www.mcloud.de/web/guest/suche/-/results/detail/33427A5A-0ADB-40B1-8A1A-390B67B0380B), erhoben im Rahmen des STADTRADELN Projekts, aufbereitet und bereitgestellt durch das MOVEBIS-Projekt, unter CC-BY-NC, © Grubitzsch P., Lißner S., Huber S., Springer T., [2021] Technische Universität Dresden, Professur für Rechnernetze und Professur für Verkehrsökologie. Die Daten haben wir für jede deutschen Kreis in eine eigenständige Datei extrahiert, abrufbar von z.B. https://data.mfdz.de/movebis/geschwindigkeiten_2020/geschwindigkeiten_2020_08111.csv wobei 08111 durch den jeweiligen 5-stelligen AGS ersetzt werden muss.

Aktuell erfolgt die Darstellung je Stadt- bzw. Landkreis. Zur Auswahl eines Kreises ist dessen fünfstelliger "Amtliche Gemeindeschlüssel (AGS)" als URL-Parameter anzugeben, z.B.

https://heatview.de/?kreis=08111

## Datensätze

### Destatis Unfallatlas
Seit 2016 veröffentlichen die statistischen Ämter des Bundes und der Länder die Daten des Unfallatlas als OpenData. Wir haben die jahresweise veröffentlichten Daten in einer CSV-Datei zusammengeführt und über [qri.cloud]((https://qri.cloud/mfdz/destatis_unfalldaten)) veröffentlicht.
Bei der Interpretation der Daten sind einige Punkte zu beachten, damit keine falschen Schlüsse gezogen werden:

* Die Daten des Unfallatlas umfassen die Jahre 2016-2019. Daten des Vorjahres werden üblicherweise im Sommer veröffentlicht. Nicht für alle Bundesländer liegen Daten bereits ab 2016 vor. Für manche Bundesländer liegen Unfalldaten erst ab späteren Jahren als 2016 vor. Mecklenburg-Vorpommern fehlt bisher noch vollständig.
* Anzahl Unfälle statt Zahlen zu Unfallopfern. Der Unfallatlas ordnet jedem Unfall eine Kategorie zu (1 = Unfall mit (mindestens einem/einer) Getöteten, 2 = Unfall mit (mindestens einem/einer) Schwerverletzten, 3 = Unfall mit (mindestens einem/einer) Leichtverletzten
* Plausibilisierung: Im Destatis-Unfallatlas werden nur diejenigen Unfälle veröffentlicht, deren Örtlichkeit (Geokoordinate) nahe genug an einer Straße im offiziellen Straßennetz-Datenbestand (Digitales Landschaftsmodell) lag und bezüglich der Straßenbezeichung stimmig zugeordnet werden konnte. Aus diesem Grund fehlen örtlich zwischen 3 und 7% der Unfälle in den Statistiken. Betroffen sind hiervon z.B. häufig Unfälle in Park-Anlagen oder Waldgebieten.

Um die Daten je Land-/Stadtkreis anzuzeigenm, haben wir die Daten zudem kreisweise aufgeteilt und unter Verwendung des Allgemeinen Gemeindeschlüssels auf [data.mfdz.de](https://data.mfdz.de/) zum Abruf bereitgestellt. Der Link lautet z.B. für den Stadtkreis Stuttgart (AGS=08111): https://data.mfdz.de/destatis/unfallatlas/unfalldaten_08111.csv

### Geschwindigkeiten d. Radfahrenden (2020)
Im Rahmen des mFund-geförderten [MOVEBIS](https://www.movebis.org)-Projekts wurden die während der STADTRADELN-Aktionen 2018-2020 gesammelten Datensätze durch die Projekt-Partner TU Chemnitz, dem Klima-Bündnis, und cyface EASY RIDING aufbereitet und auf dem mcloud-Datenportal unter CC-BY-NC Lizenz veröffentlicht.

Auch diese Daten haben wir für jede deutschen Kreis in eine eigenständige Datei extrahiert, abrufbar von z.B. https://data.mfdz.de/movebis/geschwindigkeiten_2020/geschwindigkeiten_2020_08111.csv wobei 08111 durch den jeweiligen 5-stelligen AGS ersetzt werden muss.

Zu beachten ist, dass diese Daten nur die Daten der Teilnehmenden an den STADTRADELN-Aktionen umfasst, und nicht als das gesamthafte Radverkehrsaufkommen angenommen werden kann. Auch kann die Zuordnung von Messpunkten zu Straßenabschnitten kann lokal von der tatsächlich gewählten Route abweichen (z.B. bei für den Radverkehr freigegebenen Gehwegen und den parallel verlaufenden Straßen).

## Dank und weitere Hinweise
Wir danken Destatis und dem MOVEBIS-Projekt für die Veröffentlichung der Daten, der Firma Uber für die Veröffentlichung von kepler.gl unter MIT-Lizenz.

Kommunen, die weitergehende Analysen und Auswertungen zur Planung und Verbesserung Ihrer Fahrradinfrastruktur durchführen möchten, empfehlen wir die Kontaktaufnahme mit dem [MOVEBIS-Projekt](https://www.movebis.org/news/).







