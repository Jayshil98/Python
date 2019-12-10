# PYTHON PROGRAM TO ADD 2 NUMBERS


```python
num1 = 15
num2 = 12
```


```python
#Adding two numbers
sum = num1 + num2 
```


```python
#printing values
print("Sum of {0} and {1} is {2}".format(num1,num2,sum))
```

    Sum of 10 and 20 is 60
    

# ADDING TWO NUMBER PROVIDED BY USER INPUT


```python
#Number is input by User
number1 = input("First number: ")
number2 = input("\nSecond number: ")
```

    First number: 20.5
    
    Second number: 10.5
    


```python
#Adding Two Numbers
sum = float(number1) + float(number2)
```


```python
#printing values
print("The sum of {0} and {1} is {2}" .format(number1, number2, sum))
```

    The sum of 20.5 and 10.5 is 31.0
    


```python
#printing value with different technique
f"Sum of {number1}, {number2} is {sum}"
```




    'Sum of 20.5, 10.5 is 31.0'



# ADDITION OF 3 NUMBERS


```python
num1 = 10
num2 = 20
num3 = 30
```


```python
#Adding three numbers
sum = num1 + num2 + num3
```


```python
f"Sum of {num1}, {num2} & {num3} is {sum}"
```




    'Sum of 10, 20 & 30 is 60'



# PYTHON PROGRAM FOR FACTORIAL OF A NUMBER

![](data:image/jpeg;base64,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)


```python
#logic is:- n! = n*(n-1)*(n-2)*...*1

def factorial(n):
    return 1 if (n==1 or n==0) else n*factorial(n-1);

num=5;
print("Factorial of", num, "is",factorial(num))
```

    Factorial of 5 is 120
    


```python
def factorial(n):
    return 1 if (n==1 or n==0) else n*factorial(n-1);

num = int(input("Enter number to find factorial: "))
print("Factorial of", num, "is",factorial(num))
```

    Enter number to find factorial: 5
    Factorial of 5 is 120
    

# PYTHON PROGRAM FOR COMPOUND INTEREST

![](https://www.thecalculatorsite.com/images/compound-interest-formula-diagram.png)


```python
#Compound Interest = P(1 + R/100)^nt

def compound_interest(principle, rate, time):
    result = principle * (pow((1 + rate / 100), time))
    return result

p = float(input("Enter the principal amount: "))
r = float(input("Enter the interest rate: "))
t = float(input("Enter the time in years: "))

amount = compound_interest(p, r, t)
interest = amount - p
print("Compound amount is %.2f" % amount)
print("Compound interest is %.2f" % interest)
```

    Enter the principal amount: 1200
    Enter the interest rate: 5
    Enter the time in years: 1
    Compound amount is 1260.00
    Compound interest is 60.00
    

# PYTHON PROGRAM FOR SIMPLE INTEREST

![](data:image/png;base64,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)


```python
#Simple Interest = (P*R*T)/100

def simple_interest(principle,rate,time):
    result = ((principle * rate * time)/100)
    return result

p = float(input("Enter the principal amount: "))
r = float(input("Enter the interest rate: "))
t = float(input("Enter the time in years: "))

SI = simple_interest(p,r,t)
print("Simple Interest is %.2f" % SI)
```

    Enter the principal amount: 10000
    Enter the interest rate: 5
    Enter the time in years: 5
    Simple Interest is 2500.00
    

# PYTHON PROGRAM TO CHECK WHETHER NUMBER IS ARMSTRONG OR NOT

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSJIG4iLGEMQF9gNmnfB6En4m-iErWvRjn35ggAeXvSM7RDHQDbqw&s)


```python
#A number is called Armstrong number if it is equal to the sum of the cubes of its own digits.
#For example: 153 is an Armstrong number since 153 = 1*1*1 + 5*5*5 + 3*3*3.

num = input("Enter a number: ")
sum = 0  
temp = int(num)  
  
while temp > 0:  
   digit = temp % 10  
   sum += pow(digit,len(num)) 
   temp //= 10  
  
if int(num) == sum:  
   print(num,"is an Armstrong number")  
else:  
   print(num,"is not an Armstrong number")  
```

    Enter a number: 4679307774
    4679307774 is an Armstrong number
    

# PYTHON PROGRAM TO FIND AREA OF CIRCLE

![](data:image/png;base64,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)


```python
#Area of circle:- pi * r**2 , where r is Radius.

PI = 3.14
r = float(input("Enter radius of circle: "))
area = PI * r**2

print("Area of circle is: %.2f" %area)
```

    Enter radius of circle: 12
    Area of circle is: 452.16
    

# PYTHON PROGRAM TO CHECK NUMBER IS PRIME OR NOT


```python
num = int(input("Enter a number: "))  
  
if num > 1:  
    for i in range(2,num):  
        if (num % i) == 0:       
            print(num,"is not a prime number")
            break
        
        else:
            print(num,"is a prime number")
```

    Enter a number: 12
    12 is not a prime number
    

# PYTHON PROGRAM TO PRINT ALL PRIME NUMBERS IN AN INTERVAL


