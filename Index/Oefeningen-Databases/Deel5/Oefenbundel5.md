# Oefenbundel 5

## 1. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon het spelersnummer van elke speler die geen bondsnummer heeft.**

```sql
SELECT 
    `SPELERSNR`
FROM
    `spelers`
WHERE
    `BONDSNR` IS NULL;
```

## 2. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon het totaal aantal rijen in tabel estuursleden waarvoor een einddatum is ingevuld. Gebruik kolomhoofding “Actievebestuursleden” voor deze kolom.**

```sql
SELECT 
    COUNT(SPELERSNR) AS 'Actieve bestuursleden'
FROM
    `bestuursleden`
WHERE
    `EIND_DATUM` IS NOT NULL;
```

[Terug](../Deel5.md)