int main()
{
	int age ;
	printf ("enter age =");
	scanf("%d",&age);
	if(age>0){
		if(age>=1&&age<=15){
			printf("child");
		}else if(age>15&&age<=20){
			printf("teenager");
		}else if(age>20&&age<=45){
			printf("adult");
		}else{
			printf("senior");
		}
		
	}else {
		printf("invalid age ");
	}
}
___________________________________________________________
#include<stdio.h>
int main()
{
	int num;
	printf("enter any number =");
	scanf("%d",&num);
	
		if (num<0){
			printf("number is negative\n ");
		}else if(num==0){
			printf("number is zero\n");
		}else {
			printf("number is positive \n");
			if(num%2==0){
				printf("number is even\n ");
			}else{
				printf("number is odd\n");
			}
		}
	}
____________________________________________________________

