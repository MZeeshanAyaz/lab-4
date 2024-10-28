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

