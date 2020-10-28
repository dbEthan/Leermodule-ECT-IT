# Oplossing 1

```csharp
            Random casino = new Random();
            int keuzeCasino = casino.Next(1, 7);

            Console.Write("Welke cijfer heeft de computer geworpen (1 tem 6) : ");
            int gok = int.Parse(Console.ReadLine());

            if (gok == keuzeCasino)
            {
                Random casino2 = new Random();
                int keuzeCasino2 = casino2.Next(1, 7);


                Console.Write("Welke cijfer heeft de computer geworpen (1 tem 6) : ");
                 gok = int.Parse(Console.ReadLine());


                if (gok == keuzeCasino2)
                {
                    Random casino3 = new Random();
                    int keuzeCasino3 = casino3.Next(1, 7);


                    Console.Write("Welke cijfer heeft de computer geworpen (1 tem 6) : ");
                    gok = int.Parse(Console.ReadLine());


                    if (gok == keuzeCasino3)
                    {
                        Console.WriteLine("Proficiat");
                    }



                }

                else
                {
                    Console.WriteLine("You lose");
                }

            }
            else
            {
                Console.WriteLine("You lose");
            }
```

[Terug](../Hfdst5.md)