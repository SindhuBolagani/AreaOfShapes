# AreaOfShapes
In this program, Abstract class is created named Shape, it contains two integers and an empty method named print Area(). Classes names are Rectangle, Triangle, and Circle. Each one of the class contains only the method print Area() that prints the area of the given shape.
import java.util.Scanner;

abstract class Shape
{
	public int x,y;
	public abstract void printArea();
}
class Rectangle extends Shape
{
	public void printArea()
	{
		float area;
		area=x*y;
		System.out.println("Areaof Rectangle is"+area);
	}
}
class Triangle extends Shape
{
	public void printArea() 
	{
		float area;
		area=(x*y)/2.0f;
		System.out.println("Area of Triangle is"+area);
	}
}
class Circle extends Shape
{
	public void printArea()
	{
		float area;
		area=(22*x*x)/7.0f;
		System.out.println("Area of Circle is"+area);
	}
}
public class AreaOfShapes
{

	public static void main(String[] args)
	{
		int choice;
		Scanner sc=new Scanner(System.in);
		System.out.println("Menu \n 1.Area of Rectangle \n 2.Area of Triangle \n 3.Area of Circle");
		System.out.println("Enter your choice:");
		choice=sc.nextInt();
		switch(choice)
		{
		case 1:System.out.println("Enter length and breadth for area of reactangle:");
		Rectangle r = new Rectangle();
		r.x=sc.nextInt();
		r.y=sc.nextInt();
		r.printArea();
		break;
		case 2:System.out.println("Enter breadth and height for area of reactangle:");
		Triangle t=new Triangle();
		t.x=sc.nextInt();
		t.y=sc.nextInt();
		t.printArea();
		break;
		case 3:System.out.println("Enter radius for area of circle");
		Circle c=new Circle();
		c.x=sc.nextInt();
		c.printArea();
		default:System.out.println("Enter correct choice");
		}
	}

}

