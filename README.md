# Heatview

Dieses Projekt visualisiert Rad-Unfälle und im Kontext dieser relevante Zusatzinformation, soweit diese als offene Daten bereitgestellt werden.

Es baut auf dem Datenvisualisierungs-Werkzeug kepler.gl der Firma Uber auf und nutzt derzeit die folgenden Datensätze:

* Daten des [Unfallatlas](https://qri.cloud/mfdz/destatis_unfalldaten) von destatis, unter de-dl/by-2-0, © Statistische Ämter des Bundes und der Länder
* [Geschwindigkeiten der Radfahrenden (2020)](https://www.mcloud.de/web/guest/suche/-/results/detail/33427A5A-0ADB-40B1-8A1A-390B67B0380B), erhoben im Rahmen des Stadtradeln Projekts, aufbereitet und bereitgestellt durch das MOVEBIS-Projekt, unter CC-BY-NC, © Grubitzsch P., Lißner S., Huber S., Springer T., [2021] Technische Universität Dresden, Professur für Rechnernetze und Professur für Verkehrsökologie. Die Daten haben wir für jede deutschen Kreis in eine eigenständige Datei extrahiert, abrufbar von z.B. https://data.mfdz.de/movebis/geschwindigkeiten_2020/geschwindigkeiten_2020_08111.csv wobei 08111 durch den jeweiligen 5-stelligen AGS ersetzt werden muss.

Aktuell erfolgt die Darstellung je Stadt- bzw. Landkreis. Zur Auswahl eines Kreises ist dessen fünfstelliger "Amtliche Gemeindeschlüssel (AGS)" als URL-Parameter anzugeben, z.B.

https://heatview.de/?kreis=08111






