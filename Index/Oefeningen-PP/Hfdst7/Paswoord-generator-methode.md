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

            for (int i = 0; i < length; i++)        //for-loop itereert tot de gegeven lengte van het paswoord bereikt is
            {
                int ranChooser = gen.Next(0, 3);    //genereert 1 van de 3 mogelijke unicode-karakter generators
                Ran y = (Ran)ranChooser;
                switch (y)                          
                {
                    case Ran.Ran1:                  
                        ran = gen.Next(48, 58);     //cijfers 0-9
                        break;
                    case Ran.Ran2:
                        ran = gen.Next(65, 91);     //hoofdletters A-Z
                        break;
                    case Ran.Ran3:
                        ran = gen.Next(97, 123);    //kleine letters a-z
                        break;
                }
                char x = Convert.ToChar(ran);       //1 van de 3 generators wordt geconverteerd naar een char
                result += x;                        //de gekregen char wordt toegevoegd aan de string "result"
            }
            return result;                          //het resultaat is een string van willekeurige karakters van het gegeven lengte.
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