# c-
123
using System;

namespace rendom

{
    public class Employee
    {
        public Employee()
        { }
        public double salary;
        public double bonus;
        public float pdv;
        public double a;
        public double b;
        public double c;    
        public static void Main(string[] args)
        {
            Architect architect = new Architect();
            architect.setSalary(15000);
            architect.setBonus(3000);
            architect.setPdv(2500);
            Console.WriteLine("Salary: " + architect.salary + "kn");
            Console.WriteLine("Bonus: " + architect.bonus + "kn");
            Console.WriteLine("Pdv:" + architect.pdv + "%");
            Console.WriteLine("Total: " + Math.Round(architect.SetTotalSalary(),2) + "kn");

            Doctor doctor = new Doctor();
            doctor.setSalary(13000);
            doctor.setBonus(4000);
            doctor.setPdv(2200);
            Console.WriteLine("\nSalary: " + doctor.salary + "kn");
            Console.WriteLine("Bonus: " + doctor.bonus + "kn");
            Console.WriteLine("Pdv:" + doctor.pdv + "%");
            Console.WriteLine("Total: " + Math.Round(doctor.SetTotalSalary(), 2) + "kn");

            Teacher teacher = new Teacher();
            teacher.setSalary(9000);
            teacher.setBonus(2000);
            teacher.setPdv(1800);
            Console.WriteLine("\nSalary: " + teacher.salary + "kn");
            Console.WriteLine("Bonus: " + teacher.bonus + "kn");
            Console.WriteLine("Pdv:" + teacher.pdv + "%");
            Console.WriteLine("Total: " + Math.Round(teacher.SetTotalSalary(), 2) + "kn");

            switch (architect) 
            {
                case architect.a > doctor.b and architect.a > teacher.c:
                    Console.WriteLine("Architect has the biggest salary!");
                    break;
                case architect.a < doctor.b and doctor.b > teacher.c:
                    Console.WriteLine("Doctor has the biggest salary!");
                    break;
                case teacher.c > architect.a and teacher.c > doctor.b:
                    Console.WriteLine("Teacher has the biggest salary!");
                    break;
                case architect.a == doctor.b and architect.a > teacher.c:
                    Console.WriteLine("Architect and doctor have the biggest salary!");
                    break;
                case architect.a > doctor.b and architect.a == teacher.c:
                    Console.WriteLine("Architect and teacher have the biggest salary!");
                    break;
                case teacher.c == doctor.b and teacher.c > architect.a:
                    Console.WriteLine("Teacher and doctor have the biggest salary the biggest salary!");
                    break;
                default:
                    Console.WriteLine("Everyone has the same salary");
                    break;


            }
            
            Console.ReadKey();
        }
    }
    public class Architect : Employee
    {
        public void setSalary(double _salary)
        {
            salary = _salary;
        }
        public void setBonus(float _bonus)
        {
            bonus = _bonus;
        }
        public void setPdv(int _pdv)
        {
            pdv = _pdv;
            pdv = pdv/100;
        }
        public double SetTotalSalary()
        {
            a = (salary + bonus) * (100 - pdv);
            return a;
        }
    }
    public class Doctor : Employee
    {
        public void setSalary(double _salary)
        {
            salary = _salary;
        }
        public void setBonus(float _bonus)
        {
            bonus = _bonus;
        }
        public void setPdv(int _pdv)
        {
            pdv = _pdv;
            pdv = pdv / 100;
        }
        public double SetTotalSalary()
        {
            b = (salary + bonus) * (100 - pdv);
            return b;
        }
    }
    public class Teacher : Employee
    {
        public void setSalary(double _salary)
        {
            salary = _salary;
        }
        public void setBonus(float _bonus)
        {
            bonus = _bonus;
        }
        public void setPdv(int _pdv)
        {
            pdv = _pdv;
            pdv = pdv / 100;
        }
        public double SetTotalSalary()
        {
            c = (salary + bonus)*(100-pdv);
            return c;
        }
    }
}
