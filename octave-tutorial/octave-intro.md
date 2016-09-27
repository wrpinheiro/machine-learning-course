# Octave Introduction

## Basic Math

```
octave:9> 5 + 6
ans =  11
octave:10> 3-2
ans =  1
octave:11> 1/2
ans =  0.50000
octave:12> 2^10
ans =  1024
octave:13> 1 == 2
ans = 0
octave:14> 10 == 10 % equality op
ans =  1
octave:15> 10 ~= 9 % inequality op
ans =  1
octave:16> 10 ~= 10
ans = 0

% LOGICAL OPERATORS

octave:18> 1 && 0
ans = 0
octave:19> 1 || 0
ans =  1
octave:20> 0 || 1
ans =  1
octave:21> xor(0,1)
ans =  1
octave:22> PS1('>> '); % change prompt to '>> '
>>
>> a = 3 % assignment
a =  3
>> a = 3; % ; at end suppresses the output
>>
>> c = (3 >= 1);
>> c
c =  1
>> a = pi;
>> a
a =  3.1416
>> disp(a)
 3.1416
>> disp(sprintf('2 decimals: %0.2f', a))
2 decimals: 3.14
>> disp(sprintf('6 decimals: %0.6f', a))
6 decimals: 3.141593
>> format long
>> a
a =  3.14159265358979
>> format short
>> a
a =  3.1416
```

## Matrices and Vectors

```
>> A = [1 2; 3 4; 5 6]
A =

   1   2
   3   4
   5   6

>> A = [1 2;
> 3 4;
> 5 6]
A =

   1   2
   3   4
   5   6

>> v = [1; 2; 3]
v =

   1
   2
   3

% create a vector with the 1st element equals 1, increments each element by 0.1 up to 2
>> v = 1:0.1:2
v =

    1.0000    1.1000    1.2000    1.3000    1.4000    1.5000    1.6000    1.7000    1.8000    1.9000    2.0000

% if the increment is ommited the value 1 will be assumed

>> v = 1:6
v =

   1   2   3   4   5   6

>> v = 2:6
v =

   2   3   4   5   6

>> ones(2,3)
ans =

   1   1   1
   1   1   1

>> C = 2*ones(2,3)
C =

   2   2   2
   2   2   2

>> w = ones(1,3)
w =

   1   1   1

>> w = zeros(1,3)
w =

   0   0   0

>> w = rand(3,3)
w =

   0.35475   0.89404   0.83913
   0.59934   0.74273   0.49337
   0.36400   0.13352   0.51389

>> rand(3,3)
ans =

   0.98109   0.47347   0.32385
   0.41950   0.37520   0.90965
   0.85046   0.40653   0.74837

% Gaussian distribution
>> w = randn(1, 3)
w =

   1.95924   0.52050   1.01613

>> w = randn(1, 3)
w =

  -0.81653  -0.60164  -0.23822

% shows a histogram
>> w = -6 + sqrt(10)*(randn(1,10000));
>> hist(w);
>> hist(w,50)

>> eye(4)
ans =

Diagonal Matrix

   1   0   0   0
   0   1   0   0
   0   0   1   0
   0   0   0   1

% calls help
>> help eye
```

