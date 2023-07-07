# Netzlayer - Klimadaten

## Datenquelle

bboxfinder(http://bboxfinder.com/)

Copernicus(https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels?tab=form)

Wind + Niederschlag Mai 2023, alle Uhrzeiten, Deutschland

## QGIS

1.) Welche Daten angezeigt werden, kann man über diese Felder ändern

![image](https://github.com/caaarlito/DTM/assets/134683878/e2ddb52e-ffeb-46c7-bf53-c890e9ceece3)

2.) mit dem Pfeil rechts neben den Winddaten lässt sich die Windrichtung in Pfeilen/Stromlinien/Spuren anzeigen

3.) Zeitsteuerung ist möglich

Beschriftung über temporären Layer mit Label:
```
'Luftbewegung im Mai 2023' || '\n' || format_date(@map_start_time, 'dd MMMM yyyy') || '\n' || format_date(@map_start_time, 'HH:mm') || ' Uhr'
```

4.) Transparenz richtig einstellen, um Niederschlag oder Temperatur über Karte anzeigen zu können

5.) unter dem Tab "Netz" -> "Netzrechner" lassen sich die Daten wie mit dem Feldrechner verrechnen

z.B. die Durchschnittstemperatur für den Monat
![0000](https://github.com/caaarlito/DTM/assets/134683878/040486dd-6b70-45a4-89fe-ffd961eaa991)



