# TQC+ 程式語言Python !!!

# Python 第1類：基本程式設計
## Python 101 整數格式化輸出
![](https://i.imgur.com/E5v7Tkh.png)


```python
a=input()
b=input()
c=input()
d=input()
print('|{:>5s} {:>5s}|'.format(a,b))
print('|{:>5s} {:>5s}|'.format(c,d))
print('|{:<5s} {:<5s}|'.format(a,b))
print('|{:<5s} {:<5s}|'.format(c,d))
```
##  Python 102 浮點數格式化輸出
![](https://i.imgur.com/gBlgFuu.png)

```python
a=float(input())
b=float(input())
c=float(input())
d=float(input())

print("|%7.2f %7.2f|"%(a,b))
print("|%7.2f %7.2f|"%(c,d))
print("|{:<7.2f} {:<7.2f}|".format(a,b))
print("|{:<7.2f} {:<7.2f}|".format(c,d))

```
## Python 103 字串格式化輸出
![](https://i.imgur.com/Yq6oTRc.png)

```python
a=input()
b=input()
c=input()
d=input()
print('|{:>10s} {:>10s}|'.format(a,b))
print('|{:>10s} {:>10s}|'.format(c,d))
print('|{:<10s} {:<10s}|'.format(a,b))
print('|{:<10s} {:<10s}|'.format(c,d))


```
## Python 104 圓形面積計算
![](https://i.imgur.com/nVQFNqI.png)

```python
import math

r=eval(input(""))
print("Radius = %.2f"%r)
print("Perimeter = %.2f"%(r*2*math.pi))
print("Area = %.2f"%(r*r*math.pi))
```

## Python 105 矩形面積計算
![](https://i.imgur.com/LTPCKDz.png)

```python
h=eval(input())
w=eval(input())
print('Height = %.2f'%h)
print('Width = %.2f'%w)
print('Perimeter = %.2f'%(w*2+h*2))
print('Area = %.2f'%(w*h))
```


## Python 106 公里英哩換算
![](https://i.imgur.com/4gEStEQ.png)
```python
x=float(input())
y=float(input())
z=float(input())
s = (z/1.6)/((60*x+y)/(60*60))
print("Speed = %.1f"%(s))
```
## Python 107 數值計算
![](https://i.imgur.com/cgvyQDs.png)
```python
l=[0]*5
l[0]=eval(input())
l[1]=eval(input())
l[2]=eval(input())
l[3]=eval(input())
l[4]=eval(input())
print(l[0],l[1],l[2],l[3],l[4])
print('Sum = %.1f'%sum(l))
print('Average = %.1f'%(sum(l)/len(l)))
```

## Python 108 座標距離計算
請撰寫一程式，讓使用者輸入四個數字x1、y1、x2、y2，分別代表兩個點的座標(x1, y1)、(x2, y2)。計算並輸出這兩點的座標與其歐式距離。

提示1：歐式距離 $= \sqrt{((x1-x2)^2+(y1-y2)^2)}$
提示2：兩座標的歐式距離，輸出到小數點後第4位
![](https://i.imgur.com/GAAdJ22.png)
```python
x1=eval(input())
y1=eval(input())
x2=eval(input())
y2=eval(input())
print(f'( {x1} , {y1} )')
print(f'( {x2} , {y2} )')
print('Distance = %.4f'% ((x1-x2)**2+(y1-y2)**2)**0.5)
```

## Python 109 正五邊形面積計算
請撰寫一程式，讓使用者輸入一個正數s，代表正五邊形之邊長，計算並輸出此正五邊形之面積（Area）。

提示1：建議使用import math模組的math.pow及math.tan
提示2：正五邊形面積的公式： $Area=(5 * s^2)/(4 * tan(pi/5))$
提示3：輸出浮點數到小數點後第四位。
![](https://i.imgur.com/u2vl0WZ.png)

```python
import math
s=eval(input())
print('Area = %.4f'%((5*s**2)/(4*math.tan(math.pi/5))))

```
## Python 110 正n邊形面積計算
設計說明：
請撰寫一程式，讓使用者輸入兩個正數n、s，代表正n邊形之邊長為s，計算並輸出此正n邊形之面積（Area）。

提示1：建議使用import math模組的math.pow及math.tan
提示2：正n邊形面積的公式如下：$Area = (n * s^2) / (4 * tan(pi/n))$
提示3：輸出浮點數到小數點後第四位
![](https://i.imgur.com/eooV6nO.png)
```python
import math
n=eval(input())
s=eval(input())
print('Area = %.4f'%((n*s**2)/(4*math.tan(math.pi/n))))
```
# Python 第2類：選擇敘述
## Python 201 偶數判斷
設計說明：
請使用選擇敘述撰寫一程式，讓使用者輸入一個正整數，然後判斷它是否為偶數（even）。
![](https://i.imgur.com/I6rcTPP.png)

```python
n=int(input())
if(n%2==0): print(f'{n} is an even number.')
else :  print(f'{n} is not an even number.')
```
## Python 202 倍數判斷
設計說明：
請使用選擇敘述撰寫一程式，讓使用者輸入一個正整數，然後判斷它是3或5的倍數，顯示【x is a multiple of 3.】或【x is a multiple of 5.】；若此數值同時為3與5的倍數，顯示【x is a multiple of 3 and 5.】；如此數值皆不屬於3或5的倍數，顯示【x is not a multiple of 3 or 5.】，將使用者輸入的數值代入x。
![](https://i.imgur.com/QQ0gQBX.png)
```python
x=int(input())
if(x%3==0 and x%5!=0): print(f'{x} is a multiple of 3.')
elif(x%3!=0 and x%5==0): print(f'{x} is a multiple of 5.')
elif(x%3==0 and x%5==0): print(f'{x} is a multiple of 3 and 5.')
else : print(f'{x} is not a multiple of 3 or 5.')
```
## Python 203 閏年判斷
設計說明：
請使用選擇敘述撰寫一程式，讓使用者輸入一個西元年份，然後判斷它是否為閏年（leap year）或平年。其判斷規則為：每四年一閏，每百年不閏，但每四百年也一閏。
![](https://i.imgur.com/cT40S1v.png)
```python
n=int(input())
if(n%4==0 and (n%400==0 or n%100!=0)): print(f'{n} is a leap year.')
else : print(f'{n} is not a leap year.')

```
## Python 204 算術運算
設計說明：
請使用選擇敘述撰寫一程式，讓使用者輸入兩個整數a、b，然後再輸入一算術運算子 (+、-、*、/、//、%），輸出經過運算後的結果。

![](https://i.imgur.com/7nQvOeH.png)

```python
a=eval(input())
b=eval(input())
c=str(input())
if(c=='+'): print(a+b)
elif(c=='-'): print(a-b)
elif(c=='*'): print(a*b)
elif(c=='/'): print(a/b)
elif(c=='//'): print(a//b)
elif(c=='%'): print(a%b)
```
## Python 205 字元判斷
設計說明：
請使用選擇敘述撰寫一程式，讓使用者輸入一個字元，判斷它是包括大、小寫的英文字母（alphabet）、數字（number）、或者其它字元（symbol）。例如：a為英文字母、9為數字、$為其它字元。
![](https://i.imgur.com/zMFwyzJ.png)
```python
n=str(input())
if(n.isdigit()): print(f'{n} is a number.')
elif(n.isalpha()) : print(f'{n} is an alphabet.')
else : print(f'{n} is a symbol.')
```

## Python 206 等級判斷
設計說明：
請使用選擇敘述撰寫一程式，根據使用者輸入的分數顯示對應的等級。標準如下表所示：

|分數|等級|
|---|---|
|80 ~ 100|A|
|70 ~ 79|B|
|60 ~ 69|C|
|<= 59|F|

![](https://i.imgur.com/mmShXrD.png)
```python
n=int(input())
if(n>=80 and n<=100) : print('A')
elif(n>=70 and n<80) : print('B')
elif(n>=60 and n<70) : print('C')
else : print('F')
```
## Python 207 折扣方案
設計說明：
請使用選擇敘述撰寫一程式，要求使用者輸入購物金額，購物金額需大於8,000（含）以上，並顯示折扣優惠後的實付金額。購物金額折扣方案如下表所示：

|金額|折扣|
|---|---|
|8,000（含）以上|9.5折|
|18,000（含）以上|9折|
|28,000（含）以上|8折|
|38,000（含）以上|7折|

```python
n=int(input())
if(n>=8000 and n<18000) : print(n*0.95)
elif(n>=18000 and n<28000): print(n*0.9)
elif(n>=28000 and n<38000): print(n*0.8)
elif(n>=38000): print(n*0.7)
```
## Python 208 十進位換算
設計說明：
請使用選擇敘述撰寫一程式，讓使用者輸入一個十進位整數num(0 ≤ num ≤ 15)，將num轉換成十六進位值。

提示：轉換規則=十進位0-9的十六進位值為其本身，十進位10-15的十六進位值為A-F。
![](https://i.imgur.com/So8krVa.png)
```python
n=eval(input())
if(n>=0 and n<10) : print(n)
elif (n==10) : print('A')
elif (n==11) : print('B')
elif (n==12) : print('C')
elif (n==13) : print('D')
elif (n==14) : print('E')
elif (n==15) : print('F')
```
## Python 209 距離判斷
設計說明：
請使用選擇敘述撰寫一程式，讓使用者輸入一個點的平面座標x和y值，判斷此點是否與點(5, 6)的距離小於或等於15，如距離小於或等於15顯示【Inside】，反之顯示【Outside】。

提示：計算平面上兩點距離的公式： $\sqrt{(x1-x2)^2 + (y1-y2)^2}\quad$

![](https://i.imgur.com/vupvPIn.png)
```python
x = eval(input())
y = eval(input())
d = ((x-5)**2+(y-6)**2)**0.5
if d <= 15: print('Inside')
else: print('Outside')
```
## Python 210 三角形判斷
設計說明：
請使用選擇敘述撰寫一程式，讓使用者輸入三個邊長，檢查這三個邊長是否可以組成一個三角形。若可以，則輸出該三角形之周長；否則顯示【Invalid】。

提示：檢查方法 = 任意兩個邊長之總和大於第三邊長
![](https://i.imgur.com/Xw2VRLp.png)
```python
a=int(input())
b=int(input())
c=int(input())
if(a+b>c and a+c>b and a+b>c): print(a+b+c)
else : print(Invalid)
```
# Python 第3類：迴圈敘述
## Python 301 迴圈整數連加
設計說明：
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
設計說明：
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
設計說明：
請使用迴圈敘述撰寫一程式，讓使用者輸入一個正整數（<100），然後以三角形的方式依序輸出此數的相乘結果。

提示：輸出欄寬為4，且需靠右對齊。
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
設計說明：
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
設計說明：
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
設計說明：
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
設計說明：
(1) 請使用迴圈敘述撰寫一程式，要求使用者輸入一個正整數n（n<10），顯示n*n乘法表。

(2) 每項運算式需進行格式化排列整齊，每個運算子及運算元輸出的欄寬為2，而每項乘積輸出的欄寬為4，皆靠左對齊不跳行。
![](https://i.imgur.com/PkSLngw.png)
```python
n=int(input())
for i in range(1,n+1):
  for j in range(1,n+1):
    print('{} * {} = {:<4}'.format(j,i,(j*i)),end='')
  print()
```
## Python 308 迴圈位數加總
設計說明：
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
設計說明：
請使用迴圈敘述撰寫一程式，提示使用者輸入金額（如10,000）、年收益率（如5.75），以及經過的月份數（如5），接著顯示每個月的存款總額。

提示：四捨五入，輸出浮點數到小數點後第二位。
舉例：
假設您存款$10,000，年收益為5.75%。
過了一個月，存款會是：10000 + 10000 * 5.75 / 1200 = 10047.92
過了兩個月，存款會是：10047.92 + 10047.92 * 5.75 / 1200 = 10096.06
過了三個月，存款將是：10096.06 + 10096.06 * 5.75 / 1200 = 10144.44
以此類推。
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
設計說明：
請使用迴圈敘述撰寫一程式，讓使用者輸入正整數n (1 < n)，計算以下公式的總和並顯示結果：

$$\frac{1}{1+\sqrt{2}} + \frac{1}{\sqrt{2}+\sqrt{3}} + \frac{1}{\sqrt{3}+\sqrt{4}} + ... + \frac{1}{\sqrt{n-1}+\sqrt{n}}$$

提示：輸出結果至小數點後四位。
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

# Python 第4類：進階控制流程
## Python 401 最小值
設計說明：
請撰寫一程式，由使用者輸入十個數字，然後找出其最小值，最後輸出最小值。
![](https://i.imgur.com/5DgKZKm.png)
```python
num = []
for i in range(10):
    num.append(eval(input()))
print(min(num))
```
## Python 402 不定數迴圈-最小值
設計說明：
請撰寫一程式，讓使用者輸入數字，輸入的動作直到輸入值為9999才結束，然後找出其最小值，並輸出最小值。
![](https://i.imgur.com/C2cBH1x.png)
```python
n= []
while True:
        value = eval(input())
        if value == 9999:
            break
        n.append(value)
print(min(n))
```
## Python 403 倍數總和計算
設計說明：
請撰寫一程式，讓使用者輸入兩個正整數a、b（a<=b），輸出從a到b（包含a和b）之間4或9的倍數（一列輸出十個數字、欄寬為4、靠左對齊）以及倍數之個數、總和。
![](https://i.imgur.com/ftgAeDk.png)
```python
a = int( input() )
b = int( input() )
total = 0
count = 0
for i in range( a, b + 1 ):
    if i % 4 == 0 or i % 9 == 0:
        count += 1
        print("{:<4d}".format(i), end="")
        if count % 10 == 0:
            print()
        total += i
print()
print(count)
print(total)
```
## Python 404 數字反轉判斷
設計說明：
請撰寫一程式，讓使用者輸入一個正整數，將此正整數以反轉的順序輸出，並判斷如輸入0，則輸出為0。
![](https://i.imgur.com/6jIG6q3.png)
```python
n=str(input())
s=''.join(reversed(n))
print(s)
```
## Python 405 不定數迴圈-分數等級
設計說明：
請撰寫一程式，以不定數迴圈的方式輸入一個正整數（代表分數），之後根據以下分數與GPA的對照表，印出其所對應的GPA。假設此不定數迴圈輸入-9999則會結束此迴圈。標準如下表所示：

|分數|GPA|
|---|---|
|90 ~ 100|A|
|80 ~ 89|B|
|70 ~ 79|C|
|60 ~ 69|D|
|0 ~ 59|E|

![](https://i.imgur.com/j8bGTWB.png)
```python
while True : 
    n=int(input())
    if n==-9999: break
    if(n>0 and n<60):
        print('E')
    elif(n>=60 and n<70):
        print('D')
    elif(n>=70 and n<80):
        print('C')
    elif(n>=80 and n<90):
        print('B')
    elif(n>=90 and n<=100):
        print('A')
```
## Python 406 不定數迴圈-BMI計算
設計說明：
請撰寫一程式，以不定數迴圈的方式輸入身高與體重，計算出BMI之後再根據以下對照表，印出BMI及相對應的BMI代表意義（State）。假設此不定數迴圈輸入-9999則會結束此迴圈。標準如下表所示：

|BMI值|	代表意義|
|---|---|
|BMI < 18.5|	under weight|
|18.5 <= BMI < 25|	normal|
|25.0 <= BMI < 30|	over weight|
|30 <= BMI|	fat|
提示： $BMI = 體重(kg)/身高^2(m)$，輸出浮點數到小數點後第二位。 不需考慮男性或女性標準。

![](https://i.imgur.com/2cgAcvW.png)
```python
while True:
    H = float(input())
    if H == -9999:   break
    else:
        W = float(input())
        BMI = W / (H/100)**2
        print(f'BMI: {BMI:.2f}')
        if BMI < 18.5:       print("State: under weight")
        if 18.5 <= BMI < 25: print("State: normal")
        if 25.0 <= BMI < 30: print("State: over weight")
        if 30 <= BMI:        print("State: fat")
```
## Python 407 不定數迴圈-閏年判斷
設計說明：
(1) 請撰寫一程式，以不定數迴圈的方式讓使用者輸入西元年份，然後判斷它是否為閏年（leap year）或平年。其判斷規則如下：每四年一閏，每百年不閏，但每四百年也一閏。
(2) 假設此不定數迴圈輸入-9999則會結束此迴圈。
![](https://i.imgur.com/eq4LHsb.png)
```python
year = eval(input())
while year!=-9999:
  if (year % 4 == 0 and year % 100 != 0) or year % 400 == 0:
        print('%d is a leap year.'%year)   
  else : 
        print('%d is not a leap year.'%year)
  year = eval(input())
```
## Python 408 奇偶數個數計算
設計說明：
請撰寫一程式，讓使用者輸入十個整數，計算並輸出偶數和奇數的個數。
![](https://i.imgur.com/qWhBFjV.png)
```python
even = odd = 0
for _ in range(10):
    if int(input()) % 2 == 0: even += 1
    else: odd += 1
print(f'Even numbers: {even}')
print(f'Odd numbers: {odd}')
```
## Python 409 得票數計算
設計說明：
某次選舉有兩位候選人，分別是No.1: Nami、No.2: Chopper。請撰寫一程式，輸入五張選票，輸入值如為1即表示針對1號候選人投票；輸入值如為2即表示針對2號候選人投票，如輸入其他值則視為廢票。每次投完後需印出目前每位候選人的得票數，最後印出最高票者為當選人；如最終計算有相同的最高票數者或無法選出最高票者，顯示【=> No one won the election.】。
![](https://i.imgur.com/pUfQrYH.png)

```python
count1 = 0
count2 = 0
null = 0
for i in range(5):
    vote = int(input())
    if  vote == 1:
        count1 += 1
    elif  vote == 2:
        count2 += 1
    else:
        null += 1    
    print("Total votes of No.1: Nami =  %d" % count1)
    print("Total votes of No.2: Chopper =  %d" % count2)
    print("Total null votes =  %d" % (null))
if count1 > count2:
    print("=> No.1 Nami won the election.")
elif count1 < count2:
    print("=> No.2 Chopper won the election.")
else:
    print("=> No one won the election.")
```
## Python 410 繪製等腰三角形
設計說明：
請撰寫一程式，依照使用者輸入的n，畫出對應的等腰三角形。
![](https://i.imgur.com/MbIQeI6.png)
```python
n = int(input())
for i in range(n, 0, -1):
    print(' '*(i-1) + '*'*(1+2*(n-i)))
```
# Python 第5類：函式(Function)
## Python 501 訊息顯示
設計說明：
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
設計說明：
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
設計說明：
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
設計說明：
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
設計說明：
請撰寫一程式，將使用者輸入的三個參數，變數名稱分別為a（代表字元character）、x（代表個數）、y（代表列數），作為參數傳遞給一個名為compute()的函式，該函式功能為：一列印出x個a字元，總共印出y列。

提示：輸出的每一個字元後方有一空格。
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
設計說明：
請撰寫一程式，將使用者輸入的三個整數（代表一元二次方程式 $ax^2 + bx + c = 0$ 的三個係數a、b、c）作為參數傳遞給一個名為compute()的函式，該函式回傳方程式的解，如無解則輸出【Your equation has no root.】

提示：
輸出有順序性
回傳方程式的解，無須考慮小數點位數
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
設計說明：
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
設計說明：
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
設計說明：
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
設計說明：
請撰寫一程式，計算費氏數列（Fibonacci numbers），使用者輸入一正整數num (num>=2)，並將它傳遞給名為compute()的函式，此函式將輸出費氏數列前num個的數值。

提示：費氏數列的某一項數字是其前兩項的和，而且第0項為0，第一項為1，表示方式如下：

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
# Python 第6類：串列(List)的運作(一維、二維以及多維)
## Python 601 偶數索引值加總
設計說明：
請撰寫一程式，利用一維串列存放使用者輸入的12個正整數（範圍1~99）。顯示這些數字，接著將串列索引為偶數的數字相加並輸出結果。

提示：輸出每一個數字欄寬設定為3，每3個一列，靠右對齊。
![](https://i.imgur.com/T5tuEVn.png)
```python
m={}
total=c=0
for i in range(0,12):
   m[i]=int(input())
   if(i%2==0):
     total+=m[i]
for i in range(0,12):
  print('{:>3d}'.format(m[i]),end="")
  c+=1
  if(c==3):
     print()
     c=0
print(total)
```
## Python 602 撲克牌總和
設計說明：
請撰寫一程式，讓使用者輸入52張牌中的5張，計算並輸出其總和。

提示：J、Q、K以及A分別代表11、12、13以及1。
![](https://i.imgur.com/Tvq8X4c.png)
```python
t=0
for i in range(5):
   n=str(input())
   if(n=='J'):   t+=11
   elif(n=='Q'): t+=12
   elif(n=='K'): t+=13
   elif(n=='A'): t+=1
   else :   t+=int(n)
print(t)
```
## Python 603 數字排序
設計說明：
請撰寫一程式，要求使用者輸入十個數字並存放在串列中。接著由大到小的順序顯示最大的3個數字。
![](https://i.imgur.com/JkxoZ4J.png)
```python
m=[]
for i in range(10):
   n=int(input())
   m.append(n)
m=sorted(m)
print(m[9],m[8],m[7])
```
## Python 604 眾數
設計說明：
請撰寫一程式，讓使用者輸入十個整數作為樣本數，輸出眾數（樣本中出現最多次的數字）及其出現的次數。

提示：假設樣本中只有一個眾數。
![](https://i.imgur.com/PUMSTBA.png)
### 解法(1)
```python
m=[0]*100
for i in range(10):
   n=int(input())
   m[n]+=1
print(m.index(max(m)))  #取得位址
print(max(m))
```
### 解法(2)
```python
m=[0]*100
for i in range(10):
   n=int(input())
   m[n]+=1
for i in range(0,100):
  if(max(m)==m[i]):
     print(i)
print(max(m))
```
## Python 605 成績計算
設計說明：
請撰寫一程式，讓使用者輸入十個成績，接下來將十個成績中最小和最大值（最小、最大值不重複）以外的成績作加總及平均，並輸出結果。

提示：平均值輸出到小數點後第二位。
![](https://i.imgur.com/GbiOkvH.png)
```python
n=[]
for i in range(10):
  x=eval(input())
  n.append(x)
s=sum(n)-max(n)-min(n)
print(s)
print("%.2f"%(s/(10-2)))
```
## Python 606 二維串列行列數
設計說明：
請撰寫一程式，讓使用者輸入兩個正整數rows、cols，分別表示二維串列lst 的「第一個維度大小」與「第二個維度大小」。
串列元素[row][col]所儲存的數字，其規則為：row、col 的交點值 = 第二個維度的索引col – 第一個維度的索引row。
接著以該串列作為參數呼叫函式compute()輸出串列。

提示：欄寬為4。
![](https://i.imgur.com/nRKAiV9.png)
```python
def compute(r,c):
    for i in range(r):
        for j in range(c):
          print("%4d"%(j-i), end='')
        print()
r = int(input())
c = int(input())
compute(r,c)
```
## Python 607 成績計算
設計說明：
請撰寫一程式，讓使用者輸入三位學生各五筆成績，接著再計算並輸出每位學生的總分及平均分數。

提示：平均分數輸出到小數點後第二位
![](https://i.imgur.com/S4PbmSg.png)
```python
n=["1st","2nd","3rd"]
t=[[0 for j in range(5)] for i in range(3)]
for i in range(3):
  print("The {} student:".format(n[i]))
  for j in range(5):
    t[i][j]=int(input())
 
for i in range(3):
  print("Student %d"%(i+1))
  print("#Sum %d"%(sum(t[i])))
  print("#Average %.2f"%(sum(t[i])/5))
```
## Python 608 最大最小值索引
設計說明：
請撰寫一程式，讓使用者建立一個3*3的矩陣，其內容為從鍵盤輸入的整數（不重複），接著輸出矩陣最大值與最小值的索引。
![](https://i.imgur.com/wyocxkC.png)
### 解法(1)
```python
n=[]
for i in range(9):   n.append(int(input()))
m=max(n)
mi=n.index(m)
print("Index of the largest number {} is: ({}, {})".format(m,mi//3,mi%3))
s=min(n)
si=n.index(s)
print("Index of the smallest number {} is: ({}, {})".format(s,si//3,si%3))
```
### 解法(2)
```python
a=[]
for i in range(9):
  n=int(input())
  a.append(n)
print(f'Index of the largest number {max(a)} is: ({(a.index(max(a)))//3}, {(a.index(max(a)))%3})')
print(f'Index of the smallest number {min(a)} is: ({(a.index(min(a)))//3}, {(a.index(min(a)))%3})')
```
## Python 609 矩陣相加

設計說明：
請撰寫一程式，讓使用者建立兩個2*2的矩陣，其內容為從鍵盤輸入的整數，接著輸出這兩個矩陣的內容以及它們相加的結果。
![](https://i.imgur.com/oBvmdTv.png)
```python
L1 = [[0 for i in range(2)] for j in range(2)]
L2 = [[0 for i in range(2)] for j in range(2)]
print('Enter matrix 1:')
for i in range(2):
    for j in range(2):
        L1[i][j] = int(input('[%d, %d]: '%(i+1,j+1)))
 
print('Enter matrix 2:')
for i in range(2):
    for j in range(2):
        L2[i][j] = int(input('[%d, %d]: '%(i+1,j+1)))
 
print('Matrix 1:')
for i in range(2):
    for j in range(2):
      print(L1[i][j],end=' ')
    print()
 
print('Matrix 2:')
for i in range(2):
    for j in range(2):
      print(L2[i][j],end=' ')
    print()
 
print('Sum of 2 matrices:')
for i in range(2):
    for j in range(2):
      print((L1[i][j]+L2[i][j]),end=' ')
    print()
```
## Python 610 平均溫度
設計說明：
請撰寫一程式，讓使用者輸入四週各三天的溫度，接著計算並輸出這四週的平均溫度及最高、最低溫度。

提示1：平均溫度輸出到小數點後第二位。
提示2：最高溫度及最低溫度的輸出，如為31時，則輸出31，如為31.1時，則輸出31.1。
![](https://i.imgur.com/Z8VoxTg.png)
```python
L=[]
for w in range(1,4+1):
  print("Week %d:"%w)
  for D in range(1,3+1):
    x=eval(input("Day %d:"%D))
    L.append(x)
 
A=sum(L)/len(L)
print("Average: %.2f"%A)
print("Highest:",max(L))
print("Lowest:",min(L))
```
# Python 第7類：數組（Tuple）、集合（Set）以及詞典（Dictionary）
## Python 701 串列數組轉換
設計說明：
請撰寫一程式，輸入數個整數並儲存至串列中，以輸入-9999為結束點（串列中不包含-9999），再將此串列轉換成數組，最後顯示該數組以及其長度（Length）、最大值（Max）、最小值（Min）、總和（Sum）。
![](https://i.imgur.com/FezBH03.png)
```python
LIST = []
num = eval(input())
while num!=-9999:
    LIST.append(num)
    num = eval(input())
TUPLE = tuple(LIST)
print(TUPLE)
print('Length:',len(TUPLE))
print('Max:',max(TUPLE))
print('Min:',min(TUPLE))
print('Sum:',sum(TUPLE))
```
## Python 702 數組合併排序
設計說明：
請撰寫一程式，輸入並建立兩組數組，各以-9999為結束點（數組中不包含-9999）。將此兩數組合併並從小到大排序之，顯示排序前的數組和排序後的串列
![](https://i.imgur.com/L1OO3jD.png)
### 解法(1)
```python
tuple1 = ()
num = eval(input('Create tuple1:\n'))
while num !=-9999:
    tuple1 +=(num,)
    num = eval(input())
tuple2 = ()
num = eval(input('Create tuple2:\n'))
while num !=-9999:
    tuple2 +=(num,)
    num = eval(input())
tuple1 += tuple2
print('Combined tuple before sorting:',tuple1)
LIST = list(tuple1)
LIST.sort()
print('Combined list after sorting:',LIST)
```
### 解法(2)
```python
t1=()
print('Create tuple1:')
while True : 
     n=int(input())
     if(n==-9999) : break
     t1+=(n,)
t2=()
print('Create tuple2:')
while True : 
     n=int(input())
     if(n==-9999) : break
     t2+=(n,)
t1 += t2
print('Combined tuple before sorting:',t1)
LIST = list(t1)
LIST.sort()
print('Combined list after sorting:',LIST)
```
## Python 703 數組條件判斷
設計說明：
請撰寫一程式，輸入一些字串至數組（至少輸入五個字串），以字串"end"為結束點（數組中不包含字串"end"）。接著輸出該數組，再分別顯示該數組的第一個元素到第三個元素和倒數三個元素。
![](https://i.imgur.com/7HPFCC4.png)
```python
TUPLE = ()
string = input()
while string != "end":
    TUPLE +=(string,)
    string = input()
print(TUPLE)
print(TUPLE[0:3])
print(TUPLE[-3:])
```
## Python 704 集合條件判斷
設計說明：
請撰寫一程式，輸入數個整數並儲存至集合，以輸入-9999為結束點（集合中不包含-9999），最後顯示該集合的長度（Length）、最大值（Max）、最小值（Min）、總和（Sum）。
![](https://i.imgur.com/Z3gs4it.png)
### 解法(1)
```python
set1 = set()
num = eval(input())
while num!=-9999:
    set1.add(num)
    num = eval(input())
print('Length:',len(set1))
print('Max:',max(set1))
print('Min:',min(set1))
print('Sum:',sum(set1))
```
### 解法(2)
```python
s1=set()
while True : 
  n=int(input())
  if(n==-9999) : break
  s1.add(n)
print('Length:',len(s1))
print('Max:',max(s1))
print('Min:',min(s1))
print('Sum:',sum(s1))
```
## Python 705 子集合與超集合
設計說明：
請撰寫一程式，依序輸入五個、三個、九個整數，並各自儲存到集合set1、set2、set3中。接著回答：set2是否為set1的子集合（subset）？set3是否為set1的超集合（superset）？
![](https://i.imgur.com/IknyNoc.png)
```python
set1 = set()
set2 = set()
set3 = set()

print('Input to set1:')
for i in range(5):
    set1.add(eval(input()))
    
print('Input to set2:')
for i in range(3):
    set2.add(eval(input()))
    
print('Input to set3:')
for i in range(9):
    set3.add(eval(input()))
    
print('set2 is subset of set1:',str(set2.issubset(set1)))
print('set3 is superset of set1:',str(set3.issuperset(set1)))
```
## Python 706 全字母句
設計說明：
全字母句（Pangram）是英文字母表所有的字母都出現至少一次（最好只出現一次）的句子。請撰寫一程式，要求使用者輸入一正整數k（代表有k筆測試資料），每一筆測試資料為一句子，程式判斷該句子是否為Pangram，並印出對應結果True（若是）或False（若不是）。

提示：不區分大小寫字母
![](https://i.imgur.com/G6cKzQm.png)
### 解法(1)
```python
count= eval(input())

alpha=26

for i in range(count):
 sentence = input()
 set1 = set(sentence.lower())
 if ' ' in set1:
     set1.remove(' ')
 if len(set1) >= alpha:
     print('True')
 else:
     print('False')
```
### 解法(2)
```python
n=int(input())
for i in range(n):
    a=[0]*26  #初始化 (有26個英文字母)
    f=True
    temp=input()
    temp=temp.lower()  #轉小寫去統計
    #print(temp)
    for i in range(len(temp)): #字串讀一遍
        if(temp[i]!=' '):   
            a[ord(temp[i])-ord('a')]+=1  # 登記各個字母有幾個 a放在位子[0] b放在位子[1]
    for i in range(len(a)):
        if(a[i]==0) : f=False
    #print(a)
    if(f) :  print('True')
    else : print('False')      
```
## Python 707 共同科目
設計說明：
請撰寫一程式，輸入X組和Y組各自的科目至集合中，以字串"end"作為結束點（集合中不包含字串"end"）。請依序分行顯示(1) X組和Y組的所有科目、(2)X組和Y組的共同科目、(3)Y組有但X組沒有的科目，以及(4) X組和Y組彼此沒有的科目（不包含相同科目）。

提示：科目須參考範例輸出樣本，依字母由小至大進行排序。
![](https://i.imgur.com/aU6nE2w.png)
```python
xS = set()
yS = set()
print('Enter group X\'s subjects:')
x = input()
while x != 'end':
    xS.add(x)
    x=input()  
print('Enter group Y\'s subjects:')
y = input()
while y != 'end':
    yS.add(y)
    y=input() 
print(sorted(xS.union(yS)))
print(sorted(yS.intersection(xS)))
print(sorted(yS.difference(xS)))
print(sorted(yS.symmetric_difference(xS)))
```
## Python 708 詞典合併
設計說明：
請撰寫一程式，自行輸入兩個詞典（以輸入鍵值"end"作為輸入結束點，詞典中將不包含鍵值"end"），將此兩詞典合併，並根據key值字母由小到大排序輸出，如有重複key值，後輸入的key值將覆蓋前一key值。
![](https://i.imgur.com/zji2PJk.png)
### 解法(1)
```python
x={}
y={}
print('Create dict1:')
while True:
    key = input('Key: ')
    if key == 'end':
        break
    x[key] = input('Value: ')
print('Create dict2:')
while True:
    key = input('Key: ')
    if key == 'end':
        break
    y[key] = input('Value: ')
x.update(y)
for i in sorted(x.keys()):
    print(i+": "+x[i])
```
### 解法(2)
```python
dc={}  #其實好像建一個dict就可以了
print('Create dict1:')
while True : 
   k=input('Key: ')
   if k=='end' : break
   dc[k]=input('Value: ')
print('Create dict2:')
while True : 
   k=input('Key: ')
   if k=='end' : break
   dc[k]=input('Value: ')
for i in sorted(dc.keys()):
    print(i+": "+dc[i])
```
## Python 709 詞典排序
設計說明：
請撰寫一程式，輸入一顏色詞典color_dict（以輸入鍵值"end"作為輸入結束點，詞典中將不包含鍵值"end"），再根據key值的字母由小到大排序並輸出。
![](https://i.imgur.com/pbCDGFu.png)
```python
d= {}
while True:
    key = input('Key: ')
    if key == 'end': 
        break
    d[key] = input('Value: ')
for i in sorted(d.keys()):
    print(i+': '+d[i])
```
## Python 710 詞典搜尋
設計說明：
請撰寫一程式，為一詞典輸入資料（以輸入鍵值"end"作為輸入結束點，詞典中將不包含鍵值"end"），再輸入一鍵值並檢視此鍵值是否存在於該詞典中。
![](https://i.imgur.com/1ix4UEA.png)
```python
d = {}
while True:
    key = input('Key: ') 
    if key == 'end':
        break
    d[key] = input('Value: ')
search = input('Search key: ')
print(search in d.keys())
```
# Python 第8類：字串(String)的運作
## Python 801 字串索引
設計說明：
請撰寫一程式，要求使用者輸入一字串，顯示該字串每個字元的索引。
![](https://i.imgur.com/ZimRdua.png)
```python
n=str(input(''))
for i in range(0,len(n)):
    print('Index of \''+n[i]+'\': '+str(i))
```
## Python 802 字元對應
設計說明：
請撰寫一程式，要求使用者輸入一字串，顯示該字串每個字元的對應ASCII碼及其總和。
![](https://i.imgur.com/L7v9A7R.png)
```python
n=str(input(''))
sum=0
for i in range(0,len(n)):
    sum+=ord(n[i])
    print('ASCII code for \''+n[i]+'\' is '+str(ord(n[i])))
print(sum)
```
## Python 803 倒數三個詞
設計說明：
請撰寫一程式，讓使用者輸入一個句子（至少有五個詞，以空白隔開），並輸出該句子倒數三個詞。
![](https://i.imgur.com/5G1SjJ5.png)
```python
my_list =list(map(str, input("").split()))
print(my_list[-3],my_list[-2],my_list[-1])
```
## Python 804 大寫轉換
設計說明：
請撰寫一程式，讓使用者輸入一字串，分別將該字串轉換成全部大寫以及每個字的第一個字母大寫。

![](https://i.imgur.com/TvxWDHC.png)
### 解法(1)
```python
n=input()
print(n.upper())
print(n.title())
```
### 解法(2)
```python
#不用函式的寫法，我就閒 2022/6/16
n=input()
res = ""
for i in n:
    if(i!=' ') : 
      temp=ord(i)-32
      res = res + chr(temp)
    else : 
      res +=' '
print(res)
print(n[0].upper(),end='')
for i in range(1,len(n)):
    if(n[i-1]==' '): 
        temp=ord(n[i])-32
        print(chr(temp),end='')
    elif n[i]==' ' : print(' ',end='')
    else : 
        print(n[i],end='')
```
## Python 805 字串輸出
設計說明：
請撰寫一程式，要求使用者輸入一個長度為6的字串，將此字串分別置於10個欄位的寬度的左邊、中間和右邊，並顯示這三個結果，左右皆以直線 |（Vertical bar）作為邊界。
![](https://i.imgur.com/0waajN7.png)
```python
n=input()
print('|{:<10s}|'.format(n))
print("|%s|"%n.center(10))
print('|{:>10s}|'.format(n))

```
## Python 806 字元次數計算
設計說明：
請撰寫一程式，讓使用者輸入一字串和一字元，並將此字串及字元作為參數傳遞給名為compute()的函式，此函式將回傳該字串中指定字元出現的次數，接著再輸出結果。
![](https://i.imgur.com/buqcExa.png)
### 解法(1)
```python
def compute(Str, s):  print(f'{s} occurs {Str.count(s)} time(s)')
compute(input(),input())
```
### 解法(2)
```python
def compute(Str, s):
    return Str.count(s)
Str = input()
s = input()
print(f'{s} occurs {compute(Str, s)} time(s)')
```
### 解法(3
```python
#不用函式的寫法
def compute(n,m) :
  ans=0 
  for i in range(len(n)):
    if(n[i]==m): ans+=1
  print(f'{m} occurs {ans} time(s)')
compute(input(),input())
```
## Python 807 字串加總
設計說明：
請撰寫一程式，要求使用者輸入一字串，該字串為五個數字，以空白隔開。請將此五個數字加總（Total）並計算平均（Average）。
![](https://i.imgur.com/K4etyUx.png)
```python
m=list(map(int,input().split()))
j=sum=0
for i in m:
      sum+=i
      j+=1
print(f'Total = {sum}')
print(f'Average = {sum/j}')
```
## Python 808 社會安全碼
設計說明：
請撰寫一程式，提示使用者輸入一個社會安全碼SSN，格式為ddd-dd-dddd，d表示數字。若格式完全符合（正確的SSN）則顯示【Valid SSN】，否則顯示【Invalid SSN】
![](https://i.imgur.com/eooxlKY.png)
```python
num=input().replace("-","")
if(num.isdigit()):  print('Valid SSN')  
else:               print('Invalid SSN')
```
## Python 809 密碼規則
設計說明：
請撰寫一程式，要求使用者輸入一個密碼（字串），檢查此密碼是否符合規則。密碼規則如下：
　a. 必須至少八個字元。
　b. 只包含英文字母和數字。
　c. 至少要有一個大寫英文字母。
　d. 若符合上述三項規則，程式將顯示檢查結果為【Valid password】，否則顯示【Invalid password】。
 ![](https://i.imgur.com/qN3UTMg.png)
```python
n = input()
b=0
for i in range(len(n)):
  if n[i].isupper():  b=1
if b==1 and len(n)>=8 and n.isalnum():  print("Valid password")
else:   print("Invalid password")
```
## Python 810 最大值與最小值之差
設計說明：
請撰寫一程式，首先要求使用者輸入正整數k（1 <= k <= 100），代表有k筆測試資料。每一筆測試資料是一串數字，每個數字之間以一空白區隔，請找出此串列數字中最大值和最小值之間的差。

提示：差值輸出到小數點後第二位。
![](https://i.imgur.com/bGDkwHp.png)
```python
for i in range(int(input())):
   data=list(map(float,input().split()))
   print('{:.2f}'.format( max( data ) - min( data )))
```
# Python 第9類：檔案與異常處理
## Python 901 成績資料

設計說明：
請撰寫一程式，將使用者輸入的五筆資料寫入到write.txt（若不存在，則讓程式建立它），每一筆資料為一行，包含學生名字和期末總分，以空白隔開。檔案寫入完成後要關閉。
![](https://i.imgur.com/QYyrXqk.png)
```python
n = open('write.txt','w')
for i in range(5):
    n.write(input()+'\n')
n.close()
```
## Python 902 資料加總

設計說明：
請撰寫一程式，讀取read.txt的內容（內容為數字，以空白分隔）並將這些數字加總後輸出。檔案讀取完成後要關閉。
![](https://i.imgur.com/2GVd4Y0.png)
```python
f=open("read.txt")
w=f.read()
sp=w.split(" ")
total=0
for x in sp:
  total+=eval(x)
print(total)
```
## Python 903 成績資料
設計說明：
請撰寫一程式，要求使用者輸入五個人的名字並加入到data.txt的尾端。之後再顯示此檔案的內容。
![](https://i.imgur.com/PwgHiiQ.png)
```python
with open("data.txt","a+",encoding="utf-8") as file:
    for i in range(5):
        file.write("\n"+input())
    print("Append completed!")
    print("Content of \"data.txt\":")
    file.seek(0)
    print(file.read())

```
## Python 904 資料計算
設計說明：
請撰寫一程式，讀取read.txt（每一列的格式為名字和身高、體重，以空白分隔）並顯示檔案內容、所有人的平均身高、平均體重以及最高者、最重者。

提示：輸出浮點數到小數點後第二位。
![](https://i.imgur.com/IpWAZLx.png)
```python
height=[]
weight=[]

maxh=0 
maxw=0 

f=open("read.txt","r")
w=f.readlines()

for x in w:
  print(x)
  ss=x.split(" ")
  
  height.append(eval(ss[1]))
  weight.append(eval(ss[2]))

  if (eval(ss[1])>maxh):
    maxh=eval(ss[1])
    hname=ss[0]

  if (eval(ss[2])>maxw):
    maxw=eval(ss[2]) 
    wname=ss[0] 
  
avgh=sum(height)/len(height)
avgw=sum(weight)/len(weight)

print("Average height: {:.2f}".format(avgh))
print("Average weight: {:.2f}".format(avgw))
print("The tallest is {} with {:.2f}cm".format(hname,maxh))
print("The heaviest is {} with {:.2f}kg".format(wname,maxw))
```
## Python 905 字串資料刪除
設計說明：
請撰寫一程式，要求使用者輸入檔案名稱data.txt和一字串s，顯示該檔案的內容。接著刪除檔案中的字串s，顯示刪除後的檔案內容並存檔。
![](https://i.imgur.com/FxL51Kl.png)
```python
f=input()
s=input()
with open(f,"r+",encoding="utf-8")as file:
    data=file.read()
    print("=== Before the deletion")
    print(data)
    print("=== After the deletion")
    data=data.replace(s,'')
    print(data)
    file.seek(0)
    file.write(data)
```
## Python 906 字串資料取代
設計說明：
請撰寫一程式，要求使用者輸入檔名data.txt、字串s1和字串s2。程式將檔案中的字串s1以s2取代之。
![](https://i.imgur.com/5M9ytbZ.png)
```python
fn,s1,s2=input(),input(),input()
f=open(fn,'r')
w=f.read()
print("=== Before the replacement")
print(w)
w=w.replace(s1,s2)
print("=== After the replacement")
print(w)
```
## Python 907 詳細資料顯示
設計說明：
請撰寫一程式，要求使用者輸入檔名read.txt，顯示該檔案的行數、單字數（簡單起見，單字以空白隔開即可，忽略其它標點符號）以及字元數（不含空白）。
![](https://i.imgur.com/ACHMcMR.png)
```python
f_name = input()
f_line = f_word = f_char = 0

with open(f_name, 'r') as file:
    for line in file:
        f_line += 1
        f_word += len(line.split())
        f_char += sum([len(c) for c in line.split()])

print('%d line(s)' %f_line)
print('%d word(s)' %f_word)
print('%d character(s)' %f_char)
```
## Python 908 單字次數計算
設計說明：
請撰寫一程式，要求使用者輸入檔名read.txt，以及檔案中某單字出現的次數。輸出符合次數的單字，並依單字的第一個字母大小排序。（單字的判斷以空白隔開即可）
![](https://i.imgur.com/ON7rGu7.png)
```python
fn,num=input(),eval(input())
f=open(fn,'r')
w=f.read()
sp1=w.split()
setsp1=sorted(set(sp1))
for i in setsp1:
  if(sp1.count(i) == num):
    print(i,end='\n')
```
## Python 909 聯絡人資料
設計說明：
請撰寫一程式，將使用者輸入的五個人的資料寫入data.dat檔，每一個人的資料為姓名和電話號碼，以空白分隔。再將檔案加以讀取並顯示檔案內容。
![](https://i.imgur.com/0mOPgmD.png)
```python
with open("data.dat","w",encoding="UTF-8") as fp:
  for i in range(5):
      fp.write(input()+"\n")
 
print('The content of "data.dat":')
with open("data.dat","r",encoding="UTF-8") as fp:
  for i in fp:
      print(i)
```
## Python 910 學生基本資料
設計說明：
請撰寫一程式，要求使用者讀入read.dat（以UTF-8編碼格式讀取），第一列為欄位名稱，第二列之後是個人記錄。請輸出檔案內容並顯示男生人數和女生人數（根據"性別"欄位，0為女性、1為男性）。
![](https://i.imgur.com/igVg9hc.png)
```python
M=0
F=0
f=open('read.dat','r')
w=f.readlines()
for i in w:
  print(i)
  sp=i.split()
  if(sp[2]=="1"):
    M+=1
  elif(sp[2]=="0"):
    F+=1
print("Number of males: {}".format(M))
print("Number of females: {}".format(F))
```
