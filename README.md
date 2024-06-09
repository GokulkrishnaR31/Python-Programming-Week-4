# Python-Programming-Week-4
1.Factors of a number

Determine the factors of a number (i.e., all positive integer values that evenly divide into a number).

CODE:

n = int(input())

for i in range(1, n + 1):

    if n % i == 0:

        print(i, end=" ")
      #2.Non Repeated Digit Count

Write a program to find the count of non-repeated digits in a given number N. The number will be passed to the program as an input of type int.

Assumption: The input number will be a positive integer number >= 1 and <= 25000.

Some examples are as below.

If the given number is 292, the program should return 1 because there is only 1 non-repeated digit '9' in this number

If the given number is 1015, the program should return 2 because there are 2 non-repeated digits in this number, '0', and '5'.

If the given number is 108, the program should return 3 because there are 3 non-repeated digits in this number, '1', '0', and '8'.

If the given number is 22, the function should return 0 because there are NO non-repeated digits in this number.



CODE:

n = int(input())

digit_counts = {}



for digit in str(n):

    if digit not in digit_counts:

        digit_counts[digit] = 0

    digit_counts[digit] += 1

non_repeated_count=0

for  digits, count  in  digit_counts.items():

    if  count == 1:

              non_repeated_count+=1

        print(non_repeated_count)

#3.Prime Checking

Write a program that finds whether the given number N is Prime or not. If the number is prime, the program should return 2 else it must return 1.

Assumption: 2 <= N <=5000, where N is the given number.

CODE:

n = int(input())



if n <= 1:

    print(0)

else:

    for i in range(2, int(n ** 0.5) + 1):

        if n % i == 0:

            print(1)

            break

    else:

        print(2)

#4.Next Perfect Square

Given a number N, find the next perfect square greater than N.

CODE :

n = int(input())

sqrt = n ** 0.5

for i in range(int(sqrt) + 1, n + 2):

    if i * i > n:

        print(i * i)

        break
  #5.Nth Fibonacci

Write a program to return the nth number in the fibonacci series. The value of N will be passed to the program as input.

CODE:

a = int(input())

l = [0, 1]

for i in range(2, a):

    l.append(l[i-1] + l[i-2])

print(l[a-1])

#6.Disarium Number

A Number is said to be Disarium number when the sum of its digit raised to the power of their respective positions becomes equal to the number itself. Write a program to print number is Disarium or not.

CODE:

n = int(input())

sum = 0

for i, digit in enumerate(str(n), start=1):

    sum += int(digit)**i



if sum == n:

    print("Yes")

else:

    print("No")

#7.Sum of Series

Write a program to find the sum of the series 1 +11 + 111 + 1111 + . . . + n terms (n will be given as input from the user and sum will be the output)

CODE:

n = int(input())

sum = 0

for i in range(1, n + 1):

    sum += int('1' * i)

print(sum)
#8.Unique Digit Count

Write a program to find the count of unique digits in a given number N. The number will be passed to the program as an input of type int.

Assumption: The input number will be a positive integer number >= 1 and <= 25000.

For e.g.

If the given number is 292, the program should return 2 because there are only 2 unique digits '2' and '9' in this number

If the given number is 1015, the program should return 3 because there are 3 unique digits in this number, '1', '0', and '5'.

CODE:

n = int(input())

digits = set(str(n))

print(len(digits))

#9. Product of single digit

Given a positive integer N, check whether it can be represented as a product of single digit numbers.

CODE:

n = int(input())



if n < 10:

    print("Yes")

else:

    for i in range(2, int(n ** 0.5) + 1):

        if n % i == 0 and i < 10:

            print("Yes")

            break

    else:

        print("No")

#10.Perfect Square After adding One

Given an integer N, check whether N the given number can be made a perfect square after adding 1 to 





CODE:

n = int(input())

sqrt = (n + 1) ** 0.5

if sqrt.is_integer():

    print("Yes")

else:

    print("No")




