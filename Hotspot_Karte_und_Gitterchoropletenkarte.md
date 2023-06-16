# Hotspot Karte oder Gitterchoropletenkarte

## Datenquelle

Inside Airbnb (http://insideairbnb.com/get-the-data) -> Berlin neighbourhoods.geojson/reviews.csv/listings.csv

## QGIS

1.) Daten einladen

2.) listings 4x duplizieren und jeweils Filtern

entire apt:
```
"room_type" = 'Entire home/apt' AND "price" < 9999
```

private room:
```
"room_type" = 'Private room' AND "price" < 9999
```

shared room:
```
"room_type" = 'Shared room' AND "price" < 9999
```

hotel room:
```
"room_type" = 'Hotel room' AND "price" < 9999
```

3.) Gitter erzeugen und Berlin ausschneiden

![image](https://github.com/caaarlito/DTM/assets/134683878/b50ff1f6-d8a7-4b77-9a81-96e02e781837)

![image](https://github.com/caaarlito/DTM/assets/134683878/926fc6dd-5a75-43e3-9d5c-b9352c1f7a3c)

4.) Attribute nach Position verknüpfen (Beispiel: Durchschnittspreis Hotel)

![image](https://github.com/caaarlito/DTM/assets/134683878/c308a873-f99b-4958-a7c1-28ae58e0dc31)

- bei Zusammenfassende Felder "price" wählen

- bei zu berechnende Zusammenfassungen "Durchschnitt" wählen

- dann die Gitter Symboliseung ändern -> Gitterchopletenkarte fertig

5.) Symbolisierung Heatmap der Punktwolken

![image](https://github.com/caaarlito/DTM/assets/134683878/7e462c03-f74c-43e2-85c5-22bdf93b29b1)

6.) Berlin Umrisse durch Symbolisierung von Neighbourhoods "verschmolzen"

7.) Drucklayout mit mehreren Karten

- erste Karte aufziehen und dann Layer sperren
- Karte kopieren, in QGIS die Heatmap ändern und im Drucklayout aktualisieren, danach wieder Layer sperren
- für Schrift mit Farbverlauf -> Rechteck mit Graduientenfüllung drüber legen und bei Darstellung Mischmodus = Multiplizieren

![image](https://github.com/caaarlito/DTM/assets/134683878/8ebd789c-4879-4467-be3f-79a73e96ec56)

