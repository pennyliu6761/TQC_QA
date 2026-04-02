# Python 第3類：迴圈敘述
## Python 301 迴圈整數連加
請使用迴圈敘述撰寫一程式，讓使用者輸入兩個正整數a、b（a < b），利用迴圈計算從a開始連加到b的總和。例如：輸入a=1、b=100，則輸出結果為5050（1 + 2 + … + 100 = 5050）。

![](https://i.imgur.com/LuXamdd.png)

```python
a=int(input())
b=int(input())
sum=0
for i in range (a,b+1):
    sum+=i
print(sum)
```

## Python 302 迴圈偶數連加
請使用迴圈敘述撰寫一程式，讓使用者輸入兩個正整數a、b（a < b），利用迴圈計算從a開始的偶數連加到b的總和。例如：輸入a=1、b=100，則輸出結果為2550（2 + 4 + … + 100 = 2550）。

![](https://i.imgur.com/olFEtov.png)

```python
a=int(input())
b=int(input())
sum=0
for i in range (a,b+1):
    if(i%2==0):
    sum+=i
print(sum)
```

## Python 303 迴圈數值相乘
請使用迴圈敘述撰寫一程式，讓使用者輸入一個正整數（<100），然後以三角形的方式依序輸出此數的相乘結果。
> [!TIP]
> - 輸出欄寬為4，且需靠右對齊。

![](https://i.imgur.com/1EqWR6p.png)

```python
a=eval(input())
c=0
for i in range(1,a+1):
    for j in range(1,i+1):
        c=i*j
        print("%4d"%(c),end='')
    print()
```

## Python 304 迴圈倍數總和
請使用迴圈敘述撰寫一程式，讓使用者輸入一個正整數a，利用迴圈計算從1到a之間，所有5之倍數數字總和。

![](https://i.imgur.com/xXA118o.png)

```python
n=eval(input())
sum=0
for i in range(1,n+1):
    if(i%5==0):
        sum+=i
print(sum)
```

## Python 305 數字反轉
請撰寫一程式，讓使用者輸入一個正整數，將此數值以反轉的順序輸出。

![](https://i.imgur.com/FTFy6VI.png)

**解法(1)**
```python
a=int(input())
if(a==0):
    print(0)
while (a!=0) :
    print(int(a%10),end="")
    a=a//10
```
**解法(2)**
```python
a=str(input())
reversed_string=''.join(reversed(a))
print(reversed_string)
```

## Python 306 迴圈階乘計算
請使用迴圈敘述撰寫一程式，讓使用者輸入一個正整數n，利用迴圈計算並輸出n!的值。

![](https://i.imgur.com/Qne2ROT.png)

```python
n=eval(input())
sum=1
for i in range(1,n+1):
    sum*=i
print(sum)
```

## Python 307 乘法表
1. 請使用迴圈敘述撰寫一程式，要求使用者輸入一個正整數n（n<10），顯示n*n乘法表。
2. 每項運算式需進行格式化排列整齊，每個運算子及運算元輸出的欄寬為2，而每項乘積輸出的欄寬為4，皆靠左對齊不跳行。

![](https://i.imgur.com/PkSLngw.png)

```python
n=int(input())
for i in range(1,n+1):
    for j in range(1,n+1):
        print('{} * {} = {:<4}'.format(j,i,(j*i)),end='')
    print()
```

## Python 308 迴圈位數加總
請使用迴圈敘述撰寫一程式，要求使用者輸入一個數字，此數字代表後面測試資料的數量。每一筆測試資料是一個正整數（由使用者輸入），將此正整數的每位數全部加總起來。

![](https://i.imgur.com/3dkncmL.png)

### 解法(1)
```python
for i in range(int(input())):
    n=str(input())
    a = [int(j) for j in list(str(n))] # 將對應的數字轉換成數字串列，例如 11 轉換成 [1, 1]
    print("Sum of all digits of "+str(n)+" is "+str(sum(a)))
```
### 解法(2)
```python
a=int(input())
for i in range(a):
    ans=0
    n=str(input())
    for i in range(0,len(n)):
        ans+=int(n[i])  
    print("Sum of all digits of "+str(n)+" is "+str(ans))
```
### 解法(3)
```python
n = eval(input())
for i in range(n):
    num = eval(input()) 
    t = num 
    ans = 0 
    while t!=0: 
        ans+=(t%10)  
        t=t//10 
    print('Sum of all digits of',num,'is',ans)
```

## Python 309 存款總額
請使用迴圈敘述撰寫一程式，> - 提示使用者輸入金額（如10,000）、年收益率（如5.75），以及經過的月份數（如5），接著顯示每個月的存款總額。
> [!TIP]
> - 四捨五入，輸出浮點數到小數點後第二位。
> - 舉例：
> -   假設您存款$10,000，年收益為5.75%。
> -   過了一個月，存款會是：10000 + 10000 * 5.75 / 1200 = 10047.92
> -   過了兩個月，存款會是：10047.92 + 10047.92 * 5.75 / 1200 = 10096.06
> -   過了三個月，存款將是：10096.06 + 10096.06 * 5.75 / 1200 = 10144.44
> -   以此類推。

![](https://i.imgur.com/OVKIioN.png)

```python
total = eval(input())
y = eval(input())
m = eval(input())
print('%s \t  %s' % ('Month', 'Amount'))
for i in range(1, m + 1):
    total += total * y / 1200    
    print('%3d \t %.2f' % (i, total))
```

## Python 310 迴圈公式計算
請使用迴圈敘述撰寫一程式，讓使用者輸入正整數n (1 < n)，計算以下公式的總和並顯示結果：

$$\frac{1}{1+\sqrt{2}} + \frac{1}{\sqrt{2}+\sqrt{3}} + \frac{1}{\sqrt{3}+\sqrt{4}} + ... + \frac{1}{\sqrt{n-1}+\sqrt{n}}$$

> [!TIP]
> - 輸出結果至小數點後四位。

![](https://i.imgur.com/yIf2R5l.png)

```python
x=eval(input())
i=1
tmp=0
while i<x:
    tmp+=1/((i**0.5)+((i+1)**0.5))
    i+=1
print('%.4f'%(tmp))
```
---
