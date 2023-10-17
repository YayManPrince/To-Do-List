# To-Do-List
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

class ToDo
{
    static void Main(string[] args)
    {
        Console.WriteLine("Welcome, this is a to do list");
        List<string> taskList = new List<string>();
        string option = " ";

        while (option != "e")
        {
            Console.WriteLine("what would you like to do:");
            Console.WriteLine("Enter 1. to add to the to do list");
            Console.WriteLine("Enter 2. to remove a to do");
            Console.WriteLine("Enter 3. to view the list");
            Console.WriteLine("Enter e to exit!");

            option = Console.ReadLine();

            if(option == "1")
            {
                Console.WriteLine("Add");
                string task = Console.ReadLine();
                taskList.Add(task);
            }
            else if(option == "2")
            {
                for (int i = 0; i < taskList.Count; i++)
                {
                    Console.WriteLine(i + ":" + taskList[i]);
                }
                Console.WriteLine("Please enter the number of the task to remove from the list");
                int taskNumber = Convert.ToInt32(Console.ReadLine);
                taskList.RemoveAt(taskNumber);
            }
            else if (option == "3")
            {
                Console.WriteLine("Current List");
                for (int i = 0; i < taskList.Count; i++)
                {
                    Console.WriteLine(taskList[i]);
                }

            }
            else if(option != "e")
            {
                Console.WriteLine("exiting List");
            }
            else
            {
                Console.WriteLine("Invalid Option! Try again");

            }
            Console.WriteLine("Thank You!");
        }
    }

}
