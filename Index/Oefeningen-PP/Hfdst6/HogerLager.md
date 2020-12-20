# Oplossing 1

```csharp
class Program
    {
        static void Main(string[] args)
        {
            Random dobbel = new Random();
            string keuze;

            do
            {
                Console.Clear();
                int teller = 0;
                int input = 999;
                int ranGetal = dobbel.Next(1, 101);
                Console.Write($"Welkom bij Hoger-Lager!\nVoor we beginnen: Hoeveel keer mag er geraden worden? ");
                int inputMax = int.Parse(Console.ReadLine());
                Console.Clear();
                Console.WriteLine("Raad het getal tussen 1 en 100. (druk 0 om te stoppen)");
                while (input != ranGetal && input != 0 && teller < inputMax)
                {
                    input = int.Parse(Console.ReadLine());
                    if (input < ranGetal && input != 0 && inputMax != 1)
                        Console.WriteLine("Hoger!");
                    if (input > ranGetal && input != 0 && inputMax != 1)
                        Console.WriteLine("Lager!");
                    teller++;
                }
                if (input == ranGetal)
                    Console.WriteLine($"Proficiat! Je hebt juist geraden. Je deed er {teller} gokken over.");
                else if (input == 0)
                    Console.WriteLine($"Jammer! Je deed er {teller} gokken over.");
                else if (teller == inputMax)
                    Console.WriteLine($"Jammer! Je hebt het maximaal aantal gokken overschreden.");
                Console.WriteLine("Wil je opnieuw spelen? (j/n)");
                keuze = Console.ReadLine();
            } while (keuze == "j");
        }
    }
```

[Terug](../Hfdst6.md)