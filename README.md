# What-is-the-product-
Given a positive integer n, calculate the product of all its non- prime digits. A digit is considered non- prime if it is not among {2, 3, 5, 7}. Input An integer n (0 ≤ n ≤ 10^9). Output Print an integer representing the product of all non- prime digits of n. If there are no non- prime digits in n, return 1.


def is_prime(num):
    if num < 2:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

def product_of_non_prime_digits(n):
    product = 1
    for digit in str(n):
        digit = int(digit)
        if not is_prime(digit):
            product *= digit
    return product


n = int(input())

result = product_of_non_prime_digits(n)
print(result)
