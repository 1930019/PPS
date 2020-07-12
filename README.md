

DEPARTMENT OF COMPUTER SCIENCE & ENGINEERING

GURU NANAK DEV ENGINEERING COLLEGE, LUDHIANA

CODE

1. WAP to Add two numbers.

#include<stdio.h>
int main()
{
float n1,n2,sum;
printf("Enter 1st,2nd number: ");
scanf("%f%f",&n1,&n2);
sum=n1+n2;
printf("Sum of 1st & 2nd number is = %.2f\n",sum);
return 0;
}

OUTPUT

Enter 1st,2nd number: 5 6
Sum of 1st & 2nd number is = 11.00

CODE

2. WAP to find the Average of 'n' numbers.

#include<stdio.h>
int main()
{
int n,i,a[50];
float sum=0,avg;
printf("Enter number of elements: ");
scanf("%d",&n);
printf("Enter %d elements: ",n);
for(i=0 ; i<n ; i++)
{
scanf("%d",&a[i]);
sum+=a[i];
}
avg=sum/n;
printf("Average is %.2f.\n",avg);
return 0;
}

OUTPUT

Enter number of elements: 5
Enter 5 elements: 4 5 6 7 8
Average is 6.00.

CODE

3. WAP to Print weekdays using switch statement.

#include<stdio.h>
int main()
{
int n;
printf("Enter weekday in number: ");
scanf("%d",&n);
switch(n)
{
case 1:
printf("Monday\n");    //Taking the business week
break;
case 2:
printf("Tuesday\n");
break;
case 3:
printf("Wednesday\n");
break;
case 4:
printf("Thursday\n");
break;
case 5:
printf("Friday\n");
break;
case 6:
printf("Saturday\n");
break;
case 7:
printf("Sunday\n");
break;
default:
printf("Invalid Input\n");
}
return 0;
}

OUTPUT

Enter weekday in number: 2
Tuesday

CODE

4. WAP to find whether a number is Even or Odd.

#include<stdio.h>
int main() {
int n;
printf("Enter a number: ");
scanf("%d",&n);
if(n%2==0)
printf("Number is even.\n");
else
printf("Number is odd.\n");
return 0;
}

OUTPUT

Enter a number: 77
Number is odd.

CODE

5. WAP to Print the table of 2 using for loop.

#include<stdio.h>
int main() {
int n=1,product=2;
printf("\tTable of 2\n");
printf("\t==========\n\n");
for(; n<=10 ; n++,product+=2)
if(n<=4)
printf(" 2 x %d = %d 2 x %d = %d\n", n, product, n+10, product+20);
else if(n<=9)
printf(" 2 x %d = %d 2 x %d = %d\n", n, product, n+10, product+20);
else
printf(" 2 x %d = %d 2 x %d = %d\n", n, product, n+10, product+20);
return 0;
}

CODE

6. WAP to check whether the number is an Armstrong number or not.

#include<stdio.h>
int main()
{
int n,temp,digit,sum=0;
printf("Enter any positive integer: ");
scanf("%d",&n);
temp=n;
while(temp>0)
{
digit=temp%10;    //Storing one's place
temp/=10;    //Storing number removing one's place
sum+=digit * digit * digit;    //Incrementing sum by cubing & adding all digits one-by-one
}
if(n==sum)
printf("The entered number is an Armstrong number.\n");
else
printf("The entered number is not an Armstrong number.\n");
return 0;
}

OUTPUT

Enter any positive integer: 153
The entered number is an Armstrong number.

CODE

7. WAP to Print calculator using puts.

#include<stdio.h>
void main()
{
puts(" _____________________ ");
puts("| _____________________ |\n");
puts("| 1 | 2 | 3 |\t|\n");
puts("| ___ | ___ | ___ |\t|\n");
puts("| 4 | 5 | 6 | + |\n");
puts("| ___ | ___ | ___ | ___ |\n");
puts("| 7 | 8 | 9 | - |\n");
puts("| ___ | ___ | ___ | ___ |\n");
puts("|\t0\t | * |\n");
puts("| _______________ | ___ |\n");
}

CODE

8. WAP for Bubble Sort.

#include<stdio.h>
int main()
{
int a[20],i,n,k,temp;
printf("\nEnter size of array: ");
scanf("%d",&n);
printf("\nEnter %d elements of array.\n",n);
for(i=0 ; i<n ; i++)
scanf("%d",&a[i]);
for(k=0 ; k<n-1 ; k++)
{
for(i=0 ; i<n-k-1 ; i++)
{
if(a[i]>a[i+1])
{
temp=a[i];
a[i]=a[i+1];
a[i+1]=temp;
}
}
}
printf("\nArray elements after sorting..\n");
for(i=0 ; i<n ; i++)
printf("%d ",a[i]);
printf("\n");
return 0;
}

OUTPUT

Enter size of array: 5
Enter 5 elements of array.
5 4 2 1 8
Array elements after sorting..
1 2 4 5 8

CODE

9. WAP for Binary Search.

#include<stdio.h>
int main()
{
int a[25],i,m,n,first=0,last,mid;
printf("Enter the length of array: ");
scanf("%d",&m);
printf("Enter %d elements in ascending order: ",m);
for(i=0 ; i<m ; i++)
scanf("%d",&a[i]);
printf("Enter value to find: ");
scanf("%d",&n);
last=n-1;    //To initialise to last index position
mid=(first+last)/2;
while(first<=last)
{
if(a[mid]<n)
first=mid+1;
else if(a[mid]==n)
{
printf("%d found at position #%d.\n",n,mid+1);    //mid+1 done to display location & not index position
break;
}
else
last=mid-1;
mid=(first+last)/2;
}
if(first>last)
printf("%d not found in the entered array!\n",n);    //Test expression turned false, which means desired element wasn't found
return 0;
}

