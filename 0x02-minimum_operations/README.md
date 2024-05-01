# MinOperations project

In a text file, there is a single character H. Your text editor can execute only two operations in this file: Copy All and Paste. Given a number n, write a method that calculates the fewest number of operations needed to result in exactly n H characters in the file.

Prototype: def minOperations(n)
Returns an integer
If n is impossible to achieve, return 0
Example:

n = 9

H => Copy All => Paste => HH => Paste =>HHH => Copy All => Paste => HHHHHH => Paste => HHHHHHHHH

Number of operations: 6


## Flowchart of Solution
```bash
                    +------------------+
                    |  Start function  |
                    +------------------+
                             |
                             v
                    +--------------------+
                    | Set min_operations |
                    |      to zero       |
                    +--------------------+
                            |
                            v
                    +------------------+
                    | Check if n <= 1  |
                    +------------------+
                            |
                            v
            +--+<---+ If true, return 0
            |  |
            |  v
+-------------+-------------+
|   For i in range(2, n+1)  |
+---------------------------+
            |  |
            |  v
     +------+----------+
     | Check if n is   |
     | divisible by i  |
     +------+----------+
            |  |
            v  |
     +------+-----------+
     | Divide n by i    |
     | and add i to the |
     | total            |
     +------+-----------+
            |  |
            v  |
     +------+-----------+
     | Continue to      |
     | divide n by i    |
     | until n is no    |
     | longer divisible |
     | by i             |
     +------+-----------+
            |  |
            v  |
+-----------+--+-----------+
| Return min_operations    |
+--------------------------+
```
