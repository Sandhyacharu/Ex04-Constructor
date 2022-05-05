# Ex04-Constructor
## Aim:
 To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.
 
 ## Algorithm:
### Step1:
Start.

### Step2:
Create a class and a constructor.

### Step3:
Get name, designation, noofexperience, basic salary and insurance amount from the User.

### Step4:
Call salary method in constructor to calculate salary.

### Step5:
Call display method to display the output.

### Step6:
stop.
 
## Program:
 ```c#
using System;
namespace Hello
{
    class Employee
    {
        public string name, designation;
        int experience, insurance, basicsalary;
        float hra, ta, income;

        public Employee(string name, string designation, int experience, int basicsalary, int insurance)
        {
            this.name = name;
            this.designation = designation;
            this.experience = experience;
            this.basicsalary = basicsalary;
            this.insurance = insurance;
            salary();
            display();
        }
        public void salary()
        {
            hra = (20 * basicsalary) / 100;
            ta = (10 * basicsalary) / 100;
            income = hra + basicsalary + ta - insurance;
        }
        public void display()
        {
            Console.WriteLine("Name of the employee is {0} having {1} of experience, working as {2}", this.name, this.experience, this.designation);
            Console.WriteLine("Receives {0} of salary", income);
        }
        public class program
        {
            static void Main(String[] args)
            {
                string name, designation;
                int experience, basicsalary, insurance, n;
                Console.WriteLine("No of employees: ");
                n = Convert.ToInt32(Console.ReadLine());
                for (int i = 1; i <= n; i++)
                {
                    Console.WriteLine("Name of the employee: ");
                    name = Console.ReadLine();
                    Console.WriteLine("Designation of the employee: ");
                    designation = Console.ReadLine();
                    Console.WriteLine("Years of experience: ");
                    experience = Convert.ToInt32(Console.ReadLine());
                    Console.WriteLine("Basic salary of the employee: ");
                    basicsalary = Convert.ToInt32(Console.ReadLine());
                    Console.WriteLine("insurance: ");
                    insurance = Convert.ToInt32(Console.ReadLine());
                    Employee emp = new Employee(name, designation, experience, basicsalary, insurance);
                }


            }
        }
    }
}
```
## Output:
![image](https://user-images.githubusercontent.com/75235167/166965168-39c98cb0-eac8-4b6c-ace1-79d9666f8b16.png)

## Result:
Thus the C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor is executed successfully.
