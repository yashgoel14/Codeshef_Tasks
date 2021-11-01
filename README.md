# Codeshef_Tasks

Name : Yash Goel               Date : 01/11/2021
Roll No. : RA2011047010101

                                                                          Task – 1

 ### Error Code 1:
 #### Solution :

#include <stdio.h>
int main()
{
int number, LD;
printf(" Enter a number : ");
scanf("%d", &number);
LD = number % 10;
printf(" \n The Last Digit of a Given Number %d = %d", number, LD);
return 0;
}

 ### Error Code 2 :
 #### Solution :

int sumcal(int len, int* arr, int value)
{
int sum = 0;
for(int i =0 ; i<= len-1; i++ )
{
    if(arr[i]%value == 0){
        sum += arr[i];
}
return sum;
}


 ### Error Code 3 :
 #### Solution :

#include <stdio.h>
int main()
{
for(int i=1;i <= 4;i++){
    for(int j=1;j <= 4; j++){
        if(i != j){
            printf("*");
        }
        else{
            printf(" ");
        }
    }
    printf("\n");
}
return 0;
}

 ### Error Code 4 :
 #### Solution :

#include <stdio.h>
int main() {
char a='A';
a>10?printf("Yes"):printf("No");
return 0;
}

 ### Error Code 5 :
 #### Solution :

#include <iostream>
using namespace std;
int main() {
int o, i, s;
for(o=5; o>=1; o--){
    for(s=1 ;s<=5-o ;s++){
        cout<<" ";
        for (i=1 ;i<=o ;i++){
            cout<<"*";
        }
        cout<<endl;
    }
}
return 0;
}
  
### Error Code 6:
#### Solution:

z=int(input(“Enter a number:”))
for x in range [0,9]:
    if z==x:
        print(“They are equal”)
    else:
        print(“They are not equal”)

### Error Code 7 :
#### Solution :
  
#include <iostream>
using namespace std;
class test{
    public:
    int my_variable;
};
int main() {
    test code_chef;
    cin>>code_chef.my_variable;
    if(code_chef.my_variable%2==0){
        cout<<"Even";
        }
    else{
        cout<<"odd";
    }
return 0;
}

### Error Code 8 :
#### Solution :
  
#include<iostream>
using namespace std;
void printSums(int N){
    int start=1, end=(N+1)/2;
    while (start<end){
        int sum=0;
        for (int i=start;i<=end;i++){
            sum+=i;
        }
        if (sum == N){
            for (int j=start;j<=N;j++)
            cout<<j<<" ";
            cout<<endl;
            break;
        }
        if (sum>N){
            break;
        }
        sum=0;
        start++;
    }
}
int main()
{
int n;
cin>>n;
printSums(n);
return 0;
}

### Error Code 9 :
#### Solution :
  
#include <iostream>
using namespace std;
int main() {
    int length;
    cout<<"enter the length of the array"<<endl;
    cin>>length;
    int array[length];
    for(int i=0;i<length;i++){
        cin>>array[i];
    }
    int min=array[0],max=array[0];
    for(int i=1;i<length;i++){
        if(array[i]>max)
        max = array[i];
        else if(array[i]<min)
        min = array[i];
    }
    cout<< min<<" "<<max;
    return 0;
}
                         
### Error Code 10 :
#### Solution :
                         
#include <stdio.h>
#include <string.h>
int main(){
    int t,i,diff_count;
    scanf("%d",&t);
    char s[100001];
    while(t--){
        diff_count=0;
        scanf("%s",s);
        for(int i=0;i<strlen(s)-1;i++){
            if(s[i]==s[i+1])
            diff_count++;
        }
        printf("%d\n",diff_count);
    }
return 0;
}

                                                                      Task – 2

### Ques 1.

n=int(input("Enter number of strings to compare : "))
l=[]
d={}

#Creating list of strings

for i in range(n):
    s=input("Enter string : ")
    l.append(s)
    
'''Creating dictionary by taking index as key and character at index 4
as value for len >= 4 and for len < 4 taking last character as value'''

j=0
for i in l:
    if(len(i)>=4):
        key=j
        value=i[3]
        d[key]=value
    else:
        key=j
        value=i[-1]
        d[key]=value
    j=j+1

#Sorting dictionary based on values
    
def first(element):
    return element[1]
sort_d=dict(sorted(d.items(),key=first))

#Printing list values based on keys of sorted dictionary

for i in sort_d.keys():
    print(l[i])

### Ques 2.

n=int(input("Input no. of elements required : "))
arr=[]
for i in range(0,n):
    num=int(input())
    arr.append(num)
for i in range(0,n):
    for j in range(i+1,n):
        if(arr[i]>arr[j]):
            temp=arr[i]
            arr[i]=arr[j]
            arr[j]=temp
f=int(input("Input nth smallest number to be found : "))
if(f>n):
    print("Error!!! pls input number within range",n)
else:
    print(f,"th smallest number is : ",arr[f-1])

### Ques 3.

l1=[chr(i) for i in range(65,91,4)]
l2=[chr(i) for i in range(99,120,4)]
j=0
for i in range(len(l2)):
    print(l1[j])
    print(l2[j])
    j=j+1

print(l1[-1]) #length of l1 > length of l2

### Ques 4.

k=int(input("Enter the number : "))
n=k**2
strm=str(n)
length=len(strm)
num1=int(strm[0:int(length/2)])
num2=int(strm[int(length/2):length])
if(num1+num2==k):
    print("Chef Number")
else:
    print("Not Chef Number")



















