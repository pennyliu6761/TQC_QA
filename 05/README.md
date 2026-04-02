# Python 第5類：函式(Function)
## Python 501 訊息顯示
請撰寫一程式，呼叫函式compute()，該函式功能為讓使用者輸入系別（Department）、學號（Student ID）和姓名（Name）並顯示這些訊息。

![](https://i.imgur.com/6rTdqdI.png)

```python
def compute():
    department = input()
    studentid =  input()
    name = input()
    print('Department:',department)
    print('Student ID:',studentid)
    print('Name:',name)
compute()
```

## Python 502 乘積
請撰寫一程式，將使用者輸入的兩個整數作為參數傳遞給一個名為compute(x, y)的函式，此函式將回傳x和y的乘積。

![](https://i.imgur.com/DtPDrYZ.png)

### 解法(1)
```python
def compute(x,y):
    print(x*y)
compute(int(input()),int(input()))
```
### 解法(2)
```python
def compute(x,y):
    return x*y
x = eval(input())
y = eval(input())
print(compute(x,y))
```

## Python 503 連加計算
請撰寫一程式，讓使用者輸入兩個整數，接著呼叫函式compute()，此函式接收兩個參數a、b，並回傳從a連加到b的和。

![](https://i.imgur.com/hEfFpTl.png)

```python
def compute(a,b):
    ans=0
    for i in range(a,b+1):
        ans+=i
    return ans
x = eval(input())
y = eval(input())
print(compute(x,y))
```

## Python 504 次方計算
請撰寫一程式，讓使用者輸入兩個整數，接著呼叫函式compute()，此函式接收兩個參數a、b，並回傳 $a^b$ 的值。

![](https://i.imgur.com/9A4QsOh.png)

### 解法(1)
```python
def compute(x,y):
    print(x**y)
compute(int(input()),int(input()))
```
### 解法(2)
```python
def compute(a,b):
    return pow(a,b)
x = eval(input())
y = eval(input())
print(compute(x,y))
```

## Python 505 依參數格式化輸出
請撰寫一程式，將使用者輸入的三個參數，變數名稱分別為a（代表字元character）、x（代表個數）、y（代表列數），作為參數傳遞給一個名為compute()的函式，該函式功能為：一列印出x個a字元，總共印出y列。
> [!TIP]
> - 輸出的每一個字元後方有一空格。

![](https://i.imgur.com/nOcjTfI.png)

```python
def compute(a,x,y):
    for i in range(y):
        for j in range(x):
            print('%c '%a,end='')
        print()
a = input()
x = eval(input())
y = eval(input())
compute(a,x,y)
```

## Python 506 一元二次方程式
請撰寫一程式，將使用者輸入的三個整數（代表一元二次方程式 $ax^2 + bx + c = 0$ 的三個係數a、b、c）作為參數傳遞給一個名為compute()的函式，該函式回傳方程式的解，如無解則輸出【Your equation has no root.】
> [!TIP]
> - 輸出有順序性
> - 回傳方程式的解，無須考慮小數點位數

![](https://i.imgur.com/HDSR1n3.png)

### 解法(1)
```python
def compute(a,b,c):
    temp=b**2-4*a*c
    if(temp<0): print('Your equation has no root.')
    elif(temp==0) : 
        ans=-b/2*a
        print('%.1f'%ans)
    elif(temp>0) :
        print('%.1f, %.1f'%((-b+temp**0.5)/(2*a),(-b-temp**0.5)/(2*a)))
compute(int(input()),int(input()),int(input()))
```
### 解法(2)
```python
def compute(a,b,c):
    q=b**2-4*a*c
    
    if q<0:
        print("Your equation has no root.")
    elif q==0:
        print(-b/2*a)
    else:
        q1=(-b+q**0.5)/(2*a)
        q2=(-b-q**0.5)/(2*a)
        print('{}, {}'.format(q1, q2))
a=int(input())
b=int(input())
c=int(input())
compute(a,b,c)
```

## Python 507 質數
請撰寫一程式，讓使用者輸入一個整數x，並將x傳遞給名為compute()的函式，此函式將回傳x是否為質數（Prime number）的布林值，接著再將判斷結果輸出。如輸入值為質數顯示【Prime】，否則顯示【Not Prime】。

![](https://i.imgur.com/voIVXoa.png)

```python
def compute(x):
    if x <= 1:
        return False
    for i in range(2,x):
        if x%i == 0:
            return False
    return True
x = eval(input())
if compute(x):
    print('Prime')
else:
    print('Not Prime')
```

## Python 508 最大公因數
請撰寫一程式，讓使用者輸入兩個正整數x、y，並將x與y傳遞給名為compute()的函式，此函式回傳x和y的最大公因數。

![](https://i.imgur.com/uPuMfVr.png)

### 解法(1)
```python
import math 
def compute(x,y):
    return math.gcd(x,y)
x,y=eval(input())
print(compute(x,y))
```
### 解法(2)
```python
def compute(x,y):
    while(y!=0):
        temp=y
        y=x%y
        x=temp
    print(x)
x,y=eval(input())
compute(x,y)
```

## Python 509 最簡分數
請撰寫一程式，讓使用者輸入二個分數，分別是x/y和m/n（其中x、y、m、n皆為正整數），計算這兩個分數的和為p/q，接著將p和q傳遞給名為compute()函式，此函式回傳p和q的最大公因數（Greatest Common Divisor, GCD）。再將p和q各除以其最大公因數，最後輸出的結果必須以最簡分數表示

![](https://i.imgur.com/z6Pfjx9.png)

```python
import math
def  compute(x,y):
    gcd = math.gcd(x,y)
    return gcd  
x,y = eval(input())
m,n = eval(input())
q = y*n
p = m*y+x*n
gcd=compute(p,q)
print(f'{x}/{y} + {m}/{n} = {int(p/gcd)}/{int(q/gcd)}')
```

## Python 510 費氏數列
請撰寫一程式，計算費氏數列（Fibonacci numbers），使用者輸入一正整數num (num>=2)，並將它傳遞給名為compute()的函式，此函式將輸出費氏數列前num個的數值。
> [!TIP]
> - 費氏數列的某一項數字是其前兩項的和，而且第0項為0，第一項為1，表示方式如下：

$$F_0 = 0$$ $$F_1 = 1$$ $$F_n = F_{n-1} + F_{n-2}$$

![](https://i.imgur.com/osDAZ4N.png)

### 解法(1)
```python
def compute(n):                        
    if n > 1:                      
        return compute(n-1) + compute(n-2)  # 遞迴
    return n
n=int(input())
for i in range(n):                 
    print(compute(i), end = ' ')   
```
### 解法(2)
```python
def compute(n): 
    curr = 1
    pre = 0
    print(0,1,end=' ')
    for i in range(2,n):
        temp = curr+pre
        print(temp,end=' ')
        pre = curr
        curr = temp
        
num = eval(input())
compute(num)
```
---
