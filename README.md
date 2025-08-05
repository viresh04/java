##  1st commands line
```py
class lab1{
    public static void main(String args[]){
        int i,x,big;
        big = Integer.parseInt(args[0]);
        for( i = 1; i < args.length;i++)
        {  x = Integer.parseInt(args[i]);
            if( x > big)
            {  big = x;
            }  }
        System.out.println("Biggest = " + big);
    }  }
```
## 2nd class obj
```py
import java.util.*;
class Student{
    String srn;
    String name;
    int m1;
    int m2;
    int m3;
    Double avg;
    void readdata()
    {
        Scanner s = new Scanner(System.in);
        System.out.println("Enter srn");
        srn = s.nextLine();
        System.out.println("Enter name");
        name = s.nextLine();
        System.out.println("Enter m1,m2,m3");
        m1 = s.nextInt();
        m2 = s.nextInt();
        m3 = s.nextInt();
    }
 void compute()
    {
        avg = (m1+m2+m3)/3.0;
    }

    void printdata()
    {
        System.out.println("srn = " + srn + "name = " + name + "m1 = " + m1 + "m2 = " + m2 + "m3 = " + m3 + "avg = " + avg);
    }
}
class lab2{
    public static void main (String args[])
    {
        Student st = new Student();
        st.readdata();
        st.compute();
        st.printdata();
    }
}
```
## 3rd method overloading
```py
import java.util.*;
class MeOverload{

    void area(double r)
    {
        double a = 3.142 * r * r;
        System.out.println("Area of a Circle = " + a);
    }

    void area(int b,int h)
    {
        double a = 0.5 * b * h;
        System.out.println("Area of a Circle = " + a);
    }
}
class lab3a{
    public static void main (String args[])
    {
        MeOverload m = new MeOverload();
        m.area(3,5);
        m.area(3.5);
    }
}
```
## lab3b
```py
//Constructor Overloading
class Ocons{
    String srn;
    String name;
    int marks;

    Ocons()
    {
        srn = "unknown";
        name = "unknown";
        marks = 0;
    }

    Ocons(String s,String n,int m)
    {
        srn = s;
        name = n;
        marks = m;
    }

    void printdata()
    {
        System.out.println("srn = " + srn + "name = " + name + "marks = " + marks );
    }
}
class lab3b
{
    public static void main(String args[])
    {
        Ocons o1 = new Ocons();
        Ocons o2 = new Ocons("1234","xyz",50);
        o1.printdata();
        o2.printdata();
 }
}
```
## inhertitances
```py
import java.util.*;
class A
{
    int a;
    int b;
 
    void getdata()
    {
        Scanner s = new Scanner(System.in);
        System.out.println("Enter a,b");
        a = s.nextInt();
        b = s.nextInt();
    }

    void printdata()
    {
        System.out.println("a = " + a);
        System.out.println("b = " + b);

    }
}
class B extends A{
    int s;

    void sum()
    {
        s = a + b;
        System.out.println("sum = " + s);
    }
}
class C extends B{
    int p;

    void prod()
    {
        p = a * b;
        System.out.println("prod = " + p);
    }
}
class lab4a{
    public static void main(String args[])
    {
        C x = new C();
        x.getdata();
        x.printdata();
        x.sum();
        x.prod();
    }
}
```
```py
## lab4b
//Method Overriding
class Vehicle{
    void move()
    {
        System.out.println("Vehicla move");
    }
}
class Car extends Vehicle{
    void move()
    {
        System.out.println("Drive Car");
    }
}
class Bike extends Vehicle{
    void move()
    {
        System.out.println("Ride a bike");
    }
}
class lab4b
{
    public static void main(String args[])
    {
        Car c = new Car();
        c.move();
        Bike b = new Bike();
        b.move();
    }
}
```
## interface
```py
import java.util.*;
interface AA{
    void sum(int a,int b);
}
interface BB{
    void check(int n);
}
class C implements AA,BB
{
    public void sum(int a,int b)
    {
        System.out.println("Sum =  " + (a + b));
    }
    public void check(int n)
    {
        if(n % 2 == 0)
        {
            System.out.println("Even");
        }
        else
        {
            System.out.println("Odd");
        }
    }
}
class lab5
{
    public static  void main(String args[])
    {
        int a,b,n;
        Scanner s = new Scanner(System.in);
        System.out.println("Enter a,b");
        a = s.nextInt();
        b = s.nextInt();
        C x = new C();
        x.sum(a,b);
        System.out.println("Enter n");
        n = s.nextInt();
        x.check(n);
    }
}
```



