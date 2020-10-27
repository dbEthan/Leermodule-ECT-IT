# Oplossing 1

```csharp
            Console.WriteLine("Geef de eerste 3 cijfers van je bankrekeningnummer:");
            string eerste = Console.ReadLine();

            Console.WriteLine("Geef de volgende 7 cijfers van je bankrekeningnummer:");
            string tweede = Console.ReadLine();

            Console.WriteLine("Geef de laatste 2 cijfers van je bankrekeningnummer:");
            int laatste = int.Parse(Console.ReadLine());

            int eersteTien = Convert.ToInt32(eerste + tweede);
            int rest = eersteTien % 97;



            if (rest == laatste)
            {
                Console.WriteLine("Het bankrekeningnummer is geldig!");
            }
            else
            {
                Console.WriteLine("Het bankrekeningnummer is niet geldig.");
            }
```
# Oplossing 2
            
```csharp
            Console.WriteLine("Geef de eerste 3 cijfers van je bankrekeningnummer:");
            string eerste = Console.ReadLine();

            Console.WriteLine("Geef de volgende 7 cijfers van je bankrekeningnummer:");
            string tweede = Console.ReadLine();

            Console.WriteLine("Geef de laatste 2 cijfers van je bankrekeningnummer:");
            int laatste = int.Parse(Console.ReadLine());

            int eersteTien = Convert.ToInt32(eerste + tweede);
            int rest = eersteTien % 97;



            if (rest == laatste)
            {
                Console.WriteLine("Het bankrekeningnummer is geldig!");
            }
            else
            {
                Console.WriteLine("Het bankrekeningnummer is niet geldig.");
            }
```


[Terug](../Hfdst5.md)