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
#include<stdio.h>
int main()
{
char chara ;
printf("Enter any character = ");
scanf("%c",&chara);
if(chara=='a'||chara=='A'){
	printf("character = %c is vowel",chara);}
	else if (chara=='e'||chara=='E'){
	printf("character = %c is vowel",chara);}
	else if (chara=='i'||chara=='I'){
	printf("character = %c is vowel",chara);}
	else if (chara=='o'||chara=='O'){
	printf("character = %c is vowel",chara);}
	else if (chara=='u'||chara=='U'){
	printf("character = %c is vowel",chara);}
	else{
		printf("character= %c is consonant",chara);
	}
return 0;	
}
#include<stdio.h>
int main()
{
float a,b;
char oper ;
	printf("Enter a =");
	scanf("%f",&a);
	
	printf("Enter b =");
	scanf(" %f",&b);
	
	printf("Enter operator(+,-,*,/)= ");
	scanf(" %c",&oper);
	
	switch(oper){
		case '+' : printf("%.1f+%.1f=%.1f",a,b, a+b );
		break;
		case '-' : printf("%.1f - %.1f = %.1f",a,b,a-b);
		break;
		case '*' : printf("%.1f*%.1f=%.1f",a,b,a*b);
		break;
		case '/' : printf("%.1f/%.1f=%.3f",a,b,a/b);
		break;
		default : printf("Error");
	}
	
}




#include<stdio.h>
int main ()
{
	float T,TA,NA;//I(income)T(tax)TA(TAX AMOUNT)NA(NET AMOUNT) 
	int I;
	printf("enter income =");
	scanf("%d",&I);
	if(I<=250000){
		printf("No Tax \n");
		printf("Total income is %d",I);
	}
	else if(I>=250001&&I<=500000){
		printf("tax is 5%%\n");
		printf("Total income is %d\n",I);
		TA=(I*5)/100;
		printf("Total tax on income =%.2f\n",TA);
		NA=I-TA;
		printf("Net Amount after tax=%.2f \n",NA);
		}else if (I>=500001&&I<=100000){
			printf("tax is 20%% \n");
			printf("Total income is %d",I);
		
		TA=(I*20)/100;
		printf("Total tax on income =%.2f\n",TA);
		NA=I-TA;
		printf("Net Amount after tax=%.2f \n",NA);
		}else{
			printf("tax is 30%% \n");
			printf("Total income is %d\n",I);
			
		TA=(I*30)/100;
		printf("Total tax on income =%.2f\n",TA);
		NA=I-TA;
		printf("Net Amount after tax=%.2f",NA);
		}
}

#include<stdio.h>
int main ()
{
	int TM ;
	char grade;

	printf("Enter total marks= ");
	scanf("%d",&TM);
	switch(grade){
		case 'A' : if(TM>=90&&TM<=100){printf("grade A");}
			break;
		case 'B' : if(TM>=70&&TM<90){printf("grade B");}
			break;
		case 'C ': if(TM>=70&&TM<80){printf("grade C");}
			break;
		case 'D' : if(TM>=60&&TM<70){printf("grade D");}
			break;
		case 'F' : if(TM<60&&TM>=0){printf("grade F");}
			break;
		default: printf("invalid total marks ");
			
			}
}
