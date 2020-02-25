## 解决pip下载慢的问题
1. 修改安装源方法：  
    - 临时使用：可以在使用pip的时候在后面加上-i参数，指定pip源  
    比如：
    - pip install virtualenv -i https://mirrors.aliyun.com/pypi/simple/
    - pip install django==2.2.9 -i https://mirrors.aliyun.com/pypi/simple/   
    
2. 永久使用
    windows：
    在C:\Users\xx\路径下新建一个pip文件夹。在文件夹内新建一个名为pip.ini文件，里面内容为

    ```
    [global]
    index-url = https://mirrors.aliyun.com/pypi/simple
    ```

    linux：
    修改 ~/.pip/pip.conf (没有就创建一个)，修改内容如下：

    ```
    [global]
    index-url = https://mirrors.aliyun.com/pypi/simple
    ```

