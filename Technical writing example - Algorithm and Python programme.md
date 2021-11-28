#Python Bubble Sort Algorithm

##About

The bubble sort algorithm, also referred to as the sinking sort algoritm, is one of the simplest sorting algorithms. A sorting algorithm is an algorithm that orders elements of a list. The order of the elements can be numerical or lexicographical.

##How it works

The bubble sort algorithm works as follows:

1) The algorithm starts the sorting at the beginning of the data set. 

2) It compares the first two first elements:1) 

- ( **9 5** 7 3 1)

3) If the first element is greater than the second element, the elements are swapped:

- ( **5 9** 7 3 1)

4) Next, it compares the second and third element. If the third element is greater than the second element, the elements are swapped:


```python
- ( 5 **9 7** 3 1) -> ( 5 **7 9** 3 1)
```

5) The process is repeated until the end of the data set:

- ( 5 7 **9 3** 1 ) -> ( 5 7 **3 9** 1)
- ( 5 7 3 **9 1** ) -> ( 5 7 3 **1 9**)
- ( **5 7** 3 1 9 ) -> ( **5 7** 3 1 9 )
- ( 5 **7 3** 1 9 ) -> ( 5 **3 7** 1 9 )
- ( 5 3 **7 1** 9 ) -> ( 5 3 **1 7** 9 )
- ( 5 3 1 **7 9** ) -> ( 5 3 1 **7 9** )
- ( **5 3** 1 7 9 ) -> ( **3 5** 1 7 9 )
- ( 3 **5 1** 7 9 ) -> ( 3 **1 5** 7 9 )
- ( 3 1 **5 7** 9 ) -> ( 3 1 **5 7** 9 )
- ( 3 1 5 **7 9** ) -> ( 3 1 5 **7 9** )
- ( **3 1** 5 7 9 ) -> ( **1 3** 5 7 9 )
- ( 1 **3 5** 7 9 ) -> ( 1 **3 5** 7 9 )
- ( 1 3 **5 7** 9 ) -> ( 1 3 **5 7** 9 )
- ( 1 3 5 **7 9** ) -> ( 1 3 5 **7 9** )

6) The algorithm continues with the process until a whole pass with no swaps occurs:

- ( **1 3** 5 7 9 ) >> ( **1 3** 5 7 9 )
- ( 1 **3 5** 7 9 ) >> ( 1 **3 5** 7 9 )
- ( 1 3 **5 7** 9 ) >> ( 1 3 **5 7** 9 )
- ( 1 3 5 **7 9** ) >> ( 1 3 5 **7 9** )

7) The result is a sorted list:

- ( 1 3 5 7 9 )

##Python programme

To create a Python programme for the bubble sort algorithm:

1) Define a function to sort an unsorted array:


```python
def bubble_sort(arr):
```

2) Create an outer loop to go through all the elements of the array:


```python
    for i in range(len(arr)):
```

3) Create an inner loop to go through elements in range of the lenght of the array minus 1:


```python
        for j in range(len(arr) -1):
```


      File "<ipython-input-1-4b2deeca6134>", line 1
        for j in range(len(arr) -1):
                                    ^
    SyntaxError: unexpected EOF while parsing
    


4) If the element is greater than the next element, swap them:


```python
           if arr[j] > arr[j +1]:
                arr[j], arr[j +1] = arr[j +1], arr[j]
```

5) Insert the list you want to sort into a new variable called *x*:


```python
x = ('5, 7, 3, 1, 9')
```

6) Split the list and store the outcome in the *arr* variable:


```python
arr = x.split()
```

7) Call the function:


```python
bubble_sort(arr)
```

8) Print the result:


```python
print (*arr)
```

9) Let's run the entire programme:


```python
def bubble_sort(arr):
    for i in range(len(arr)):
        for j in range(len(arr) -1):
            if arr[j] > arr[j +1]:
                arr[j], arr[j +1] = arr[j +1], arr[j]
                
x = ('5 9 7 3 1')
arr = x.split()

bubble_sort(arr)
print(*arr)
```

    1 3 5 7 9
    
