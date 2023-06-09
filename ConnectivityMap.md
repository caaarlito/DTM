# Connectivity Maps / Ursprungs-Ziel-Karte

## Datenquelle

UNHCR: https://www.unhcr.org/refugee-statistics/download/?url=MZhA2i

Natural Earth: https://www.naturalearthdata.com/downloads/110m-cultural-vectors/

## QGIS

1.) Daten als getrennte Textdatei einladen (im Beispiel 14 Kopfzeilen überspringen) und mit Landpolygonen joinen

![image](https://github.com/caaarlito/DTM/assets/134683878/211d688c-f812-4db4-8141-20b6bc8a80a1)

2.) Zentroide der gejointen Polygone erstellen

![image](https://github.com/caaarlito/DTM/assets/134683878/8da8ba93-4e7e-40b9-a9a4-68cdc4898988)

3.) Zentroide mit Ausdruck wählen, dann Auswahl umkehren und restliche löschen -> Export

```
"Refugees under UNHCR's mandate"  > 0
```

4.) wenn nötig Zentroide per Hand an bessere Position verschieben

![image](https://github.com/caaarlito/DTM/assets/134683878/09ca9b64-c28f-42d3-9e1e-01924d89018c)

5.) Neue Felder anlegen

x_dest *real*:
```
$x 
```

y_dest *real*:
```
$y
```

6.) Ukraine Zentroid wählen und dann als gewähltes Objekt exportieren, ebenfalls x- und y-Koordinatenfeld anlegen

x_dest *real*:
```
$x 
```

y_dest *real*:
```
$y
```

7.) bei den Länderpolygonen neue Felder anlegen:

x_origin *real*:
```
Koordinaten vom Ukraine Zentroid übertragen -> 31.229
```

y_origin *real*:
```
Koordinaten vom Ukraine Zentroid übertragen -> 49.149
```

8.) "Shape Tools" Plugin installieren

![image](https://github.com/caaarlito/DTM/assets/134683878/32871be6-c50c-4216-b10d-0aca9a6f8caa)

9.) Unter Vektor, Shape Tools das "XY to line" Tool verwenden

![image](https://github.com/caaarlito/DTM/assets/134683878/91d41773-c0a7-4132-bf0d-4787d6338abd)

10.) Neue Projektion auswählen -> Einstellungen, Benutzerprojektionen

![image](https://github.com/caaarlito/DTM/assets/134683878/8dd0a5dd-8108-4bb7-9e43-e94a71e78fde)

Parameter:
```
+proj=ortho +lat_0=49.1 +lon_0=31.2 +x_0=0 +y_0=0 +a=6371000 +b=6371000 +units=m +no_defs
```

11.) Ukraine Zentroid exportieren mit eigenem Koordinatensystem, dann Symbolisierung anpassen

![image](https://github.com/caaarlito/DTM/assets/134683878/67010633-02d4-464b-99c0-d607f1279554)

```
buffer(make_point(0,0),6350000,20)
```

12.) Symbolisierung

Ukraine Zentroid:

![image](https://github.com/caaarlito/DTM/assets/134683878/4acbf4c2-fda4-4ba1-af34-14a58c4da13e)

Effekteigenschaften:

![image](https://github.com/caaarlito/DTM/assets/134683878/b2505ef3-74ed-4c7f-8f60-6f8681ee9857)

Länder:

![image](https://github.com/caaarlito/DTM/assets/134683878/81ac205d-c442-4839-8325-f6098b039480)

Linien:

![image](https://github.com/caaarlito/DTM/assets/134683878/ab787992-b1a3-4925-9f18-0593a8fbdcb1)

Punkte:

![image](https://github.com/caaarlito/DTM/assets/134683878/c82a2a65-f88a-4767-a554-ca20ba2bb54e)

