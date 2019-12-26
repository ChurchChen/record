## NGC Note

* 1）如何申请NGC账号并介绍上面的各种资源；

* **2） 从本机联上NGC，演示pull, install, start镜像，挂载磁盘，数据读写等基本使用操作；** 

* 3）进入容器，介绍pycharm 的使用，编译运行一个python小程序或进入keras 环境跑一段小代码

  ---

  [Github: Nvidia Docker ](https://github.com/NVIDIA/nvidia-docker)

> 确保docker/nvidia-docker已经安装成功
>
> 验证nvidia-docker安装成功
>
> ```shell
> nvidia-docker run hello-world
> ```
>
> ![1571985817153](https://github.com/ChurchChen/record/blob/master/images/1571985817153.png)
---





NGC支持的显卡[架构]( https://docs.nvidia.com/ngc/ngc-titan-setup-guide/index.html )，本机的Titan V是Volta架构

+ Pascal
+ Volta
+ Turing

---

## 使用NGC

如果是第一次使用NGC，需要[注册账号]( https://ngc.nvidia.com/signup ) 

![1571986579397](https://github.com/ChurchChen/record/blob/master/images/1571986579397.png)

登录之后进入[SETUP界面]( https://ngc.nvidia.com/setup )，点击Get API Key

![1571986906055](https://github.com/ChurchChen/record/blob/master/images/1571986906055.png)

![1571986949478](https://github.com/ChurchChen/record/blob/master/images/1571986949478.png)

![1571987066300](https://github.com/ChurchChen/record/blob/master/images/1571987066300.png)

 生成 API Key 成功后，回到 GPU 云服务器命令行，运行如下命令进行登录： 

```shell
docker login nvcr.io
Username: $oauthtoken
Password: <Your Key> 
```

 其中用户名固定为 **$oauthtoken**，密码即前面生成的 **API Key**。 

**登录成功**

![1571987308898](https://github.com/ChurchChen/record/blob/master/images/1571987308898.png)

---

下面获取官方Docker Image, 回到[容器镜像]( https://ngc.nvidia.com/catalog/containers )页面：NGC 提供的深度学习环境镜像 

![1571987535894](https://github.com/ChurchChen/record/tree/master/images/1571987535894.png)

选择需要拉取的镜像，进入对应的页面，以[PyTorch]( https://ngc.nvidia.com/catalog/containers/nvidia:pytorch )为例
![1571987788457](https://github.com/ChurchChen/record/tree/master/images/1571987788457.png)

 运行如下命令 pull 该 image（整个image pull下来需要很长的时间）：

```shell
docker pull nvcr.io/nvidia/pytorch:19.09-py3
```

点击[这里]( https://docs.nvidia.com/deeplearning/frameworks/pytorch-release-notes/rel_19-09.html#rel_19-09 )可以看到对应镜像版本中包含的全部软件

![1572152887759](https://github.com/ChurchChen/record/tree/master/images/1572152887759.png)

拉取镜像完成之后，运行如下命令查看docker中的镜文件

```shell
docker images
```

![1572152437814]( https://github.com/ChurchChen/record/tree/master/images/1572152437814.png)



---



## 启动 NGC 容器

运行一下命令启动NGC容器

```shell
nvidia-docker run -ti -v /mnt:/mnt 9d6 /bin/bash
```

 其中 9d6 为上一步 pull 下来 image 的 ID 前 3 个字母，缩写是为了输入方便

也可以使用镜像名：版本号（nvcr.io/nvidia/pytorch :19.09-py3）。

-v /mnt:  /mnt 表示将本地 /mnt 目录映射到 Docker 容器 /mnt 位置，方便 Docker 与主机之间互拷文件。 

启动界面如下

![1572152964058](https://github.com/ChurchChen/record/tree/master/images/1572152964058.png)

 检查容器中 GPU 驱动是否正常： 

```shell
nvidia-smi
```

![1572153025760](https://github.com/ChurchChen/record/tree/master/images/1572153025760.png)
