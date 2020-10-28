# Oplossing 1

```csharp
            Console.WriteLine("Antwoord met (j/n)");
            Console.Write("Werk je veel? ");
            string antwoord = Console.ReadLine();

            switch (antwoord)
            {
                case "j":
                    Console.Write("Koop je soms bruin brood? ");
                    antwoord = Console.ReadLine();

                    switch (antwoord)
                    {
                        case "j":
                            Console.Write("Ben je een seut? ");
                            antwoord = Console.ReadLine();
                            switch (antwoord)
                            {
                                case "j":
                                    Console.ForegroundColor = Color.Orange;
                                    Console.WriteLine("CD&V");
                                    Console.ResetColor();
                                    break;
                                case "n":
                                    Console.Write("Heb je vrienden? ");
                                    antwoord = Console.ReadLine();
                                    switch(antwoord)
                                    {
                                        case "j":
                                            Console.Write("Staat je wagen, huis, ... op naam van jouw ouders? ");
                                            antwoord = Console.ReadLine();

                                            switch (antwoord)
                                            {
                                                case "j":
                                                    Console.Write("OPEN", Color.Aqua);
                                                    Console.BackgroundColor = Color.Blue;
                                                    System.Console.WriteLine("VLD", Color.White);
                                                    Console.ResetColor();
                                                    break;

                                                case "n":
                                                    Console.ForegroundColor = Color.Red;
                                                    Console.WriteLine("BLANCO");
                                                    Console.ResetColor();
                                                    break;
                                            }
                                            break;
                                        case "n":
                                            Console.WriteLine("NVA");
                                            break;
                                    }
                                    break;
                            }
                            break;
                        case "n":
                            Console.WriteLine("VLAAMS BELANG");
                            break;
                    }
                    break;


                case "n":
                    Console.Write("Eet je Quinoa? ");
                    antwoord = Console.ReadLine();

                    switch (antwoord)
                    {
                        case "j":
                            Console.ForegroundColor = Color.Green;
                            Console.WriteLine("GROEN");
                            Console.ResetColor();
                            break;
                        case "n":
                            Console.Write("Krijg je vaak schuld van alles? ");
                            antwoord = Console.ReadLine();

                            switch (antwoord)
                            {
                                case "j":
                                    Console.ForegroundColor = Color.Red;
                                    Console.WriteLine("SPA");
                                    Console.ResetColor();
                                    break;
                                case "n":
                                    Console.Write("Geloof je nog in Sinterklaas? ");
                                    antwoord = Console.ReadLine();

                                    switch (antwoord)
                                    {
                                        case "j":
                                            Console.ForegroundColor = Color.Red;
                                            Console.WriteLine("PVDA");
                                            Console.ResetColor();
                                            break;
                                        case "n":
                                            Console.ForegroundColor = Color.Red;
                                            Console.WriteLine("BLANCO");
                                            Console.ResetColor();
                                            break;
                                    }
                                    break;
                            }
                            break;

                    }
                    break;
            }
```

[Terug](../Hfdst5.md)