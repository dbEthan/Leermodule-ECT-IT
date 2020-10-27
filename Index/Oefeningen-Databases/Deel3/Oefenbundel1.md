# Oefenbundel 1

## 1. Schrijf de SQL-instructie die ervoor zorgt dat een database met naam “Learning” aangemaakt wordt. Zorg ervoor dat deze database alfanumerieke karakters in het formaat UT8 zal bewaren.De database zal definities van cursussen bevatten. Deze definities kunnen uitgerold worden naar andere databases voor specifieke klanten.

## 2. Schrijf de SQL-instructie die ervoor zorgt dat in dedatabase “Learning” onderstaande tabel aangemaakt wordt. Hou rekening met karaktersets!

![Deel3_Oefenbundel6_Oefening2_1](/Index/Pictures/Deel3_Oefenbundel1_Oef2_1.PNG)

```sql
    create table if not exists Learning.tblLanguages
    (
        `Id` TINYINT UNSIGNED AUTO_INCREMENT,
        `Name` varchar (20) NOT NULL,
        Primary key (`Id`),
        UNIQUE (`Name`)
    );
```

## 3. Schrijf de SQL-instructie die ervoor zorgt dat in dedatabase “Learning” onderstaande tabel aangemaakt wordt.Hou rekening met karaktersets!

![Deel3_Oefenbundel6_Oefening_1](/Index/Pictures/Deel3_Oefenbundel1_Oef3_1.PNG)

```sql
    create table if not exists Learning.tblCourseDefinitions
    (
        `Id` MEDIUMINT primary key,
        `LanguageId` SMALLINT UNSIGNED NOT NULL,
        `Name` VARCHAR(100) NOT NULL,
        `ReplicationKey` CHAR(36) CHARSET latin NOT NULL,
        PRIMARY KEY(`Id`),
        UNIQUE(`ReplicationKey`),
        FOREIGN KEY(`LanguageId`),
        REFERENCES `Learning`.`tblLanguages`(`Id`)
    );
```

- [Terug](../Deel3.md)