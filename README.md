using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Enter the number of ingredients");
            int num_ingredients = Convert.ToInt32(Console.ReadLine());
            string[] ingredients = new string[num_ingredients];
            int[] quantity = new int[num_ingredients];
            string[] unit = new string[num_ingredients];
            for (int i = 0; i < num_ingredients; i++)
            {
                Console.WriteLine("Enter the name of the ingredient");
                ingredients[i] = Console.ReadLine();
                Console.WriteLine("Enter the quantity of the ingredient");
                quantity[i] = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("Enter the unit of the ingredient");
                unit[i] = Console.ReadLine();
            }
            Console.WriteLine("Enter the number of steps");
            int num_steps = Convert.ToInt32(Console.ReadLine());
            string[] steps = new string[num_steps];
            for (int i = 0; i < num_steps; i++)
            {
                Console.WriteLine("Enter the description of the step");
                steps[i] = Console.ReadLine();
            }
            Console.WriteLine("Enter the factor by which you want to scale the recipe");
            int factor = Convert.ToInt32(Console.ReadLine());
            for (int i = 0; i < num_ingredients; i++)
            {
                quantity[i] = quantity[i] * factor;
            }
            Console.WriteLine("Enter the factor by which you want to reset the recipe");
            factor = Convert.ToInt32(Console.ReadLine());
            for (int i = 0; i < num_ingredients; i++)
            {
                quantity[i] = quantity[i] / factor;
            }
            Console.WriteLine("Enter the factor by which you want to clear the recipe");
            factor = Convert.ToInt32(Console.ReadLine());
            for (int i = 0; i < num_ingredients; i++)
            {
                quantity[i] = 0;
            }
            for (int i = 0; i < num_ingredients; i++)
            {
                Console.WriteLine(ingredients[i] + " " + quantity[i] + " " + unit[i]);
            }
            for (int i = 0; i < num_steps; i++)
            {
                Console.WriteLine(steps[i]);
            }
        }
    }
}
