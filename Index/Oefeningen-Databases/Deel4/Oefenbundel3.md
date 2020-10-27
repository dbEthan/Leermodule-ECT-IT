# Oefenbundel 3

## 1. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon voor elke speler de spelersnummer, de naam en het telefoonnummer. Het telefoonnummer moet naar het formaat omgezet worden zoals in onderstaand voorbeeld met INTTELEFOON als kolomhoofding.**

**Huidig formaat: 070-237893**
**Gewenst formaat: +31(0)70-237893**

**Gebruik de gepaste scalaire functies om dit formaat te bekomen**

```sql
    SELECT
        `SPELERSNR`,
        `NAAM`,
        CONCAT('+31(0)', RIGHT(`TELEFOON`,(LENGT(`TELEFOON`)-1))
        ) AS 'INTELEFOON'
    FROM
        `spelers`;
```

## 2.Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon voor elke speler de spelersnummer en de vermelding “jarig” of “niet jarig”. Voor de vermelding “jarig” of “niet jarig” gebruik je de kolomhoofding “FEEST”.**

**Hint: gebruik functies CURRENT_DATE, MONTH en DAY**

```sql
    SELECT
        `SPELERSNR`,
        CASE
            WHEN
            (
                MONTH(`GEB_DATUM`) = MONTH(CURRENT_DATE())
                AND DAY(`GEB_DATUM`) = DAY(CURRENT_DATE())
            ) THEN 'JARIG'
            ELSE 'NIET JARIG'
        END AS 'FEEST'
    FROM
        `spelers`;
```

- [Terug](../Deel4.md)