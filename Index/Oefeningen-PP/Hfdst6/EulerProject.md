# Oplossing 1

```csharp
class Program
    {
        static void Main(string[] args)
        {
            int som = 0;
            for (int getal = 0; getal <= 1000; getal++)
            {
                if (getal % 3 == 0 || getal % 5 == 0)
                    som += getal;
            }
            Console.WriteLine(som);
        }
    }
```

[Terug](../Hfdst6.md)   