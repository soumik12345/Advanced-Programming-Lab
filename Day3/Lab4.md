
# Lab 4

```
Q 1. WAP to calculate average of 3 numbers using function.
Q 2. WAP to find factorial of a number using function.
Q 3. WAP to find out HCF and LCM of 2 numbers using function.
Q 4. WAP to print sum of series 1 + 2 + 3 + .... n using recursive function.
Q 5. WAP to reverse a number using recursive function.
Q 6. WAP to print Simple Interest from P, R, T
Q 7. WAP to convert decimal to binary using recursive function.
Q 8. WAP to find factorial using recursive function.
Q 9. WAP to find sum of 1^2 + 2^2 + 3^2 + ... + n^2 using recursive function.
Q 10. WAP to create a function get 5 numbers and displays the sum, averave and standard deviation.
```


```R
# Q1
average <- function(a, b, c) {
    return ((a + b + c) / 3)
}
cat("Average: ", average(10, 20, 30))
```

    Average:  20


```R
# Q2
factorial <- function(n) {
    f = 1
    for (i in 2 : n) {
        f = f * i
    }
    return (f)
}
cat("Factorial: ", factorial(10))
```

    Factorial:  3628800


```R
# Q3
gcd <- function(a, b) {
    if (b != 0) {
        return (gcd(b, a %% b))
    }
    return (a)
}

lcm <- function(a, b) {
    return (a * b / gcd(a, b))
}

cat("HCF: ", gcd(10, 20), "\n")
cat("LCM: ", lcm(10, 20), "\n")
```

    HCF:  10 
    LCM:  20 



```R
# Q4
add_series <- function(n) {
    if (n != 0) {
        return (n + add_series(n - 1))
    }
    return (0)
}

cat("Sum: ", add_series(10))
```

    Sum:  55


```R
# Q5
reverse_util <- function(n, r) {
    if (n != 0) {
        return (reverse((floor(n / 10)), (r * 10 + n %% 10)))
    }
    return (r)
}

reverse <- function(n) {
    return (reverse_util(n, 0))
}

cat("Reverse: ", reverse(122))
```


    Error in reverse((floor(n/10)), (r * 10 + n%%10)): unused argument ((r * 10 + n%%10))
    Traceback:


    1. cat("Reverse: ", reverse(122))

    2. reverse(122)

    3. reverse_util(n, 0)   # at line 10 of file <text>

    4. reverse((floor(n/10)), (r * 10 + n%%10))   # at line 4 of file <text>



```R
# Q6
simple_interest <- function(p, t, r = 10) {
    return (p * t * r / 100)
}

cat("Simple Intererst: ", simple_interest(100, 2))
```

    Simple Intererst:  20


```R
# Q7
binary <- function(n) {
    if (n == 0) {
        return (0)
    }
    return (n %% 2 + 10 * binary(floor(n / 2)))
}

cat("Binary:", binary(10))
```

    Binary: 1010


```R
# Q8
factorial <- function(n) {
    if (n != 0) {
        return (n * factorial(n - 1))
    }
    return (1)
}

cat("Factorial: ", factorial(10))
```

    Factorial:  3628800


```R
# Q9
add_square_series <- function(n) {
    if (n != 0) {
        return ((n * n) + add_square_series(n - 1))
    }
    return (0)
}

cat("Sum: ", add_square_series(10))
```

    Sum:  385


```R
# Q10
statistics <- function(a) {
    cat("Sum: ", sum(a), "\n")
    cat("Average:", mean(a), "\n")
    cat("Standard Deviation: ", sqrt(sum((a - mean(a)) ^ 2 / (length(a) - 1))), "\n")
}

statistics(c(20, 1212, 232, 33, 69))
```

    Sum:  1566 
    Average: 313.2 
    Standard Deviation:  509.5456 

