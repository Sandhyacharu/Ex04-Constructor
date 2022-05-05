# Ex04-Constructor
## Aim:
 To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.
 
 ## Algorithm:
 ### Step1:
 
 
 
 ## Program:
 ```c#
 using System;
namespace Hello
{
    class Employee
    {
        public string name, designation;
        public int experience, insurance, basicsalary;
        public float hra, ta, income;
        public Employee(string name, string designation, int experience, int basicsalary, int insurance)
        {
            this.name = name;
            this.designation = designation;
            this.experience = experience;
            this.basicsalary = basicsalary;
            this.insurance = insurance;
        }
            public void salary()
            {
                hra = (20 / 100) * this.basicsalary;
                ta = (10 / 100) * this.basicsalary;
                income = hra + ta + this.basicsalary - this.insurance;
            }
            void display()
            {
                Console.WriteLine("Name of the employee is {0} having {1} of experience, working as {2}", this.name, this.experience, this.designation);
                Console.WriteLine("Receives {0} of salary", income);
            }
            static void Main(String[] args)
            {
                Employee emp1 = new Employee("Hari", "Tester", 10, 30000, 1000);
                emp1.salary();
                emp1.display();
            }
        }

    }
```
 ## Output:
 ![image](https://user-images.githubusercontent.com/75235167/166907329-b53bad31-b1b4-4f24-be0a-7ec501d4e894.png)

 ## Result:
