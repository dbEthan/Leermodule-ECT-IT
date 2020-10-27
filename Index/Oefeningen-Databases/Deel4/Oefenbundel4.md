# Oefenbundel 4

## 1.Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Bereken van alle wedstrijden het maximale verschil tussen gewonnen en verloren sets en toon dit. Gebruik kolomhoofding “Maximaal” voor deze kolom.**

```sql
    SELECT
        MAX(`GEWONNEN`-`VERLOREN`) AS Maximaal
    FROM
        wedstrijden;
```

## 2. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Bereken het totaal aantal gespeelde wedstrijden en toon dit.Gebruik kolomhoofding “Aantal” voor deze kolom.**

```sql
    SELECT
        COUNT(*) AS Aantal
    FROM
        wedstrijden;
```

- [Terug](../Deel4.md)