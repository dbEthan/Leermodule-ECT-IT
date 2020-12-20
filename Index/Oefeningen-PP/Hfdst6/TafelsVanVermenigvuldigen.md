# Oplossing 1

```csharp
class Program
    {
        static void Main(string[] args)
        {
            int tellerA = 0;
            int tellerB = 0;
            int product = 0;
            
            while (tellerA < 10)
            {
                tellerA++;
                tellerB = 0;
                while (tellerB < 10)
                {
                    tellerB++;
                    product = tellerA * tellerB;
                    Console.WriteLine($"{tellerA} * {tellerB} = {product}");
                }

            }
        }
    }
```

[Terug](../Hfdst6.md)