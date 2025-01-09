# Unit-1 [Basics of an Algorithm and its Properties](https://egyankosh.ac.in/bitstream/123456789/73664/4/Unit-1.pdf)

## Algorithm
The word *algorithm* is derived from the mathematician of the ninth century *Abdullah Jafar Muhammad ibn Musa Al-khowarizmi*. The word *al-khowarizmi* is 'Algorismus' in Latin which became Algorithm after his name.

He defined Algoritm as:
- An algorithm is a set of rules for carrying out calculation either by hand or on a machine.
- An algorithm is a well-defined computational procedure that takes input and produces output.
- An algorithm is a finite sequence of instructions or steps to achieve some particular output.

> An algorithm is a set of steps to solve a problem or a set of problems. Also, an algorithm is a step by step procedure to solve logical and mathematical or computational problems.

### Important Characteristics of an Algorithm
1. **Input**: There must be a finite number of inputs for the algorithm.
2. **Output**: There must be some output produced as a result of execution of the algorithm.
3. **Definiteness**: There must be a definite sequence of operations for transformation of input into output.
4. **Effectiveness**: Every step of the algorithm should be basic and essential
5. **Finiteness**: The transformation of input to output must be achieved in finite steps.

### Desirable Characteristics of an Algorithm
1. **General**: The algorithm should be general and is able to solve several cases.
2. **Efficiency**: The algorithm should use resources efficiently, i.e. takes less time and money in producing the result.
3. **Understandability**: The algorithms should be understandable and apply it to own problem.
4. **Uniqueness**: The algorithm should follow uniqueness such that instruction of the algorithm is unambiguous (synonyms : precise/absolute) and clear.

### Example

#### Euclid’s Algorithm
##### Pseudo Code:
```plaintext
// a and b are two positive numbers where a is the dividend and b is the divisor.
1. If b = 0, return a and exit.
2. Else, go to step 3.
3. Divide a by b and assign the remainder to r.
4. Assign the value of b to a and the value of r to q.
5. Repeat steps 1-4 until b = 0.
```

##### Euclid's algorithm impementation
```
begin [start of the algorithm]
{
    while (b != 0)
    {
        r <- a mod b
        a <- b
        b <- r
    } [end of while loop]
    return (b)
} [end of the algorithm]
```

##### GCD of a = 1071 and b = 462 using Euclid’s Algorithm
###### Iteration 1:
1. Divide a = 1071 by b = 462 and store the remainder in r.  
    r = 1071 % 462 (here, % represents the remainder operator)  
    r = 147  
2. If r = 0, the algorithm terminates and b is the GCD. Otherwise, go to step 3.  
    Here, r is not zero, so we will go to step 3.
3. The integer a will get the current value of integer q, and the new value of integer b will be the current value of r.  
  Here, a = 462 and b = 147
4. Go back to step 1.

###### Iteration 2:
1. Divide a = 462 by b = 147 and store the remainder in r.  
    r = 462 % 147 (here, % represents the remainder operator)  
    r = 21 
2. If r = 0, the algorithm terminates and b is the GCD. Otherwise, go to step 3.  
  Here, r is not zero, so we will go to step 3.
3. The integer a will get the current value of integer q, and the new value of integer b will be the current value of r.  
  Here, a = 147 and b = 21
4. Go back to step 1.

###### Iteration 3:
1. Divide a = 147 by b = 21 and store the remainder in r.  
  r = 147 % 21 (here, % represents the remainder operator)
  r = 0
2. If r = 0, the algorithm terminates and b is the GCD. Otherwise, go to step 3.  
  Here, r is zero, so the algorithm terminates and b is the answer, i.e. 21.

