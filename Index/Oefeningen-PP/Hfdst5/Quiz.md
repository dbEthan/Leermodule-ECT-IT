# Oplossing 1

```csharp
            int resultaat1 = 0;
            int resultaat2 = 0;
            int resultaat3 = 0;
            
            //VRAAG 1
            Console.BackgroundColor = ConsoleColor.Blue;
            Console.Clear();
            Console.ForegroundColor = ConsoleColor.Red;
            Console.WriteLine("Vierkants wortel van 121 is ");
            Console.ResetColor();
            Console.WriteLine("a.9\nb.10\nc.11\nd.12");
            string c = Console.ReadLine();
            Console.Clear();

            //VRAAG 2
            Console.BackgroundColor = ConsoleColor.DarkRed;
            Console.Clear();
            Console.ForegroundColor = ConsoleColor.Gray;
            Console.WriteLine("Hoeveel gb is 1mb");
            Console.ResetColor();
            Console.WriteLine("a.0.001\nb.10\nc.0.1\nd.1000");
            string a = Console.ReadLine();
            Console.Clear();

            //VRAAG 3
            Console.BackgroundColor = ConsoleColor.DarkMagenta;
            Console.Clear();
            Console.ForegroundColor = ConsoleColor.Yellow;
            Console.WriteLine("Hoeveel bits is 1byte");
            Console.ResetColor();
            Console.WriteLine("a.6\nb.10\nc.12\nd.8");
            string d = Console.ReadLine();
            Console.Clear();

           


            switch (c)
            {
                case "a":
                case "b":
                case "d":
                    resultaat1 = -1;
                    break;
                case "c":
                    resultaat1 = +2;
                    break;
               
            }


            switch (a)
            {
                case "a":
                    resultaat2 = +2;
                    break;
                case "b":
                case "c":
                case "d":
                    resultaat2 = -1;
                    break;
            }

            switch (d)
            {
                case "a":
                case "b":
                case "c":
                    resultaat3 = -1;
                    break;
                case "d":
                    resultaat3 = +2;
                    break;
            }



            Console.WriteLine(resultaat1 + resultaat2 + resultaat3);
```

[Terug](../Hfdst5.md)