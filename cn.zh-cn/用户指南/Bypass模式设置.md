# Bypass模式设置<a name="waf_01_0069"></a>

该任务指导用户通过Web应用防火墙服务进行Bypass设置，即该域名的请求直接到达其后端服务器，不再经过WAF。

## 前提条件<a name="section1196116321023"></a>

-   已获取管理控制台的账号和密码。
-   防护域名的“工作模式“为“防护模式“或者“暂停防护“。
-   Web应用防火墙之前未使用代理。

## 操作步骤<a name="section344311262515"></a>

1.  登录管理控制台（https://console.huaweicloud.com/）。
2.  单击页面上方的“服务列表“，选择“安全  \>  Web应用防火墙“，在左侧导航树中选择“域名配置“，进入“域名配置“页面，如[图1](#waf_01_0003_zh-cn_topic_0110861354_fig15593418182219)所示。

    **图 1**  域名配置列表<a name="waf_01_0003_zh-cn_topic_0110861354_fig15593418182219"></a>  
    ![](figures/域名配置列表.jpg "域名配置列表")

3.  在目标域名所在行的“操作“列中，单击“切换工作模式“。
4.  在弹出的对话框中，选择“Bypass“，单击“确定“，页面右上角弹出“设置成功“，Bypass模式设置成功。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >当在Web应用防火墙前使用代理时，不能进行“Bypass“操作。  


