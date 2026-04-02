# Python 第9類：檔案與異常處理
## Python 901 成績資料
請撰寫一程式，將使用者輸入的五筆資料寫入到write.txt（若不存在，則讓程式建立它），每一筆資料為一行，包含學生名字和期末總分，以空白隔開。檔案寫入完成後要關閉。

![](https://i.imgur.com/QYyrXqk.png)

```python
n = open('write.txt','w')
for i in range(5):
    n.write(input()+'\n')
n.close()
```

## Python 902 資料加總
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
請撰寫一程式，讀取read.txt（每一列的格式為名字和身高、體重，以空白分隔）並顯示檔案內容、所有人的平均身高、平均體重以及最高者、最重者。
> [!TIP]
> - 輸出浮點數到小數點後第二位。

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
---
