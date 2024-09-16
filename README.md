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


