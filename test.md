//Task 2

double LineLength(double x1, double y1, double z1, double x2, double y2, double z2)
{
    double line1Length = x2 - x1;
    double line2Length = y2 - y1;
    double line3Length = z2 - z1;
    double result = Math.Sqrt(Math.Pow(line1Length, 2) + Math.Pow(line2Length, 2) + Math.Pow(line3Length, 2));
    return result;
}

Console.Write("Введите координату Х первой точки: ");
double x1 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату Y первой точки: ");
double y1 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату Z первой точки: ");
double z1 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату Х второй точки: ");
double x2 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату Y второй точки: ");
double y2 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату Z второй точки: ");
double z2 = Convert.ToDouble(Console.ReadLine());

Console.WriteLine("Длина отрезка: " + Math.Round(LineLength(x1,y1,z1,x2,y2,z2), 2));

//Task 3
/* bool IsPalindrome(int number)
{
    int number1 = number, number2 = 0;
    while(number1 > 0)
    {
        number2 = number2 * 10 + number1 % 10;
        number1 /= 10;
    }
    return number2 == number;
}

Console.Write("Enter N: ");
int num = Convert.ToInt32(Console.ReadLine());
Console.WriteLine($"Число {num} " + (IsPalindrome(num) ? "": "не ") + "является палиндромом.");
*/





/* Задача 23
Напишите программу, которая принимает на вход число (N) и выдаёт таблицу кубов чисел от 1 до N.
3 -> 1, 8, 27; 5 -> 1, 8, 27, 64, 125  */

int number = ReadInt("Введите число: ");

for (int i = 1; i <= number; i++)
{
    Console.Write($"{i * i * i}, ");
}

// Метод
int ReadInt(string message)
{
    Console.Write(message);
    return Convert.ToInt32(Console.ReadLine());
}
