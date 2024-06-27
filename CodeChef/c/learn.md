```
#include <stdio.h>
int main() {
    printf("This is a backslash: \\");
    return 0;
}
```
- Here there is 2 \\ to print one \ because the compiler mistakes it as a format specifier and skips it . 
```
#include <stdio.h>
int main() 
{ 
    printf(" For printing %% we use %%%%"); 
     return (0); 
}
```
- For printing % we use %%
```
  #include <stdio.h>
int main() {
    float num = 10 / 3;
    printf("%f\n", num);
    return 0;
}
```
-3.000000
-Explanation:
-10 / 3 evaluates to 3 (as per integer division) as both 10 and 3 are integer, then 3 gets assigned to float variable resulting in 3.000000

-there is no long float in C


