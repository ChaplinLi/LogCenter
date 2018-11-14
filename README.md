# LogCenter
Android 悬浮日志输出库

## 开发环境：
Android Studio

## 创建Library项目：

    1.新建项目NewProject

    2.新建库NewModule->Android Library(minSDK建议选择android-19)

    3.将代码及资源分别拷贝到java和res下

    4.生成aar文件，Gradle->(Your Library)->Tasks->build->assembleDebug,(Your Library)->build->outputs->aar下生成对应的aar文件

    5.使用7-zip（或者改成zip文件）解压，抽取res文件夹修改为Eclipse导入项目名（例如：P），修改classes.jar文件名为你要改的库名字，拷贝到P目录的libs下面，AndroidManifest.xml文件拷贝到P目录下

    6.在P目录下创建project.properties文件，添加如下内容：
    target=android-19
    android.library=true
    
    7.在Eclipse中引入P项目，在目标项目中添加P项目作为Library

    8.接入以下接口


## 接口说明：

1.LogCenter.init(Context);

    --初始化悬浮窗口，创建log文件

2.LogCenter.onResume();

    --当应用由后台重新回到最上层界面时，显示悬浮窗口

3.LogCenter.onStop();

    --当应用退出到后台是隐藏悬浮窗口

4.LogCenter.onDestory();

    --当应用注销时关闭Log服务
