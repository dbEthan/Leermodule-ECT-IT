# Oplossing 1

```csharp
            Console.WriteLine("Voer bedrag in?");
            double bedrag1 = double.Parse(Console.ReadLine());

            Console.WriteLine($"De poef staat op {bedrag1} euro. \r\nVoer een bedrag in? ");
            double bedrag2 = double.Parse(Console.ReadLine());

            Console.WriteLine($"De poef staat op {bedrag1 + bedrag2} euro. \r\nVoer een bedrag in? ");
            double bedrag3 = double.Parse(Console.ReadLine());

            Console.WriteLine($"De poef staat op {bedrag1 + bedrag2 + bedrag3} euro. \r\nVoer een bedrag in? ");
            double bedrag4 = double.Parse(Console.ReadLine());

            Console.WriteLine($"De poef staat op {bedrag1 + bedrag2 + bedrag3 + bedrag4} euro. \r\nVoer een bedrag in? ");
            double bedrag5 = double.Parse(Console.ReadLine());

            double totaal = bedrag1 + bedrag2 + bedrag3 + bedrag4 + bedrag5;
            double weken = Math.Ceiling(totaal / 10);
          

            Console.WriteLine($"De poef staat op {totaal} euro.");


            Console.WriteLine("*************************");
            Console.WriteLine($"Het totaal van {totaal} de poef is en zal {weken} weken duren om volledig afbetaald te worden.");
```

[Terug](../Hfdst4.md)