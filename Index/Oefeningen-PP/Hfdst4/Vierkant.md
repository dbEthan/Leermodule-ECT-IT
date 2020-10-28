# Oplossing 1

```csharp
            double zijde;

            Console.Write("Lengte zijde: ");

            zijde = Double.Parse(Console.ReadLine());

            double omtrek = zijde * 4;
            double oppervlakte = Math.Pow(zijde,2);
            double oppervlakte2 = Math.Round(oppervlakte, 2);

            Console.WriteLine($"Zijde: {zijde}");
            Console.WriteLine($"Omtrek: {omtrek}");
            Console.WriteLine($"Oppervlakte: {oppervlakte2} ");
```

[Terug](../Hfdst4.md)