# Oefenbundel 2

## 1. Om de oefeningen in deze bundel te maken gaan we een duplicaat maken van de database “Tennis”.
a. Kopieer de inhoud van het SQL-script van de database “Tennis”.
b. Plak de inhoud in een leeg query editor venster.
c. Wijzig de naam “Tennis” in “Tennis2”.
d. Voer het SQL-script uit om het duplicaat aan te maken.

Gebruik deze database “Tennis2” bij de volgende oefeningen in deze oefenbundel.

## 2. Schrijf de SQL-instructies die ervoor zorgen dat alle tabellen in de database “Tennis2” de prefix “tbl” krijgen

```sql
    USE `tennis2`
    RENAME TABLE `bestuursleden` TO `tblBestuursleden`;
    RENAME TABLE `boetes` TO `tblBoetes`;
    RENAME TABLE `spelers` To `tblSpelers`;
    RENAME TABLE `teams` TO `tblSpelers`;
    RENAME TABLE `wedstrijden` TO `tblWedstijden`;
```

## 3. Schrijf de SQL-instructie die in tabel “tblBoetes” een kolom “REDEN” toevoegt. Deze kolom heeft als datatype VARCHAR(255).

```sql
    ALTER TABLE `tblBoetes` ADD
    (
        `REDEN` VARCHAR(255)
    );
```

## 4. Schrijf de SQL-instructie die in tabel “tblSpelers” een kolom “VOORNAAM” toevoegt. Deze kolom heeft als datatype VARCHAR(50).

```sql
    ALTER TABLE `tblSpelers` ADD
    (
        `VOORNAAM` VARCHAR(50)
    );
```

## 5. Schrijf de SQL-instructie die in tabel “tblBoetes” een kolom “PAYMENTDATE” toevoegt. Je gebruikt hiervoor het datatype DATE.
Opgelet! Deze kolom moet toegevoegd worden tussen kolommen “BEDRAG” en de hiervoor aangemaakte kolom “REDEN”.Zoek op internet op hoe je dit kan doen in MySQL.

```sql
    ALTER TABLE `tblBoetes`
    ADD `PAYMENTDATE` DATE AFTER `BEDRAG`;
```

## 6. Schrijf de SQL-instructie die in tabel “tblSpelers” de kolom “VOORLETTERS” zal verwijderen.

```sql
    ALTER TABLE `tblSpelers`
    DROP `VOORLETTERS`;
```

## 7. Schrijf de SQL-instructie die in tabel “tblBoetes” de naam van kolom “PAYMENTDATE” wijzigt in “BETALINGSDATUM”.

```sql
    ALTER TABLE `tblBoetes`
    CHANGE `PAYMENTDATE` `BETALINGSDATUM` DATE;
```

## 8. Schrijf de SQL-instructie die in tabel “tblSpelers” het datatype van de kolom “NAAM” wijzigt naar VARCHAR(50). Daarnaast mag deze kolom geen NULL toelaten.

```sql
    ALTER TABLE `tblSpelers`
    CHANGE `NAAM` `NAAM` VARCHAR(50) NOT NULL;
```

## 9. Schrijf de SQL-instructie die in tabel “tblSpelers” ervoor zorgt dat er een alternatieve sleutel wordt gelegd op de combinatie van kolommen “NAAM”,“STRAAT”,”HUISNR” en “POSTCODE”.

```sql
    ALTER TABLE `tblSpelers` ADD CONSTRAINT
    UNIQUE(`NAAM`, `STRAAT`, `HUISNR`, `POSTCODE`);
```

- [Terug](../Deel3.md)