# Python 第6類：串列(List)的運作(一維、二維以及多維)
## Python 601 偶數索引值加總
請撰寫一程式，利用一維串列存放使用者輸入的12個正整數（範圍1~99）。顯示這些數字，接著將串列索引為偶數的數字相加並輸出結果。
> [!TIP]
> - 輸出每一個數字欄寬設定為3，每3個一列，靠右對齊。

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
請撰寫一程式，讓使用者輸入52張牌中的5張，計算並輸出其總和。
> [!TIP]
> - J、Q、K以及A分別代表11、12、13以及1。

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
請撰寫一程式，讓使用者輸入十個整數作為樣本數，輸出眾數（樣本中出現最多次的數字）及其出現的次數。
> [!TIP]
> - 假設樣本中只有一個眾數。

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
請撰寫一程式，讓使用者輸入十個成績，接下來將十個成績中最小和最大值（最小、最大值不重複）以外的成績作加總及平均，並輸出結果。
> [!TIP]
> - 平均值輸出到小數點後第二位。

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
請撰寫一程式，讓使用者輸入兩個正整數rows、cols，分別表示二維串列lst 的「第一個維度大小」與「第二個維度大小」。
串列元素[row][col]所儲存的數字，其規則為：row、col 的交點值 = 第二個維度的索引col – 第一個維度的索引row。
接著以該串列作為參數呼叫函式compute()輸出串列。
> [!TIP]
> - 欄寬為4。

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
請撰寫一程式，讓使用者輸入三位學生各五筆成績，接著再計算並輸出每位學生的總分及平均分數。
> [!TIP]
> - 平均分數輸出到小數點後第二位。

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
請撰寫一程式，讓使用者輸入四週各三天的溫度，接著計算並輸出這四週的平均溫度及最高、最低溫度。
> [!TIP]
> - 平均溫度輸出到小數點後第二位。
> - 最高溫度及最低溫度的輸出，如為31時，則輸出31，如為31.1時，則輸出31.1。

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
---
