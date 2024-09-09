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
