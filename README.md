# Python core part 1

## abstract
  we will look some basic stuff in python, we can do much more with python ofcourse.

## python interpreter
    - python interpreter is usually located in /usr/local/bin 
    - By default, Python source files are treated as encoded in UTF-8. In that encoding, characters of most languages in the world can be used simultaneously in string literals, identifiers and comments  although the standard library only uses ASCII characters for identifiers, a convention that any portable code should follow.
    - On Unix, the Python 3.x interpreter is by default not installed with the executable named python, so that it does not conflict with a simultaneously installed Python 2.x executable.


## An informal introduction to python
### Numbers and strings
    - you can use python as calculator
    - we use + for adding - for substracting * for multiplying ** for power // for floor division % for remainder of the division.
    - = sign is used to assign a value to a variable.
    - we can use * with strings to repeat it
            a = 3 * 'num'
            print(a)

            O/P -> numnumnum
            # Explanation: string 'num' is getting repeated 3 times. 
    - + sign for concatanation.
            a = 'abc' + 'def'
            print(a)

            output -> abcdef
            # Explanation : 'abc' and 'def' got concatanated.

    - Strings can be indexed (subscripted), first letter is on index 0
            a = 'aditya'
            print(a[0])

            output : a
            # Explanation : first letter got printed as it was on index 0.

    - In addition to indexing, slicing is also supported. While indexing is used to obtain individual characters, slicing allows you to obtain substring
            example 1:
            a = 'aditya bhushan'
            print([:5])

            output: adity
            # Explanation: default value is for digit before colon is 0 thats why it prints from 0th index(included) to 5th index(excluded)

            example 2:
            a = 'aditya bhushan'
            print([5:])

            output: a bhushan
            # Explanation : it is printing from index 5(included) to end of the string

            example 3:
            a = 'aditya bhushan'
            print([4:8])
            output : ya b
            # Explanation : It is printing from 4th index(included) to 8th index(excluded)

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
