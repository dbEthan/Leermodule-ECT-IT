# Oplossing 1

```csharp
class Program
    {
        static void Main(string[] args)
        {
            string input;
            string output = "";
            string conversion = "";
            int teller = 0;

            while (teller < 12)
            {
                input = Console.ReadLine();
                if (input == "G")
                    output = "C";
                else if (input == "C")
                    output = "G";
                else if (input == "T")
                    output = "A";
                else if (input == "A")
                    output = "U";
                conversion += output;
                teller++;
            }
            Console.WriteLine(conversion);
        }
    }
```

[Terug](../Hfdst6.md)