#include <iostream>
#include <string>
#include <Windows.h>
using namespace std;

/* 7. Напишіть програму, в якій створюються два об'єкти типу “Студент”. 
Встановіть їх вік, стать та стипендію за допомогою методів доступу. 
Надрукуйте значення окремих членів-даних об'єктів на екрані, використовуючи методи доступу. 
Визначте та роздрукуйте середній вік та сумарну стипендію цих двох студентів.
*/

class Student
{
private:
	int age;
	string sex;
	int money;
public:
	// методи доступу: 
	void input()
	{
		cout << "Введіть вік: ";
		cin >> age;
		cout << "Введіть стать: ";
		cin >> sex;
		cout << "Введіть стипендію: ";
		cin >> money;
	}
	void print()
	{
		cout << "\nВік студента: " << age << "\nСтать студента: " << sex << "\nСтипендія студента: " << money << endl << "\n";
	}
	// конструктори і деструктор:
	Student(int x, string y, int z)
	{
		age = x;
		sex = y;
		money = z;
	} 
	Student()
	{
		age = 0;
		sex = "-";
		money = 0;
	}
	~Student()
	{
		// cout << "Виклик деструктора." << endl;
	}
	// гетери і сеттери (теж методи доступу):
	int getAge()
	{
		return age;
	}
	string getSex()
	{
		return sex;
	}
	int getMoney()
	{
		return money;
	}
	void setAge(int a)
	{
		age = a;
	}
	void setSex(const string& s)
	{
		sex = s;
	}
	void setMoney(int m)
	{
		money = m;
	}
};

void main()
{
	SetConsoleOutputCP(1251);
	SetConsoleCP(1251);
	
	Student Vlad; // заповнюємо об'єкти класа через сеттери і виводимо за допомогою гетерів (методів доступу)
	Vlad.setAge(18);
	Vlad.setSex("male");
	Vlad.setMoney(3000);
	cout << "Перший студент." << endl;
	cout << "Вік: " << Vlad.getAge() << endl;
	cout << "Стать: " << Vlad.getSex() << endl;
	cout << "Стипендія: " << Vlad.getMoney() << endl;
	Student Anna;
	Anna.setAge(19);
	Anna.setSex("female");
	Anna.setMoney(1200);
	cout << "\nДругий студент." << endl;
	cout << "Вік: " << Anna.getAge() << endl;
	cout << "Стать: " << Anna.getSex() << endl;
	cout << "Стипендія: " << Anna.getMoney() << endl;
	cout << "\n";

	double averageAge = (Vlad.getAge() + Anna.getAge()) / 2; // шукаємо середній вік студентів, число "2" - це кількість студентів
	int totalMoney = Vlad.getMoney() + Anna.getMoney(); // шукаємо сумарну стипендію
	cout << "Середній вік студентів: " << averageAge << endl;
	cout << "Сумарна стипендія студентів: " << totalMoney << endl;
}
