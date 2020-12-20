# Oplossing 1

```csharp
class Program
    {
        static void Main(string[] args)
        {
            int beer = 100;
            do
            {
                Console.WriteLine($"{beer} bottles of beer on the wall, {beer} bottles of beer.");
                beer--;
                Console.WriteLine($"Take one down and pass it around, {beer} bottles of beer on the wall.");
                Console.WriteLine();
                System.Threading.Thread.Sleep(50);
                if (beer == 1)
                {
                    Console.WriteLine($"{beer} bottle of beer on the wall, {beer} bottle of beer.");
                    Console.WriteLine("Take it down and pass it around, no more bottles of beer on the wall.");
                    Console.WriteLine();
                    Console.WriteLine("No more bottles of beer on the wall, no more bottles of beer.");
                    Console.WriteLine($"Go to the store and buy some more, 99 bottles of beer on the wall!");
                }
            } while (beer > 1);
        }
    }
```

[Terug](../Hfdst6.md)