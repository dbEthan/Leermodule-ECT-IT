# Oefenbundel 5

## 1. Schrijf de SQL-instructie die een nieuwe database “AP” aanmaakt.

```sql
    CREATE DATABASE `AP`;
```

## 2. Schrijf een SQL-instructie die in de database “AP” een tabel “AFDELING” aanmaakt. De tabel moet aan volgende vereisten voldoen:

![Deel5_Oef2](/Index/Pictures/Deel2_Oefenbundel5_Oef2.PNG)

```sql
    CREATE TABLE `AP`.`AFDELING`
    (
        AFDNR Char(5) PRIMARY KEY,
        BUDGET DECIMAL(8,2)NOT NULL,
        LOCATIE VARCHAR(30),
        ISACTIEF TINYINT UNSIGNED DEFAULT FALSE,
        GEMPUNTEN DECIMAL (4,2)
    );
```

## 3. Een INSERT-instructie zal een nieuwe record toevoegen in een tabel. Onderzoek hoe je een dergelijke instructie moet opstellen en schrijfvervolgens zo’n instructie die een nieuw record invoegt in tabel AFDELING in de database AP. Gebruik volgende waarden:

- AFDNR = 12345
- BUDGET = 2000.25
- LOCATIE= Campus Ellermanstraat
- ISACTIEF = FALSE
- GEMPUNTEN = 12.43

```sql
    INSERT INTO AFDELING VALUES 
    (12345, 2000.25, "Campus Ellermanstraat", FALSE, 12.43);
```

## 4. Controleer of de INSERT-instructie is gelukt met onderstaande instructie

```sql
    SELECT * FROM AP.AFDELING;
```

- [Terug](../Deel2.md)