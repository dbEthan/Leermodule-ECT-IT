# Oefenbundel 1

## 1. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon debetalingsnummer en het boetebedragvan de boetes waarvan het boetebedrag hoger is dan € 60.**

```sql
SELECT 
    `BETALINGSNR`, `BEDRAG`
FROM
    `boetes`
WHERE
    `BEDRAG` > 60;
```
## 2. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de spelers nummer, het aantal gewonnen sets, het aantal verloren sets en de som van beiden voor de wedstrijden waarvan deze som 5 bedraagt. Zorg ervoor dat de kolomnaam van deze bewerking AANTAL_SETS is.**

```sql
SELECT 
    `SPELERSNR`,
    `GEWONNEN`,
    `VERLOREN`,
    (`GEWONNEN` + `VERLOREN`) AS 'AANTAL_SETS'
FROM
    `wedstrijden`
WHERE
    (`GEWONNEN` + `VERLOREN`) = '5';
```

## 3. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de naam en plaats van de spelers die in Den Haag of in Rijswijk wonen.**

```sql
SELECT 
    `NAAM`, `PLAATS`
FROM
    `spelers`
WHERE
    `PLAATS` = 'Den Haag'
        OR `PLAATS` = 'Rijswijk';
```

## 4. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de naam, geslachten plaats van de vrouwelijke spelers die in Zoetermeerwonen.**

```sql
SELECT 
    `NAAM`, `GESLACHT`, `PLAATS`
FROM
    `spelers`
WHERE
    `GESLACHT` = 'V'
        AND `PLAATS` = 'Zoetermeer';
```

## 5. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon alle informatie van:**
    **a. De boetes uitgedeeld aan de speler met nummer 44 in het jaar 1980**
    **b. De boetes die niet uitgedeeld werden in december.**

```sql
SELECT 
    *
FROM
    `boetes`
WHERE
    ((`SPELERSNR` = 44)
        AND (YEAR(`DATUM`) = '1980'))
        OR MONTH(`DATUM`) <> '12';
```

## 6. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de spelers nummer, naam, plaats en straat van de spelers die in een straat wonenwaarvan de naam begint met een s. De speler mag daarbovenop niet in Den Haag wonen.**

```sql
SELECT 
    `SPELERSNR`, `NAAM`, `PLAATS`, `STRAAT`
FROM
    `spelers`
WHERE
    LEFT(`STRAAT`, 1) = 's'
        AND (`PLAATS` <> 'Den Haag');
```

## 7. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de spelersnummer, naamen jaar van toetreding voor de spelers die vanaf 1982 zijn toegetreden.**

```sql
SELECT 
    `SPELERSNR`, `NAAM`, `JAARTOE`
FROM
    `spelers`
WHERE
    `JAARTOE` = '1982'; 
```

## 8. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de spelersnummer, naam en plaat van elke vrouwelijke speler die niet in Den Haag woonachtig is.**

```sql
SELECT 
    `SPELERSNR`, `NAAM`, `PLAATS`
FROM
    `spelers`
WHERE
    `GESLACHT` = 'v'
        AND `PLAATS` <> 'Den Haag';
```
[Terug](../Deel5.md)
