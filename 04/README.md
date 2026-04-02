# Python 第4類：進階控制流程
## Python 401 最小值
請撰寫一程式，由使用者輸入十個數字，然後找出其最小值，最後輸出最小值。

![](https://i.imgur.com/5DgKZKm.png)

```python
num = []
for i in range(10):
    num.append(eval(input()))
print(min(num))
```

## Python 402 不定數迴圈-最小值
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
請撰寫一程式，讓使用者輸入一個正整數，將此正整數以反轉的順序輸出，並判斷如輸入0，則輸出為0。

![](https://i.imgur.com/6jIG6q3.png)

```python
n=str(input())
s=''.join(reversed(n))
print(s)
```

## Python 405 不定數迴圈-分數等級
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
請撰寫一程式，以不定數迴圈的方式輸入身高與體重，計算出BMI之後再根據以下對照表，印出BMI及相對應的BMI代表意義（State）。假設此不定數迴圈輸入-9999則會結束此迴圈。標準如下表所示：

|BMI值|	代表意義|
|---|---|
|BMI < 18.5|	under weight|
|18.5 <= BMI < 25|	normal|
|25.0 <= BMI < 30|	over weight|
|30 <= BMI|	fat|

> [!TIP]
> -  $BMI = 體重(kg)/身高^2(m)$，輸出浮點數到小數點後第二位。 不需考慮男性或女性標準。

![](https://i.imgur.com/2cgAcvW.png)

```python
while True:
    H = float(input())
    if H == -9999:
        break
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
1. 請撰寫一程式，以不定數迴圈的方式讓使用者輸入西元年份，然後判斷它是否為閏年（leap year）或平年。其判斷規則如下：每四年一閏，每百年不閏，但每四百年也一閏。
2. 假設此不定數迴圈輸入-9999則會結束此迴圈。

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
請撰寫一程式，讓使用者輸入十個整數，計算並輸出偶數和奇數的個數。

![](https://i.imgur.com/qWhBFjV.png)

```python
even = odd = 0
for i in range(10):
    if int(input()) % 2 == 0: even += 1
    else: odd += 1
print(f'Even numbers: {even}')
print(f'Odd numbers: {odd}')
```

## Python 409 得票數計算
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
請撰寫一程式，依照使用者輸入的n，畫出對應的等腰三角形。

![](https://i.imgur.com/MbIQeI6.png)

```python
n = int(input())
for i in range(n, 0, -1):
    print(' '*(i-1) + '*'*(1+2*(n-i)))
```
---
