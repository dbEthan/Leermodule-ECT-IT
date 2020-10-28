# Oplossing 1

```csharp
            const int schoenZonderKorting = 20;
            const int schoenMetKorting = 10;

            Console.Write("Voor hoeveel schoenen geldt de korting niet: ");
            int geenKorting = int.Parse(Console.ReadLine());

            Console.Write("Hoeveel paar schoenen: ");
            int aantalSchoenen = int.Parse(Console.ReadLine());

            if (aantalSchoenen >= geenKorting)
            {
                Console.WriteLine($"Voor {aantalSchoenen} schoenen moet je {(geenKorting * schoenZonderKorting) + ((aantalSchoenen-geenKorting)*schoenMetKorting)} euro betalen. ");
            }

            else
            {
                Console.WriteLine($"Voor {aantalSchoenen} moet je {aantalSchoenen*schoenZonderKorting} euro betalen");
            }
```

[Terug](../Hfdst5.md)