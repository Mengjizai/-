国能日新光伏功率预测大赛
------
感谢队友的baseline，我只开源了队友的baseline部分和我的相关特征，线上成绩1284。

 ##比赛链接
http://www.dcjingsai.com/common/cmpt/%E5%9B%BD%E8%83%BD%E6%97%A5%E6%96%B0%E5%85%89%E4%BC%8F%E5%8A%9F%E7%8E%87%E9%A2%84%E6%B5%8B%E5%A4%A7%E8%B5%9B_%E6%8E%92%E8%A1%8C%E6%A6%9C.html

 ##题目思考

1.摘了光伏论文中的一段话：“由于存在不同类型天气状况，使得光伏电池板所接收的辐照强度、湿度、温度有很大变化，会导致光伏输出有较大的差异。”
直接影响光伏板发电功率的三个因素是：**辐照强度、湿度、温度**。这三个量要多加关注。

2.其中测试集中出现了时间、辐照度、风速、风向、温度、压强、湿度、实发辐照度 8个特征，但是训练集中没有实发辐照度。这一点怎么处理，是最前排的关键。开源部分直接拿掉实发辐射度。

3.题目预测的是：实发功率，即每个时刻的发电功率。细粒度的特征对于这道题很有效，能反应该时刻个性化的量更有效。继续按这个思路做，保守还能做3到4个千。

4.特征中很多差值效果比较好。想想原因，因为温度等特征本身就是预测值，预测值作差后会更稳定。

5.特征大力出奇迹，大概确定下方向，暴力提取的特征。

6.特征筛选，特征洪重要性和相关系数

 ##不足

1.异常值没处理

2.实发辐照度没用。

不足之处太多了，欢迎讨论交流。小萌鸡qq：2281894258




