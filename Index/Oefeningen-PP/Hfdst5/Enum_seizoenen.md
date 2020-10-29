# Oplossing 1

```csharp
        public enum Seizoenen
        {
            Winter,
            Zomer,
            Lente,
            Herfst
        }
        static void Main(string[] args)
        {
            Console.Write("Geef een maandnummer: ");
            int maand = int.Parse(Console.ReadLine());

            Seizoenen seizoen = Seizoenen.Herfst;

            switch (maand)
            {
                case 1:
                case 2:
                case 3:
                    seizoen = Seizoenen.Winter;
                    Console.WriteLine(seizoen);
                    break;
                case 4:
                case 5:
                case 6:
                    seizoen = Seizoenen.Lente;
                    Console.WriteLine(seizoen);
                    break;
                case 7:
                case 8:
                case 9:
                    seizoen = Seizoenen.Zomer;
                    Console.WriteLine(seizoen);
                    break;
                case 10:
                case 11:
                case 12:
                    seizoen = Seizoenen.Herfst;
                    Console.WriteLine(seizoen);
                    break;
                default:
                    Console.WriteLine("Niets gevonden");
                    break;
            }

            if (seizoen == Seizoenen.Lente || seizoen == Seizoenen.Zomer)
            {
                Console.WriteLine("Warm seizoen");
            }
            else
            {
                Console.WriteLine( "Koud seizoen");
            }
        }
```

[Terug](../Hfdst5.md)