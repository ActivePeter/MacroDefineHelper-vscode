[English](./README.md)

# MacroDefineHelper README

一个可以根据项目中的配置文件生成配置树，然后再通过配置树生成包含宏定义的头文件的 vscode 插件

可以用来方便的配置修改宏定义

<img src="https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613185245774.png" alt="image-20210613185245774" style="zoom:67%;" />

<img src="https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613185555981.png" alt="image-20210613185555981" style="zoom: 67%;" />

<img src="https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613184934920.png" alt="image-20210613184934920" style="zoom:50%;" />

<img src="https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613185038846.png" alt="image-20210613185038846" style="zoom:50%;" />

## 开发

1. ### 打包

   vsce package

2. ### 第一次打开

   npm install

## 安装

从这里下载 [releases](https://github.com/ActivePeter/MacroDefineHelper-vscode/releases/tag/0.0.2).

## 使用

1. ### 生成和打开配置文件

   ![image-20210613192841677](https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613192841677.png)

   ![image-20210613192714030](https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613192714030.png)

   右键侧边栏或输入命令

   选择第一个选项

   ![image-20210613192958303](https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613192958303.png)

   移除注释并且修改值

   ---

   //  "**libConfFilePath**": "填写最终生成头文件的位置",

   //  "**defaultConfFileName**": "填写默认头文件名称",

   //  "**libSrcPath**": "通用库源码路径",

   //  "**describeFileFolderName**": "描述文件的文件夹名",

   //  "**describeFileName**": "描述文件的文件名"

   ---

   比如

   ```json
   {
       "libConfFilePath": "./AutoGenHeader",
       "defaultConfFileName": "AllConfig.h",
       "libSrcPath": "./paLibSubs",
       "describeFileFolderName": "",
       "describeFileName": "describe.txt"
   }
   ```

2. ### 往需要宏定义设置的库中添加描述文件 （上方配置中的describe.txt)

   如下：

   ![image-20210613195312288](C:\Users\sjjmw\AppData\Roaming\Typora\typora-user-images\image-20210613195312288.png)

   我的oled库中需要一个宏定义值

   所以我在oled库中创建了describe.txt

   使用**|**来划分 **宏名称** 和 **宏的默认值

   ----

   如果需要特定的头文件名，可以添加如下语句

   ![image-20210613195854159](C:\Users\sjjmw\AppData\Roaming\Typora\typora-user-images\image-20210613195854159.png)

3. ### 生成配置树

   右键侧边栏 或 输入指令, 选择第二项

   ![image-20210613200017719](C:\Users\sjjmw\AppData\Roaming\Typora\typora-user-images\image-20210613200017719.png)

   我们会获得一个配置树

   ![image-20210613200107695](C:\Users\sjjmw\AppData\Roaming\Typora\typora-user-images\image-20210613200107695.png)

   我们可以轻松的修改宏的值，然后保存

4. ### 根据配置树生成头文件

   右键侧边栏 或输入命令，选择第三项
   
   相应的头文件会生成在目标目录中
   
   ![image-20210613200340874](https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613200340874.png)
   
   

