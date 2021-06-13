[中文](./README_CN.md)

# MacroDefineHelper README

A vscode extension to generate a config tree from the describe files in project.

Then you can edit the describe tree and generate head files from the tree

<img src="https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613185245774.png" alt="image-20210613185245774" style="zoom:67%;" />

<img src="https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613185555981.png" alt="image-20210613185555981" style="zoom: 67%;" />

<img src="https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613184934920.png" alt="image-20210613184934920" style="zoom:50%;" />

<img src="https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613185038846.png" alt="image-20210613185038846" style="zoom:50%;" />

## developement

1. ### pack

   vsce package

2. ### first open

   npm install

## install

You can download it from [releases](https://github.com/ActivePeter/MacroDefineHelper-vscode/releases/tag/0.0.2).

## use

1. ### generate and open config file

   ![image-20210613192841677](https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613192841677.png)

   ![image-20210613192714030](https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613192714030.png)

   right click side bar or input command

   choose the first selection

   ![image-20210613192958303](https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613192958303.png)

   remove the ’//‘ and set the values

   ---

   **"libConfFilePath"**  the path of generated headers

   **"defaultConfFileName"**  default head file name

   ***"libSrcPath"***   the directory path need to look for describe file 

   ***"describeFileFolderName"***  the name of the folder which contains the describe file

   ***"describeFileName"***   the name of describe file

   ---

   for example

   ```json
   {
       "libConfFilePath": "./AutoGenHeader",
       "defaultConfFileName": "AllConfig.h",
       "libSrcPath": "./paLibSubs",
       "describeFileFolderName": "",
       "describeFileName": "describe.txt"
   }
   ```

2. ### add describe file（describe.txt in the example above） in libs need define setting 

   for example：

   ![image-20210613200523702](https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613200523702.png)

   there is a define value needed in my oled lib

   then I created a **describe.txt** in oled lib's directory

   use a `|` to divide the define value and default value

   ----

   if it needs a special head file we can add a line like following:

   ![image-20210613195854159](https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613195854159.png)

3. ### generate config json tree

   right click or input command, choose the second option

   ![image-20210613200017719](https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613200017719.png)

   we will get a json tree file

   ![image-20210613200107695](https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613200107695.png)

   we can easily change the tree node value and save the file

4. ### generate head files from tree

   right click or input command, choose the third option

   the head file will be generated in the target directory

   ![image-20210613200340874](https://hanbaoaaa.xyz/tuchuang/images/2021/06/13/image-20210613200340874.png)