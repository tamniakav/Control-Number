using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Exam6
{
    class Exam6
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());
            int m = int.Parse(Console.ReadLine());
            int num = int.Parse(Console.ReadLine());

            int sum = 0;
            int b = 0;

            for (int i = 1; i <= n; i++)
            {
                int a = m;            

                for (int j = m - 1; j >= 0; j--)
                {
                    sum = sum + (i * 2) + (a * 3);
                    a--;
                    if (sum >= num)
                    {
                        b = i * m - j;
                        break;
                    }
                }
                if (sum >= num)
                {
                    break;
                }
            }
            if (sum >= num)
            {
                Console.WriteLine("{0} moves", b);
                Console.WriteLine("Score: {0} >= {1}", sum, num);
            }
            else
            {
                Console.WriteLine("{0} moves", m * n);
            }
        }
    }
}
