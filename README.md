#include<stdio.h>
#include<string.h>

int main (){
	int n;
	
	printf("Enter the size of class students : ");
	scanf("%d", &n);
	
	
	char names[n][50];
	
	
	printf("Enter %d names ", n);
	
	for(int i=0;i<=n;i++)
	{
		gets(names[i]);
				
	}
	
	for(int i=0;i<=n;i++)
	{
		
		puts(names[i]);
				
	}
}
_________________________________________________________________________________________________________
#include<stdio.h>
int calculator(int a ,int b){
	int options;
	int c;
	printf("1.+ \n 2.-\n 3.*\n 4.-\n");
	scanf("%d",&options);
	switch(options){
		case 1 :  c=a+b;
				
				break;
		case 2 :  c=a-b;
				
				break;
		case 3 :  c=a*b;
				
				break;
		case 4 :  c=a/b;
				
				break;
		default : printf("error");		
	}
	return c;

}
int main ()
{
	int a ,b;
	printf("Enter a and b =");
	scanf("%d %d",&a,&b);
	printf(" %d",calculator(a,b)) ;
	
	
	
}
