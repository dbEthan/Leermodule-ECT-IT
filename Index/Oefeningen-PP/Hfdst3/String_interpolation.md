# Oplossing 1

```csharp
            Console.Write("Kies een bedrag in euro ");
            euro = Convert.ToDouble(Console.ReadLine());

            const double EUR_USD_RATIO = 1.17;
            double dollar = euro * EUR_USD_RATIO;

            Console.WriteLine($"{euro} EUR is gelijk aan {dollar} USD");

            Console.WriteLine("Druk op enter voor de volgende voorbeeld");
            Console.ReadLine();
            Console.Clear();

            Console.WriteLine("Oefening BTW");

            const double BTW = 0.21;
            double Prijs = 26;
            double PrijsMetBtw = ((Prijs * BTW) + Prijs);

            Console.WriteLine($"Prijs zonder BTW is {Prijs} met BTW is  {PrijsMetBtw}");
```

[Terug](../Hfdst3.md)