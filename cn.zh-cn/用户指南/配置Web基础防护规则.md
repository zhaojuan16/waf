# 配置Web基础防护规则<a name="waf_01_0008"></a>

该任务指导用户通过Web应用防火墙服务配置Web基础防护。

Web基础防护开启后，可防范以下常规的web攻击：

-   SQL（Structured Query Language）注入攻击

    是一种常见的Web攻击方法，攻击者通过把SQL命令注入到数据库的查询字符串中，最终达到欺骗服务器执行恶意SQL命令的目的。例如可以从数据库获取敏感信息，或者利用数据库的特性执行添加用户、导出文件等一系列恶意操作，甚至有可能获取数据库乃至系统用户最高权限。

-   XSS跨站脚本攻击

    是一种网站应用程序的安全漏洞攻击，攻击者将恶意代码注入到网页上，用户在浏览网页时恶意代码会被执行，从而达到恶意盗取用户信息的目的。

-   命令注入攻击

    通过命令拼接、绕过黑名单等方式在服务端形成对业务攻击的系统命令，利用各种系统命令调用Web应用接口，从而实现对业务的攻击。

-   代码注入攻击

    利用Web应用在输入校验上的逻辑缺陷，或者部分脚本函数本身存在的代码执行漏洞，而实现的攻击手法。

-   爬虫检测

    防护常见的扫描器Nessus、AWVS、爬虫脚本等攻击。

-   Webshell检测

    Webshell是一种Web入侵的脚本攻击工具，攻击者在入侵一个网站后，将asp、php、jsp或者cgi等脚本文件与正常的网页文件混在一起，然后使用浏览器访问asp或者php后门，得到一个命令执行环境，以达到控制网站服务器的目的。因此也有人称之为网站的后门工具。


## 前提条件<a name="section2256777914731"></a>

-   已获取管理控制台的帐号和密码。
-   已添加防护域名。

## 操作步骤<a name="section61533550183130"></a>

1.  登录管理控制台（https://console.huaweicloud.com/）。
2.  单击页面上方的“服务列表“，选择“安全  \>  Web应用防火墙“，在左侧导航树中选择“域名配置“，进入“域名配置“页面。
3.  在目标域名所在行的“防护策略“栏中，单击策略名称，进入防护配置页面，如[图1](#fig164792010154510)所示。

    **图 1**  防护策略<a name="fig164792010154510"></a>  
    ![](figures/防护策略.jpg "防护策略")

4.  在“Web基础防护“配置框中，用户可根据自己的需要配置Web基础防护的状态，选择“拦截“或者“仅记录“模式，如[图2](#fig193788379)所示，各参数说明如[表1](#table42360431192825)所示。

    **图 2**  Web基础防护配置框<a name="fig193788379"></a>  
    ![](figures/Web基础防护配置框.png "Web基础防护配置框")

    **表 1**  防护动作参数说明

    <a name="table42360431192825"></a>
    <table><thead align="left"><tr id="row66262481192825"><th class="cellrowborder" valign="top" width="36.28%" id="mcps1.2.3.1.1"><p id="p54075445192825"><a name="p54075445192825"></a><a name="p54075445192825"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="63.72%" id="mcps1.2.3.1.2"><p id="p18034950192825"><a name="p18034950192825"></a><a name="p18034950192825"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row8899732153112"><td class="cellrowborder" valign="top" width="36.28%" headers="mcps1.2.3.1.1 "><p id="p189011132173111"><a name="p189011132173111"></a><a name="p189011132173111"></a>状态</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.72%" headers="mcps1.2.3.1.2 "><p id="p11901832163110"><a name="p11901832163110"></a><a name="p11901832163110"></a>Web应用防护攻击的状态。</p>
    <p id="p211311517318"><a name="p211311517318"></a><a name="p211311517318"></a><a name="image119605216318"></a><a name="image119605216318"></a><span><img id="image119605216318" src="figures/开启图标.png" width="48.877500000000005" height="19.950000000000003"></span>：开启状态。</p>
    <p id="p214615715311"><a name="p214615715311"></a><a name="p214615715311"></a><a name="image868051143212"></a><a name="image868051143212"></a><span><img id="image868051143212" src="figures/关闭图标.jpg" width="47.88" height="23.94"></span>：关闭状态。</p>
    <p id="p20490135531515"><a name="p20490135531515"></a><a name="p20490135531515"></a>单击<a name="image2010173342314"></a><a name="image2010173342314"></a><span><img id="image2010173342314" src="figures/关闭图标.jpg"></span>，开启防护检测。</p>
    </td>
    </tr>
    <tr id="row28096830192825"><td class="cellrowborder" valign="top" width="36.28%" headers="mcps1.2.3.1.1 "><p id="p10384205820363"><a name="p10384205820363"></a><a name="p10384205820363"></a>模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.72%" headers="mcps1.2.3.1.2 "><a name="ul946621183715"></a><a name="ul946621183715"></a><ul id="ul946621183715"><li>拦截：发现攻击行为后立即阻断并记录。</li><li>仅记录：发现攻击行为后只记录不阻断攻击。</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

5.  在“Web基础防护“配置框中，单击“高级设置“，进入“Web基础防护“界面，根据您的业务场景，开启合适的防护功能，如[图3](#fig17347539113910)所示。

    用户可根据业务需要，在不需要防护的类型所在行操作栏中，单击![](figures/开启图标.png)关闭检测，关闭检测后，页面右上角弹出“关闭成功”，![](figures/开启图标.png)变更为![](figures/关闭图标.jpg)则说明检测项关闭成功。

    **图 3**  Web基础防护<a name="fig17347539113910"></a>  
    ![](figures/Web基础防护.png "Web基础防护")

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >在页面右上角，选择防护等级，Web基础防护设置了三种防护等级：“宽松“、“中等“、“严格“。  
    >-   默认情况下，选择“中等“。  
    >-   当您发现“中等“防护规则下存在较多的误拦截，或者业务存在较多不可控的用户输入，建议您选择“宽松“。  
    >-   当您需要更严格的防护等级时，建议选择“严格“。  


