# Oplossing 1

```csharp
            int r1;
            int r2;
            int r3;


            Console.Write("Ring 1: ");
            r1 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Ring 2: ");
            r2 = Convert.ToInt32(Console.ReadLine());

            Console.Write("Ring 3: ");
            r3 = Convert.ToInt32(Console.ReadLine());


            double totaal = ((r1 * 10) + (r2)) * Math.Pow(10, r3);
            totaal = Math.Round(totaal, 2);
            Console.Clear();

            Console.WriteLine($"╔═══════════════╦═══════════════╗");
            Console.WriteLine($"║  R1 ║ R2 ║  R3║  Totaal(ohm)  ║");
            Console.WriteLine($"╟───────────────╫───────────────╢");
            Console.Write("║");
            switch (r1)
            {
                case 0:
                    Console.ForegroundColor = Color.Black;
                    Console.BackgroundColor = Color.White;
                    Console.Write($"  {r1}  ");
                    break;
                case 1:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Brown;
                    Console.Write($"  {r1}  ");
                    break;
                case 2:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Red;
                    Console.Write($"  {r1}  ");
                    break;
                case 3:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Orange;
                    Console.Write($"  {r1}  "); ;
                    break;
                case 4:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Yellow;
                    Console.Write($"  {r1}  ");
                    break;
                case 5:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Green;
                    Console.Write($"  {r1}  ");
                    break;
                case 6:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Blue;
                    Console.Write($"  {r1}  ");
                    break;
                case 7:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Purple;
                    Console.Write($"  {r1}  ");
                    break;
                case 8:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Gray;
                    Console.Write($"  {r1}  ");
                    break;
                case 9:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.White;
                    Console.Write($"  {r1}  ");
                    break;
                default:
                    Console.WriteLine("N/A");
                    break;
            }

            Console.ResetColor();
            Console.Write("║");

            switch (r2)
            {
                case 0:
                    Console.ForegroundColor = Color.Black;
                    Console.Write($" {r2}  ");
                    break;
                case 1:
                    Console.ForegroundColor = Color.Brown;
                    Console.Write($" {r2}  ");
                    break;
                case 2:
                    Console.ForegroundColor = Color.Red;
                    Console.Write($" {r2}  ");
                    break;
                case 3:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Orange;
                    Console.Write($"  {r2} ");
                    break;
                case 4:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Yellow;
                    Console.Write($"  {r2} ");
                    break;
                case 5:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Green;
                    Console.Write($"  {r2} ");
                    break;
                case 6:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Blue;
                    Console.Write($"  {r2} ");
                    break;
                case 7:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Purple;
                    Console.Write($"  {r2} ");
                    break;
                case 8:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Gray;
                    Console.Write($"  {r2} ");
                    break;
                case 9:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.White;
                    Console.Write($"  {r2} ");
                    break;
                default:
                    Console.WriteLine("N/A");
                    break;
            }

            Console.ResetColor();
            Console.Write("║");

            switch (r3)
            {

                case -2:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Silver;
                    Console.Write($" {r3} ");
                    break;
                case -1:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Gold;
                    Console.Write($" {r3} ");
                    break;
                case 0:
                    Console.ForegroundColor = Color.Black;
                    Console.BackgroundColor = Color.White;
                    Console.Write($" {r3}  ");
                    break;
                case 1:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Brown;
                    Console.Write($" {r3}  ");
                    break;
                case 2:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Red;
                    Console.Write($" {r3}  ");
                    break;
                case 3:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Orange;
                    Console.Write($" {r3}  ");
                    break;
                case 4:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Yellow;
                    Console.Write($" {r3}  ");
                    break;
                case 5:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Green;
                    Console.Write($" {r3}  ");
                    break;
                case 6:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Blue;
                    Console.Write($" {r3}  ");
                    break;
                case 7:
                    Console.ResetColor();
                    Console.ForegroundColor = Color.Purple;
                    Console.Write($" {r3}  ");
                    break;
                default:
                    Console.WriteLine("N/A");
                    break;
            }

            Console.ResetColor();
            Console.Write("║");

            Console.ResetColor();
            Console.WriteLine($"    {totaal} ohm  ");
            Console.WriteLine("╚═══════════════╩═══════════════╝");

            Console.ResetColor();
            Console.WriteLine($"De weerstandswaarde is {totaal} ohm.");
            System.Console.WriteLine();
            System.Console.WriteLine("-1 = goud \n 1 = bruin \n 3 = oranje\n-2 = zilver\n 9 = wit");
```

[Terug](../Hfdst3.md)