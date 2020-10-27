# Oefenbundel 2

## 1. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet.

**Toon voor elke wedstrijd de spelersnummer, de teamnummer en de vermelding van het resultaat. Het resultaat toont de waarde “Gewonnen” als het aantal gewonnen sets groter is dan het aantal verloren sets is. Het resultaat toont de waarde “Verloren” als het aantal verloren sets groter is dan het aantal gewonnen sets. Eendraw is niet mogelijk in een tenniswedstrijd.Gebruik kolomhoofding “RESULTAAT” voor deze kolom.**

```sql
    SELECT
        `SPELERSNR`,
        `TEAMNR`,
        CASE
            WHEN (`GEWONNEN`>`VERLOREN`) THEN 'Gewonnen'
            ELSE 'Verloren'
        END AS `RESULTAAT`
    FROM
        `wedstrijden`;
```

## 2. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet

**Toon voor elke speler de spelersnummer, het jaar van toetreding en de vermelding tot welke groep de speler behoort.**

**a. Een speler behoort tot de groep ‘Ouderen’ als hij/zij voor 1980 is toegetreden.**
**b. Een speler behoort tot de groep ‘Jongeren’ als hij/zij vanaf 1980 en voor 1983 is toegetreden.**
**c. Een speler behoort tot de groep ‘Kinderen’ als hij/zij vanaf 1983 of later is toegetreden.**

**Gebruik kolomhoofding “GROEP” voor deze kolom.**

```sql
    SELECT
        `SPELERSNR`,
        `JAARTOE`,
        CASE
            WHEN (`JAARTOE`< 1980) THEN 'Ouderen'
            WHEN (JAARTOE >= 1980 AND JAARTOE < 1983) THEN 'Jongeren'
            ELSE 'Kinderen'
        END AS 'GROEP'
    FROM
        `spelers`;
```

## 3. Schrijf de SQL-instructie die in de volgende informatiebehoefte voorziet

**Verfijn oefening 2 zodat de groep ‘Ouderen‘nog verder wordt onderverdeeld in ‘Ouderen wedstrijd’ en ‘Ouderen recreatief’.‘Ouderen wedstrijd’ is van toepassing als de speler een bondsnummer heeft.**

HINT: gebruik IS NULL om te controleren of een bondsnummer ontbreekt.

```sql
SELECT
    `SPELERSNR`,
    `JAARTOE`,
    CASE
        WHEN (`JAARTOE`< 1980) THEN
            CASE
                WHEN (`BONDSNR` IS NULL) THEN 'Ouderen recreatief'
                ELSE 'Ouderen wedstrijd'
            END
        WHEN (`JAARTOE` >= 1980 AND JAARTOE < 1983) THEN 'Jongeren'
        ELSE 'Kinderen'
    END AS `GROEP`
FROM
    `spelers`;
```

- [Terug](../Deel4.md)