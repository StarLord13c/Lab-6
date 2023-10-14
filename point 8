#include <iostream>
#include <string>
#include <Windows.h>
using namespace std;

/* 8. *** Напишіть оголошення та реалізацію закритого класу для роботи з датою, що складається з трьох цілих чисел : день, місяць, рік.
Включіть до складу класу конструктори, деструктор, методи доступу, логічні методи для перевірки частин дати та визначення високосного року,
роздруківки дати у кількох форматах(“дд.мм.гг”, “дд / мм / гггг”, “mmm - dd - yyyy ”).
Протестуйте цей клас. */

class Date
{
private:
	int day;
	int month;
	int year;

public:
	// конструктори і деструктор
	Date(int x, int y, int z)
	{
		day = x;
		month = y;
		year = z;
	}
	Date()
	{
		day = 0;
		month = 0;
		year = 0;
	}
	~Date()
	{
		day = 0;
		month = 0;
		year = 0;
		cout << "\nДеструктор: " << "\nday = 0" << "\nmonth = 0" << "\nyear = 0" << endl;
	}

	// методи доступу
	int getDay()
	{
		return day;
	}
	int getMonth()
	{
		return month;
	}
	int getYear()
	{
		return year;
	}
	void setDate(int d, int m, int y)
	{
		day = d;
		month = m;
		year = y;
	}

	bool LeapYear() 
	{
		// якщо хоч одна з цих умов виконується, то рік вважаємо високосним ((або рік кратний 4 "кон'юнкія" не є століттям) "диз'юнкція" (або рік кратний 400))
		if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) // парні роки кінця сторіч (ті, номер яких закінчується на «00») є високосними роками, лише якщо їх номер ділиться на 400.
		{
			return true; // якщо умова виконується повертаємо так(1)
		}
		return false; // якщо умова не виконується повертаємо ні(0)
	}

	// методи для виводу класу різними варіантами
	void format1() 
	{
	   cout << (day < 10 ? "0" : "") << day << "." 
	   << (month < 10 ? "0" : "") << month << "." 
	   << (year % 100 < 10 ? "0" : "") << year % 100 << endl;
	}
	void format2()
	{
		cout << (day < 10 ? "0" : "") << day << " / "
			<< (month < 10 ? "0" : "") << month << " / "
		    << year << endl;
	}
	void format3()
	{
		string months[] = { "Jan", "Feb", "Mar", "Apr", "May", "Jun",
								"Jul", "Aug", "Sep", "Oct", "Nov", "Dec" };
		cout << months[month - 1] << " - "
			<< (day < 10 ? "0" : "") << day << "."
			<< " - " << year << endl;
	}
};

void main()
{
	SetConsoleOutputCP(1251);
	SetConsoleCP(1251);
	
	Date birthday;

	int x, y, z;
	cout << "Введіть день: ";
	cin >> x;
	cout << "Введіть місяць: ";
	cin >> y;
	cout << "Введіть рік: ";
	cin >> z;

	birthday.setDate(x, y, z); // використовуємо сеттер

    cout << "Дата у форматі 'дд.мм.гг': "; // виводимо різними способами 
	birthday.format1();
	cout << "Дата у форматі 'дд / мм / гггг': ";
	birthday.format2();
	cout << "Дата у форматі 'mmm - dd - yyyy': ";
	birthday.format3();

	cout << "\nДень: " << (birthday.getDay() < 10 ? "0" : "") << birthday.getDay() << endl; // якщо число меньше 10 то добавляємо перед ним "0", це для гарного вигляду
	cout << "Місяць: " << (birthday.getMonth() < 10 ? "0" : "") << birthday.getMonth() << endl;
	cout << "Рік: " << birthday.getYear() << endl;
	cout << "Чи є рік високосним? " << (birthday.LeapYear() ? "Так" : "Ні") << endl; // виводимо результат чи рік високосний (викорситовуємо тернарний оператор)
}
