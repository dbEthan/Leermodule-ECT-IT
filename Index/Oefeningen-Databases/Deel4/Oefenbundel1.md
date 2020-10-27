# Oefenbundel 1

## 1. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon voor elke boete het betalingsnummer en het boete bedrag.**

```sql
    SELECT
        `BETALINGSNR`,
        `BEDRAG`
    FROM
        `BOETES`;
```

## 2. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon voor elke wedstrijd de spelersnummer, de teamnummer en het verschil tussen de gewonnen-en verloren sets.**

```sql
    SELECT
        `SPELERSNR`,
        `TEAMNR`,
        (`GEWONNEN`-`VERLOREN`)
    FROM
        `wedstrijden`;
```

## 3. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon voor elke wedstrijd despelersnummer, de teamnummer en het verschil tussen de gewonnen-en verloren sets. Zorg ervoor dat de kolomnaam van deze bewerking RESULTAAT is.**

```sql
    SELECT
        `SPELERSNR`,
        `TEAMNR`,
        `GEWONNEN`-`VERLOREN` AS `RESULTAAT`
    FROM
        `wedstrijden`;
```

- [Terug](../Deel4.md)