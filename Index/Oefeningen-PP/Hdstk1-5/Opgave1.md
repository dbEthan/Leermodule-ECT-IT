# Oplossing 1

```csharp
        enum Menu
        {
            Rekenmachine=1,
            PasswordTester,
            Recyclage,
            ComputerSolver,
        }
        enum Seizoen
        {
            Lente,
            Zomer,
            Herfst,
            Winter
        }
        static void Main(string[] args)
        {
            Console.WriteLine($"Welkom in deze multitool-applicatie! \nKies een item om uit te voeren: \n1. Rekenmachine \n2. Password Tester \n3. Recyclage - Seizoenen \n4. Computer Solver");
            int input = int.Parse(Console.ReadLine());

            Menu keuze = (Menu)input;

            switch (keuze)
            {
                case Menu.Rekenmachine:

                    Console.Clear();
                    Console.WriteLine("Voer 1ste getal in:");
                    double getal1 = double.Parse(Console.ReadLine());
                    Console.WriteLine("Voer 2de getal in:");
                    double getal2 = double.Parse(Console.ReadLine());

                    Console.WriteLine($"Kies een operator: (+, -, *, /, %)");
                    char inputOperator = Convert.ToChar(Console.ReadLine());

                    switch (inputOperator)
                    {
                        case '+':
                            double oplossing = getal1 + getal2;
                            if (oplossing < 0)
                            {
                                Console.ForegroundColor = ConsoleColor.Red;
                                Console.WriteLine($"Het resultaat is {oplossing}.");
                                Console.ResetColor();
                            }
                            else
                            {
                                Console.WriteLine($"Het resultaat is {oplossing}.");
                            }
                            break;
                        case '-':
                            oplossing = getal1 - getal2;
                            if (oplossing < 0)
                            {
                                Console.ForegroundColor = ConsoleColor.Red;
                                Console.WriteLine($"Het resultaat is {oplossing}.");
                                Console.ResetColor();
                            }
                            else
                            {
                                Console.WriteLine($"Het resultaat is {oplossing}.");
                            }
                            break;
                        case '*':
                            oplossing = getal1 * getal2;
                            if (oplossing < 0)
                            {
                                Console.ForegroundColor = ConsoleColor.Red;
                                Console.WriteLine($"Het resultaat is {oplossing}");
                                Console.ResetColor();
                            }
                            else
                            {
                                Console.WriteLine($"Het resultaat is {oplossing}.");
                            }
                            break;
                        case '/':
                            oplossing = getal1 / getal2;
                            if (oplossing < 0)
                            {
                                Console.ForegroundColor = ConsoleColor.Red;
                                Console.WriteLine($"Het resultaat is {oplossing}");
                                Console.ResetColor();
                            }
                            else
                            {
                                Console.WriteLine($"Het resultaat is {oplossing}.");
                            }
                            break;
                        case '%':
                            oplossing = getal1 % getal2;
                            if (oplossing < 0)
                            {
                                Console.ForegroundColor = ConsoleColor.Red;
                                Console.WriteLine($"Het resultaat is {oplossing}");
                                Console.ResetColor();
                            }
                            else
                            {
                                Console.WriteLine($"Het resultaat is {oplossing}.");
                            }
                            break;
                        default:
                            Console.WriteLine("Voer een geldige input in.");
                            break;
                    }
                    break;

                case Menu.PasswordTester:

                    Console.Clear();
                    const string PASSWORD = "TrumpSux";
                    Console.WriteLine("Gelieve je paswoord in te voeren:");
                    string inputPaswoord = Console.ReadLine();
                    if (inputPaswoord == PASSWORD)
                    {
                        Console.ForegroundColor = ConsoleColor.Green;
                        Console.WriteLine("Toegelaten.");
                        Console.ResetColor();
                    }
                    else
                    {
                        Console.ForegroundColor = ConsoleColor.Red;
                        Console.WriteLine("Verboden.");
                        Console.ResetColor();
                    }
                    break;

                case Menu.Recyclage:
                    
                    // Voeg hier je gerecycleerde code toe.

                    break;
                case Menu.ComputerSolver:
                    
                    Console.WriteLine("Deze applicatie zal je helpen met het oplossen van een computerprobleem. Druk op ENTER om te beginnen.");
                    Console.ReadLine();
                    Console.Clear();
                    Console.WriteLine("Does the computer turn on? (y/n)");
                    string solverInput = Console.ReadLine();
                    if (solverInput == "y")
                    {
                        Console.Clear();
                        Console.WriteLine("Are there any error messages? (y/n)");
                        solverInput = Console.ReadLine();
                        if (solverInput == "y")
                        {
                            Console.WriteLine("Perform a search for the error message.");
                        }
                        else if (solverInput == "n")
                        {
                            Console.WriteLine("Computer is fine.");
                        }
                        else
                        {
                            Console.WriteLine("Please enter a valid input.");
                        }
                    }
                    else if (solverInput == "n")
                    {
                        Console.Clear();
                        Console.WriteLine("Is the computer power light on? (y/n)");
                        solverInput = Console.ReadLine();
                        if (solverInput == "y")
                        {
                            Console.WriteLine("Turn the computer monitor on.");
                        }
                        else if (solverInput == "n")
                        {
                            Console.WriteLine("Check the computer power cord.");
                        }
                        else
                        {
                            Console.WriteLine("Please enter a valid input.");
                        }
                    }
                    else
                    {
                        Console.WriteLine("Please enter a valid input.");
                    }
                    break;
                default:
                    Console.WriteLine("Gelieve één van de 5 opties te kiezen.");
                    break;
            }
        }
```

[Terug](../Hfdst5.md)