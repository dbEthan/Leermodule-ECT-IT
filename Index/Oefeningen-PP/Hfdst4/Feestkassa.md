# Oplossing 1

```csharp
            const int PRIJS_FRIETJES = 20;
            const int PRIJS_KONINGINNENHAPJE = 10;
            const int PRIJS_IJSJES = 3;
            const int PRIJS_DRANK = 2;

            Console.WriteLine("Frietjes?");
            int aantalFriet = int.Parse(Console.ReadLine());
            int totaalF = aantalFriet * PRIJS_FRIETJES;
            Console.WriteLine($"Tussenprijs = {totaalF} euro");

            Console.WriteLine("koninginnenhapje?");
            int aantalKoninginnenhapje = int.Parse(Console.ReadLine());
            int totaalK = PRIJS_KONINGINNENHAPJE * aantalKoninginnenhapje;
            Console.WriteLine($"Tussenprijs = {totaalF} euro + {totaalK} euro");

            Console.WriteLine("Ijsjes?");
            int aantalIjsjes = int.Parse(Console.ReadLine());
            int totaalI = PRIJS_IJSJES * aantalIjsjes;
            Console.WriteLine($"Tussenprijs = {totaalF} euro + {totaalK} euro + {totaalI} euro");

            Console.WriteLine("Dranken");
            int aantalDranken = int.Parse(Console.ReadLine());
            int totaalD = aantalDranken * PRIJS_DRANK;
            Console.WriteLine($"Tussenprijs = {totaalF} euro + {totaalK} euro + {totaalI} euro  + {totaalD} euro");

            int totaal = totaalF + totaalK + totaalI + totaalD ;

            Console.WriteLine();

            Console.WriteLine($"Het totaal te betalen bedrag is {totaal} EURO.");

```

[Terug](../Hfdst4.md)