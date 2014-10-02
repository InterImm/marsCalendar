marsCalendar
============

火星历与地球历的换算


火星历与地球历的换算
-------------------


**地球上某个日期 eD 换算到火星上的日期 mD**，此处 eD 最好包括小时和分钟，若不包括就以 00:00:00 作为默认。计算的是从地球的 UTC 换算到火星的0°经线时间。

1. 找出地球历法中 2010-01-06 对应的 Julian date，记作 eJ0
2. 计算火星上从火星元年（即， 1970-04-28 ）开始直到地球上 2010-01-06 对应的火星太阳日的数目，记作 mS0
3. 计算 eD 与 eJ0 之间的秒，记作 dSec
4. 将 dSec 换算成火星日的数目，mdDay，火星上一个平均太阳日的时间是地球上一天的 1.027491252 倍，所以也可以先把秒换算成地球上的天数 edDay，然后按照这个比例获得火星天数
5. 按照历法以 2010-01-06 为基准计算火星历中对应的日期



修正：

1. 在 2012-07-01 添加了闰年时间 35+32.84 s，因此计算这个日期之后的日期需要修正
2. There is a slight adjustment as the midnights weren't perfectly aligned. Allison, M., and M. McEwen 2000 has &minus;0.00072 but the Mars24 site gives a more up-to-date &minus;0.00096. -- http://jtauber.github.io/mars-clock/
