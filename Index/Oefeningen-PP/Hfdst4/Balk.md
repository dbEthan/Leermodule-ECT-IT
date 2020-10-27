# Oplossing 1

```csharp
            Console.Write("lengte: ");
            double lengte = double.Parse(Console.ReadLine());

            Console.Write("breedte: ");
            double breedte = double.Parse(Console.ReadLine());

            Console.Write("hoogte: ");
            double hoogte = double.Parse(Console.ReadLine());

            double oppervlakte = Math.Round(2 * (lengte * hoogte) + 2*(lengte *breedte) + 2 * (hoogte * breedte),2);

            double inhoud =Math.Round(lengte * hoogte * breedte,2);

            Console.WriteLine($"oppervlakte: {oppervlakte}");
            Console.WriteLine($"inhoud: {inhoud}");

```

[Terug](../Hfdst4.md)