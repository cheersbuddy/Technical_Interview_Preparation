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

```
#include <stdio.h>
int main() {
    char a[1],b[1];
    int c;
    scanf("%d", &a);
    scanf("%d", &b);
    c = a + b;
    printf("%d", c);
    return 0;
}
```
-The code will lead to a compilation error.

-Explanation:
-The code will throw a compilation error because 'a' and 'b' are declared as char arrays, but the code is reading input as an integer.

```
scanf("%[^\n]%*c", &s);

..
printf("%s",s);
```
-all the characters entered as the input, including the spaces, until we hit the enter button are stored in the variable, name
-%[^\n]" means 'read everything that is not a newline'

- %*c read the next character but don't save it anywhere'; 
this gets rid of the newline that we didn't read in the first part.

- %s is used as format specifier instead of %c because of %*c which expects a pointer
  
   ```
  scanf("%[^\n]%*c",&sen);
   ...
    printf("%s",s); // a random statement
    printf("\n%s",sen);
   ```
   - \n cannot be used in the end of the second statement but the begining of third because the format specifier used in scanf will read a new line character which is executed at the end of the previous statement
     

