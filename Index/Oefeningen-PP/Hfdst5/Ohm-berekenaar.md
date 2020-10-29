# Oplossing 1

```csharp
            Console.WriteLine("Stroom(1), Spanning(2), Weerstand(3)");
            Console.Write("Wat wil je berekenen (1,2,3): ");
            int keuze = int.Parse(Console.ReadLine());

            if (keuze==1)
            {
                Console.Write("Spanning: ");
                double spanning = int.Parse(Console.ReadLine());

                Console.Write("Weerstand: ");
                double weerstand = int.Parse(Console.ReadLine());

                Console.WriteLine($"De stroom is {spanning/weerstand} ampere");
            }

            else if (keuze == 2)
            {
                Console.Write("Stroom: ");
                double stroom = int.Parse(Console.ReadLine());

                Console.Write("Weerstand: ");
                double weerstand = int.Parse(Console.ReadLine());

                Console.WriteLine($"De spanning is { stroom * weerstand} volt");
            }

            else if (keuze == 3)
            {
                Console.Write("Stroom: ");
                double stroom = int.Parse(Console.ReadLine());

                Console.Write("Spanning: ");
                double spanning = int.Parse(Console.ReadLine());

                Console.WriteLine($"De weerstand is { spanning / stroom } Ohm");
            }
```

[Terug](../Hfdst5.md)