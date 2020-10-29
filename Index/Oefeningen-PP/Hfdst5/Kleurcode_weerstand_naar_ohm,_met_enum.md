# Oplossingen

## Oplossing 1

```csharp
        enum kleuren
        {
            zwart,
            bruin,
            rood,
            oranje,
            geel,
            groen,
            blauw,
            violet,
            wit,
            grijs,
            goud,
            zilver
        }

        static void Main(string[] args)
        {
            int ring1 = 0;
            int ring2 = 0;
            int ring3 = 0;



            Console.WriteLine("Inputs: zwart, bruin, rood, oranje, geel, groen, blauw, violet, wit, grijs, goud, zilver");
            Console.WriteLine("Programma is hoofdletter gevoelig");

            Console.WriteLine("Geef de ringen");

            Console.Write("Ring1: ");
            string ringEen = Console.ReadLine();
            Console.Write("Ring2: ");
            string ringTwee = Console.ReadLine();
            Console.Write("Ring3: ");
            string ringDrie = Console.ReadLine();


            //EERSTE RING
            if (ringEen == Convert.ToString(kleuren.zwart))
            {
                ring1 = 0;
            }

            else if (ringEen == Convert.ToString(kleuren.bruin))
            {
                ring1 = 1;
            }

            else if (ringEen == Convert.ToString(kleuren.rood))
            {
                ring1 = 2;
            }

            else if (ringEen == Convert.ToString(kleuren.oranje))
            {
                ring1 = 3;
            }

            else if (ringEen == Convert.ToString(kleuren.geel))
            {
                ring1 = 4;
            }

            else if (ringEen == Convert.ToString(kleuren.groen))
            {
                ring1 = 5;
            }

            else if (ringEen == Convert.ToString(kleuren.blauw))
            {
                ring1 = 6;
            }
            else if (ringEen == Convert.ToString(kleuren.violet))
            {
                ring1 = 7;
            }
            else if (ringEen == Convert.ToString(kleuren.wit))
            {
                ring1 = 8;
            }
            else if (ringEen == Convert.ToString(kleuren.grijs))
            {
                ring1 = 9;
            }

            //TWEEDE RING
            if (ringTwee == Convert.ToString(kleuren.zwart))
            {
                ring2 = 0;
            }

            else if (ringTwee == Convert.ToString(kleuren.bruin))
            {
                ring2 = 1;
            }

            else if (ringTwee == Convert.ToString(kleuren.rood))
            {
                ring2 = 2;
            }

            else if (ringTwee == Convert.ToString(kleuren.oranje))
            {
                ring2 = 3;
            }

            else if (ringTwee == Convert.ToString(kleuren.geel))
            {
                ring2 = 4;
            }

            else if (ringTwee == Convert.ToString(kleuren.groen))
            {
                ring2 = 5;
            }

            else if (ringTwee == Convert.ToString(kleuren.blauw))
            {
                ring2 = 6;
            }
            else if (ringTwee == Convert.ToString(kleuren.violet))
            {
                ring2 = 7;
            }
            else if (ringTwee == Convert.ToString(kleuren.wit))
            {
                ring2 = 8;
            }
            else if (ringTwee == Convert.ToString(kleuren.grijs))
            {
                ring2 = 9;
            }

            //DERDE RING
            if (ringDrie == Convert.ToString(kleuren.zwart))
            {
                ring3 = 0;
            }

            else if (ringDrie == Convert.ToString(kleuren.bruin))
            {
                ring3 = 1;
            }

            else if (ringDrie == Convert.ToString(kleuren.rood))
            {
                ring3 = 2;
            }

            else if (ringDrie == Convert.ToString(kleuren.oranje))
            {
                ring3 = 3;
            }

            else if (ringDrie == Convert.ToString(kleuren.geel))
            {
                ring3 = 4;
            }

            else if (ringDrie == Convert.ToString(kleuren.groen))
            {
                ring3 = 5;
            }

            else if (ringDrie == Convert.ToString(kleuren.blauw))
            {
                ring3 = 6;
            }
            else if (ringDrie == Convert.ToString(kleuren.violet))
            {
                ring3 = 7;
            }
            else if (ringDrie == Convert.ToString(kleuren.goud))
            {
                ring3 = -1;
            }
            else if (ringDrie == Convert.ToString(kleuren.zilver))
            {
                ring3 = -2;
            }

            //RESULTAAT
            double resultaat = ((ring1 * 10) + ring2) * Math.Pow(10, ring3);
            Console.WriteLine($"Deze weerstand heeft een waarde van {resultaat} Ohm");
        }

```

## Oplossing 2

```csharp
        enum kleuren
        {
            zilver = -2,
            goud,
            zwart,
            bruin,
            rood,
            oranje,
            geel,
            groen,
            blauw,
            violet,
            wit,
            grijs
        }
        static void Main(string[] args)
        {



            Console.WriteLine("Inputs: zwart, bruin, rood, oranje, geel, groen, blauw, violet, wit, grijs, goud, zilver");
            Console.WriteLine("Programma is hoofdletter gevoelig");

            Console.WriteLine("Geef de ringen");
            Console.Write("Ring1: ");
            kleuren ringEen = (kleuren)Enum.Parse(typeof(kleuren), Console.ReadLine());
            Console.Write("Ring2: ");
            kleuren ringTwee =(kleuren)Enum.Parse(typeof(kleuren), Console.ReadLine());
            Console.Write("Ring3: ");
            kleuren ringDrie = (kleuren)Enum.Parse(typeof(kleuren), Console.ReadLine());

            int ring1 = (int)ringEen;
            int ring2 = (int)ringTwee;
            int ring3 = (int)ringDrie;

            double resultaat = ((ring1 * 10) + ring2) * Math.Pow(10, ring3);
            Console.WriteLine($"Deze weerstand heeft een waarde van {resultaat} Ohm");
        }

[Terug](../Hfdst5.md)