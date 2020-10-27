# Oplossing 1

```csharp
            Console.Write("Geef een jaartal: ");
            double jaar = double.Parse(Console.ReadLine());
            double deelBaar400 = jaar % 400;
            double deelBaar100 = jaar % 100;
            double deelBaar4 = jaar % 4;

            if ((deelBaar400 == 0) && (deelBaar100 == 0) && (deelBaar4 == 0))
            {
                Console.WriteLine($"{jaar}: wél schrikkeljaar");
            }
            else if ((deelBaar100 == 0) && (deelBaar4 == 0))
            {
                Console.WriteLine($"{jaar}: geen schrikkeljaar");
            }
            else if (deelBaar4 == 0)
            {
                Console.WriteLine($"{jaar}: wél schrikkeljaar");
            }
            else
            {
                Console.WriteLine($"{jaar}: geen schrikkeljaar");
            }
```

[Terug](../Hfdst5.md)