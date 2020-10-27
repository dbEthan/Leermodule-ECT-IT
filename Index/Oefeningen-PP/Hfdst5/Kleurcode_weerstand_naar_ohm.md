# Oplossing 1

```csharp
            int ring1 = 0;
            int ring2 = 0;
            int ring3 = 0;

            Console.WriteLine("Geef de ringen");
            string ringEen = Console.ReadLine();
            string ringTwee = Console.ReadLine();
            string ringDrie = Console.ReadLine();

            //RING1

            switch (ringEen)
            {
                case "zwart":
                    ring1 = 0;
                    break;

                case "bruin":
                    ring1 = 1;
                    break;

                case "rood":
                    ring1 = 2;
                    break;

                case "oranje":
                    ring1 = 3;
                    break;

                case "geel":
                    ring1 = 4;
                    break;

                case "groen":
                    ring1 = 5;
                    break;

                case "blauw":
                    ring1 = 6;
                    break;

                case "violet":
                    ring1 = 7;
                    break;

                case "grijs":
                    ring1 = 8;
                    break;

                case "wit":
                    ring1 = 9;
                    break;

            }

            //RING2
            switch (ringTwee)
            {
                case "zwart":
                    ring2 = 0;
                    break;

                case "bruin":
                    ring2 = 1;
                    break;

                case "rood":
                    ring2 = 2;
                    break;

                case "oranje":
                    ring2 = 3;
                    break;

                case "geel":
                    ring2 = 4;
                    break;

                case "groen":
                    ring2 = 5;
                    break;

                case "blauw":
                    ring2 = 6;
                    break;

                case "violet":
                    ring2 = 7;
                    break;

                case "grijs":
                    ring2 = 8;
                    break;

                case "wit":
                    ring2 = 9;
                    break;

            }

            //RING3
            switch (ringDrie)
            {
                case "zwart":
                    ring3 = 0;
                    break;

                case "bruin":
                    ring3 = 1;
                    break;

                case "rood":
                    ring3 = 2;
                    break;

                case "oranje":
                    ring3 = 3;
                    break;

                case "geel":
                    ring3 = 4;
                    break;

                case "groen":
                    ring3 = 5;
                    break;

                case "blauw":
                    ring3 = 6;
                    break;

                case "violet":
                    ring3 = 7;
                    break;

                case "goud":
                    ring3 = -1;
                    break;

                case "zilver":
                    ring3 = -2;
                    break;

            }

            double resultaat = ((ring1 * 10) + ring2) * Math.Pow(10, ring3);
            Console.WriteLine($"Deze weerstand heeft een waarde van {resultaat}");
```

[Terug](../Hfdst5.md)