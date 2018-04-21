# What is holer
Holer exposes local servers behind NATs and firewalls to the public internet over secure tunnels. <br/>
Support forwarding message based on TCP protocol.<br/><br/>
Holer是一个将局域网服务器代理到公网的内网穿透工具，支持基于TCP协议的报文转发。

# How it works
#### 1. Download software package [*`holer-client.zip`*](https://github.com/Wisdom-Projects/holer/blob/master/Binary);
     下载软件包[`holer-client.zip`](https://github.com/Wisdom-Projects/holer/blob/master/Binary)；

#### 2. Install `Java 1.7` or higher version;
     使用前请先安装`Java 1.7`或者更高版本；

#### 3. Unzip `holer-client.zip`, modify configuration file
     解压`holer-client.zip`，修改配置文件<br/><br/>
     `holer-client/conf/holer.conf`<br/><br/>
     Set the following configurations:<br/>
     设置以下配置：

     `HOLER_ACCESS_KEY=HOLER_CLIENT-2F8D8B78B3C2A0AE`<br/>
     `HOLER_SERVER_HOST=106.14.70.153`<br/>
     `HOLER_SERVER_PORT=6060`<br/>
     
#### 4. Start holer
     启动Holer服务<br/>
     `cd holer-client/bin`<br/><br/>
     **Windows**:<br/>
     Run command `startup.bat` or double click `startup.bat`<br/><br/>
     **Linux**:<br/>
     Run command `sh startup.sh`
     
#### 5. Internet and local address mapping
     公网和内网的地址映射关系

Access Key                    |Internet Address    | Local Address
------------------------------|--------------------|---------------
HOLER_CLIENT-2F8D8B78B3C2A0AE |106.14.70.153:65530 |127.0.0.1:8080
HOLER_CLIENT-3C07CDFD1BF99BF2 |106.14.70.153:65531 |127.0.0.1:8088
HOLER_CLIENT-2A623FCB6E2A7D1D |106.14.70.153:65532 |127.0.0.1:80

#### 6. Demo
     使用示例<br/>
     If your tomcat program local URL: <br/>
     如果您本地的tomcat服务地址：<br/>
     `http://127.0.0.1:8088`<br/><br/>
     
     Exposes to the public internet URL: <br/>
     需要代理到公网上的服务地址为：<br/>
     `http://106.14.70.153:65531`<br/><br/>
     
     Only need modify configuration file to set `HOLER_ACCESS_KEY`: <br/>
     只需要在配置文件里设置`HOLER_ACCESS_KEY`即可：<br/>
     `holer-client/conf/holer.conf`<br/>
     `HOLER_ACCESS_KEY=HOLER_CLIENT-3C07CDFD1BF99BF2`<br/><br/>
     
     **Note:** only need set `HOLER_ACCESS_KEY`, for `HOLER_SERVER_HOST` and `HOLER_SERVER_PORT` please keep in line with step 3. <br/>

     **注意：** 这里只需要修改`HOLER_ACCESS_KEY`即可, `HOLER_SERVER_HOST`和`HOLER_SERVER_PORT`设置跟步骤3保持一致。
     
     
