# Oefenbundel 4

## 1. We bewaren in tabel “tblPersons” alle inwoners van België. Een van de gegevensvelden is de straat van de woonplaats van de inwoners.Welk datatype zal je gebruiken voor straat? Motiveer je antwoord!

> Je kan op zoek gaan naar de langste straatnaam in België. Dan kom je uit op een 54-tal karakters. Voor de veiligheid voorzien we nog een beetje extra in geval van nieuwe straatnamen die net iets langer zouden kunnen worden. We opterendus voor een VARCHAR(60).

###### 2. Op een blikje frisdrank kan je een barcode terugvinden.Het type barcode is een EAN-13 barcode. Onder de barcode kunnen we de numerieke waarde van zo’n EAN-13 code terugvinden.Welk datatype zal je gebruiken voor deze numerieke code? Motiveer je antwoord!

> Aangezien de code altijd evenveel cijfers bevat opteren we voor datatype CHAR. We kiezen geen INT omdat in dergelijke codes voorloopnullen kunnen voorkomen die in dat geval weg zouden vallen. Aangezien de code steeds 13 cijfers lang is resulteert dit in een CHAR(13).

## 3. In tabel “tblCities” houden we alle Belgische steden en gemeentes bij.Welk datatype zal je gebruiken voor de kolom waarin denaam van de stad/gemeentewordtbewaard? Motiveer je antwoord!

> We kunnen hiervoor de lijst met steden en gemeenten downloaden bij bpost. Door de lengte te bepalen van elke gemeentenaam kunnen we terugvinden dat de langste gemeentenaam 50 is. Ook hier nemen we een kleine marge waardoor we uitkomen op VARCHAR(60).

## 4. In dezelfde tabel “tblCities” houden we ook de postcodes bij van alle Belgische steden en gemeentes. Welk datatype zal je gebruiken voor de kolom waarin de postcode van de stad/gemeente wordt bewaard? Motiveer je antwoord!

> We kunnen ook hier de lijst met steden en gemeenten van bpost gebruiken. Door de lengte te bepalen van elke postcode kunnen we terugvinden dat elke postcode uit 4 cijfers bestaat. We opteren bijgevolg voor datatype CHAR(4).

- [Terug](../Deel2.md)