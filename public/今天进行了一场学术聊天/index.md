# 今天进行了一场学术聊天


今天跟A神聊了几句天，刚好在我办公室，顺便用了一下board. 这样既轻松活泼又严肃认真的聊天，貌似是第一次。

也发现了有很多东西我已经不知道它们的中文是什么了，发现了跟人聊一聊是可以帮助自己理清研究思路的，发现真正懂行的人确实是可以做到深入浅出，而且只有那些能把事情讲明白的才是真的明白。

小趣题一则，A神用这个例子给了我“MATLAB尽量要少用for循环”的温馨提示。

如果你有一个矩阵，如何把这个矩阵的1与n，2与n-1，等等互换。

我说，那就从1到n/2取下限，每次c=a, a=b, b=c做交换，结束。如果n奇数，中间那行正好不用管。

A神说，更简单的方法呢？

求提示。

单位矩阵。

呀，矩阵乘法。怎么乘呢。

左乘，右乘，从右上到左下的1的矩阵。

是啊！左乘这个矩阵，可以上下换行；右乘这个矩阵，可以左右换列。

好神奇的说。

回头再看for循环... 这个计算量，还是算了吧。

简而言之，奥卡姆剃刀原则，小技巧，勤动脑。

$latex a=[1,2,3;4,5,6;7,8,9]; $
$latex b=[0,0,1;0,1,0;1,0,0]$

$latex b*a$

ans =

7     8     9
4     5     6
1     2     3

$latex a*b$

ans =

3     2     1
6     5     4
9     8     7

