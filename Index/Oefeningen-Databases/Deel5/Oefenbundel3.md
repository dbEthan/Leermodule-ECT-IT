# Oefenbundel 3

## 1. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de betalingsnummer van elke boete die tussen € 50 en € 100 ligt.**

```sql
SELECT 
    `BETALINGSNR`
FROM
    `boetes`
WHERE
    `BEDRAG` BETWEEN '50' AND '100';
```

## 2. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de betalingsnummer van elke boete die niet tussen € 50 en € 100 ligt.**

```sql
SELECT 
    `BETALINGSNR`
FROM
    `boetes`
WHERE
    `BEDRAG` NOT BETWEEN '50' AND '100';
```

## 3. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon alle informatie van de wedstrijden vanaf wedstrijdnummer 5 tot en met 10 die niet door spelers met spelersnummer 8 en 27 werden gespeeld.**

```sql
SELECT 
    *
FROM
    `wedstrijden`
WHERE
    `WEDSTRIJDNR` BETWEEN '5' AND '10'
        AND `SPELERSNR` NOT BETWEEN '8' AND '27';
```

[Terug](../Deel5.md)