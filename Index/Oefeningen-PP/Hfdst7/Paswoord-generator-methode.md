# Oplossing 1

```csharp
class Program
    {
        enum Ran { Ran1, Ran2, Ran3}
        static string RandomPassGen(int length)
        {
            /* Unicode numbers: 
             * 0-9 = 48 - 57
             * A-Z = 65 - 90
             * a - z = 97 - 122
             */
            Random gen = new Random();
            string result = "";
            int ran = 0;

            for (int i = 0; i < length; i++)
            {
                int ranChooser = gen.Next(0, 3);
                Ran y = (Ran)ranChooser;
                switch (y)
                {
                    case Ran.Ran1:
                        ran = gen.Next(48, 58);
                        break;
                    case Ran.Ran2:
                        ran = gen.Next(65, 91);
                        break;
                    case Ran.Ran3:
                        ran = gen.Next(97, 123);
                        break;
                }
                char x = Convert.ToChar(ran);
                result += x;
            }
            return result;
        }
        static void Main(string[] args)
        {
            Console.Write($"- random password generator -\nEnter length of new password: ");
            int input = int.Parse(Console.ReadLine());
            Console.Write($"\nYour new password is: ");
            Console.WriteLine(RandomPassGen(input));
        }
    }
}
```
[Terug](../Hfdst7.md)