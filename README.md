# GuessTheNumber-UDP

1A2B-猜數字</br>
創建一個UDP_SERVER玩猜數字遊戲</br>
最多可以三個人同時遊玩</br>
採計時制，可以比賽看誰先解完</br>

## 流程介紹

1.首先用random產生一個答案</br>
2.客戶端傳值(4個數字)</br>
3.Server判斷是否為正確格式</br>
4.判斷輸入的數字 位置且數字也對回傳A 位置錯但數字對回傳B </br>
5.客戶端得到回覆(?A?B)</br>
6.以此類推直到猜中正確答案</br>
7.顯示花費多少時間

## 主要判斷式
```python
for i in range(4):
            if int(data[i]) in sum1:
                if int(data[i]) == sum1[i]:
                    a += 1
                else:
                    b += 1
            else:
                    continue
        if a != 4:
            data = str(a)+"A"+str(b)+"B"
            message = data
            sock.sendto(message.encode('ascii'), address)
	  else:
            message = " You are right!!!!!"
```

## Demo
![image](https://github.com/Xiang511/GuessTheNumber-UDP/assets/120042360/aa53a0f3-691a-454f-a549-71b2ff904ac7)
