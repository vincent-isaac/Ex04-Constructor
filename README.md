### EX NO : 04
# <p align="center">Constructor</p>
## Aim:
 To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.
 
 ## Algorithm:
 ### Step1: 
Start
### Step2:
Create a class and a constructor
### Step3:
Get name, designation, noofexperience, basic salary and insurance amount from the User.
### Step4:
call salary method in constructor to calculate salary.
### Step5:
call display method to display the output.
### Step6:
stop

<br/><br/><br/><br/><br/><br/><br/>


 ## Program:
 ```c#
using System;
namespace program4
{
   public class employee
   {
       public string name, designation;
       public int exp, bs, ins, hra = 0, ta = 0, s = 0;
       void salary(int bs,int ins)
       {
           hra = (20 * bs) / 100;
           ta = (10 * bs) / 100;
           s = bs + hra + ta-ins;
       }
       void display()
       {
           Console.WriteLine("Name of the employee is "+this.name+ " having "+this.exp+ " of experience, working as "+this.designation);
           Console.WriteLine("Receives " + s + " of salary");
       }
       public employee(string name, string designation, int exp, int bs, int ins)
       {
           this.name = name;
           this.designation = designation;
           this.exp = exp;
           this.bs = bs;
           this.ins = ins;
           salary(bs,ins);
           display();
       }
           
   }
   public class program
   {   
       static void Main(String[] args)
       {
           string nam, desig;
           int exp, bs, ins,n;
           Console.WriteLine("Enter no of employees: ");
           n = Convert.ToInt32(Console.ReadLine());
           for (int i = 1; i <= n; i++)
           {
               Console.WriteLine("Enter name of the employee: ");
               nam = Console.ReadLine();
               Console.WriteLine("Enter designation of the employee: ");
               desig = Console.ReadLine();
               Console.WriteLine("Enter years of experience of the employee: ");
               exp = Convert.ToInt32(Console.ReadLine());
               Console.WriteLine("Enter basic salary of the employee: ");
               bs = Convert.ToInt32(Console.ReadLine());
               Console.WriteLine("Enter insurance amount: ");
               ins = Convert.ToInt32(Console.ReadLine());
               employee emp = new employee(nam,desig,exp,bs,ins);
           }

           
       }
   }
}
 ```
 ## Output:
 ![exp4 c#](https://user-images.githubusercontent.com/75234588/190058462-c2fe77b9-c4ca-4b1c-ad82-258563102431.PNG)


 ## Result:
 Thus C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor is executed successfully.
