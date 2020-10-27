# Oefenbundel 4

## 1. Om de oefeningen in deze bundel te maken werken we verder met de database “Tennis3”.

## 2. Schrijf de SQL-instructie die ervoor zorgt dat het bedrag van elke boete verhoogdwordt met 5%.

```sql
    UPDATE `BOETES` SET
    `BEDRAG` = `BEDRAG` * 1.05;
```

## 3. Schijf de SQL-instructie die ervoor zorgt dat het bedrag van de boetes uit het jaar 2020 aangepast wordt naar €120.

Onderzoek hiervoor hoe je een eenvoudige filterconditie kan samenstellen met behulp van internet

```sql
    UPDATE `BOETES` SET
        `BEDRAG` = 120
    WHERE
        YEAR(`DATUM`) = 2020;
```

- [Terug](../Deel3.md)