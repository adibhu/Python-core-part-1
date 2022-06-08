# Python core part 1

## abstract
  we will look some basic stuff in python, we can do much more with python ofcourse.

## python interpreter
   -python interpreter is usually located in /usr/local/bin 
   -By default, Python source files are treated as encoded in UTF-8. In that encoding, characters of most languages in the world can be used simultaneously     in string literals, identifiers and comments  although the standard library only uses ASCII characters for identifiers, a convention that any portable     code should follow.
   - On Unix, the Python 3.x interpreter is by default not installed with the executable named python, so that it does not conflict with a simultaneously        installed Python 2.x executable.


## An informal introduction to python
### Numbers and strings
   * you can use python as calculator
   * we use + for adding - for substracting * for multiplying ** for power // for floor division % for remainder of the division.
   * = sign is used to assign a value to a variable.
   * we can use * with strings to repeat it
            
            a = 3 * 'num'
            print(a)
            
            Output -> numnumnum
            Explanation: string 'num' is getting repeated 3 times. 
   *  '+' sign for concatanation.
            
            a = 'abc' + 'def'
            print(a)

          output -> abcdef
          Explanation : 'abc' and 'def' got concatanated.

   * Strings can be indexed (subscripted), first letter is on index 0
            
            a = 'aditya'
            print(a[0])

         output : a
         Explanation : first letter got printed as it was on index 0.

   * In addition to indexing, slicing is also supported. While indexing is used to obtain individual characters, slicing allows you to obtain substring
            
            example 1:
            a = 'aditya bhushan'
            print([:5])

         output: adity
         Explanation: default value is for digit before colon is 0 thats why it prints from 0th index(included) to 5th index(excluded)

        
         example 2:
         a = 'aditya bhushan'
         print([5:])

         output: a bhushan
         Explanation : it is printing from index 5(included) to end of the string

         example 3:
         a = 'aditya bhushan'
         print([4:8])
         output : ya b
         Explanation : It is printing from 4th index(included) to 8th index(excluded)
   
   * Now here comes the point where we have to sort the String, Let's have a look a how to sort Strings in Python.
         
         For sorting strings in Python we can't use sort function directly and it will tell us that **'str' object has no attribute 'sort'**
         
           Example for Sorting a String - 

           temp_string = "This is Testing String"
           temp = ''.join(sorted(temp_string))
           print(temp)

           O/P - STTegghiiiinnrssstt

           // Now here we have used sorted function which will give us sorted list of all characters in given string and then we can join it using join function
         
### Lists
   - Python knows a number of compound data types, used to group together other values. The most versatile is the list, which can be written as a list of comma-separated values (items) between square brackets. Lists might contain items of different types, but usually the items all have the same type.
   - Like strings, lists can be indexed and sliced.
       
         Example: 
           a = [0,1,2,3,4,5,6]
           print(a[2])
           
         output : 2
           
         a = [0,1,2,3,4,5,6]
            print(a[2:5])
           
         output : [2,3,4]
        
   - append is used to add data in list
            
            a = [0,1,2,3,4,5,6]
            a.append(5)
            print(a)
            
         output : [0,1,2,3,4,5,6,5]
        
   - len is used to get the length of the lists.
            
            a = [0,1,2,3,4,5,6]
            print(len(a))
            
         output : 7


## More control flow tools
### if statement
   - if is used where we have to check any condition
         
         a = 6
          if a == 6:
             print('six')
             
         output : six
          
   - else can be used with if , although it is optional.
          
          a = 5
          if a == 6:
             print('six')
          else:
            print('not six')
           output: not six
           
   - elif is the short for 'else if'.
          
          a = 6
          if a == 6:
             print('six')
          elif a == 5:
             print('five')
             
         output : six

### for statement
   - for statement in python is little different for other programming languages lik c , in python we can iterate over items of lists or strings
       
         a = [0,1,2,3]
         for i in a:
            print(i)
        
          output : 0
                   1
                   2
                   3
                 

### the range function
   - If you do need to iterate over a sequence of numbers, the built-in function range() comes in handy. It generates arithmetic progressions.
     
          for i in range(4):
          print(i)
    
    output : 0
             1
             2
             3
             
### break and continue statement:
   - break statement is used to jump out of for loop or while loop.
        
         for i in range(5):
           print(i)
           break
          
         output: 0
         Explanation : for loop runs 1 time only because when it encounters break statement it jumps out of loop.
        
   - by using continue statement control can jump on next iteration of loop.
            
           for num in range(2, 10):
              if num % 2 == 0:
              print("Found an even number", num)
              continue
              print("Found an odd number", num)

        
         output: Found an even number 2
                Found an odd number 3
                Found an even number 4
                Found an odd number 5
                Found an even number 6
                Found an odd number 7
                Found an even number 8
                Found an odd number 9
                    
        
         Explanation: when num%2 == 0 condition satisfies control enters into if statement and prints 'Found an een number' and then it encounters                  break statement and it comes out of the loop and in next iteration condition fails and it prints 'Found an odd nuber'.           
                    
### pass statement:
   - The pass statement does nothing. It can be used when a statement is required syntactically but the program requires no action. For example:
        
         while True:
           pass  
           
        
         Explanation: Busy-wait for keyboard interrupt (Ctrl+C)
         
