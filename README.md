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
#include<stdio.h>
int main()
{
	int num;
	printf("enter any number =");
	scanf("%d",&num);
	if(num%3==0&&num%5==0){
		printf("number is divisible by both 3 and 5\n ");
	}else {
		printf("number is not divisible by both 3 and 5\n ");
	}
	return 0;
		
	}
 _______________________________________________________________________
 #include <stdio.h>

int main() {
    int a, b, c;

    printf("Enter a, b, and c: ");
    scanf("%d %d %d", &a, &b, &c);

    if (a > b) {
        if (a > c) {
            printf("a is greater\n");
        } else {
            printf("c is greater\n");
        }
    } else {
        if (b > c) {
            printf("b is greater\n");
        } else {
            printf("c is greater\n");
        }
    }

    return 0;
}
_____________________________________________________________________________________
#include <stdio.h>

int main() {
	char a;
	printf("enter a = ");
	scanf("%c",&a);
	
	if(a>=65&&a<=90){
		printf("%c is upper case letter",a);
	}else if (a>=97&&a<=122){
		printf("%c is lower case letter",a);
	}else if (a>=48&&a<=57){
		printf("%c is a digit ",a);
		
	}else {
		printf("%c is a special character ",a);
	}
   
}


	



	

 
