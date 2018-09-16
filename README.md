# assignment


question 1

#include <stdio.h>
void main()  
{	int a,b,c;
	printf("please enter the number and press enter::");
	printf("number 1:");
	scanf("%d",&a);
	printf("number 2:");
	scanf("%d",&b);
	printf("number 3:");
	scanf("%d",&c);
	if(((a==b ) && (b==c)) || ((a==b) || (b==c) || (c==a))){
		printf("0\n");
			}
	else{
		printf("1\n");
		}
}

question 2

#include<stdio.h>
void  main()
{
int m,n,s,f;
s=m/n;
f=0;
printf("Enter two numbers");
scanf("%d\n%d",&m,&n);
if(m%n==0)
printf("%d",s);
else
printf("%d",f);
}

question 3

#include<stdio.h>
void main()
{
int a,b,c,g,h;
g=1;
h=0;
printf("Enter three lengths of triangle");
scanf("%d\n%d\n%d",&a,&b,&c);
if((a+b>=c)&&(b+c>=a)&&(c+a>=b))
printf("%d",g);
else
printf("%d",h);
}

question 5


#include <stdio.h>
#include <stdlib.h>

int main ()
{
char ipAddr[20]; //= "192.168.1.255";
scanf("%s",ipAddr);
int a=0,b=0,c=0,d=0,e=0;
int con = sscanf(ipAddr, "%d.%d.%d.%d.%d", &a, &b, &c, &d, &e);
if ( con == 4 )
{
printf("scanned ip=%s had %d octets\n a=%d, b=%d, c=%d, d=%d\n", ipAddr, con, a, b, c, d);
if ((0<=a && a<=255) && (0<=b && b<=255) && (0<=c && c<=255) && (0<=d && d<=255) )
printf("valid ip address\n");
else
printf("not valid ip address\n");
}
else
{
printf("malformed ip address\n");
}
return 0;

}

question 6

#include<stdio.h>
#include<string.h>
 
int digit(char);
 
int main(){
 
    char roman_Number[1000];
    int i=0;
    long int number =0;
 
    printf("Enter any roman number (Valid digits are I, V, X, L, C, D, M):  \n");
    scanf("%s",roman_Number);
 
    while(roman_Number[i]){
 
         if(digit(roman_Number[i]) < 0){
             printf("Invalid roman digit : %c",roman_Number[i]);
             return 0;
         }
 
         if((strlen(roman_Number) -i) > 2){
             if(digit(roman_Number[i]) < digit(roman_Number[i+2])){
                 printf("Invalid roman number");
                 return 0;
             }
         }
 
         if(digit(roman_Number[i]) >= digit(roman_Number[i+1]))
             number = number + digit(roman_Number[i]);
         else{
             number = number + (digit(roman_Number[i+1]) - digit(roman_Number[i]));
             i++;
         }
         i++;
    }
 
    printf("Its decimal value is : %ld",number);
 
    return 0;
 
}
 
int digit(char c){
 
    int value=0;
 
    switch(c){
         case 'I': value = 1; break;
         case 'V': value = 5; break;
         case 'X': value = 10; break;
         case 'L': value = 50; break;
         case 'C': value = 100; break;
         case 'D': value = 500; break;
         case 'M': value = 1000; break;
         case '\0': value = 0; break;
         default: value = -1; 
    }
 
    return value;
}

question 7 

#include <stdio.h>
void main()
{
system("pstree");
return 0;
}
