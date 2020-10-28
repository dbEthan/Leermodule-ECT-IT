# Oplossing 1

```csharp
            // decimal is beter voor zaken rond geld.
            const double BTW = 0.21;
            double prijsProductmetBTW = 2.99;
            double prijsProductzonderBTW = prijsProductmetBTW - (prijsProductmetBTW * BTW);
            Console.WriteLine("De koekjes van de ALDI kosten " + prijsProductmetBTW + " euro met BTW");
            Console.WriteLine("De koekjes van de ALDI kosten " + prijsProductzonderBTW + " euro zonder BTW");
```

[Terug](../Hfdst2.md)