### Defining functions:
   - def keyword is used to define functions in python
         
         def MyFunction(n):
             print(n)
           
   #### Default argument values:
   - The most useful form is to specify a default value for one or more arguments. This creates a function that can be called with fewer arguments than          it is defined to allow.
        
         def MyFunction(n=5):
            print(n)
            
         Explanation: If argument will be passed to the function MyFunction while calling it that balue would be taken as n otherwise n's default value 5            will be taken.
        
   #### Keyword argument:
   - Functions can also be called using keyword arguments of the form kwarg=value. For instance, the following function
           
           def MyFunction(n, m=5):
              print(n, m)
              
        
           Explanation : above function accepts one required argument n and one optional argument m.
         
         
         
   #### Lambda expression:
   - lambda keyword can be use to create small one liner functions.
          
          x = lambda a : a + 10
          print(x(5)) 
                
          output: 15
          Explanation: x is function which takes one argument a and returns a + 10
            
            
   ## Data structures:
   ### More on lists:
   - list.append(x) is used to add an item at the end of the list  equivalent to a[len(a):] = [x].
            
            a = [1,2,3]
            a.append(4)
            print(a)
              
          output: [1,2,3,4]
           
   - list.insert(i, x) is used to insert item at a specific index.
              
              a = [1,2,3]
              a.insert(0, 4)
              print(a)
              
             output: [4,1,2,3]
            
   -  list.remove(x) is used to remove remove the first item from the list whose value is equal to x. It raises a ValueError if there is no such item
                
                a = [1,2,3]
                a.remove(3)
                print(a)
              
               output: [1,2]
             
        - list.pop(i) is used to remove an item at a given index.
               
               a = [1,2,3]
                a.pop(1)
                print(a)
              
              output: [1,3]
             
        - list.clear() is used remove all the items from the list.
              
              a = [1,2,3]
                a.clear()
                print(a)
              
              output: []
              
        - list.index(x) is used to get index of first item whose value is equal to x.
              
              a = [1,2,3]
                b = a.index(2)
                print(b)
              
              output: 1
              
        - list.count(x) is used to get the count of x in the list.
                 
                 a = [1,2,3]
                 b = a.count(2)
                   print(b)
              
              output: 1
              
        -  list.sort() can be used to sort items in list.
              
                a = [1,2,3,0]
                a = a.sort()
                  print(a)
                      
                 output: [0,1,2,3]
                    
        - list.reverse() can be used to reverse elements of list in place.
                      
                      a = [1,2,3,0]
                      a = a.reverse()
                      print(a)
              
              output: [0,3,2,1]
                    
        - list.copy() returns a shallow copy of the list.
                      
                      a = [1,2,3,0]
                      b = a.copy()
                      print(b)
                      
              output: [1,2,3,0]
                    
   ### The del statement
   - There is way to delete an element from list given its index instead of its value.
                      
                      a = [1,2,3,0]
                      del a[2]
                      print(a)
                      
          output: [1,2,0]
   ### Tuples and sequences:
   - A tuple consists of a number of values separated by commas.
        
          t = 12345, 54321, 'hello!'
          print(t)
        
          output: (12345, 54321, 'hello!')
       
          Explanation: parentheses is included in output always to keep it unambiguous in case of nested tuple.
          
   - A tuple is a collection which is ordered and unchangeable.
              
              When we say that tuples are ordered, it means that the items have a defined order, and that order will not change.
              Tuples are unchangeable, meaning that we cannot change, add or remove items after the tuple has been created.
   - Tuple items are indexed, the first item has index [0], the second item has index [1] etc.
   - Since tuples are indexed, they can have items with the same value:
        
   ### sets
   -  A set is an unordered collection with no duplicate elements.
           
           myset = {"apple", "banana", "cherry"}
           print(myset)
            
          output: {'cherry', 'banana', 'apple'}
            
   - Unordered - Unordered means that the items in a set do not have a defined order.
   - unchangeble - Set items are unchangeable, meaning that we cannot change the items after the set has been created.
        
   - Set objects also support mathematical operations like union, intersection, difference, and symmetric difference.

### Dictionaries
   - Dictionary contains data in form of key value pairs.        
      
          mydict = { 'apple' : 2, 'mango' : 3, 'orange' : 4 }
            print(mydict)
            
            output: {'apple': 2, 'mango': 3, 'orange': 4}
   
   - Sorting Dictionary Using Keys
       
           // Here we will use x[0] for sorting Dictionary using it's Keys.

           temp_dict = {1:4, 3:2, 2:3, 4:1, 0:5}
           temp_dict = dict(sorted(temp_dict.items(), key=lambda x: x[0]))
           print(temp_dict)

           O/P - {0: 5, 1: 4, 2: 3, 3: 2, 4: 1}
       
   - Using Values
       
           // Here we will use x[1] for sorting Dictionary using it's Values.  

           temp_dict = {1:4, 3:2, 2:3, 4:1, 0:5}
           temp_dict = dict(sorted(temp_dict.items(), key=lambda x: x[1]))
           print(temp_dict)

           O/P - {4: 1, 3: 2, 2: 3, 1: 4, 0: 5}
   
   - Sorting Dictionary in Reverse Order
      
          // For sorting in Reverse or Descending Order we can use reverse option in sorted function.

          temp_dict = {1:4, 3:2, 2:3, 4:1, 0:5}
          temp_dict = dict(sorted(temp_dict.items(), key=lambda x: x[1], reverse=True))
          print(temp_dict)

          O/P - {0: 5, 1: 4, 2: 3, 3: 2, 4: 1}
            
 ### Looping techniques
        
   - When looping through dictionaries, the key and corresponding value can be retrieved at the same time using the items() method.
         
         knights = {'gallahad': 'the pure', 'robin': 'the brave'}
         for k, v in knights.items():
         print(k, v)
        
         output: gallahad the pure
         robin the brave
         
  ## Conclusion
        Python is easy to read programing language most of the keywords are very obvious to understand.
  ## Reference
   - [w3schools](www.w3schools.com)
   - [Python documentation](https://docs.python.org/3/tutorial/)
