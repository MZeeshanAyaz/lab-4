#include<stdio.h>
#include<string.h>
#include<math.h>
int options;
int quantity;
int total=0;

void mainmenu();
void pizzassizes();
void pizzasflavours();
void normalfalvours();
void specialflavours();

int main (){
	mainmenu();
	pizzassizes();
	pizzasflavours();
	specialflavours();
	normalfalvours();
	
}

void normalfalvours(){
	while (1){
		
		printf("1.Chicken Tikka(spicy)\n2.Chicken Supreme(spicy)\n3.Chicken Fajita(mild spicy)\n4.Fajita Sicilian(spicy)\n5.Veggie Lover(non spicy)\n6.Cheese Lover(non spicy)\n7.Back\n");
		printf("Enter your choice :");
		scanf("%d",&options);
		system("cls");
		switch(options){
			case 1 :printf("");
					pizzassizes();
					break;
			case 2: printf("");
					pizzassizes(); 
					break;
			case 3:printf("");
					pizzassizes();
					break;
			case 4:printf("");
					pizzassizes();
					break;
			case 5:printf("");
					pizzassizes();
					break;
			case 6:printf("");
					pizzassizes();
					break;
			case 7 :system("cls");
					pizzasflavours();
					break;
			default : printf("Error : Please enter options from 1-7");
					break;
		}
		
	}
}
void specialflavours(){
	while (1){
		
		printf("1.Ranch(spicy)\n2.Sirracha(spicy)\n3.Creamy Tikka(mild spicy)\n4.Chipotle(mild spicy)\n5.Back\n");
		printf("Enter your choice :");
		scanf("%d",&options);
		system("cls");
		switch(options){
			case 1:printf("");
					pizzassizes();
					break;
			case 2:printf("");
				   pizzassizes();
					break;
			case 3:printf("");
					pizzassizes();
					break;
			case 4:printf("");
					pizzassizes();
					break;
			case 5 :system("cls");
					pizzasflavours();
					break;
			default : printf("Error : Please enter options from 1-5");
					break;
		}
		
	}
}
void pizzasflavours(){
	while (1){
		printf("1.Special Flavours\n2.Normal flavours\n3.Back\n");
		printf("Enter your choice :");
		scanf("%d",&options);
		system("cls");
		switch(options){
			case 1 :specialflavours();
					break;
			case 2 :normalfalvours();
					break;
			case 3 :system ("cls");
					pizzassizes();
					break;
			default :printf("Error : Please Enter options from 1-3\n");
					break;
		}
	}
	
}
void mainmenu(){
	while (1){
		printf("1.Pizzas\n2.Burgers\n3.Sidelines\n4.Drinks\n5.view Bill\n6.Quit\n");
		printf("Enter your choice :");
		scanf("%d",&options);
		system("cls");
		switch(options){
			case 1 :pizzassizes();
				break;
			case 2 :
				break;
			case 3 :
				break;
			case 4 :
				break;
			case 5 :
				break;
			case 6 :return 0;
				break;
		}
		
	}
}

void pizzassizes(){
	while (1){
		printf("1.Small\t\tRs 450\n2.Regular\tRs 600\n3.Large\t\tRs 900\n4.Jumbo\t\tRs 1200\n5.Back\n");
		printf("Enter your choice : ");
		scanf("%d",&options);
		system("cls");
		switch(options){
			case 1:
				   printf("Enter quantity = ");
				   scanf("%d",&quantity);
				   total+=450*quantity;
				   pizzasflavours();
				   break;
			case 2:
			       printf("Enter quantity = ");
				   scanf("%d",&quantity);
				   total+=600*quantity;
				   pizzasflavours();
				   break;
			case 3:
			       printf("Enter quantity = ");
				   scanf("%d",&quantity);
				   total+=900*quantity;
				   pizzasflavours();
				   break;
			case 4:
			       printf("Enter quantity = ");
				   scanf("%d",&quantity);
				   total+=900*quantity;
				   pizzasflavours();
				   break;
			case 5:system("cls");
				   mainmenu();
				   break;
			default : printf("Error : Please Enter options from 1-5");
		}
		
	}
	
}
