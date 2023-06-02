# Bivariate Choropletenkarte in QGIS

## Datenquelle

World Happiness Report (https://www.kaggle.com/datasets/ajaypalsinghlo/world-happiness-report-2023)

World Countries Esri (https://hub.arcgis.com/datasets/2b93b06dc0dc4e809d3c8db5cb96ba69/explore)

Daten verknüpen:

![image](https://github.com/caaarlito/DTM/assets/134683878/b3760723-a272-4706-87b6-59231abd654b)

## QGIS

1.) Layer duplizieren

2.) Eines der beiden Layer ausdünnen, um nur Länder mit vorhandenen Daten anzuzeigen.

Rechtsklick -> Filter
```
"Ladder sco" IS NOT NULL
```

3.) Symbolisierung Abgestuft nach "Logged GDP" beim gefilterten Layer

Im Beispiel 3 Klassen:

![image](https://github.com/caaarlito/DTM/assets/134683878/e6a8773a-a1cc-4088-8ad1-fbafec95b9e0)

4.) Duplikat erzeugen -> Symbolisierung Abgestuft nach "Freedom to make Life Choices" mit einem komplimentären Farbverlauf

Im Beispiel 3 Klassen:

![image](https://github.com/caaarlito/DTM/assets/134683878/cc49b70e-4d5e-472b-81ba-83d583f23fef)

5.) Im GDP Field Calculator neue Felder anlegen

"BIP_red" als int:
```
CASE 
WHEN  "Logged GDP" > 10.2 THEN 3
WHEN  "Logged GDP" > 9.1 THEN 2
ELSE 1 
END
```

"F_red" als string: 
```
CASE
WHEN  "Freedom to" > 0.852 THEN 'C'
WHEN  "Freedom to" > 0.76 THEN 'B'
ELSE 'A'
END
```

"GDP_F" als string:
```
"BIP_red" || "F_red"
```

6.) Den Klassen Farben zuweisen

mit einem Color Picker aus einem 4x4 Farbfeld die Farbcodes kopieren:

![image](https://github.com/caaarlito/DTM/assets/134683878/1a03f13a-9fd2-4641-895d-efbf7330f6fe)

zum Beispiel mit Photoshop den Hex-Code kopieren:

![image](https://github.com/caaarlito/DTM/assets/134683878/8e7522d6-cfbc-411c-996a-5d4ce152fac5)

GDP Symbolisierung auf Kategorisiert nach "GDP_F" setzen und Farben übertragen:

![image](https://github.com/caaarlito/DTM/assets/134683878/73f2d3c4-505f-4bc0-bcfc-0009703e270a)

## Ergebnis

![image](https://github.com/caaarlito/DTM/assets/134683878/f074e7b9-020e-466a-9e43-36713dfce95e)

