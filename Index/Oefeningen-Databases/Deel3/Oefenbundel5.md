# Oefenbundel 5

## 1. Om de oefeningen in deze bundel te maken werken we verder met de database “Tennis3”.

## 2. Schrijf de SQL-instructie die ervoor zorgt dat alle records uit tabel “BESTUURSLEDEN” worden verwijderd.

```sql
    DELETE FROM `BESTUURSLEDEN`;
```

## 3.Schijf de SQL-instructie die ervoor zorgt dat de boetes van speler 7 worden verwijderd.

Onderzoek hiervoor (indien nodig) hoe je een eenvoudige filterconditie kan samenstellen met behulp van internet!

```sql
    DELETE FROM `BOETES`
    WHERE
        `SPELERSNR` = 7;
```

- [Terug](../Deel3.md)
