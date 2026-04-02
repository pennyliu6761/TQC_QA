# Python 第1類：基本程式設計
## Python 101 整數格式化輸出
請撰寫一程式，輸入四個整數，然後將這四個整數以欄寬為5、欄與欄間隔一個空白字元，再以每列印兩個的方式，先列印向右靠齊，再列印向左靠齊，左右皆以直線 |（Vertical bar）作為邊界。

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
請撰寫一程式，輸入四個分別含有小數1到4位的浮點數，然後將這四個浮點數以欄寬為7、欄與欄間隔一個空白字元、每列印兩個的方式，先列印向右靠齊，再列印向左靠齊，左右皆以直線 |（Vertical bar）作為邊界。
> [!TIP]
> - 輸出浮點數到小數點後第二位。

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
請撰寫一程式，輸入四個單字，然後將這四個單字以欄寬為10、欄與欄間隔一個空白字元、每列印兩個的方式，先列印向右靠齊，再列印向左靠齊，左右皆以直線 |（Vertical bar）作為邊界。

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
請撰寫一程式，輸入一圓的半徑，並加以計算此圓之面積和周長，最後請印出此圓的半徑（Radius）、周長（Perimeter）和面積（Area）。
> [!TIP]
> - 需import  math模組，並使用math.pi。
> - 輸出浮點數到小數點後第二位。

![](https://i.imgur.com/nVQFNqI.png)

```python
import math
r=eval(input(""))
print("Radius = %.2f"%r)
print("Perimeter = %.2f"%(r*2*math.pi))
print("Area = %.2f"%(r*r*math.pi))
```

## Python 105 矩形面積計算
請撰寫一程式，輸入兩個正數，代表一矩形之寬和高，計算並輸出此矩形之高（Height）、寬（Width）、周長（Perimeter）及面積（Area）。
> [!TIP]
> - 輸出浮點數到小數點後第二位。

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
假設一賽跑選手在x分y秒的時間跑完z公里，請撰寫一程式，輸入x、y、z數值，最後顯示此選手每小時的平均英哩速度（1英哩等於1.6公里）。
> [!TIP]
> - 輸出浮點數到小數點後第一位。

<img width="877" height="249" alt="image" src="https://github.com/user-attachments/assets/5bd5bde4-285e-4760-bd33-cec70fc5f89e" />

```python
x=float(input())
y=float(input())
z=float(input())
s = (z/1.6)/((60*x+y)/(60*60))
print("Speed = %.1f"%(s))
```

## Python 107 數值計算
請撰寫一程式，讓使用者輸入五個數字，計算並輸出這五個數字之數值、總和及平均數。
> [!TIP]
> - 總和與平均數皆輸出到小數點後第1位。

<img width="883" height="322" alt="image" src="https://github.com/user-attachments/assets/dc34ec19-ed16-4662-b949-748786d20def" />

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
> [!TIP]
> -  $歐式距離 = \sqrt{((x1-x2)^2+(y1-y2)^2)}$
> - 兩座標的歐式距離，輸出到小數點後第4位

<img width="887" height="306" alt="image" src="https://github.com/user-attachments/assets/a4586ebe-0900-45b5-9c26-0b1114c1f4d3" />

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
> [!TIP]
> - 建議使用import math模組的math.pow及math.tan
> - 正五邊形面積的公式： $Area=(5 * s^2)/(4 * tan(pi/5))$
> - 輸出浮點數到小數點後第四位。

<img width="873" height="206" alt="image" src="https://github.com/user-attachments/assets/76388d95-70f5-479b-8fdf-4e2f39564b67" />

```python
import math
s=eval(input())
print('Area = %.4f'%((5*s**2)/(4*math.tan(math.pi/5))))
```

## Python 110 正n邊形面積計算
請撰寫一程式，讓使用者輸入兩個正數n、s，代表正n邊形之邊長為s，計算並輸出此正n邊形之面積（Area）。
> [!TIP]
> - 建議使用import math模組的math.pow及math.tan
> - 正n邊形面積的公式如下： $Area = (n * s^2) / (4 * tan(pi/n))$
> - 輸出浮點數到小數點後第四位

<img width="868" height="228" alt="image" src="https://github.com/user-attachments/assets/b968deb4-c24d-433d-9ab0-c81809fb880b" />

```python
import math
n=eval(input())
s=eval(input())
print('Area = %.4f'%((n*s**2)/(4*math.tan(math.pi/n))))
```
---
