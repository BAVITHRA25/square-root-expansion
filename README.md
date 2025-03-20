Python Source Code
from decimal import getcontext, Decimal
N,P = int(input()), int(input())

getcontext().prec = P + 4

total_sum = 0
for number in range(2, N+1):
    square_root = Decimal(number).sqrt()
    if square_root % 1 != 0:
        t = str(square_root).replace('.','')[:P]
        total_sum+= sum(int(digit) for digit in t)

print(total_sum)
