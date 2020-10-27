# Oplossing 1

```csharp
        enum chess
        {
            pion,
            paard,
            koning,
            dame,
            loper,
            toren,
        }
        enum kleur
        {
            witte,
            zwarte
        }
        static void Main(string[] args)
        {
            Random rand = new Random();
            int gok = rand.Next(0, 6);
            int gok2 = rand.Next(0, 6);
            int gok3 = rand.Next(0, 6);

            int keuze = rand.Next(0, 2);
            int keuze2 = rand.Next(0, 2);
            int keuze3 = rand.Next(0, 2);

            chess stuk1 = (chess)gok;
            chess stuk2 = (chess)gok2;
            chess stuk3 = (chess)gok3;

            kleur kleur1 = (kleur)keuze;
            kleur kleur2 = (kleur)keuze2;
            kleur kleur3 = (kleur)keuze3;

            Console.WriteLine($"{kleur1} {stuk1}");
            Console.WriteLine($"{kleur2} {stuk2}");
            Console.WriteLine($"{kleur3} {stuk3}");
        }
    }
```

[Terug](../Hfdst5.md)