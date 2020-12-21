using System;
public class Program
{
	class Car{
		public string marka;
		public string model;
		public int yearProd;
		public int obmDvig;
	}
		public static void Main()
	{		
	Car myCar= new Car();
			Console.WriteLine("Въведете марка автомобил: ");myCar.marka=Console.ReadLine();
			Console.WriteLine("Въведете модел на автомобила: ");myCar.model=Console.ReadLine();
			Console.WriteLine("Въведете година на производство: ");myCar.yearProd=int.Parse(Console.ReadLine());
			Console.WriteLine("Въведете обем на двигател: ");myCar.obmDvig=int.Parse(Console.ReadLine());
			double taksa=0.2*myCar.obmDvig;
			if(myCar.yearProd<=2000){
				taksa=taksa+50;
				}else if(myCar.yearProd<=2010){
				taksa+=60;
			}else
			{
				taksa+=70;
			}
			Console.WriteLine("Данъкът на {0} {1}  ", myCar.marka, myCar.model);
			Console.WriteLine("С обем на двигателя {0} ",myCar.obmDvig);
			Console.WriteLine("e {0} лева ",taksa);
	}
}
