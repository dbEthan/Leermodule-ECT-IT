# Oplossing 1

```csharp
class Program
    {
        enum Keuze
        {
            Schaar=1,
            Steen,
            Papier
        }
        static void Main(string[] args)
        {
            Random dobbel = new Random();
            bool win = false;
            int scoreUser = 0;
            int scorePc = 0;

            Console.Write($"Welkom bij Schaar-Steen-papier! De eerste met 10 punten wint! ");
            while (scoreUser < 10 && scorePc < 10)
            {
                win = false;
                Console.WriteLine("Kies:\n1. Schaar\n2. Steen\n3. Papier");
                int userKeuze = int.Parse(Console.ReadLine());
                Console.Clear();
                Keuze user = (Keuze)userKeuze;

                int pcKeuze = dobbel.Next(1, 4);
                Keuze pc = (Keuze)pcKeuze;

                switch (user)
                {
                    case Keuze.Schaar:
                        if (pc == Keuze.Papier)
                            win = true;
                        break;
                    case Keuze.Steen:
                        if (pc == Keuze.Schaar)
                            win = true;
                        break;
                    case Keuze.Papier:
                        if (pc == Keuze.Steen)
                            win = true;
                        break;
                    default:
                        break;
                }
                
                if (win)
                {
                    scoreUser++;
                    Console.WriteLine($"Jij wint! De huidige score is {scoreUser} voor jou en {scorePc} voor de computer.");
                }
                else if (user == pc)
                {
                    Console.WriteLine("Stalemate! Niemand wint een punt.");
                }
                else if (!win)
                {
                    scorePc++;
                    Console.WriteLine($"De computer wint. De huidige score is {scoreUser} voor jou en {scorePc} voor de computer.");
                }
            }
            Console.Clear();
            if (scoreUser == 10)
                Console.WriteLine("Proficiat! U bent de winnar!");
            else
                Console.WriteLine("De computer wint.");
        }
    }
```

[Terug](../Hfdst6.md)