using System;

class Program { static void Main() { Console.WriteLine("1. Daire"); Console.WriteLine("2. Duzbucaqli"); Console.WriteLine("3. Ucbucaq");

    Console.Write("Fiqur secin: ");
    int secim = int.Parse(Console.ReadLine());

    switch (secim)
    {
        case 1:
            Console.Write("Radiusu daxil edin: ");
            double radius = double.Parse(Console.ReadLine());

            double daireSahe = Math.PI * Math.Pow(radius, 2);

            Console.WriteLine("Dairenin sahesi: " + Math.Round(daireSahe, 2));
            break;

        case 2:
            Console.Write("Uzunlugu daxil edin: ");
            double uzunluq = double.Parse(Console.ReadLine());

            Console.Write("Enini daxil edin: ");
            double en = double.Parse(Console.ReadLine());

            double duzbucaqliSahe = uzunluq * en;

            Console.WriteLine("Duzbucaqlinin sahesi: " + Math.Round(duzbucaqliSahe, 2));
            break;

        case 3:
            Console.Write("1-ci teref: ");
            double a = double.Parse(Console.ReadLine());

            Console.Write("2-ci teref: ");
            double b = double.Parse(Console.ReadLine());

            Console.Write("3-cu teref: ");
            double c = double.Parse(Console.ReadLine());

            double s = (a + b + c) / 2;

            double ucbucaqSahe = Math.Sqrt(
                s * (s - a) * (s - b) * (s - c)
            );

            Console.WriteLine("Ucbucagin sahesi: " + Math.Round(ucbucaqSahe, 2));
            break;

        default:
            Console.WriteLine("Yanlis secim!");
            break;
    }
}
}
