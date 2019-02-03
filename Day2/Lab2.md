Q1. WAP to check if a number is positive or not

```
n = 10
if(n > 0){
    print("Positive")
}
```
Output:
```
"Positive"
```

Q2. WAP to check if a number is positive or negative.
```
n = 10
if(n > 0){
    print("Positive")
} else{
    print("Negative")
}
```
Output:
```
"Positive"
```

Q 3.1. WAP to generate the series 1, 4, 9, ...., n^2
```
n = 10
for(i in 1:n){
    cat((i * i), " ")
}
```
Output:
```
1  4  9  16  25  36  49  64  81  100 
```

Q 3.2. WAP to find factorial of a given number within for loop.
```
n = 10
f = 1
for(i in 2:n){
    f = f * i
}
cat("Factorial: ", f)

```
Output:
```
Factorial:  3628800
```

Q 3.3. WAP to solve the following: 1^2 + 3^2 + ... + 39^2
```
n = 39
s = 0
for(i in 1:39){
    if(i %% 2 != 0){
        s = s + i * i
    }
}
print(s)
```
Output:
```
10660
```

Q 3.4. WAP to check if a given number is pallindrome or not.
```
n = 121
p = n
r = 0
while (n != 0) {
    a = n %% 10
    r = r * 10 + a
    n = floor(n / 10)
}
if (r == p) {
    print("Palindrome")
} else {
    print("Not Palindrome")
}
```
Output:
```
"Palindrome"
```

Q 3.5. WAP to check if a given number is perfect or not.
```
n = 6
div = seq_len(abs(n) - 1)
if (sum(div[n %% div == 0]) == n) {
    print("Perfect")
} else {
    print("Not Perfect")
}
```
Output:
```
"Perfect"
```

Q 3.6. WAP to generate Fibonacci Series upto n terms.
```
n = 10
a = 0
b = 1
cat("0  1  ")
for (i in 1 : (n - 2)) {
    c = a + b
    cat(c, " ")
    a = b
    b = c
}
```
Output:
```
0  1  1  2  3  5  8  13  21  34
```

Q 3.7. WAP to generate Floyd's Triangle.
```
rows = 4
num = 1
for (i in 1 : rows) {
    for (j in 1 : i) {
        cat(num, " ")
        num = num + 1
    }
    cat("\n")
}
```
Output:
```
1  
2  3  
4  5  6  
7  8  9  10  
```

Q 3.8. WAP to generate the following pattern:
```
   *
  * *
 * * *
* * * *
```
```
rows = 4
space = rows - 1
for (i in 1 : rows) {
    if (space != 0) {
        for (k in 1 : space) {
            cat(" ")
        }
    }
    space = space - 1
    for (j in 1 : i) {
        cat("* ")
    }
    cat("\n")
}
```
Output:
```
   *
  * *
 * * *
* * * *
```
