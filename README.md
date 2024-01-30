        static void Main(string[] args)
        {
            Random RandomObj = new Random();

            int tæller = 0;
            int[] AntalØjne = new int[6];

            do
            {

                int øjne = RandomObj.Next(1, 7);
                tæller++;
                Console.WriteLine("Terning viste: {0}", øjne);
                AntalØjne[øjne - 1]++; // Tæller antallet af øjne
            }

            while (tæller < 1000);
            Console.Clear();
            Console.WriteLine("***********************");
            Console.WriteLine("Så mange 1-6'ere har du");
            Console.WriteLine("");

            for (int i = 0; i < AntalØjne.Length; i++)
            {
                Console.WriteLine("{0} -> {1} Øjne", i + 1, AntalØjne[i]);
            }
            Console.ReadKey();
        }
    }
}
