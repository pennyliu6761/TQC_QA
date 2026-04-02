# Python 第8類：字串(String)的運作
## Python 801 字串索引
請撰寫一程式，要求使用者輸入一字串，顯示該字串每個字元的索引。

![](https://i.imgur.com/ZimRdua.png)

```python
n=str(input(''))
for i in range(0,len(n)):
    print('Index of \''+n[i]+'\': '+str(i))
```

## Python 802 字元對應
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
請撰寫一程式，讓使用者輸入一個句子（至少有五個詞，以空白隔開），並輸出該句子倒數三個詞。

![](https://i.imgur.com/5G1SjJ5.png)

```python
my_list =list(map(str, input("").split()))
print(my_list[-3],my_list[-2],my_list[-1])
```

## Python 804 大寫轉換
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
請撰寫一程式，要求使用者輸入一個長度為6的字串，將此字串分別置於10個欄位的寬度的左邊、中間和右邊，並顯示這三個結果，左右皆以直線 |（Vertical bar）作為邊界。

![](https://i.imgur.com/0waajN7.png)

```python
n=input()
print('|{:<10s}|'.format(n))
print("|%s|"%n.center(10))
print('|{:>10s}|'.format(n))

```

## Python 806 字元次數計算
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
請撰寫一程式，> - 提示使用者輸入一個社會安全碼SSN，格式為ddd-dd-dddd，d表示數字。若格式完全符合（正確的SSN）則顯示【Valid SSN】，否則顯示【Invalid SSN】

![](https://i.imgur.com/eooxlKY.png)

```python
num=input().replace("-","")
if(num.isdigit()):  print('Valid SSN')  
else:               print('Invalid SSN')
```

## Python 809 密碼規則
請撰寫一程式，要求使用者輸入一個密碼（字串），檢查此密碼是否符合規則。密碼規則如下：
1. 必須至少八個字元。
2. 只包含英文字母和數字。
3. 至少要有一個大寫英文字母。
4. 若符合上述三項規則，程式將顯示檢查結果為【Valid password】，否則顯示【Invalid password】。

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
請撰寫一程式，首先要求使用者輸入正整數k（1 <= k <= 100），代表有k筆測試資料。每一筆測試資料是一串數字，每個數字之間以一空白區隔，請找出此串列數字中最大值和最小值之間的差。
> [!TIP]
> - 差值輸出到小數點後第二位。

![](https://i.imgur.com/bGDkwHp.png)

```python
for i in range(int(input())):
    data=list(map(float,input().split()))
    print('{:.2f}'.format( max( data ) - min( data )))
```
---
