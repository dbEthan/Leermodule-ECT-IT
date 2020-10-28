# Oplossing 1

```csharp
            Random orakel = new Random();

            Console.Write("Geslacht (m/v): ");
            string geslacht = Console.ReadLine();

            Console.Write("Leeftijd: ");
            int leeftijd = int.Parse(Console.ReadLine());

            if (geslacht == "m" && leeftijd < 120)
            {
               
                Console.WriteLine($"Je zal nog {orakel.Next(0, (121 - leeftijd))} jaren leven.");
            }
            else if (geslacht =="v"  && leeftijd < 150)
            {
                Console.WriteLine($"Je zal nog {orakel.Next(0, (151 - leeftijd))} jaren leven.");
            }
            else if ((leeftijd >= 120) || (leeftijd >= 150))
            {
                Console.WriteLine("Je zal binnenkort dood gaan.");
            }
```

[Terug](../Hfdst5.md)