OUTPUT

Enter the length of array: 4
Enter 4 elements in ascending order: 2 6 7 9
Enter value to find: 7
7 found at position #3.

CODE

10. WAP to find the Factorial of a number.

#include<stdio.h>
int main()
{
int n,i, fac=1;
printf("Enter number which you want to get factorial of: ");
scanf("%d",&n);
for(i=n ; i>1 ; i--)    //i>0 can also be set as test expression, but multiplying with 1 changes nothing
fac*=i;
printf("\n%d! = %d\n",n,fac);
return 0;
}

OUTPUT

Enter number which you want to get factorial of: 6
6! = 720

CODE

11. WAP for Fizz-Buzz.

#include<stdio.h>
int main() {
for(int d=1 ; d<=30 ; d++) {
if(d%3==0 && d%5==0)
printf("FizzBuzz\n");
else if(d%3==0)
printf("Fizz\n");
else if(d%5==0)
printf("Buzz\n");
else
printf("%d\n",d);
}
return 0;
}

OUTPUT

1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
16
17
Fizz
19
Buzz
Fizz
22
23
Fizz
Buzz
26
Fizz
28
29
FizzBuzz

CODE

12. WAP to find the Sum of first 100 numbers.

#include<stdio.h>
int main() {
int sum=0,n;
n=1;
while(n<=100)
{
sum+=n;
n++;
}
printf("Sum of first 100 +ve integers = %d\n",sum);
return 0;
}

OUTPUT

Sum of first 100 +ve integers = 5050

CODE

13. WAP to find the Greater of two numbers.

#include<stdio.h>
int main() {
int a,b;
printf("Enter any 2 no.s: ");
scanf("%d%d",&a,&b);
if(a>b)
printf("a is greater.\n");
else if(b>a)
printf("b is greater.\n");
else
printf("a is equal to b.\n");
return 0;
}

OUTPUT

Enter any 2 no.s: 5 4
a is greater.

CODE

14. WAP to find the Greatest of three numbers.

#include<stdio.h>
int a,b,c;
int largestof3(int a,int b,int c)    //Function definition
{ int largest=0;
if(a>b && a>c)
largest=a;
else if(b>c)
largest=b;
else
largest=c;
return largest;
}
int main()
{
printf("Enter 3 numbers: ");
scanf("%d %d %d",&a,&b,&c);
printf("The largest of the 3 numbers entered is %d.\n",largestof3(a,b,c));    //Function call
return 0;
}

OUTPUT

Enter 3 numbers: 33 34 35
The largest of the 3 numbers entered is 35.

CODE

15. WAP to find G.C.D. of two numbers.

#include<stdio.h>
int main()
{
int n1,n2,i,gcd;
printf("Enter 2 integers: ");
scanf("%d %d",&n1,&n2);
for(i=1 ; i<=n1 && i<=n2 ; i++)
if(n1%i==0 && n2%i==0)
gcd=i;
printf("GCD of %d and %d is %d.\n",n1,n2,gcd);
return 0;
}

OUTPUT

Enter 2 integers: 20 125
GCD of 20 and 125 is 5.

CODE

16. WAP to find whether the year is Leap year or not.

#include<stdio.h>
int main() {
int year;
printf("Enter an year: ");
scanf("%d",&year);
if(year%4==0)    //Only considering the simple condition as asked to
printf("Leap Year\n");
else
printf("Not a Leap Year\n");
return 0;
}

OUTPUT

Enter an year: 2016
Leap Year

CODE

17. WAP for Linear Search.

#include<stdio.h>
int main()
{
int i,m,a[25],n;
printf("Enter the length of array: ");
scanf("%d",&m);
printf("Enter %d elements: ",m);
for(i=0;i<m;i++)
scanf("%d",&a[i]);
printf("Enter the number you wish to find: ");
scanf("%d",&n);
for(i=0;i<m;i++)
{
if(a[i]==n)
{
printf("Search is successful. Element present at #%d\n",i+1);    //i+1 done to display location & not index position
break;
}
}
if(i==m)
printf("Search is unsuccessful.\n");    //Test expression turned false, which means desired element wasn't found
return 0;
}

OUTPUT

Enter the length of array: 5
Enter 5 elements: 1 3 4 2 0
Enter the number you wish to find: 4
Search is successful. Element present at #3

CODE

18. WAP for Matrix Addition.

#include<stdio.h>
void main()
{
int m, n, i, j;
float m1[10][10], m2[10][10], m3[10][10];
printf("Enter size of Matrix A & B as m,n: ");
scanf("%d%d",&m,&n);
printf("Enter elements of Matrix A row wise\n\n");
for( i=0 ; i<m ; i++ )
{
for( j=0 ; j<n ; j++ )
scanf("%f",&m1[i][j]);
}
printf("Enter elements of Matrix B row wise\n\n");
for( i=0 ; i<m ; i++ )
{
for( j=0 ; j<n ; j++ )    //Matrices to be added must have the same order
scanf("%f",&m2[i][j]);
}
printf("The resultant matrix:\n");
for( i=0 ; i<m ; i++ )
{
printf("\n");
for( j=0 ; j<n ; j++ )
{
m3[i][j]=m1[i][j]+m2[i][j];
printf("%.1f ",m3[i][j]);
}
}
printf("\n\n");
}

OUTPUT

Enter size of Matrix A & B as m,n: 2 2
Enter elements of Matrix A row wise
5.5 5.6
5 6.7
Enter elements of Matrix B row wise
3 2
1 0
The resultant matrix:
8.5 7.6
6.0 6.7

CODE
