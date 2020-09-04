# seu-gap-calculator
just a try
//made by c++
#include<iostream>
#include<cstdlib>
struct lession
{
	int score;
	double credit;
};
double point(int score)
{
	if (score >= 96)
		return 4.8;
	else if (score >= 93)
		return 4.5;
	else if (score >= 90)
		return 4.0;
	else if (score >= 86)
		return 3.8;
	else if (score >= 83)
		return 3.5;
	else if (score >= 80)
		return 3.0;
	else if (score >= 76)
		return 2.8;
	else if (score >= 73)
		return 2.5;
	else if (score >= 70)
		return 2.0;
	else if (score >= 66)
		return 1.8;
	else if (score >= 63)
		return 1.5;
	else if (score >= 60)
		return 1.0;
	else
		return 0;
}
using namespace std;
int main()
{
	lession l[20];
	cout << "欢迎使用东南大学绩点计算器。" << endl;
	for (int i = 0; i==0||l[i - 1].score > 0; i++)
	{
		cout << "请输入该科学分和你的分数，都输入0结束输入：";
		cin >> l[i].credit;
		cin.get();
		cin >> l[i].score;
		cin.get();
	}
	double sumgetcredit=0;
	double sumcredit=0;
	double gpa=0;
	for (int i = 0;l[i].score >0; i++)
	{
		sumgetcredit += l[i].credit*point(l[i].score);
		sumcredit += l[i].credit;
	}
	gpa = sumgetcredit / sumcredit;
	cout << "你的gpa为：" << gpa;
	system("pause");
	return 0;
}
