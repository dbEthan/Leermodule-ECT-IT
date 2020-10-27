# Oefenbundel 3

## 1. We bewaren in tabel “tblGames” alle gekende games inclusief hun prijs. De prijs van games wordtuitgedrukt in euro.Welk datatype zal je gebruiken voor deprijs? Motiveer je antwoord!

> We opterenhier voorhet datatypeDECIMAL(5,2). De prijs van een enkel game bedraagt normaal gezien niet meer dan € 100, echter sommige bundels wel. We voorzien daarom 5 digits waarvan 2 na de komma. Zo blijven er 3 digits over waarmee we een maximumprijs van € 999,99 kunnen bewaren.

## 2. We wensen te weten hoeveel lak er nodig is om een wagen te spuiten. Hiervoor hebben we de afmetingen nodig van een wagenzoals hoogte, breedte, lengte,enz. Elke afmeting wordt uitgedrukt in meter, nauwkeurig tot op de millimeter.Welk datatype zal je gebruiken voor bv. de lengte van een wagen te bewaren? Motiveer je antwoord!

> We opterenhier voor het datatypeDECIMAL(5,3).Een millimeter is een duizendste van een meter dus we hebben 3 cijfers na de komma nodig. Een wagen is in principe minder dan 10m lang, behoudens enkele uitzonderingen zoals misschien een limousine. We reserveren dus 2 cijfers voor de komma en 3 erna.

## 3. Op facturen wordt soms een korting toegekend in de vorm van een percentage. We willen dit percentage zodanig bewaren in een tabel dat we enkel het subtotaal van een factuur moeten vermenigvuldigen met het percentage om het kortingsbedrag te berekenen.Welk datatype zal je gebruiken om het percentage bewaren? Motiveer je antwoord!

> Een percentage wordt altijd bewaard als een kommagetal.Geef je 10% korting wordt dit 0,1. We opteren hier dus voor het datatypeDECIMAL(3,2).

- [Terug](../Deel2.md)
