# record
+ reading record
+ 根据月份建立目录
+ 记录一些Tips


## notes
### 激活函数的作用 
+ 是为了增加神经网络模型的非线性。否则你想想，没有激活函数的每层都相当于矩阵相乘。就算你叠加了若干层之后，无非还是个矩阵相乘罢了。所以你没有非线性结构的话，根本就算不上什么神经网络。

### [深度学习的本质](https://datawhalechina.github.io/leeml-notes/#/chapter13/chapter13?id=本质：通过隐藏层进行特征转换)
+ 通过隐藏层进行特征转换   
把隐藏层通过特征提取来替代原来的特征工程，这样在最后一个隐藏层输出的就是一组新的特征（相当于黑箱操作）而对于输出层，其实是把前面的隐藏层的输出当做输入（经过特征提取得到的一组最好的特征）然后通过一个多分类器（可以是softmax函数）得到最后的输出y。
