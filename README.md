# Operator-Overloading

## Aim:
 To write a C# program to find the volume of a box using operator overloading
 
 ## Algorithm:
 ### Step 1:
 Create a class for operator overloading.

 ### Step 2:
 Get inputs for length,breadthandheight of the box fromthe user and then calculate the volume in overloading function.

 ### Step 3:
After that return a new object for the calculated volume.

 ### Step 4:
 Then create a new object to store the return object.

 ### Step 5:
After that print the calculated volume.

 
 
 
 ## Program:
 ```
using System;
namespace ConsoleApp1
{
    class box
    {
        public int length, breadth, height,volume;
        public static box operator+(box b1,box b2)
        {
            box b3 = new box();
            b3.length = b1.length + b2.length;
            b3.breadth = b1.breadth + b2.breadth;
            b3.height = b1.height + b2.height;
            b1.volume = b1.length * b1.breadth * b1.height;
            b2.volume = b2.length * b2.breadth * b2.height;
            b3.volume = b3.length * b3.breadth * b3.height;
            return b3;
        }
        public static void Main()
        {
            box b1 = new box();
            Console.WriteLine("Enter the Length of Box1");
            b1.length = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Enter the Breadth of Box1");
            b1.breadth = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Enter the Height of Box1");
            b1.height = Convert.ToInt32(Console.ReadLine());
            box b2 = new box();
            Console.WriteLine("Enter the Length of Box2");
            b2.length = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Enter the Breadth of Box2");
            b2.breadth = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Enter the Height of Box2");
            b2.height = Convert.ToInt32(Console.ReadLine());
            box b4 = new box();
            b4 = b1 + b2;
            Console.WriteLine("Volume of Box1");
            Console.WriteLine(b1.volume);
            Console.WriteLine("Volume of Box2");
            Console.WriteLine(b2.volume);
            Console.WriteLine("Volume of Box3");
            Console.WriteLine(b4.volume);

        }
    }
}
 ```
 
 ## Output:
 ![image](https://user-images.githubusercontent.com/94164665/170739200-4d6eede5-95c8-4042-bdbc-be4207047143.png)

 
 ## Result:
 Thus the C# program to find the volume of a box using operator overloading is implemented successfully.


