```
#include <stdio.h>
#include <stdlib.h>
int main()
{

	//int pi = 13;
	//double pd = 3.14;
	//char pc = 'a';

	//int* apd = &pd;
	//int* api = &pi;
	//int* apc = &pc;

	//int ipd = (int)pd;
	//int ipi = (int)pi;
	//int ipc = (int)pc;

	//printf("pd\t=\t%.2f,\tapd\t=\t%p,\tipd\t=\t%d\n", pd, apd, ipd);
	//printf("pi\t=\t%d,\tapi\t=\t%p,\tipi\t=\t%d\n", pi, api, ipi);
	//printf("pc\t=\t%c,\tapc\t=\t%p,\tipc\t=\t%d\n", pc, apc, ipc);

	int n = 0, i = 0;
	double min = 0.0, max = 0.0;

	printf("Vvedite N\n");
	scanf_s("%d", &n);

	printf("Vvedite min\n");
	scanf_s("%lf", &min);

	printf("Vvedite max\n");
	scanf_s("%lf", &max);

	for (i = 0; i < n; i++)
	{
		double value = (((double)rand()) / RAND_MAX) * (max = min) + min;
		printf("value[%d]\ %.5lf\n", i, value);
	}



	return 0;
};
```
```
#include <windows.h>
#include <time.h>
#include <stdio.h>
#include <stdlib.h>
#include <locale.h>
int main()
{
	int n = 0, i = 0;
	int iMax = 0, iMin = 0, max = 0, min = 0, sum = 0;
	int grade = 0;
	int a = 0, b = 0;

	int gradeCount[11];
	int* grades = 0;
	int i1, i2 = 0;
	char** studNames;

	char* em[10];

	//setlocale(LC_ALL, "Russia");
	SetConsoleOutputCP(65001);
	SetConsoleCP(65001);
	srand(time(0));

	//printf("Введите число студентов: ");
	scanf_s("%d", &n);

	if (n <= 0)
	{
		printf("Количество студентов должна быть больше нуля");
		return 1;
	}

	grade = rand() % 10 + 1;
	max = grade;
	min = grade;


	for (i = 1; i < n; i++)
	{
		grade = rand() % 10 + 1;
		if (grade > max)
		{
			max = grade;
			iMax = i;
		}
		if (grade < min)
		{
			min = grade;
			iMin = i;
		}
		sum += grade;
		printf("Оценка студента %d \t = \t %d \n", i + 1, grade);
	}

	printf("Минимальная оценка %d у студента %d\n", min, iMin);
	printf("Максимальная оценка %d у студента %d\n", max, iMax);
	printf("Средняя оценка = %.3lf", (double)sum / n);

	for (i = 1, i < 11; i++)
	{
		printf("Оценка %d встречается %d раз\n", i, gradeCount[i]);
		if (i <= 5)
			a += gradeCount[i];
		else
			b += gradeCount[i];
	}

	printf("a = % d\tb = % d\n", a, b);

	//printf("Введите интересуемую оценку");
	//scanf("%d %d", &i1, &i2);

	//for (i = 0; i < n; i++)
	//{
	//	if (grades[i] == i1 || grades[i] == i2)
	//		printf("Оценка студента %d \t=\t %d \n", i + 1, grades[i])
	//}

	return 0;
}
```
