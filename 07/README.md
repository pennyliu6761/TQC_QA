# Python 第7類：數組（Tuple）、集合（Set）以及詞典（Dictionary）
## Python 701 串列數組轉換
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
全字母句（Pangram）是英文字母表所有的字母都出現至少一次（最好只出現一次）的句子。請撰寫一程式，要求使用者輸入一正整數k（代表有k筆測試資料），每一筆測試資料為一句子，程式判斷該句子是否為Pangram，並印出對應結果True（若是）或False（若不是）。
> [!TIP]
> - 不區分大小寫字母

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
請撰寫一程式，輸入X組和Y組各自的科目至集合中，以字串"end"作為結束點（集合中不包含字串"end"）。請依序分行顯示(1) X組和Y組的所有科目、(2)X組和Y組的共同科目、(3)Y組有但X組沒有的科目，以及(4) X組和Y組彼此沒有的科目（不包含相同科目）。
> [!TIP]
> - 科目須參考範例輸出樣本，依字母由小至大進行排序。

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
---
