# raspberry-AI-Speech-robot


ReSpeaker 2-Mics Pi HAT是专为AI和语音应用设计的Raspberry Pi双麦克风扩展板。 这意味着您可以构建一个集成Amazon Amazona语音服务，Google助手等的功能更强大，更灵活的语音产品。
该板是基于WM8960开发的低功耗立体声编解码器。 电路板两侧有两个麦克风采集声音，还提供3个APA102 RGB LED，1个用户按钮和2个板载Grove接口，用于扩展应用程序。 此外，3.5mm音频插孔或JST 2.0扬声器输出均可用于音频输出。配合树莓派使用可以搭建一个类似Google智能音响、亚马逊Alexa音响的智能音响。
产品特征
Raspberry Pi兼容（Raspberry Pi 2 B、Raspberry Pi 3 B和Raspberry Pi 3 B+）
2个麦克风
2个Grove接口
1个自定义按钮
3.5mm音频接口
JST2.0音频输出接口
创意应用
声音交互应用
AI助手


关于SDK的更新
安装语音识别 Python SDK
语音识别 Python SDK目录结构

├── README.md
├── aip                   //SDK目录
│   ├── __init__.py       //导出类
│   ├── base.py           //aip基类
│   ├── http.py           //http请求
│   └── speech.py //语音识别
└── setup.py              //setuptools安装
支持Python版本：2.7.+ ,3.+

安装使用Python SDK有如下方式：

如果已安装pip，执行pip install baidu-aip即可。
如果已安装setuptools，执行python setup.py install即可。
新建AipSpeech
AipSpeech是语音识别的Python SDK客户端，为使用语音识别的开发人员提供了一系列的交互方法。

参考如下代码新建一个AipSpeech：

from aip import AipSpeech

""" 你的 APPID AK SK """
APP_ID = '你的 App ID'
API_KEY = '你的 Api Key'
SECRET_KEY = '你的 Secret Key'

client = AipSpeech(APP_ID, API_KEY, SECRET_KEY)
在上面代码中，常量APP_ID在百度云控制台中创建，常量API_KEY与SECRET_KEY是在创建完毕应用后，系统分配给用户的，均为字符串，用于标识用户，为访问做签名验证，可在AI服务控制台中的应用列表中查看。

配置AipSpeech
如果用户需要配置AipSpeech的网络请求参数(一般不需要配置)，可以在构造AipSpeech之后调用接口设置参数，目前只支持以下参数：

接口	说明
setConnectionTimeoutInMillis	建立连接的超时时间（单位：毫秒
setSocketTimeoutInMillis	通过打开的连接传输数据的超时时间（单位：毫秒）



如果需要个性化的语音模型，当然也可以自己训练
链接如下：
https://ai.baidu.com/ai-doc/SPEECH/Kk3h1cpoc

一起打造属于自己的智能家居和语音助手吧





