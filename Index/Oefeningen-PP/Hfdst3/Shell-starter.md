# Oplossing 1

```csharp
            System.Diagnostics.Process process = new System.Diagnostics.Process();
            process.StartInfo.FileName = "hostname";
            process.StartInfo.Arguments = "";
            process.StartInfo.UseShellExecute = false;
            process.StartInfo.RedirectStandardOutput = true;
            process.StartInfo.RedirectStandardError = true;
            process.Start(); //start process

            // Read the output (or the error)
            string output = process.StandardOutput.ReadToEnd(); //normal output
            Console.WriteLine(output);
            string err = process.StandardError.ReadToEnd(); //error output (if any)
            Console.WriteLine(err);
            //Continue
            Console.WriteLine("Klaar");
            process.Close();

            System.Diagnostics.Process process2 = new System.Diagnostics.Process();
            process.StartInfo.FileName = "arp";
            process.StartInfo.Arguments = "-a";
            process.StartInfo.UseShellExecute = false;
            process.StartInfo.RedirectStandardOutput = true;
            process.StartInfo.RedirectStandardError = true;
            process.Start(); //start process

            // Read the output (or the error)
            string output2 = process.StandardOutput.ReadToEnd(); //normal output
            Console.WriteLine(output2);
            string err2 = process.StandardError.ReadToEnd(); //error output (if any)
            Console.WriteLine(err);
            //Continue
            Console.WriteLine("Klaar");
            process.Close();


            System.Diagnostics.Process process3 = new System.Diagnostics.Process();
            process.StartInfo.FileName = "getmac";
            process.StartInfo.Arguments = "";
            process.StartInfo.UseShellExecute = false;
            process.StartInfo.RedirectStandardOutput = true;
            process.StartInfo.RedirectStandardError = true;
            process.Start(); //start process


            // Read the output (or the error)
            string output3 = process.StandardOutput.ReadToEnd(); //normal output
            Console.WriteLine(output3);
            string err3 = process.StandardError.ReadToEnd(); //error output (if any)
            Console.WriteLine(err);
            //Continue
            Console.WriteLine("Klaar");
            process.Close();


            System.Diagnostics.Process process4 = new System.Diagnostics.Process();
            process.StartInfo.FileName = "nslookup ";
            process.StartInfo.Arguments = "google.com";
            process.StartInfo.UseShellExecute = false;
            process.StartInfo.RedirectStandardOutput = true;
            process.StartInfo.RedirectStandardError = true;
            process.Start(); //start process

            // Read the output (or the error)
            string output4 = process.StandardOutput.ReadToEnd(); //normal output
            Console.WriteLine(output4);
            string err4 = process.StandardError.ReadToEnd(); //error output (if any)
            Console.WriteLine(err);
            //Continue
            Console.WriteLine("Klaar");
            process.Close();

            System.Diagnostics.Process process5 = new System.Diagnostics.Process();
            process.StartInfo.FileName = "netstat";
            process.StartInfo.Arguments = "";
            process.StartInfo.UseShellExecute = false;
            process.StartInfo.RedirectStandardOutput = true;
            process.StartInfo.RedirectStandardError = true;
            process.Start(); //start process

            // Read the output (or the error)
            string output5 = process.StandardOutput.ReadToEnd(); //normal output
            Console.WriteLine(output5);
            string err5 = process.StandardError.ReadToEnd(); //error output (if any)
            Console.WriteLine(err);
            //Continue
            Console.WriteLine("Klaar");
            process.Close();
```

[Terug](../Hfdst3.md)