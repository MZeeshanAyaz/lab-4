#include<stdio.h>
#include<string.h>
#include<math.h>
int options;
int quantity;
int total prize=0;
void pizzasflavours(){
	while (1){
		printf("1.Special Flavours\n2.Normal flavours\n3.Back\n");
		printf("Enter your choice :");
		scanf("%d",&options);
		switch(1){
			case 1 :
				break;
			case 2 :
				break;
			case 3 :system ("cls");
					pizzassizes();
					break;
			default :printf("Error : Please Enter options from 1-3\n");
		}
	}
	
}

void pizzassizes(){
	while (1){
		printf("1.Small\tRs 450\n2.Regular\tRs 600\n3.Large\tRs 900\n4.Jumbo\tRs 1200\n5.Back\n");
		printf("Enter your choice : ");
		scanf("%d",options);
		switch(1){
			case 1:printf("Enter quantity = ");
				   scanf("%d",&quantity);
				   totalprize+=450*quantity;
				   break;
			case 2:printf("Enter quantity = ");
				   scanf("%d",&quantity);
				   totalprize+=600*quantity;
				   break;
			case 3:printf("Enter quantity = ");
				   scanf("%d",&quantity);
				   totalprize+=900*quantity;
				   break;
			case 4:printf("Enter quantity = ");
				   scanf("%d",&quantity);
				   totalprize+=900*quantity;
				   break;
			case 5:system("cls");
			
				   break;
			default : printf("Error : Please Enter options from 1-5");
		}
		
	}
	
}
