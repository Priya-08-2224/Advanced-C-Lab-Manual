# EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
# Aim:
To write a C program print the lowercase English word corresponding to the number
# Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
# Program:


```

#include<stdio.h> 
#include<math.h>
int main()
{
     int n;
     scanf("%d",&n);
     if(n>=1 && n<=pow(4,3))
     {
     switch(n)
     {
     case 5:
     printf("forty one");
     break;
     case 6:
     printf("forty two");
     break;
     case 13:
     printf("forty three");
     break;
     case 14:
     printf("forty four");
     break;
     case 15:
     printf("forty five");
     break;
     case 16:
     printf("forty six");
     break;
     case 5:
     printf("forty seven");
     break;
     case 6:
     printf("forty eight");
     break;
     case 13:
     printf("forty nine");
     break;
     default:
     printf("Greater than 13");
}

```



# Output:


<img width="622" height="230" alt="image" src="https://github.com/user-attachments/assets/d76d1494-0053-4b1f-b11a-7f647c0a719c" />








# Result:
Thus, the program is verified successfully
 
# EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
# Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
# Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
# Program:

```
#include<string.h>
int main()
{
     char a[50];
     scanf("%s",a);
     int l=strlen(a);
     char h='0';
     for(int i=0;i<4;i++)
     {
          int c=0;
          for(int j=0;j<l;j++)
          {
               if(a[j]==h)
               {
                      c+=1;
         }
     }
    printf("%d ",c); h++;
    }
}
```




# Output:



<img width="825" height="162" alt="image" src="https://github.com/user-attachments/assets/417b0f78-6e2a-4294-a772-9d0a31bfe5e0" />







# Result:
Thus, the program is verified successfully

# EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
# Aim:
To write a C program to print all of its permutations in strict lexicographical order.

# Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
# Program:

```
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
#define MAX 10
#define LEN 100

void swap(char arr[MAX][LEN],int i,int j)
{
    char temp[LEN];
    strcpy(temp,arr[i]);
    strcpy(arr[i],arr[j]);
    strcpy(arr[j],temp);
}
int next_permutation(char arr[MAX][LEN],int n){
    int i=n-2;
    while(i>=0 && strcmp(arr[i],arr[i+1])>=0)i--;
    if(i<0) return 0;
    int j=n-1;
    while(strcmp(arr[i],arr[j])>=0)j--;
    swap(arr,i,j);
    int left =i+1,right=n-1;
    while(left<right) swap(arr,left++,right--);
    return 1;
}
int cmp(const void*a,const void*b){
    return strcmp((char*)a,(char*)b);
}
int main()
{
    int n;
    scanf("%d",&n);
    char arr[MAX][LEN];
    for(int i=0;i<n;i++) scanf("%s",arr[i]);
    qsort(arr,n,LEN,cmp);
    do{
        for(int i=0;i<n;i++) printf("%s ",arr[i]);
        printf("\n");
    }while(next_permutation(arr,n));
}
```




# Output:



<img width="457" height="400" alt="image" src="https://github.com/user-attachments/assets/1a4bde6b-bb37-4b48-91a8-1c1119a2e233" />







# Result:
Thus, the program is verified successfully
 
# EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
# Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
# Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
# Program:
```
#include<stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    int size=2*n-1;
    for(int i=0;i<size;i++)
    {
        for(int j=0;j<size;j++)
        {
            int value=n-(i<j?(i<size-j-1?i:size-j-1):(j<size-i-1?j:size-i-1));
            printf("%d ",value);
        }
        printf("\n");
    }
}

```


# Output:



<img width="656" height="675" alt="image" src="https://github.com/user-attachments/assets/ce6e6e55-2bb8-49b7-9a20-d594aee3b413" />







# Result:
Thus, the program is verified successfully

# EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

# Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

# Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

# Program:
```
#include <stdio.h>
void square();
int main(){
    
    square();
    return 0;
}
void square(){
    int a;
    scanf("%d",&a);
    float ans = a*a;
    printf("The square of %d is : %.2f",a,ans);
}
```





# Output:



<img width="827" height="198" alt="image" src="https://github.com/user-attachments/assets/be801231-ed10-4940-85fe-23512504f917" />







# Result:
Thus, the program is verified successfully



























