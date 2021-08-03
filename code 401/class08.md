## Read 08
## Game of Greed 3
### [List Comprehensions in Python](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)

List comprehensions provide a concise way to create lists.

#### Syntax
`new_list = [expression(i) for i in old_list if filter(i)]
`
#### Examples:

    #### Create a simple list:
    ```
        x = [i for i in range(10)]
           print x

           # This will give the output:
           [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    ```
   
    #### Create a list using loops and list comprehension:
    
    
  ```
     # You can either use loops:
     squares = []

     for x in range(10):
     squares.append(x**2)
 
     print squares
     [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

     # Or you can use list comprehensions to get the same result:
     squares = [x**2 for x in range(10)]

     print squares
     [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
  ```
    
    #### Multiplying parts of a list:
    
    ```
        list1 = [3,4,5]
 
         multiplied = [item*3 for item in list1] 
 
         print multiplied 
         [9,12,15]
    ```
