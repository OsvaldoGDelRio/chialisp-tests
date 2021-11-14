# Chialisp
Learning and practice with ChiaLisp
[Mortgage Coin Case](https://github.com/OsvaldoGDelRio/chialisp-tests#mortgagecoin)
[Loops and recursion](https://github.com/OsvaldoGDelRio/chialisp-tests#loops)



## READ FIRST

This is not a tutorial, I am learning, I do not recommend trying to create these coins, unless it is in test environment, like Testnet 

### mortgagecoin

Trying:

1. Allice is going to lend Bob X amount, but Bob will leave X amount of XCH in mortgage as guarantee of payment.

2. Allice cannot foreclose if the established time has not passed (TIME_TO_PAY)

3. Bob can make payments and the coin recreates itself.

4. If the same amount as the mortgage and payment (+ MORTGAGE_AMOUNT AMOUNT_TO_PAID) is deposited before the due date, the mortgage is returned and the fee payment is executed.

run results
```
(a (q 2 (i (> 10 5) (q 4 22 (c 23 (c 383 ()))) (q 2 (i (= 383 (+ 95 11)) (q 4 (c 22 (c 47 (c 11 ()))) (c (c 22 (c 23 (c (- 383 11) ()))) ())) (q 2 (i (> 383 (+ 95 11)) (q 4 (c 22 (c 47 (c 11 ()))) (c (c 22 (c 23 (c (- 383 11) ()))) ())) (q 4 (c 22 (c 767 (c 383 ()))) (c (c 8 (c -65 ())) (c (c 12 (c 767 ())) (c (c 30 (c 383 ())) ()))))) 1)) 1)) 1) (c (q (73 . 72) 80 51 . 60) 1))
```

solution
```
(600 10000 0xa11ce 0x426f62 100 0 0 0xcaf33f00d)
; TIME_TO_PAY MORTGAGE_AMOUNT MORTGAGE_EXECUTION_PUZZLE DEBTOR_PUZZLE AMOUNT_TO_PAID my_amount new_amount my_puzzlehash
```
brun
```
((51 0x0caf33f00d ()) (73 ()) (72 0x0caf33f00d) (60 ()))
```


### loops

Trying:

1. Iterate lists
2. Recursion

### To consider

The more calculations, operations and functions that are done in the program, the more cost is added, for the moment I am not considering the cost, only exploring the functionality and the limits.

Although, if one of the advantages of being able to program a currency / contract is that its behavior can be delimited, why leave functions out of the same currency? that will depend on each purpose and case. 