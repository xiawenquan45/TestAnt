
注意事项：
1、配置local.properties
sdk.dir=G:\\android_develop\\android_sdk  改为你自己的sdk路径,注意用双斜杠转义

2、配置ant.properties

application.package=com.example.testant2   程序包名
ant.project.name=TestAnt2 项目名称
java.encoding=GBK 项目编码

out.absolute.dir=G:/test_ant/temp  临时文件存放位置
gos.path=G:/test_ant/apk   apk文件存放位置

key.store=G:/android_workspace/TestAnt2/test.keystore  秘钥所在位置
key.store.password=123456  秘钥密码
key.alias=test.keystore   秘钥别名
key.alias.password=123456  别名密码

app_version=1.1.0  版本
market_channels=default,baidu,google  渠道名称，要以逗号分隔，必须在一行内

3、以上这些都配置好后，即可巡行ant 打包应用，也可以通过eclipse插件快速运行编译指令，以上过程已运行成功，并且换了不同项目也同样没问题。
最后一个问题就是，这个ant的build.xml文件尚未对引用到library项目作出编译,所以有引用到library项目的不能运行成功，解决办法是将library项目所有资源文件copy到现有项目
中，方能编译成功。

