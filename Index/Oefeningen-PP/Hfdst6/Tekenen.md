# Oplossing 1

```csharp
class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Geef breedte: ");
            int breedte = int.Parse(Console.ReadLine());

            Console.Write("Geef hoogte: ");
            int hoogte = int.Parse(Console.ReadLine());

            for (int i = 0; i < hoogte; i++) //deze loop gaat elke lijn af, per lijn wordt de geneste loop in zijn volledigheid uitgevoerd
            {
                for (int j = 0; j < breedte; j++) //deze loop wordt uitgevoerd bij elke iteratie van de buitenste loop. Hier wordt er op de lijn zelf gecontroleerd
                {
                    if (i == 0 || i == hoogte - 1 || j == 0 || j == breedte - 1) //als één van deze condities TRUE is, zal er een sterretje verschijnen.
                        Console.Write("*");
                    else
                        Console.Write(" ");
                }
                Console.WriteLine(); //op het einde van elke iteratie van de binnenste loop zal dit er voor zorgen dat er naar de volgende lijn geprint wordt.
            }
        }
    }
```

[Terug](../Hfdst6.md) 