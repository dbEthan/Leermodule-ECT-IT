# Oplossing 1

```csharp
            Random getal = new Random();
            int Randomgetal = getal.Next(1,6);
            Console.WriteLine("Welke getal van 1 t.e.m. 6 denk jij dat de computer heeft geworpen?");
            int inputg = int.Parse(Console.ReadLine());
            if (Randomgetal == inputg)
            {
                Console.WriteLine("Proficiat!");
            }
            else
            {
                Console.WriteLine("You lose!");
            }
```

[Terug](../Hfdst5.md)