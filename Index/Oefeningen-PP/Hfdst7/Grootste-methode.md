# Oplossing 1

```csharp
class Program
    {
        static int GrootsteGetal(int a, int b, int c)
        {
            int result = a;
            if (b > a && b > c)
                result = b;
            else if (c > a && c > b)
                result = c;
            return result;
        }
        static void Main(string[] args)
        {
            Console.WriteLine("Voer 3 getallen in: (druk telkens op ENTER)");
            int a = int.Parse(Console.ReadLine());
            int b = int.Parse(Console.ReadLine());
            int c = int.Parse(Console.ReadLine());
            Console.Write("Het grootste getal is: ");
            Console.WriteLine(GrootsteGetal(a, b, c));
        }
    }
```
[Terug](../Hfdst7.md)