# CSHARPNOTES
1
static void Main(string[] args)
        {
            Console.WriteLine("Bir isim giriniz: ");
            string name = Console.ReadLine();
            Console.WriteLine("İsminiz:" + name);
        }
2
static void Main(string[] args)
        {
            Console.WriteLine("Bir isim giriniz: ");
            string name = Console.ReadLine();

            while (true)
            {
                if (name.Length < 6)
                {
                    break;
                }

                Console.WriteLine("İsminizin harf sayısı 6dan fazla oldu lütfen tekrardan giriniz: ");
                name = Console.ReadLine();              
            }
        }
3
static void Main(string[] args)
        {
            int number1 = 0;
            int number2 = 0;

            Console.WriteLine("Bir sayı giriniz: ");
            number1 = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Bir sayı daha giriniz: ");
            number2 = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("İki sayının toplamı: " + (number1 + number2));
        }
4
static void Main(string[] args)
        {
            int number1 = 0;
            int number2 = 0;

            Console.WriteLine("Bir sayı giriniz: ");
            number1 = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Bir sayı daha giriniz: ");
            number2 = Convert.ToInt32(Console.ReadLine());

            if (number1 % number2 == 0 && number2 % number1 == 0)
            {
                Console.WriteLine("Sayılar birbirlerinin katıdır");
            }

            else
            {
                Console.WriteLine("Sayılar birbirlerinin katı değildir");
            }
        }
5

6
 static void Main(string[] args)
        {
            int number1 = 0;

            int digit1 = 0;
            int digit3 = 0;

            Console.WriteLine("Bir sayı giriniz: ");
            number1 = Convert.ToInt32(Console.ReadLine());

            while (true)
            {
                if (number1 > 99 && number1 < 1000)
                {
                    break;
                }

                Console.WriteLine("Girdiğiniz sayı 100den büyük ve 1000den küçük olmalıdır lütfen tekrardan giriniz: ");
                number1 = Convert.ToInt32(Console.ReadLine());
            }

            digit1 = number1 % 100;
            digit3 = number1 / 100;

            Console.WriteLine($"Birler Basamağı: " + digit1);
            Console.WriteLine($"Yüzlerler Basamağı: " + digit3);
        }
7?
static void Main(string[] args)
        {
            int number1 = 100;
            int count = 0;

            int digit1 = number1 % 100;
            int digit2 = (number1 % 100) / 10;
            int digit3 = number1 / 100;

            while (number1 < 1000)
            {
                digit1 = number1 % 100;
                digit2 = (number1 % 100) / 10;
                digit3 = number1 / 100;

                if (digit1 != digit2 && digit1 != digit3 && digit2 != digit3)
                {
                    //Console.WriteLine(number1);
                    count++;
                }

                number1++;
            }

            Console.WriteLine(count);
        }
8
static void Main(string[] args)
        {
            int number1 = 100;
            int number2 = 0;

            int digit1 = number1 % 100;
            int digit2 = (number1 % 100) / 10;
            int digit3 = number1 / 100;

            while (number1 < 1000)
            {
                digit1 = number1 % 100;
                digit2 = (number1 % 100) / 10;
                digit3 = number1 / 100;

                if (digit1 != digit2 && digit1 != digit3 && digit2 != digit3 && number1 % 2 == 0)
                {
                    //Console.WriteLine(number1);


                    number2 = number2 + number1;
                }

                number1++;
            }

            Console.WriteLine(number2);
        }
9 
static void Main(string[] args)
        {
             

            int okunanSayfaSayısı = 5;
            int okuduguSayfa = 10;
            int toplamSayfaSayısı = 3100;
            int count = 1;

            while (okunanSayfaSayısı < toplamSayfaSayısı)
            {
                okunanSayfaSayısı = okunanSayfaSayısı + okuduguSayfa;
                okuduguSayfa = okuduguSayfa + 10;
                count++;
            }

            Console.WriteLine(count);
        }
----------------------------------------------------------------------------------
1
static void Main(string[] args)
        {
            Console.WriteLine("Telefon Numarası Giriniz: ");
            string phone = Console.ReadLine();

            string part1 = phone.Substring(0, 3);
            string part2 = phone.Substring(3, 3);
            string part3 = phone.Substring(6);
            string outcome = string.Format("{0}-{1}-{2}", part1, part2, part3);

            Console.WriteLine(outcome);
        }
2?
 static void Main(string[] args)
        {
            int number1 = 0;

            int digit1 = number1 % 1000;
            int digit2 = (number1 % 100) / 10;
            int digit3 = (number1 % 1000) / 100;
            int digit4 = number1 / 1000;

            int armstrong1 = digit1 * digit1 * digit1 * digit1;
            int armstrong2 = digit2 * digit2 * digit2 * digit2;
            int armstrong3 = digit3 * digit3 * digit3 * digit3;
            int armstrong4 = digit4 * digit4 * digit4 * digit4;

            int armstrongSum = armstrong1 + armstrong2 + armstrong3 + armstrong4;


            Console.WriteLine("Dört basamaklı bir sayı giriniz");
            number1 = Convert.ToInt32(Console.ReadLine());         
            
            while (true)
            {
                if (number1 > 999 && number1 < 10000)
                {
                    break;
                }

                Console.WriteLine("Girdiğiniz sayı 1000den büyük ve 10000den küçük olmalıdır lütfen tekrardan giriniz: ");
                number1 = Convert.ToInt32(Console.ReadLine());
            }

            if (armstrongSum == number1)
            {
                Console.WriteLine("Sayı bir armstrong sayıdır");
            }

            else
            {
                Console.WriteLine("Sayı bir armstrong sayı değildir");
            }

        }
3
---
4
---
5
static void Main(string[] args)
        {
            Random rnd = new Random();

            int count = 0;

            for (int i = 0; i < 10000; i++)
            {
                int num = rnd.Next(3, 13);

                if (num == 5)
                {
                    count++;
                }
            }

            Console.WriteLine(count);
        }
6
static void Main(string[] args)
        {
            Random rnd = new Random();

            int number1 = 0;
            int count = 0;

            Console.WriteLine("Bir sayı giriniz");
            number1 = Convert.ToInt32(Console.ReadLine());

            while (true)
            {
                if (number1 > 3 && number1 < 13)
                {
                    break;
                }

                Console.WriteLine("Girdiğiniz sayı 3ten büyük ve 13ten küçük olmalıdır lütfen tekrardan giriniz: ");
                number1 = Convert.ToInt32(Console.ReadLine());
            }

            for (int i = 0; i < 10000; i++)
            {
                int num = rnd.Next(3, 13);

                if (num == number1)
                {
                    count++;
                }
            }

            Console.WriteLine(count);
        }
7
 
