# Control Statements

```
>> v = zeros(10,1)
>> for i = 1:10,
> v(i) = 2^i;
> end;
>> indices = 1:10;
>> for i = indices,
>   disp(i);
> end;
 1
 2
 3
 4
 5
 6
 7
 8
 9
 10
>> i = 1
i =  1
>> while i <= 5,
> v(i) = 100;
> i = i + 1;
> end;
>> i = 1
i =  1
>> while true,
> i = i + 1;
> if i == 6,
> break;
> end;
> end;
>> v
v =

    100
    100
    100
    100
    100
     64
    128
    256
    512
   1024

>> v(1) = 2
v =

      2
    100
    100
    100
    100
     64
    128
    256
    512
   1024

>> v
v =

      2
    100
    100
    100
    100
     64
    128
    256
    512
   1024

>> if v(1) == 1,
>   disp('The value is one');
> elseif v(1) == 2,
>   disp('The value is two');
> else
>   disp('The value is not one or two');
> end
The value is two
```

## Creating functions

A function is created in a file with the same name of the function and extension `.m`. For example, to create a `squareThisNumber` a file with name `squareThisNumber.m` must be created. The content of this file is:

```
function y = squareThisNumber(x)
  y = x^2
```

To call the function use:

```
>> squareThisNumber(2)
ans =  4

% function [y1,y2] = squareThisNumber(x)
%   y1 = x^2
%   y2 = x^3

>> squareAndCubeThisNumber(2)
y1 =  4
y2 =  8
ans =  4
>> [a,b] = squareAndCubeThisNumber(2)
y1 =  4
y2 =  8
a =  4
b =  8
>> a
a =  4
>> b
b =  8

>> X = [1 1; 1 2; 1 3]
X =

   1   1
   1   2
   1   3

>> y = [1; 2; 3]
y =

   1
   2
   3

>> theta = [0;1]
theta =

   0
   1

% function J = costFunctionJ(X, y, theta)
%   m = size(X,1);
%   predictions = X*theta;
%   sqErrors = (predictions - y) .^ 2;
%
%   J = 1/(2*m) * sum(sqErrors);

>> costFunctionJ(X,y,theta)
ans = 0
>> j = costFunctionJ(X,y,theta)
j = 0
>> theta = [0;0]
theta =

   0
   0

>> j = costFunctionJ(X,y,theta)
j =  2.3333
>>
