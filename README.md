#include<stdio.h>
int main()
{
	int num;
	printf("Enter number= ");
	scanf("%d",&num);
	if (num%2==0){
		printf("num=%d is Even number",num);
	}else{
		printf("num=%d is Odd number",num);
	}
}

