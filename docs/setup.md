# 实验环境准备

## Event Engine 登录

## 准备 Cloud9 环境

AWS Cloud9是基于云的集成开发环境（IDE），可让您仅使用浏览器即可编写，运行和调试代码。 它包括代码编辑器，调试器和终端。 Cloud9预先打包了用于流行编程语言的基本工具，并且预先安装了AWS Command Line Interface（CLI），因此您无需为此研讨会安装文件或配置笔记本电脑。 您的Cloud9环境将有权访问与您登录AWS管理控制台的用户相同的AWS资源。

分步说明

1. 转到AWS管理控制台，单击服务，然后在开发人员工具下选择Cloud9。

2. 单击创建环境。

3. 在名称中输入Development并提供描述。

4. 单击下一步。

5. 您可以将环境设置保留为默认值，以启动新的t2.micro EC2实例，该实例在闲置30分钟后将暂停。

6. 单击下一步。

7. 查看环境设置，然后单击“创建环境”。 调配和准备环境需要几分钟。

8. 准备就绪后，您的IDE将打开欢迎屏幕。 在其下，您应该看到类似于以下内容的终端提示：
![setup-cloud9-terminal](images/setup-cloud9-terminal.png)

您可以在此处运行AWS CLI命令，就像在本地计算机上一样。 通过运行来验证您的用户已登录
```
aws sts get-caller-identity
```

您会看到显示指示您的帐户和用户信息的输出：
```
Admin:~/environment $ aws sts get-caller-identity
```

```
{
    "Account": "123456789012",
    "UserId": "AKIAI44QH8DHBEXAMPLE",
    "Arn": "arn:aws:iam::123456789012:user/Alice"
}
```

在整个研讨会中，请始终在选项卡中打开AWS Cloud9 IDE