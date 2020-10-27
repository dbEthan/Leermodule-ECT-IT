# Oefenbundel 5

## 1. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de volledige inhoud van tabel “tblconsoles”. Bouw je instructie op de meest efficiënte manier op!**

```sql
    SELECT
        *
    FROM
        `tblconsoles`;
```

## 2. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**oon de namen van alle uitgeverijen. Vervang hierbij eventuele spaties in de naam door een underscore. Gebruik kolomhoofding “Uitgever” voor deze kolom.**

```sql
    SELECT
        REPLACE(`naam`,' ','_') AS 'Uitgever'
    FROM
        `tbluitgevers`;
```

## 3.Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de namen van alle game definities in kleine letters.**

```sql
    SELECT
        LCASE(`naam`) AS `Uitgever`
    FROM
        `tblgamedefinitions`;
```

## 4. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de namen van alle game definities in kleine letters. Vervang hierbij streepjes en/of spaties in de naam door een underscore. Gebruik kolomhoofding"Game"voor deze kolom.**

```sql
    SELECT
        REPLACE
        (
            REPLACE(LOWER(`naam`),'-','_')
            ' ','_'
        ) AS `Game`
    FROM
        `tblgamedefinitions`;
```

## 5. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de namen en releasedatums  van alle consoles. Maak daarbij de releasedatums op in het formaat “MM-DD-YYYY”.Gebruik kolomhoofding “Releasedatum” voor deze kolom.**

Zonder leftpadding (voorloopkarakters toevoegen):

```sql
    SELECT
        `naam`,
        CONCAT
        (
            MONTH(`releasedatum`),'-',
            DAY(`releasedatum`),'-',
            YEAR(`releasedatum`)
        ) AS `Releasedatum`
    FROM
        `tblgamedefinitions`;
```

Met leftpadding:

```sql
    SELECT
        `naam`,
        CONCAT
        (
            LPAD(MONTH(`releasedatum`),2,'0'),'-',
            LPAD(DAY(`releasedatum`),2,'0'),'-',
            YEAR(`releasedatum`)
        ) AS `Releasedatum`
    FROM
        `tblgamedefinitions`;
```

## 6. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de namenen hun lengte van alle game definities. Gebruik kolomhoofding “lengte” voor de kolom waarin de lengte getoond wordt.**

```sql
    SELECT
        `naam`,
        LENGTH(`naam`) AS `lengte`
    FROM
        `tblgamedefinitions`;
```

## 7. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de hoogste prijs van een game. Gebruik kolomhoofding “Hoogste_prijs” voor deze kolom.**

```sql
    SELECT
        MAX(`price`) AS 'Hoogste_prijs'
    FROM
        `tblgames`;
```

## 8.Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon de totaalwaarde van alle games die verkocht worden. Gebruik kolomhoofding “max_omzet” voor deze kolom.**

```sql
    SELECT
        SUM(`price`) AS `max_omzet`
    FROM
        `tblgames`;
```

## 9. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon alle kolommen van tabel “tblgames”. Je vervangt hierbij de waarde die refereert naar “New game” door “Nieuw”, de waarde die refereert naar “USED game” door “Occasie” voor kolom “gametypeid”. Gebruik kolomhoofding “gametype” voor deze kolom.**

```sql
    SELECT
        `gamedefinitionsid`,
        `consoleid`,
        CASE `gametypeid`
            WHEN 1 THEN 'Nieuw'
            WHEN 2 THEN 'Occassie'
        END AS 'Gametype'
        `price`,
        'btw_percentage'
    FROM
        `tblgames`;

```

## 10. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon alle game definitiesin het formaat dat gebruikt wordt bij .csv-bestanden.Je plakt dus voor elke rij alle waarden aan elkaar. De waarden worden gescheiden door het karakter “;”.Gebruik kolomhoofding “csv” voor deze kolom.**

```sql
    SELECT
        CONCAT
        (
            `id`,';',
            'naam',';',
            `uitgever`,';',
            `releasedatum`,';'
        ) AS 'csv'
    FROM
        'tblgamedefinitions'
```

- [Terug](../Deel4.md)