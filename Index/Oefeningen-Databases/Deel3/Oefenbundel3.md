# Oefenbundel 3

## 1. Om de oefeningen in deze bundel te maken gaan we een duplicaat maken van de database “Tennis”.

a. Kopieer de inhoud van het SQL-script vande database “Tennis”.
b. Plak de inhoud in een leeg query editor venster.
c. Wijzig de naam “Tennis” in “Tennis3”.
d. Voer het SQL-script uit om het duplicaat aan te maken.

Gebruik deze database “Tennis3” bij de resterende oefenbundels van deze les.

## 2. Schrijf de SQL-instructie die ervoor zorgt dat een nieuw record wordt toegevoegd aan tabel “Boetes”.Het betalingsnummer van de boete is 15, de spelernr is 27, de betaaldatum 8 augustus 2020 en het boetebedrag €75.

```sql
    USE `tennis3`;

    INSERT INTO `BOETES` VALUES (15.27,'2020-08-08',75); 
```

## 3. Er werden 3 nieuwe boetes geregistreerd:

a. De 1ste is voor spelernr 7 en heeft 16 als betalingsnr. Het bedrag van de boete is €50 en werd betaald op 12 augustus 2020.
b. De 2de is voor spelernr 44 en heeft 18 als betalingsnr. Het bedrag van de boete is €60en werd betaald op 21 augustus 2020.
c. De laatste boete is opnieuw voor spelernr 7 en heeft 19 als betalingsnr. Het bedrag van de boete is €100 en werd betaald op 10 september 2020.

Schrijf de SQL-instructie die met één INSERT-instructie deze 3 boetes toevoegt.

```sql
    INSERT  INTO `BOETES` VALUES
    (16,7,'2020-08-12',50) 
    (18,44,'2020-08-21',60)
    (19,7,'2020-09-10',100)
```

- [Terug](../Deel3.md)