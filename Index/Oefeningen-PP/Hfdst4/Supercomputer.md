# Oplossing 1

```csharp
            double getal1, getal2, getal3;

            Console.Write("Kommagetal1: ");
            getal1 = double.Parse(Console.ReadLine());

            Console.Write("Kommagetal2: ");
            getal2 = double.Parse(Console.ReadLine());

            Console.Write("Kommagetal3: ");
            getal3 = double.Parse(Console.ReadLine());

            double gemiddelde = Math.Round((getal1 + getal2 + getal3) / 3,2);
            Console.WriteLine($"Gemiddelde van de 3 kommagetallen is {gemiddelde}");
```

[Terug](../Hfdst4.md)