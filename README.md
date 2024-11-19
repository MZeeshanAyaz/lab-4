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
#include<stdio.h>
#include<string.h>
#include<math.h>

int options;
int quantity;
int total = 0;

// File pointer for saving the bill
FILE *billFile;

void mainmenu();
void pizzassizes();
void pizzasflavours();
void normalflavours();
void specialflavours();
void viewBill();
void saveToFile(const char *item, int quantity, int price);

int main() {
    mainmenu();
}

void normalflavours() {
    while (1) {
        printf("1.Chicken Tikka(spicy)\n2.Chicken Supreme(spicy)\n3.Chicken Fajita(mild spicy)\n");
        printf("4.Fajita Sicilian(spicy)\n5.Veggie Lover(non spicy)\n6.Cheese Lover(non spicy)\n7.Back\n");
        printf("Enter your choice : ");
        scanf("%d", &options);
        system("cls");
        switch (options) {
            case 1:
                saveToFile("Chicken Tikka", 1, 0); // Flavour name only, price is handled elsewhere
                return;
            case 2:
                saveToFile("Chicken Supreme", 1, 0);
                return;
            case 3:
                saveToFile("Chicken Fajita", 1, 0);
                return;
            case 4:
                saveToFile("Fajita Sicilian", 1, 0);
                return;
            case 5:
                saveToFile("Veggie Lover", 1, 0);
                return;
            case 6:
                saveToFile("Cheese Lover", 1, 0);
                return;
            case 7:
                system("cls");
                pizzasflavours();
                return;
            default:
                printf("Error: Please enter options from 1-7\n");
                break;
        }
    }
}

void specialflavours() {
    while (1) {
        printf("1.Ranch(spicy)\n2.Sirracha(spicy)\n3.Creamy Tikka(mild spicy)\n");
        printf("4.Chipotle(mild spicy)\n5.Back\n");
        printf("Enter your choice : ");
        scanf("%d", &options);
        system("cls");
        switch (options) {
            case 1:
                saveToFile("Ranch", 1, 0);
                return;
            case 2:
                saveToFile("Sirracha", 1, 0);
                return;
            case 3:
                saveToFile("Creamy Tikka", 1, 0);
                return;
            case 4:
                saveToFile("Chipotle", 1, 0);
                return;
            case 5:
                system("cls");
                pizzasflavours();
                return;
            default:
                printf("Error: Please enter options from 1-5\n");
                break;
        }
    }
}

void pizzasflavours() {
    while (1) {
        printf("1.Special Flavours\n2.Normal flavours\n3.Back\n");
        printf("Enter your choice : ");
        scanf("%d", &options);
        system("cls");
        switch (options) {
            case 1:
                specialflavours();
                break;
            case 2:
                normalflavours();
                break;
            case 3:
                system("cls");
                pizzassizes();
                return;
            default:
                printf("Error: Please enter options from 1-3\n");
                break;
        }
    }
}

void mainmenu() {
    while (1) {
        printf("1.Pizzas\n2.Burgers\n3.Sidelines\n4.Drinks\n5.View Bill\n6.Quit\n");
        printf("Enter your choice : ");
        scanf("%d", &options);
        system("cls");
        switch (options) {
            case 1:
                pizzassizes();
                break;
            case 2:
                printf("Burgers are not implemented yet!\n");
                break;
            case 3:
                printf("Sidelines are not implemented yet!\n");
                break;
            case 4:
                printf("Drinks are not implemented yet!\n");
                break;
            case 5:
                viewBill();
                break;
            case 6:
                printf("Exiting... Thank you!\n");
                return;
            default:
                printf("Error: Please select a valid option\n");
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
                printf("Enter quantity: ");
                scanf("%d", &quantity);
                for (int i = 0; i < quantity; i++) {
                    printf("\nSelect flavour for Pizza %d:\n", i + 1);
                    pizzasflavours();
                }
                saveToFile("Small Pizza", quantity, 450);
                break;
            case 2:
                printf("Enter quantity: ");
                scanf("%d", &quantity);
                for (int i = 0; i < quantity; i++) {
                    printf("\nSelect flavour for Pizza %d:\n", i + 1);
                    pizzasflavours();
                }
                saveToFile("Regular Pizza", quantity, 600);
                break;
            case 3:
                printf("Enter quantity: ");
                scanf("%d", &quantity);
                for (int i = 0; i < quantity; i++) {
                    printf("\nSelect flavour for Pizza %d:\n", i + 1);
                    pizzasflavours();
                }
                saveToFile("Large Pizza", quantity, 900);
                break;
            case 4:
                printf("Enter quantity: ");
                scanf("%d", &quantity);
                for (int i = 0; i < quantity; i++) {
                    printf("\nSelect flavour for Pizza %d:\n", i + 1);
                    pizzasflavours();
                }
                saveToFile("Jumbo Pizza", quantity, 1200);
                break;
            case 5:
                system("cls");
                mainmenu();
                return;
            default:
                printf("Error: Please enter options from 1-5\n");
                break;
        }
    }
}

void saveToFile(const char *item, int quantity, int price) {
    total += price * quantity;
    billFile = fopen("bill.txt", "a");
    if (billFile == NULL) {
        printf("Error opening file!\n");
        return;
    }
    fprintf(billFile, "%s x%d = Rs %d\n", item, quantity, price * quantity);
    fclose(billFile);
}

void viewBill() {
    char line[256];
    billFile = fopen("bill.txt", "r");
    if (billFile == NULL) {
        printf("No items in the bill yet.\n");
        return;
    }

    printf("----- Your Bill -----\n");
    while (fgets(line, sizeof(line), billFile)) {
        printf("%s", line);
    }
    fclose(billFile);
    printf("Total Amount: Rs %d\n", total);
    printf("---------------------\n");
}
