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