```python
start = int(input("Enter starting Number: "))
end = int(input("Enter Last Number: "))

for val in range(start, end + 1):
    if val > 1:
        for n in range(2,val):
            if(val%n)==0:
                break
        
        else:
            print(val)
```

# PYTHON PROGRAM FOR nth FIBONACCI NUMBER

![](data:image/png;base64,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)


```python
def Fibonacci(n): 
    if n<0: 
        print("Incorrect input") 
    # First Fibonacci number is 0 
    elif n==1: 
        return 0
    # Second Fibonacci number is 1 
    elif n==2: 
        return 1
    else: 
        return Fibonacci(n-1)+Fibonacci(n-2) 
  
fb = Fibonacci(int(input("Enter number: ")))
```

# PYTHON PROGRAM FOR TABLES


```python
n = int(input("Enter number: "))
for num in range(1,n+1):
    print(f"\nTable of {num}\n")
    for i in range(1,11):
        print(num,'x',i,'=',num*i)
        print("===============")
```

    Enter number: 10
    
    Table of 1
    
    1 x 1 = 1
    ===============
    1 x 2 = 2
    ===============
    1 x 3 = 3
    ===============
    1 x 4 = 4
    ===============
    1 x 5 = 5
    ===============
    1 x 6 = 6
    ===============
    1 x 7 = 7
    ===============
    1 x 8 = 8
    ===============
    1 x 9 = 9
    ===============
    1 x 10 = 10
    ===============
    
    Table of 2
    
    2 x 1 = 2
    ===============
    2 x 2 = 4
    ===============
    2 x 3 = 6
    ===============
    2 x 4 = 8
    ===============
    2 x 5 = 10
    ===============
    2 x 6 = 12
    ===============
    2 x 7 = 14
    ===============
    2 x 8 = 16
    ===============
    2 x 9 = 18
    ===============
    2 x 10 = 20
    ===============
    
    Table of 3
    
    3 x 1 = 3
    ===============
    3 x 2 = 6
    ===============
    3 x 3 = 9
    ===============
    3 x 4 = 12
    ===============
    3 x 5 = 15
    ===============
    3 x 6 = 18
    ===============
    3 x 7 = 21
    ===============
    3 x 8 = 24
    ===============
    3 x 9 = 27
    ===============
    3 x 10 = 30
    ===============
    
    Table of 4
    
    4 x 1 = 4
    ===============
    4 x 2 = 8
    ===============
    4 x 3 = 12
    ===============
    4 x 4 = 16
    ===============
    4 x 5 = 20
    ===============
    4 x 6 = 24
    ===============
    4 x 7 = 28
    ===============
    4 x 8 = 32
    ===============
    4 x 9 = 36
    ===============
    4 x 10 = 40
    ===============
    
    Table of 5
    
    5 x 1 = 5
    ===============
    5 x 2 = 10
    ===============
    5 x 3 = 15
    ===============
    5 x 4 = 20
    ===============
    5 x 5 = 25
    ===============
    5 x 6 = 30
    ===============
    5 x 7 = 35
    ===============
    5 x 8 = 40
    ===============
    5 x 9 = 45
    ===============
    5 x 10 = 50
    ===============
    
    Table of 6
    
    6 x 1 = 6
    ===============
    6 x 2 = 12
    ===============
    6 x 3 = 18
    ===============
    6 x 4 = 24
    ===============
    6 x 5 = 30
    ===============
    6 x 6 = 36
    ===============
    6 x 7 = 42
    ===============
    6 x 8 = 48
    ===============
    6 x 9 = 54
    ===============
    6 x 10 = 60
    ===============
    
    Table of 7
    
    7 x 1 = 7
    ===============
    7 x 2 = 14
    ===============
    7 x 3 = 21
    ===============
    7 x 4 = 28
    ===============
    7 x 5 = 35
    ===============
    7 x 6 = 42
    ===============
    7 x 7 = 49
    ===============
    7 x 8 = 56
    ===============
    7 x 9 = 63
    ===============
    7 x 10 = 70
    ===============
    
    Table of 8
    
    8 x 1 = 8
    ===============
    8 x 2 = 16
    ===============
    8 x 3 = 24
    ===============
    8 x 4 = 32
    ===============
    8 x 5 = 40
    ===============
    8 x 6 = 48
    ===============
    8 x 7 = 56
    ===============
    8 x 8 = 64
    ===============
    8 x 9 = 72
    ===============
    8 x 10 = 80
    ===============
    
    Table of 9
    
    9 x 1 = 9
    ===============
    9 x 2 = 18
    ===============
    9 x 3 = 27
    ===============
    9 x 4 = 36
    ===============
    9 x 5 = 45
    ===============
    9 x 6 = 54
    ===============
    9 x 7 = 63
    ===============
    9 x 8 = 72
    ===============
    9 x 9 = 81
    ===============
    9 x 10 = 90
    ===============
    
    Table of 10
    
    10 x 1 = 10
    ===============
    10 x 2 = 20
    ===============
    10 x 3 = 30
    ===============
    10 x 4 = 40
    ===============
    10 x 5 = 50
    ===============
    10 x 6 = 60
    ===============
    10 x 7 = 70
    ===============
    10 x 8 = 80
    ===============
    10 x 9 = 90
    ===============
    10 x 10 = 100
    ===============
    
