# Meteors

## Datenquelle

MeteorMap 12-08-2022 (https://tammojan.github.io/meteormap/)
![image](https://github.com/caaarlito/DTM/assets/134683878/f268cb99-9169-48fd-8933-ec9f36c9e9ee)

## QGIS

1.) Daten einladen + dunkle Hintergrundkarte (z.B. Dark Matters [no labels])

2.) Symbolisierung

![image](https://github.com/caaarlito/DTM/assets/134683878/5c53d133-e3a8-4284-90dd-c45b5de6548e)

![image](https://github.com/caaarlito/DTM/assets/134683878/d0f0a3a6-1a41-4a1d-9e39-c65f5a4988ee)

3.) Monatsdaten einladen und Stil kopieren

4.) Zeitsteuerung aktivieren

![image](https://github.com/caaarlito/DTM/assets/134683878/ef7aafd1-6164-4979-bfed-9f0f71471fc7)

![image](https://github.com/caaarlito/DTM/assets/134683878/7d305b18-6167-4b68-b449-4e5aa20751da)

![image](https://github.com/caaarlito/DTM/assets/134683878/4bbb7905-b6d1-4b54-92b3-e737df04edc2)

5.) Neuen Layer fürs Datum anlegen

![image](https://github.com/caaarlito/DTM/assets/134683878/c0f7bbf5-f7ff-49a8-8a2d-ae3a9e2f7a3a)

Punkt hinzufügen, wo Beschriftung sein soll:

![image](https://github.com/caaarlito/DTM/assets/134683878/28a3d0f6-8a36-4d89-b925-4a4a4f24ae4c)

unter Labels, Einzelne Beschriftung, beim Ausdrucksdialog (E) Werte festlegen:
```
'Sternschnuppen' || '\n' || format_date(@map_start_time, 'dd MMMM yyyy')
```

unter Symbolisierung Symbol entfernen:

![image](https://github.com/caaarlito/DTM/assets/134683878/a82e6dbc-2678-4800-a5f2-b22f5fce3c5b)

Zeitsteuerung auf Layer anwenden:

![image](https://github.com/caaarlito/DTM/assets/134683878/247c46b8-4534-43a2-b21b-6710de437a93)

6.) Unter Ansicht -> Dekoration Urheberechtshinweis hinzufügen

7.) Animation exportieren

![image](https://github.com/caaarlito/DTM/assets/134683878/3f5e6f50-6a4b-4836-949f-c4a984cf26e3)

8.) In Photoshop laden und mit Leitfaden in Animation umwandeln

https://helpx.adobe.com/de/photoshop/how-to/make-animated-gif.html

