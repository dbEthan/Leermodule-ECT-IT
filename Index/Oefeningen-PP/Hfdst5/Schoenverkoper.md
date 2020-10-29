# Oplossing 1

```csharp
            const int SCHOEN_ZONDER_KORTING = 20;
            const int SCHOEN_MET_KORTING = 10;

            Console.Write("Voor hoeveel schoenen geldt de korting niet: ");
            int geenKorting = int.Parse(Console.ReadLine());

            Console.Write("Hoeveel paar schoenen: ");
            int aantalSchoenen = int.Parse(Console.ReadLine());

            if (aantalSchoenen >= geenKorting)
            {
                Console.WriteLine($"Voor {aantalSchoenen} schoenen moet je {(geenKorting * SCHOEN_ZONDER_KORTING) + ((aantalSchoenen-geenKorting)*SCHOEN_MET_KORTING)} euro betalen. ");
            }

            else
            {
                Console.WriteLine($"Voor {aantalSchoenen} moet je {aantalSchoenen*SCHOEN_ZONDER_KORTING} euro betalen");
            }
```

[Terug](../Hfdst5.md)