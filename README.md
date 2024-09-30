#include<stdio.h>
int main ()
{
	int i,j=0 ;
	do{
		printf("enter a number =");
		scanf("%d",&i);
		j+=i;
		printf("%d \n",j);
	}while(i!=0);
	
}
_______________________________________________
#include<stdio.h>
int main ()
{
int n;
printf("Enter a number = ");
scanf("%d",&n);
int i,j=1;
for(i=n;i>0;i--)
	{	
		j*=i;
	}	
printf("%d",j);
}
__________________________________________________________
#include<stdio.h>
int main ()
{
int n;
printf("Enter a number = ");
scanf("%d",&n);
int i,j=0,k=0;
for(i=n;i>0;i--)
	{	
		if(i%2==0){
			j+=1;
		}else{
			k+=1;
		}
	}	
printf("Even=%d\n",j);
printf("Odd=%d\n",k);
}
_____________________________________________________________________
#include<stdio.h>
int main ()
{
int n;
printf("Enter a number = ");
scanf("%d",&n);
int i,j=0;
for(i=n;i>0;i--)
	{	
		if(i%2==0){
		j+=i;
		}	
}
printf("sum of Even numbers =%d\n",j);
}
_________________________________________________________________________
#include<stdio.h>
int main ()
{
int n;
printf("Enter a number = ");
scanf("%d",&n);

int i=0;
while(n!=0){
	i=n%10+i*10;
	
	n=n/10;
	}
printf("reversed number =%d\n",i);	
}
_____________________________________________________________________________________


