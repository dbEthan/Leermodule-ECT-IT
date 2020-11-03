# Oplossing 1

```csharp
        enum Fase
        {
            A,
            B,
            C,
            Onbekend
        }
        static void Main(string[] args)
        {
            Console.WriteLine("Zet de computer aan.");
            Console.WriteLine("Gaat de computer aan? (j/n)");
            string input = Console.ReadLine();

            Fase eindFase = Fase.Onbekend;

            if (input == "j")
            {
                Console.Clear();
                Console.WriteLine("Zijn er foutboodschappen? (j/n)");
                input = Console.ReadLine();
                if (input == "j")
                {
                    eindFase = Fase.A;
                }
                else if (input == "n")
                {
                    eindFase = Fase.B;
                }
            }
            else if (input == "n")
            {
                Console.Clear();
                Console.WriteLine("Gaat het power light aan? (j/n)");
                input = Console.ReadLine();
                if (input == "j")
                {
                    Console.Clear();
                    Console.WriteLine("Zet het computerscherm aan.");
                }
                else if (input == "n")
                {
                    Console.Clear();
                    Console.WriteLine("Controleer de voedingskabel.");
                }
                Console.Clear();
                Console.WriteLine("Probleem opgelost? (j/n)");
                input = Console.ReadLine();
                if (input == "j")
                {
                    eindFase = Fase.B;
                }
                else if (input == "n")
                {
                    eindFase = Fase.C;
                }
            }

            if (eindFase == Fase.A)
            {
                Console.Clear();
                Console.WriteLine("Dien de foutcode in:");
                int foutcode = int.Parse(Console.ReadLine());
                if (foutcode >= 0 && foutcode <= 9)
                {
                    double aantalMinuten = Math.Sqrt(foutcode * 3);
                    Console.ForegroundColor = ConsoleColor.Red;
                    Console.WriteLine($"Gelieve je computer gedurende {aantalMinuten:F1} minuten af te zetten.");
                    Console.ResetColor();
                }
                else
                {
                    Console.WriteLine("Los het dan zelf op hé!");
                }
            }
            else if (eindFase == Fase.B)
            {
                Random ranGen = new Random();
                int ranGetal = ranGen.Next(0, 4); 

                Console.Clear();
                Console.WriteLine("Mooi zo, alles werkt.");
                if (ranGetal == 0)
                {
                    Console.WriteLine("En u wint ook nog eens 1 jaar gratis IT support!");
                }
            }
            else if (eindFase == Fase.C)
            {
                int procCount = Environment.ProcessorCount;
                bool is64Bit = Environment.Is64BitOperatingSystem;
                const int REP_PRIJS = 50; //euro

                Console.Clear();
                if (procCount == 1)
                {
                    Console.BackgroundColor = ConsoleColor.Red;
                    Console.ForegroundColor = ConsoleColor.White;
                    Console.WriteLine("1 processor");
                    Console.ResetColor();
                }
                else if (procCount >= 2)
                {
                    Console.BackgroundColor = ConsoleColor.Green;
                    Console.ForegroundColor = ConsoleColor.Blue;
                    Console.WriteLine($"{procCount} processors");
                    Console.ResetColor();
                }
                if (procCount < 5)
                {
                    Console.WriteLine($"{procCount * REP_PRIJS} euro");
                }
                else
                {
                    Console.WriteLine("200 euro");
                }
                if (is64Bit == true)
                {
                    Console.WriteLine("Hier een bon!");
                }
            }
        }
```

[Terug](../Hfdst5.md)