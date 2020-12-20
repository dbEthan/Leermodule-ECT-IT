# Oplossing 1

```csharp
class Program
    {
        enum Menu
        {
            Spelen=1,
            Level,
            Studeren,
        }
        static void Main(string[] args)
        {
            Random dobbel = new Random();
            const int START_W = 1;
            const int EIND_W = 10;
            int a = 0;
            int b = 0;
            int product = 0;
            int teller = 0;
            int level = 1; //level vd speler


            Console.WriteLine($"Welkom bij de wiskundequiz! Kies één van volgende opties:\n1. Gewoon spelen\n2. Start op een bepaald level\n3. Studeren");
            int input = int.Parse(Console.ReadLine());
            Menu menuKeuze = (Menu)input;

            switch (menuKeuze)
            {
                case Menu.Spelen:
                    Console.Clear();
                    break;
                case Menu.Level:
                    Console.WriteLine("Voer het level in van waar je wil beginnen spelen:");
                    level = int.Parse(Console.ReadLine());
                    Console.Clear();
                    break;
                case Menu.Studeren:
                    break;
                default:
                    Console.WriteLine("Dit is geen optie. Programma wordt afgesloten.");
                    Environment.Exit(0);
                    break;
            }

            input = product;
            Console.WriteLine("Geef de oplossingen voor volgende vermenigvuldigingen:");
            do
            {
                a = dobbel.Next(START_W, (EIND_W + 1) * level);
                b = dobbel.Next(START_W, (EIND_W + 1) * level);
                product = a * b;
                Console.Write($"{a} * {b} = ");
                if (menuKeuze == Menu.Studeren)
                {
                    Console.WriteLine(product);
                    input = product;
                    System.Threading.Thread.Sleep(5000);
                }
                if (menuKeuze == Menu.Spelen || menuKeuze == Menu.Level)
                    input = int.Parse(Console.ReadLine());
                if (input == product)
                    teller++;
                if (teller % 5 == 0 && input == product)
                {
                    level++;
                    Console.Clear();
                    Console.WriteLine($"Level {level} bereikt!");
                }
            } while (input == product);

            Console.WriteLine($"Fout! Je hebt {teller} keer juist geantwoord.");
        }
    }
```

[Terug](../Hfdst6.md)