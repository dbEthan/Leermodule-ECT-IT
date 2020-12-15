# Oplossing 1

```csharp
class Program
    {
        static void MyIntro(string naam, int leeftijd, string straat)
        {
            Console.WriteLine($"Mijn naam is {naam}, ik ben {leeftijd} jaar oud en ik woon in de {straat}.");
        }
        static void Main(string[] args)
        {
            Console.Write("Voer je naam in: ");
            string a = Console.ReadLine();
            Console.Write("Voer je leeftijd in: ");
            int b = int.Parse(Console.ReadLine());
            Console.Write("Voer je straatnaam in: ");
            string c = Console.ReadLine();
            MyIntro(a, b, c);
        }
    }
```
[Terug](../Hfdst7.md)