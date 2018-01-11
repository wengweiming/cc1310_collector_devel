## 如何使用

1. 使用 Git 将源码下载到本地，此时在当前目录下会有一个 *cc1310_collector_devel* 文件夹 

   ``` shell
   git clone http://Aifrutech_ninghongye@157.7.129.177:10080/Aifrutech_ninghongye/cc1310_collector_devel.git
   ```

2. 打开 code composer studio ，并打开一个新的 workspace ，将 workspace 目录位置设置为 *cc1310_collector_devel* 文件夹，点击 **Ok** 

   ![](http://oqhmohmaq.bkt.clouddn.com/2018-1-11-01.png)

3. 点击 **View --> Resource Explorer** ，在主界面找到 SimpleLink CC13x0 SDK ，选择 **1.50.00.08** 的 SDK 版本进行下载安装

   ![](http://oqhmohmaq.bkt.clouddn.com/2018-1-11-02.png)

   > 如果你之前已经下载了该版本 SDK ，请将 **Resource Explorer** 的 SDK 存储位置设置为自己的 SDK 目录位置，因为编译的时候会在该位置寻找需要用到的 SDK 文件
   >
   > ![](http://oqhmohmaq.bkt.clouddn.com/2018-1-11-03.png)

4. 点击 **FIle --> Import** 进行工程导入，类型选择 **C/C++ --> CCSProjects** ，工程路径选择工作区间目录

   ![](http://oqhmohmaq.bkt.clouddn.com/2018-1-11-04.png)

5. 工程导入后，查看 **Includes** 目录下文件的路径是否为自己 SDK 的目录，如果正确，则可进行编译

6. 下载之前，需要配置自己板子 XDS 串口号

   * 打开 **targetConfigs** 下的 CC1310F128.ccxml 文件

   * 选择 **Advanced Setup** 中的 Target Configuration

   * 在 **Enter the serial number** 下填写板子的 XDS 串口号

     ![](http://oqhmohmaq.bkt.clouddn.com/2018-1-11-05.png)

     > **如何查看板子的串口号**
     >
     > * **windows**
     >
     >   命令行中输入 `c:\ti\ccsv7\ccs_base\common\uscif\xds110\xdsdfu.exe -e`
     >
     > * **Linux**
     >
     >   使用 `sudo dmesg` 命令查看插入板子后新增的信息

7. 至此可以对工程进行下载

