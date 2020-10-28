# Oefenbundel 7

## 1.Schrijf de SQL-instructie die ervoor zorgt dat een database met naam “Planes” aangemaakt wordt.

```sql
    CREATE DATABASE `Planes`;
```

## 2.SchrijfSQL-instructiesdie onderstaande tabellen creëren in database Planes. De tabellenmoetenaan volgende vereisten voldoen:

![Deel6_Oef2_4](/Index/Pictures/Deel2_Oefenbundel7_Oef2_1.PNG)

```sql
    CREATE TABLE IF NOT EXISTS `tblManufacturers`
    (
        `Id` SMALLINT UNSIGNED AUTO_INCREMENT,
        `Name` VARCHAR (70) NOT NULL UNIQUE,
        PRIMARY KEY(`Id`)
    ) AUTO_INCREMENT = 101;
```

![Deel6_Oef2_4](/Index/Pictures/Deel2_Oefenbundel7_Oef2_2.PNG)

```sql
    CREATE TABLE IF NOT EXISTS `tblPlaneDefinitions`
    (
        `Id` MEDIUMINT UNIQUE AUTO_INCREMENT,
        `ManufacturerId` SMALLINT,
        `Name` VARCHAR(100) NOT NULL,
        `DesignDate` DATE NOT NULL,
        `IsMilitary` TINYINT UNSIGNED,
        `NumberOfEngines` TINYINT UNSIGNED,
        `Weigt` DECIMAL(5,2)
        PRIMARY KEY (`Id`),
        UNIQUE(`ManufacturerId`,`Name`,`DesignDate`),
        Foreign KEY (ManufacturerId)
        References tblManufacturers(`Id`)
        On delete restrict     
    ) AUTO_INCREMENT = 1;
```

- [Terug](../Deel2.md)