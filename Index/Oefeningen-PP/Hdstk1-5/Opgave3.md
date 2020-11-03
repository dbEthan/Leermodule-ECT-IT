# Oplossing 1

```csharp
        enum Pizzabodem
        {
            CheesyCrust=1,
            MartianMeal,
            PegasusLime
        }
        enum Pizzatopping
        {
            EndraliPies=1,
            ItalianCheese,
            Geen,
        }
        static void Main(string[] args)
        {
            //Alle prijzen worden uitgedrukt in IC (Intergalactic Credits)
            //Pizzabodems:
            const double CHEESY_C = 5;
            const double MARTIAN_M = 2.8;
            const double PEGASUS_L = 12.4;
            //Toppings:
            const double ENDRALI_CC = 10;
            const double ENDRALI_REST = 15;
            const double ITA_C = 5.5;
            const double CHEF = 1;
            //start values
            double prijsBodem = 0;
            double prijsTopping = 0;
            double prijsAfstand = 0;
            bool wiltExtra = false;
            string bodemstr = "";
            string toppingstr = "";
            //bevraging pizzabodems
            Console.WriteLine($"Pizzabodem? \n1) Cheesy Crust \n2) Martial Meal \n3) Pegasus Lime");
            int bodemKeuze = int.Parse(Console.ReadLine());
            Pizzabodem pizzabodem = (Pizzabodem)bodemKeuze;
            switch (pizzabodem)
            {
                case Pizzabodem.CheesyCrust:
                    prijsBodem = CHEESY_C;
                    bodemstr = "Cheesy Crust";
                    break;
                case Pizzabodem.MartianMeal:
                    prijsBodem = MARTIAN_M;
                    bodemstr = "Martian Meal";
                    Console.WriteLine($"Opgelet: de Martial Meal is niet geschikt voor kinderen onder de 54 jaar. \nVoer uw leeftijd in:");
                    int leeftijd = int.Parse(Console.ReadLine());
                    if (leeftijd < 54)
                    {
                        Console.ForegroundColor = ConsoleColor.Red;
                        Console.WriteLine("ERROR");
                        Console.ResetColor();
                        Environment.Exit(0);
                    }
                    break;
                case Pizzabodem.PegasusLime:
                    prijsBodem = PEGASUS_L;
                    bodemstr = "Pegasus Lime";
                    break;
            }
            //bevraging pizzatoppings
            Console.WriteLine($"Topping? \n1) Endrali Pies \n2) Italian Cheese \n3) Geen topping");
            int toppingKeuze = int.Parse(Console.ReadLine());
            Pizzatopping pizzatopping = (Pizzatopping)toppingKeuze;
            switch (pizzatopping)
            {
                case Pizzatopping.EndraliPies:
                    if (pizzabodem == Pizzabodem.CheesyCrust)
                    {
                        prijsTopping = ENDRALI_CC;
                    }
                    else
                    {
                        prijsTopping = ENDRALI_REST;
                    }
                    toppingstr = "Endrali Pies";
                    break;
                case Pizzatopping.ItalianCheese:
                    prijsTopping = ITA_C;
                    toppingstr = "Italian Cheese";
                    break;
                case Pizzatopping.Geen:
                    Console.WriteLine("Chef's extra toevoegen? (j/n)");
                    char extra = Convert.ToChar(Console.ReadLine());
                    if (extra == 'j')
                    {
                        wiltExtra = true;
                        prijsTopping = CHEF;
                        toppingstr = "Chef's keuze";
                    }
                    else
                    {
                        toppingstr = "Geen topping";
                    }
                    break;
            }
            //bevraging afstand
            Console.WriteLine("Hoe ver is het adres in lichtjaren? (1-100)");
            int afstand = int.Parse(Console.ReadLine());
            if (afstand < 1 || afstand > 100)
            {
                Console.ForegroundColor = ConsoleColor.Red;
                Console.WriteLine("ERROR");
                Console.ResetColor();
                Environment.Exit(0);
            }
            Console.Clear();

            //visualisatie
            switch (pizzabodem)
            {
                case Pizzabodem.CheesyCrust:
                    Console.ForegroundColor = ConsoleColor.Yellow;
                    Console.Write("C");
                    break;
                case Pizzabodem.MartianMeal:
                    Console.ForegroundColor = ConsoleColor.Red;
                    Console.Write("M");
                    break;
                case Pizzabodem.PegasusLime:
                    Console.ForegroundColor = ConsoleColor.Green;
                    Console.Write("P");
                    break;
            }
            switch (pizzatopping)
            {
                case Pizzatopping.EndraliPies:
                    Console.ForegroundColor = ConsoleColor.Blue;
                    Console.Write("O");
                    break;
                case Pizzatopping.ItalianCheese:
                    Console.ForegroundColor = ConsoleColor.Yellow;
                    Console.Write("O");
                    break;
                case Pizzatopping.Geen:
                    if (wiltExtra == true)
                    {
                        Console.ForegroundColor = ConsoleColor.White;
                        Console.Write("E");
                    }
                    else
                    {
                        Console.ForegroundColor = ConsoleColor.Yellow;
                        Console.Write("Z");
                    }
                    break;
            }
            Console.ResetColor();
            Console.WriteLine("");

            //prijsberekening
            double prijsPizza = prijsBodem + prijsTopping;
            if (afstand < 10)
            {
                prijsAfstand = 25;
            }
            else
            {
                prijsAfstand = Math.Floor(Math.Sqrt(afstand / prijsPizza) + prijsPizza);
            }
            if (wiltExtra == true)
            {
                prijsAfstand = prijsAfstand - (prijsAfstand / 100 * 10);
            }
            double prijsTotaal = prijsPizza + prijsAfstand;
            
            //Random korting module
            Random ranKorting = new Random();
            int korting = ranKorting.Next(0, 51);
            prijsTotaal = prijsTotaal - (prijsTotaal / 100 * korting);

            //Ticket
            Console.WriteLine($"{bodemstr}\t\t\t{prijsBodem} IC");
            Console.WriteLine($"{toppingstr}\t\t\t{prijsTopping} IC");
            Console.WriteLine("-    -   -   -   -   -   -   -   -   -   -");
            Console.WriteLine($"Totaal pizza\t\t\t{prijsPizza} IC");
            Console.WriteLine("");
            Console.WriteLine($"Afstand\t\t\t\t{afstand} lichtjaren");
            Console.WriteLine($"Transportkosten\t\t\t{prijsAfstand} IC");
            Console.WriteLine("-    -   -   -   -   -   -   -   -   -   -");
            Console.WriteLine($"Korting\t\t\t\t{korting}%");
            Console.WriteLine($"TOTAAL\t\t\t\t{prijsTotaal:F2} IC");
            
            //Benzine module
            int benzineTon = Convert.ToInt32(Math.Ceiling((double)afstand / 5));
            int rest = afstand % 5;
            int benzineVerbruikt = rest * 20;
            int BenzineOver = 100 - benzineVerbruikt;
            if (rest == 0)
            {
                BenzineOver = 0;
            }
            Console.WriteLine("******************************************");
            Console.WriteLine("Informatie voor de piloot:");
            Console.WriteLine($"Benzinetonnen in te laden\t{benzineTon}");
            Console.WriteLine($"Benzine over in laatste ton\t{BenzineOver}%");
        }
```

[Terug](../Hfdst1-5.md)