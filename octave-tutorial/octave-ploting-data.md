# Ploting Data

```
>> t = [0:0.01:0.98];
>> y1 = sin(2*pi*4*t);
>> plot(t,y1)
>> y2 = cos(2*pi*4*t);
>> plot(t,y2)
>> plot(t,y1)
>> hold on
>> plot(t,y2,'r')
>> xlabel('time')
>> ylabel('value')
>> legend('sin', 'cos')
>> title('my plot')
>> cd '/Users/wpinhei/projetos/coursera/machine-learning'
>> print -dpng 'my-plot.png'
>> close
>> figure(1); plot(t,y1);
>> figure(2); plot(t,y2);
>> subplot(1,2,1); % Divides the plot a 1x2 grid, access 1st element
>> plot(t,y1);
>> subplot(1,2,2)
>> plot(t,y2);
>> axis([0.5 1 -1 1])
>> clf;
>> A = magic(5)
A =

   17   24    1    8   15
   23    5    7   14   16
    4    6   13   20   22
   10   12   19   21    3
   11   18   25    2    9

>> imagesc(A)
>> imagesc(A), colorbar, colormap gray;
>> A(1,2)
ans =  24
>> A(4,5)
ans =  3
>> imagesc(magic(15)), colorbar, colormap gray;
>> a = 1, b = 2, c = 3
a =  1
b =  2
c =  3
```
