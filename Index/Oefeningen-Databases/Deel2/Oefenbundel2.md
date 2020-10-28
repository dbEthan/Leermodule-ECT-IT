# Oefenbundel 2

## 1. We bewaren in tabel “tblGameGenres” alle gekende genres. Elk genre krijgt een uniekvolgnummer, startend vanaf 1,die bewaard wordt in kolom “Id”. Er zijn een 60-tal genres gedefinieerd. Welk datatype zal je gebruiken voor deze kolom? Motiveer je antwoord

> We opteren voor het datatype TINYINT UNSIGNED. Het bereik van TINYINT gaat van 0 tot 255 als we de tekenbitweglaten. Hierin kunnen probleemloos de 60 genres. We kunnen de tekenbit weglaten omdat dit een “Id” veld is en bijgevolg niet met negatieve waarden werkt. De integriteitsregel UNSIGNED zorgt hiervoor.

## 2. Op een weerbericht wordt de temperatuur getoond. We bewaren deze waarden in kolom “Temperature” van tabel“tblTemperatureHistory”. Welk datatype zal je gebruiken voor deze kolom? Motiveer je antwoord!

> We opteren voor het datatype TINYINT met gebruik van een tekenbit. Temperaturen kunnen immers ook negatief zijn. We mogen er vanuit gaan dat temperaturen in een weerbericht nooit hoger dan 100 of lager dan -100 zullen gaan. Een TINYINT volstaat dus qua bereik.

## 3. Jaarlijks wordthet aantal inwonersvan België geteld. Dit aantal wordt bewaard in kolom “InhabitantCount” van tabel“tblDemoGraphicData”.Welk datatype zal je gebruiken voor deze kolom? Motiveer je antwoord!

> We opteren hier voor het datatype MEDIUMINT UNSIGNED of INT UNSIGNED. We gebruiken geen tekenbit omdat er geen negatieve waarde kan en mag zijn. Op dit moment bedraagt het aantal inwoners ongeveer 11 miljoen. Dat past perfect in een MEDIUMINT UNSIGNED met nog een deel marge. Als we al verder vooruit willen denken naar eennog groter aantal inwoners dan 16 777 215 inwoners kiezen we voor INT UNSIGNED. Dit is ruim voldoende voor huidige en toekomstige inwonersaantallen te bevatten.

## 4. Veel mensen bestellen jaarlijks artikelen via Amazon. Een bestelling heeft daarbijminimaal één, mogelijk meerderedetaillijnen per artikel. Elke detaillijn van een bestelling krijgt een uniek volgnummer toegewezen. Welk datatype zal je gebruiken voor dit volgnummer? Motiveer je antwoord!

> We opteren hier voor het datatype BIGINT UNSIGNED. Ook hier hebben we geen tekenbit nodig omdat er nooit negatieve getallen in mogen kunnen. Door te opteren voor een BIGINT kunnen we het maximaal mogelijk aantal lijnen definiëren. Aangezien Amazon wereldwijd producten verkoopt is dat geen overbodige luxe!

- [Terug](../Deel2.md)