# Oefenbundel 6

## 1. Schrijfde SQL-instructie die tabel AFDELING verwijderd in database AP.

```sql
    DROP TABLE `AP`.`AFDELING`;
 ```

## 2. Schrijf SQL-instructiesdie onderstaande tabellen creëren in database AP. De tabellenmoetenaan volgende vereisten voldoen:

![Deel6_Oef2_1](/Index/Pictures/Deel2_Oefenbundel6_Oef2_1.PNG)

```sql
    CREATE TABLE `AP`.`tblOpleidingen`
    (
        `Code` VARCHAR(10) PRIMARY KEY,
        `OMSCHRIJVING` MEDIUMTEXT,
        `DUUR` varchar(2)
    );
```

![Deel6_Oef2_2](/Index/Pictures/Deel2_Oefenbundel6_Oef2_2.PNG)

```sql
    CREATE TABLE `AP`.`tblAfdelingen`
    (
        `Nr` INT UNSIGNED PRIMARY KEY AUTO_INCREMENT,
        `Naam` VARCHAR (100),
        `Replicatiecode` CHAR (36)
        PRIMARY KEY(`Nr`)
    ) AUTO_INCREMENT = 10;
```

![Deel6_Oef2_3](/Index/Pictures/Deel2_Oefenbundel6_Oef2_3.PNG)

```sql
    CREATE TABLE AP.tblMedewerkers
    (
        `Nr` MEDIUMINT UNSIGNED  auto_increment,
        `Naam` VARCHAR (100),
        `Adres` VARCHAR (135),
        `AfdelingNr` SMALLINT UNSIGNED,
        PRIMARY KEY (`Nr`)
        FOREIGN KEY (`VAfdelingNr`)
        REFERENCES `tblAfdelingen`(`Nr`)
    ) AUTO_INCREMENT = 1;
```

![Deel6_Oef2_4](/Index/Pictures/Deel2_Oefenbundel6_Oef2_4.PNG)

```sql
    CREATE TABLE tblGevolgdeOpleidingen
    (
        `MedewerkerNr` MEDIUMINT UNSIGNED,
        `Opleidingscode` VARCHAR (10),
        `Datum` DATE,
        `Voltooid` BIGINT UNSIGNED,
        PRIMARY KEY(`Medewerkernr`, `Opleidingscode`, `Datum`)
        FOREIGN KEY(`MedewerkerNr`),
        REFERENCES `tblMedewerkers`(`Nr`),
        FOREIGN KEY(`Opleidingscode`),
        REFERENCES `tblOpleidingen`(`Code`)
    );
```

- [Terug](../Deel2.md)
