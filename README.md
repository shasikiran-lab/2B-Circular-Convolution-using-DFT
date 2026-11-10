# EXPT 2B:CIRCULAR-CONVOLUTION-USING-DFT

## AIM
To perform and verify circular convolution operation of two given sequences using SCILAB.

## APPARATUS REQUIRED
PC installed with SCILAB

## PROGRAM:
## CIRCULAR CONVOLUTION
clc; 

clear;

x=[1 2 3 4];

n1=0:1:length(x)-1;

subplot(3,1,1);

plot2d3(n1,x);

xlabel('time');

ylabel('amplitude');

title('input sequence');

h=[2 4 8 6];

n2=0:1:length(h)-1;

subplot(3,1,2);

plot2d3(n2,h);

xlabel('time');

ylabel('amplitude');

title('impulse sequence');

N1=length(x);

N2=length(h);

N=max(N1,N2);

N3=N1-N2;

if(N3>0)

h=[h,zeros(1,N3)];

else

x=[x,zeros(1,abs(N3))];

end

disp(x)

disp(h)

for n=1:N

y(n)=0;

for i=1:N

j=n-i+1;

if(j<=0)

j=N+j;

end

y(n)=y(n)+x(i)*h(j);

end

end

disp(y)

n=0:N-1;

subplot(3,1,3);

plot2d3(n,y);

xlabel('time');

ylabel('amplitude');

title('circular convolution');


### CALCULATIONS:
<img width="912" height="1280" alt="image" src="https://github.com/user-attachments/assets/9b8f5e3d-6cb3-44ad-8982-b2ea2668aec4" />

### SAMPLE OUTPUT:
<img width="1179" height="854" alt="image" src="https://github.com/user-attachments/assets/3b484af8-3be3-4bd4-b326-e46a69a47af1" />

## RESULT:

Thus, the circular convolution of the two given sequences were performed and its result was verified.
