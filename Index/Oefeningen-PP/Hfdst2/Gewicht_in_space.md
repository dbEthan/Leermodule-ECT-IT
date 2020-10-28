# Oplossing 1

```csharp
            //input van de gebruiker
            double gewichtopAarde = 76.0;
            double factorMercurius = 0.38;
            double factorVenus = 0.91;
            double factorMars = 038;
            double factorJupiter = 2.34;
            double factorSaturnus = 1.06;
            double factorUranus = 0.92;
            double factorNeptunus = 1.19;
            double factorPluto = 0.06;

            double gewichtopMercurius = gewichtopAarde * factorMercurius;
            double gewichtopVenus = gewichtopAarde * factorVenus;
            double gewichtopMars = gewichtopAarde * factorMars;
            double gewichtopJupiter = gewichtopAarde * factorJupiter;
            double gewichtopSaturnus = gewichtopAarde * factorSaturnus;
            double gewichtopUranus = gewichtopAarde * factorUranus;
            double gewichtopNeptunus = gewichtopAarde * factorNeptunus;
            double gewichtopPluto = gewichtopAarde * factorPluto;

            Console.WriteLine("Je weegt op Mercurius " + gewichtopMercurius + "Kg.");
            Console.WriteLine("Je weegt op Venus " + gewichtopVenus + "Kg.");
            Console.WriteLine("Je weegt op Aarde " + gewichtopAarde + "Kg.");
            Console.WriteLine("Je weegt op Mars " + gewichtopMars + "Kg.");
            Console.ForegroundColor = ConsoleColor.Red;
            Console.WriteLine("Je weegt op Jupiter " + gewichtopJupiter + "Kg.");
            Console.ResetColor();
            Console.WriteLine("Je weegt op Saturnus " + gewichtopSaturnus + "Kg.");
            Console.WriteLine("Je weegt op Uranus " + gewichtopUranus + "Kg.");
            Console.WriteLine("Je weegt op Neptunus " + gewichtopNeptunus + "Kg.");
            Console.ForegroundColor = ConsoleColor.Green;
            Console.WriteLine("Je weegt op Pluto " + gewichtopPluto + "Kg.");
            Console.ResetColor();
```

[Terug](../Hfdst2.md)