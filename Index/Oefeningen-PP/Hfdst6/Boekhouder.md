# Oplossing 1

```csharp
class Program
    {
        static void Main(string[] args)
        {
            string input;
            int getal = 0;
            int som = 0;
            int somNeg = 0;
            int somPos = 0;
            double gemiddelde = 0;
            int teller = 0;

            do
            {
                Console.SetCursorPosition(0, 0);
                Console.Write("Geef een getal in: ");
                input = Console.ReadLine();
                Console.Clear();
                if (input != "q")
                {
                    getal = Convert.ToInt32(input);
                    som += getal;
                    Console.WriteLine($"\n\nBalans van alle ingevoerde getallen:\t\t{som}.");
                    if (getal < 0)
                    {
                        somNeg += getal;
                    }
                    Console.WriteLine($"Balans van alle negatieve getallen:\t\t{somNeg}.");
                    if (getal > 0)
                    {
                        somPos += getal;
                    }
                    Console.WriteLine($"Balans van alle positieve getallen:\t\t{somPos}.");
                    teller++;
                    gemiddelde = som / teller;
                    Console.WriteLine($"Gemiddelde van alle ingevoerde getallen:\t{gemiddelde}.");
                }
            } while (input != "q");
            Console.WriteLine($"FINAAL:\n\nBalans van alle ingevoerde getallen:\t\t{som}.\nBalans van alle negatieve getallen:\t\t{somNeg}." +
                $"\nBalans van alle positieve getallen:\t\t{somPos}.\nGemiddelde van alle ingevoerde getallen:\t{gemiddelde}.");
        }
    }
```

[Terug](../Hfdst6.md)