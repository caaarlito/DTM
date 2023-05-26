# Value By Alpha Maps in QGIS

## Datenquelle (Wahlgeometrien & Wahlergebnisse)
(Bundestagswahl 2021)(https://www.bundeswahlleiterin.de/bundestagswahlen/2021/ergebnisse/opendata.html)

Tabelle (kerg1.csv) mit Wahlergebnissen bereinigen
![image](https://github.com/caaarlito/DTM/assets/134683878/97bd9975-2694-431f-b1f5-7431c5072b37)

## QGIS

1.) Vergleich SPD vs. CDU: Stimmenstärkere Partei regelbasiert darstellen

Regel SPD
```
 "SPD" >  "CDU" 
```
Regel CDU
```
 "CDU" >  "SPD" 
```

2.) Ebene "Alpha" ergänzen und auf Symbolebene 1 setzen

![image](https://github.com/caaarlito/DTM/assets/134683878/55eab9cf-8234-43d4-b665-21e6abf32295)

3.) Regel für Ebene "Alpha": über "Einfache Füllung unter "Füllfarbe" > "Datendefinierte Übersteuerung" 

![image](https://github.com/caaarlito/DTM/assets/134683878/31171d85-4707-4c09-a802-61259e9a0c0e)

Grundprinzip:
```
set_color_part(
'black', 
'alpha',
126
)
```

Statt einem festen Alpha-Wert, wird dieser wertebasiert aus einem anderen Attribut für jede Bezugseinheit berechnet
```
set_color_part(
'black', 
'alpha',
scale_linear(
 "G",
 100000, 200000,
 230, 0)
)
```
