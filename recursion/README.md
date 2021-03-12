# Recursion
People end up saying that recursion is a technique in which function calls itself, which is not completely wrong but let's have a look from different perspective.

so recursion is used to solve a bigger problem by solving smaller of same nature.
suppose we want to calculate factorial of a number 

```c++
#include<iostream>
using namespace std;

int factorial(int n){
    int n*factorial(n-1);
}
int main(){
    int n;
    cout<<factorial(n);
    return 0;
}
```
now the problem with the above code is it will get compiled successfully but it will give segmentation fault when executed. why? because there is no base case provided 

now what's the base case?
base case it certain condition when wee are confirm that we will get our solution at a particular point.
why we need to give base case?
because base case is used to terminate the code from being executed after the correct solution is found.

so suppose if n = 5 in the above code then,
![factorial](https://github.com/garooda/data-structures/blob/main/recursion/photo_2021-03-12_14-57-49.jpg)

above code will never terminate and hence it will give segmentation fault when executed.

so the correct code will be


```c++
#include<iostream>
using namespace std;

int factorial(int n){
    if(n==0 || n==1){              //base case
        return n;
    }
    else{
    int n*factorial(n-1);
    }
}
int main(){
    int n;
    cout<<factorial(n);
    return 0;
}
```
