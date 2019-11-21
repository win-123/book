一、 三角形示例

 三角形的三边接受整数a, b, c 为输入, 用作三角形的三角形的三边,编写测试用例

|     满足 | 不满足 |
| :--- | :--- |
| 1, a &lt; b + c ; b &lt; a +c ; c &lt; a + b | a &lt; 0; b &lt; 0; c &lt; 0,  |
| a=b; a=c; b=c  | 不能同时满足编号1 |
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



