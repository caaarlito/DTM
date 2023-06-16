# Hotspot Karte

## Datenquelle

Inside Airbnb (http://insideairbnb.com/get-the-data) -> Berlin neighbourhoods.geojson/reviews.csv/listings.csv

## QGIS

1.) Daten einladen

2.) listings 4x duplizieren und jeweils Filtern

entire dpt:
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


