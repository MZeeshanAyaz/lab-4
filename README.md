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
________________________________________________________________
#include<stdio.h>
#include<string.h>
int main (){
	FILE *ptr1;
	FILE *ptr2;
	FILE *ptr3;
	
	char a1[20];
	char a2[20];
	char a3[20];
	
	ptr1=fopen("ptr1.txt","w");
	if(ptr1==NULL){
		printf("ptr1.txt failed to open \n");
		}else{
		
	gets(a1);
	fputs(a1,ptr1);
	fclose(ptr1);
}
	ptr2=fopen("ptr2.txt","w");
	if(ptr2==NULL){
		printf("ptr2.txt failed to open \n");
		}else{
		
	gets(a2);
	fputs(a2,ptr2);
	fclose(ptr2);
}
	strcat(a1," ");
 	strcat(a1,a2);
 	strcat(a3,a1);
 	
 	
 	
	ptr3=fopen("ptr3.txt","w");
	if(ptr3==NULL){
		printf("ptr3.txt failed to open \n");
		}else{
	fputs(a3,ptr3);
	fclose(ptr3);	
	
}
 

}
____________________________________________________________________
#include <stdio.h>
#include <stdlib.h> 
#include <string.h>
#include <math.h>

int orderID = 1;
int options;
int quantity;
int total = 0;

void mainmenu();
void pizzassizes();
void pizzasflavours();
void normalfalvours();
void specialflavours();

void clear_screen() {
    #ifdef _WIN32
        system("cls");  
    #else
        system("clear");
    #endif
}

int main() {
    mainmenu();
    pizzassizes();
    pizzasflavours();
    specialflavours();
    normalfalvours();
}

void normalfalvours() {
    while (1) {
        printf("1.Chicken Tikka(spicy)\n2.Chicken Supreme(spicy)\n3.Chicken Fajita(mild spicy)\n4.Fajita Sicilian(spicy)\n5.Veggie Lover(non spicy)\n6.Cheese Lover(non spicy)\n7.Back\n");
        printf("Enter your choice :");
        scanf("%d", &options);
        clear_screen(); 
        switch (options) {
            case 1:
                printf("Chicken Tikka\n");
                pizzassizes();
                break;
            case 2:
                printf("Chicken Supreme\n");
                pizzassizes();
                break;
            case 3:
                printf("Chicken Fajita\n");
                pizzassizes();
                break;
            case 4:
                printf("Fajita Sicilian\n");
                pizzassizes();
                break;
            case 5:
                printf("Veggie Lover\n");
                pizzassizes();
                break;
            case 6:
                printf("Cheese Lover\n");
                pizzassizes();
                break;
            case 7:
                clear_screen();
                pizzasflavours();
                break;
            default:
                printf("Error : Please enter options from 1-7\n");
                break;
        }
    }
}

void specialflavours() {
    while (1) {
        printf("1.Ranch(spicy)\n2.Sirracha(spicy)\n3.Creamy Tikka(mild spicy)\n4.Chipotle(mild spicy)\n5.Back\n");
        printf("Enter your choice :");
        scanf("%d", &options);
        clear_screen(); 
        switch (options) {
            case 1:
                printf("Ranch\n");

                break;
            case 2:
                printf("Sirracha\n");

                break;
            case 3:
                printf("Creamy Tikka\n");

                break;
            case 4:
                printf("Chipotle\n");

                break;
            case 5:
                clear_screen();
                pizzasflavours();
                break;
            default:
                printf("Error : Please enter options from 1-5\n");
                break;
        }
    }
}

void pizzasflavours() {
    while (1) {
        printf("1.Special Flavours\n2.Normal flavours\n3.Back\n");
        printf("Enter your choice :");
        scanf("%d", &options);
        clear_screen(); 
        switch (options) {
            case 1:
                specialflavours();
                break;
            case 2:
                normalfalvours();
                break;
            case 3:
                clear_screen();
                pizzassizes();
                break;
            default:
                printf("Error : Please Enter options from 1-3\n");
                break;
        }
    }
}

void mainmenu() {
    while (1) {
        printf("1.Pizzas\n2.Burgers\n3.Sidelines\n4.Drinks\n5.view Bill\n6.Quit\n");
        printf("Enter your choice :");
        scanf("%d", &options);
        clear_screen(); 
        switch (options) {
            case 1:
                pizzassizes();
                break;
            case 2:
                break;
            case 3:
                break;
            case 4:
                break;
            case 5:
                break;
            case 6:
                return;
                break;
        }
    }
}

void pizzassizes() {
    while (1) {
        printf("1.Small\t\tRs 450\n2.Regular\tRs 600\n3.Large\t\tRs 900\n4.Jumbo\t\tRs 1200\n5.Back\n");
        printf("Enter your choice : ");
        scanf("%d", &options);
        system("cls");  

        switch (options) {
            case 1:
                printf("Enter quantity = ");
                scanf("%d", &quantity);

                for (int i = 0; i < quantity; i++) {
                    printf("\nFor Pizza %d:\n", i + 1);
                    pizzasflavours();  
                }
                total += 450 * quantity;
                break;
            case 2:
                printf("Enter quantity = ");
                scanf("%d", &quantity);
                for (int i = 0; i < quantity; i++) {
                    printf("\nFor Pizza %d:\n", i + 1);
                    pizzasflavours();  
                }
                total += 600 * quantity;
                break;
            case 3:
                printf("Enter quantity = ");
                scanf("%d", &quantity);
                for (int i = 0; i < quantity; i++) {
                    printf("\nFor Pizza %d:\n", i + 1);
                    pizzasflavours();  
                }
                total += 900 * quantity;
                break;
            case 4:
                printf("Enter quantity = ");
                scanf("%d", &quantity);
                for (int i = 0; i < quantity; i++) {
                    printf("\nFor Pizza %d:\n", i + 1);
                    pizzasflavours();  
                }
                total += 1200 * quantity;
                break;
            case 5:
                system("cls");
                mainmenu();
                break;
            default:
                printf("Error: Please Enter options from 1-5\n");
                break;
        }
    }
}
																																																																																																																																							
