# Oefenbundel 4

## 1. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de spelersnummer, naam en straat voor elke spelerdie in een straat woont waarvan de naam eindigt op ‘weg’.**

```sql
SELECT 
    `SPELERSNR`, `NAAM`, `STRAAT`
FROM
    `spelers`
WHERE
    `STRAAT` LIKE '%weg';
```

## 2. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de spelersnummer, naam en straat voor elke speler die in een straat woont waarvan de naam begint met de letter ‘h’en de letter ‘e’ bevat.**

```sql
SELECT 
    `SPELERSNR`, `NAAM`, `STRAAT`
FROM
    `spelers`
WHERE
    `STRAAT` LIKE 'h%e%';
```

## 3. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de spelers nummer en naam voor elke speler waarvan de 2de letter van de naam geen letter ‘i’ is.**

```sql
SELECT 
    `SPELERSNR`, `NAAM`
FROM
    `spelers`
WHERE
    `NAAM` NOT LIKE '_i%';
```

## 4. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de spelersnummer en naam van elke speler waarvan de naam van elke speler op de tweede en de op een na laatste positie de letter ‘e’ bevat.**

```sql
SELECT 
    `SPELERSNR`, `NAAM`
FROM
    `spelers`
WHERE
    `NAAM` LIKE '_e%e_';
```
[Terug](../Deel5.md)