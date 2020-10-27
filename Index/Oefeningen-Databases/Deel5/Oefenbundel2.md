# Oefenbundel 2

## 1. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de betalingsnummer en het bedrag van elke boete waarvan het bedrag € 50, € 75 of € 100.Gebruik de IN operator.**

```sql
SELECT 
    `BETALINGSNR`, `BEDRAG`
FROM
    `boetes`
WHERE
    `BEDRAG` IN (50 , 75, 100);
```

## 2. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon alle gegevens van de wedstrijden die niet door de spelers met spelersnummer 8, 27 en 112 gespeeld zijn.**

```sql
SELECT 
    *
FROM
    `wedstrijden`
WHERE
    `SPELERSNR` NOT IN (8 , 27, 112);
```

## 3. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de spelersnummer,naamen straatvan elke speler waarvan de eerste letter van de straat eene, l of s is.**

```sql
SELECT 
    `SPELERSNR`, `NAAM`, `STRAAT`
FROM
    `spelers`
WHERE
    LEFT(`STRAAT`, 1) IN ('e' , 'l', 's');
```

## 4. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon voor elke speler de spelersnummer, het jaar van toetreding, de geboortedatum, het aantal jaren dat een speler lid isen de opdeling in duurtijd als lid.De opdeling gebeurt als volgt:**
    
**a. Een speler behoort tot de groep ‘35+’ als hij/zij minstens 35 jaar lid is**
**b. Een speler behoort tot de groep ‘40+’ als hij/zijminstens 40 jaar lid is**
**c. Een speler behoort tot de groep ‘45+’ als hij/zij minstens 45 jaar lid is.**

**Gebruik kolomhoofdingen “Aantaljaren” en “Duurtijd” voor deze kolommen. Je toont deze info enkel voor de spelers die geboren zijn in 1956, 1963 of 1970.**

```sql
SELECT 
    `SPELERSNR`,
    `JAARTOE`,
    `GEB_DATUM`,
    (YEAR(CURRENT_DATE()) - `JAARTOE`) AS 'Aantal jaren',
    CASE
        WHEN (YEAR(CURRENT_DATE()) - `JAARTOE`) > '45' THEN '45+'
        WHEN (YEAR(CURRENT_DATE()) - `JAARTOE`) > '40' THEN '40+'
        WHEN (YEAR(CURRENT_DATE()) - `JAARTOE`) > '35' THEN '35+'
        ELSE ''
    END AS 'Duurtijd'
FROM
    `spelers`
WHERE
    YEAR(`GEB_DATUM`) IN (1956 , 1963, 1970);
```

[Terug](../Deel5.md)