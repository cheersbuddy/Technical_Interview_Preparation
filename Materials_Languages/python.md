~~~
print(8)

print(13, end=" ")

print(21)
~~~
//end = is used to add string at the end of the line. 

~~~
OUTPUT:
8
13 21
~~~
~~~
x, y = map(int,input().split())
print(x * y)

INPUT
3 2

OUTPUT
6
~~~
//Input Function:

python
Copy code
input()
This function waits for the user to input a line of text. By default, it reads the input as a string.

Splitting the Input:

python
Copy code
input().split()
input() reads the entire input line as a string.
.split() method splits this string into a list of substrings based on whitespace (spaces, tabs, etc.). For example, if the user inputs "3 4", input().split() will produce the list ["3", "4"].
Mapping to Integers:

python
Copy code
map(int, input().split())
map() applies a function to all items in an input list.
int is the function we are applying, which converts strings to integers.
input().split() provides the list of strings.
map(int, input().split()) converts each substring in the list to an integer. In our example, it converts ["3", "4"] to [3, 4].
Unpacking the List:

python
Copy code
x, y = map(int, input().split())
This line unpacks the two integers from the map object and assigns them to the variables x and y.
In our example, x gets the value 3 and y gets the value 4.
Multiplying and Printing the Result:

python
Copy code
print(x * y)
This line multiplies x and y.
In our example, it calculates 3 * 4 which equals 12.
print() then outputs the result to the screen.
//
