一、 三角形示例

三角形的三边接受整数a, b, c 为输入, 用作三角形的三角形的三边,编写测试用例

| 满足 | 不满足 |
| :--- | :--- |
| 1, a &lt; b + c ; b &lt; a +c ; c &lt; a + b | a &lt; 0; b &lt; 0; c &lt; 0, |
| a=b; a=c; b=c | 不能同时满足编号1 |
| a=b=c |  |
| a\*a + b\*b = c\*c; a\*a+c\*c=b\*b; b\*b+c\*c=a\*a |  |

```
def triangle(a,b,c):

    if (a + b > c) and (a + c > b) and (b + c > a):  # 判断是否是三角形
        if a == b == c:
            print("等边三角形")  # 等边三角形
        elif (a == b or a == c or b == c):
            print("等腰三角形")  # 等腰三角形
        elif (a * a + b * b == c * c) or (a * a + b * b == c * c) or (a * a + b * b == c * c):
            print("直角三角形")  # 直角三角形
        else:
            print("不规则")  # 不规则三角形
    else:
        print("不能构成三角形")


triangle(3, 5, 5)
```

二、 当前给出日期的下一天的日期

| 满足 | 不满足 |
| :--- | :--- |
| 年:          1970 &lt;= year &lt;= 2090 | 程序的时间开始1970 |
| 月            1&lt;=month&lt;= 12 | 0, 13, |
| 日            1&lt;= day &lt;= 31 | 0, 32 |

```
year = int(input(‘year:’))
month = int(input(‘month:’))
day = int(input(‘day:’))

day_list = [0,31,59,90,120,151,182,213,243,273,304,334]

num_day = 0

if 0<month<12:
num_day = day_list[month-1]
else:
print(“error”)

num_day += day

if (year % 400 == 0) or ((year % 4 == 0) and (year % 100 != 0)):
if month > 2 :
num_day += 1

print(num_day)

```

三、银行ATM





