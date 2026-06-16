# Python 第2類：選擇敘述
## Python 201 偶數判斷
請使用選擇敘述撰寫一程式，讓使用者輸入一個正整數，然後判斷它是否為偶數（even）。

![](https://i.imgur.com/I6rcTPP.png)

```python
n=int(input())
if(n%2==0): print(f'{n} is an even number.')
else :  print(f'{n} is not an even number.')
```

## Python 202 倍數判斷
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
請使用選擇敘述撰寫一程式，讓使用者輸入一個西元年份，然後判斷它是否為閏年（leap year）或平年。其判斷規則為：每四年一閏，每百年不閏，但每四百年也一閏。

![](https://i.imgur.com/cT40S1v.png)

```python
n=int(input())
if(n%4==0 and (n%400==0 or n%100!=0)): print(f'{n} is a leap year.')
else : print(f'{n} is not a leap year.')
```

## Python 204 算術運算
請使用選擇敘述撰寫一程式，讓使用者輸入兩個整數a、b，然後再輸入一算術運算子 (+、-、*、/、//、%），輸出經過運算後的結果。

![](https://i.imgur.com/7nQvOeH.png)

```python
a=eval(input())
b=eval(input())
c=input()
if(c=='+'): print(a+b)
elif(c=='-'): print(a-b)
elif(c=='*'): print(a*b)
elif(c=='/'): print(a/b)
elif(c=='//'): print(a//b)
elif(c=='%'): print(a%b)
```

## Python 205 字元判斷
請使用選擇敘述撰寫一程式，讓使用者輸入一個字元，判斷它是包括大、小寫的英文字母（alphabet）、數字（number）、或者其它字元（symbol）。例如：a為英文字母、9為數字、$為其它字元。

![](https://i.imgur.com/zMFwyzJ.png)

```python
n=str(input())
if(n.isdigit()): print(f'{n} is a number.')
elif(n.isalpha()) : print(f'{n} is an alphabet.')
else : print(f'{n} is a symbol.')
```

## Python 206 等級判斷
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
請使用選擇敘述撰寫一程式，要求使用者輸入購物金額，購物金額需大於8,000（含）以上，並顯示折扣優惠後的實付金額。購物金額折扣方案如下表所示：

|金額|折扣|
|---|---|
|8,000（含）以上|9.5折|
|18,000（含）以上|9折|
|28,000（含）以上|8折|
|38,000（含）以上|7折|

<img width="372" height="217" alt="image" src="https://github.com/user-attachments/assets/42c28e5d-3c32-4cb7-bb8f-4c252e567631" />

```python
n=int(input())
if(n>=8000 and n<18000) : print(n*0.95)
elif(n>=18000 and n<28000): print(n*0.9)
elif(n>=28000 and n<38000): print(n*0.8)
elif(n>=38000): print(n*0.7)
```

## Python 208 十進位換算
請使用選擇敘述撰寫一程式，讓使用者輸入一個十進位整數num(0 ≤ num ≤ 15)，將num轉換成十六進位值。
> [!TIP]
> - 轉換規則=十進位0-9的十六進位值為其本身，十進位10-15的十六進位值為A-F。

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
請使用選擇敘述撰寫一程式，讓使用者輸入一個點的平面座標x和y值，判斷此點是否與點(5, 6)的距離小於或等於15，如距離小於或等於15顯示【Inside】，反之顯示【Outside】。
> [!TIP]
> - 計算平面上兩點距離的公式： $\sqrt{(x1-x2)^2 + (y1-y2)^2}\quad$

![](https://i.imgur.com/vupvPIn.png)

```python
x = eval(input())
y = eval(input())
d = ((x-5)**2+(y-6)**2)**0.5
if d <= 15: print('Inside')
else: print('Outside')
```

## Python 210 三角形判斷
請使用選擇敘述撰寫一程式，讓使用者輸入三個邊長，檢查這三個邊長是否可以組成一個三角形。若可以，則輸出該三角形之周長；否則顯示【Invalid】。
> [!TIP]
> - 檢查方法 = 任意兩個邊長之總和大於第三邊長

![](https://i.imgur.com/Xw2VRLp.png)

```python
a=int(input())
b=int(input())
c=int(input())
if(a+b>c and a+c>b and b+c>a): print(a+b+c)
else : print(Invalid)
```
---
