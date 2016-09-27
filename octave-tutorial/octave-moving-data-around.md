# Moving Data Around

```
% create a matrix
>> A = [1 2; 3 4; 5 6]
A =

   1   2
   3   4
   5   6

% the size o A (dimensions)
>> size(A)
ans =

   3   2

>> sz = size(A)
sz =

   3   2

>> size(sz)
ans =

   1   2

>> size(A, 1)
ans =  3

>> size(A, 2)
ans =  2

>> v = [1 2 3 4]
v =

   1   2   3   4

>> length(v)
ans =  4

>> size(v)
ans =

   1   4

>> length(A)
ans =  3

>> length([1;2;3;4;5])
ans =  5

>> pwd
ans = /Users/wpinhei

>> cd '/Users/wpinhei/projetos/coursera/machine-learning'

>> pwd
ans = /Users/wpinhei/projetos/coursera/machine-learning

>> ls
features.dat    priceY.dat

>> load featuresX.dat
>> load priceY.dat

>> who
Variables in the current scope:

A          B          C          I          a          ans        c          featuresX  priceY     sz         v          w

>> featuresX
featuresX =

   120     3
    80     2
   103     3
   150     4
    72     2
    55     1
   420     5
   305     4
   180     3
    90     2
    35     1
    53     2
    40     1
    81     3
   145     3
   203     4
   185     4
    72     3
    89     3
   245     4

>> featuresX(1,2)
ans =  3

>> featuresX(1,1)
ans =  120

>> size(featuresX)
ans =

   20    2

>> size(priceY)
ans =

   20    1

>> who
Variables in the current scope:

A          B          C          I          a          ans        c          featuresX  priceY     sz         v          w

>> whos
Variables in the current scope:

   Attr Name           Size                     Bytes  Class
   ==== ====           ====                     =====  =====
        A              3x2                         48  double
        B              2x2                         32  double
        C              2x3                         48  double
        I              6x6                         48  double
        a              1x1                          8  double
        ans            1x2                         16  double
        c              1x1                          1  logical
        featuresX     20x2                        320  double
        priceY        20x1                        160  double
        sz             1x2                         16  double
        v              1x4                         32  double
        w              1x10000                  80000  double

Total is 10122 elements using 80729 bytes

>> clear featuresX

>> whos
Variables in the current scope:

   Attr Name        Size                     Bytes  Class
   ==== ====        ====                     =====  =====
        A           3x2                         48  double
        B           2x2                         32  double
        C           2x3                         48  double
        I           6x6                         48  double
        a           1x1                          8  double
        ans         1x2                         16  double
        c           1x1                          1  logical
        priceY     20x1                        160  double
        sz          1x2                         16  double
        v           1x4                         32  double
        w           1x10000                  80000  double

Total is 10082 elements using 80409 bytes

>> v = priceY(1:10)
v =

   250
   200
   330
   250
   210
   190
   550
   430
   320
   185

>> whos
Variables in the current scope:

   Attr Name        Size                     Bytes  Class
   ==== ====        ====                     =====  =====
        A           3x2                         48  double
        B           2x2                         32  double
        C           2x3                         48  double
        I           6x6                         48  double
        a           1x1                          8  double
        ans         1x2                         16  double
        c           1x1                          1  logical
        priceY     20x1                        160  double
        sz          1x2                         16  double
        v          10x1                         80  double
        w           1x10000                  80000  double

Total is 10088 elements using 80457 bytes

>> v
v =

   250
   200
   330
   250
   210
   190
   550
   430
   320
   185

>> save hello.mat v;

>> clear

>> whos

>> load hello.mat
>> whos
Variables in the current scope:

   Attr Name        Size                     Bytes  Class
   ==== ====        ====                     =====  =====
        v          10x1                         80  double

Total is 10 elements using 80 bytes

>> save hello.txt v -ascii

>> A = [1 2; 3 4; 5 6]
A =

   1   2
   3   4
   5   6

>> A(3,2)
ans =  6

>> A(2,:)
ans =

   3   4

>> A(2,:) % ":" means every element along that row/column
ans =

   3   4

>> A(:,2)
ans =

   2
   4
   6

>> A([1 3], :)
ans =

   1   2
   5   6

>> A([1 3], :) %  get everything form the 1st and 3rd row
ans =

   1   2
   5   6

>> A
A =

   1   2
   3   4
   5   6

>> A(:,2)
ans =

   2
   4
   6

>> A(:,2) = [10; 11; 12]
A =

    1   10
    3   11
    5   12

>> A = [A, [100; 101; 102]] % append another column vector to right
A =

     1    10   100
     3    11   101
     5    12   102

>> A
A =

     1    10   100
     3    11   101
     5    12   102

>> [[200; 201; 202], A] % append another column vector to right
ans =

   200     1    10   100
   201     3    11   101
   202     5    12   102

>> A(:)
ans =

     1
     3
     5
    10
    11
    12
   100
   101
   102

>> A = [1 2; 3 4; 5 6]
A =

   1   2
   3   4
   5   6

>> B = [11 12; 13 14; 15 16]
B =

   11   12
   13   14
   15   16

>> C = [A B]
C =

    1    2   11   12
    3    4   13   14
    5    6   15   16

>> C = [A; B]
C =

    1    2
    3    4
    5    6
   11   12
   13   14
   15   16

>> size(C)
ans =

   6   2
```
