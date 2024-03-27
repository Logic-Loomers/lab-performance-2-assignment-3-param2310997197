[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/Fmb6W2KK)
Design a C++ program for an employee payroll system. Create classes for Employee and Payroll. Users can add employees, enter hours worked, calculate salaries, and generate payroll reports.
code:
#include<iostream>
using namespace std;
class employee
{
public:
    string employee_name;
    int hrs_worked;
    int rate_per_hour = 500;
    float tax=10;
    float salary;
    void get()
    {
        cout<<"\nEnter name of employee:";
        cin>>employee_name;
        cout<<"\nEnter No. of hours worked:";
        cin>>hrs_worked;
        salary = hrs_worked * rate_per_hour;
    }
    void display()
    {
        cout<<"\nName of Employee is:"<< employee_name<< endl;
        cout<<"\nNo. of hours Worked:"<< hrs_worked<< endl;
    }
};
class payroll
{
  public:
  void payrollcalculator(employee ob1)
  {
    cout<<"\nSalary of employee is:"<< ob1.salary<< endl;
    cout<<"\nPayroll of an employee is:"<<ob1.salary-(ob1.salary*ob1.tax/100)<<endl;
  }
};
int main()
{
    employee ob[3];
    payroll payroll;;
    for (int i=0;i<3;i++)
    {
        ob[i].get();
        ob[i].display();
        payroll.payrollcalculator(ob[i]);
    }
    return 0;
}
