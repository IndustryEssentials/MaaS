<a name="readme-top"></a>

<!-- PROJECT LOGO -->

<div align="center">


  <h3 align="center">欢迎使用 MaaS  预览版👋👋👋</h3>

  <p align="center">
     MaaS 是一款基于云计算技术的AI服务，支持模型管理、模型推理API生成和在线API使用等功能，旨在帮助用户快速部署和使用深度学习模型，提高模型的生产效率和推理性能。
    <br />
    <br />
    <br />
    ·
    <a href="https://github.com/IndustryEssentials/MaaS/issues">反馈</a>
    ·
    <a href="https://github.com/IndustryEssentials/MaaS/issues">讨论</a>
  </p>
</div>



## 主要功能

### 模型管理
模型管理是平台的核心功能，支持上传、部署、更新和删除模型.用户可以通过界面拉取公共算法模型，平台会将模型转换为可用于推理的格式，并自动部署到推理服务中。用户可以随时更新或删除模型。

### API生成
平台支持将训练好的模型部署为RESTful API，支持在线调用和批量调用。平台会自动根据模型生成API接口，并提供文档和SDK供用户使用。

### 在线API使用
平台提供了API文档和在线接口测试工具，方便用户使用API。用户可以通过API文档了解API的功能、输入输出格式、参数、错误码等信息，并使用在线接口测试工具来测试API。请求和响应的日志也会被记录到日志存储中，方便用户查看和分析。

### 弹性扩展
平台支持弹性扩展，可以根据实际负载来自动扩展推理服务的实例数量，保证服务的稳定性和性能。同时也支持自动缩减实例数量，以避免资源浪费。


<!-- GETTING STARTED -->
## 安装部署

### 1 clone 本仓库
请执行以下命令：
```bash
git clone https://github.com/IndustryEssentials/MaaS.git

cd MaaS
```

### 2 配置
打开`.env`文件，根据实际情况修改配置。
- `SERVER_HOST_DNS`: 服务使用的`DNS`，请改成服务器的IP地址或域名。
- `SERVER_HOST_PORT`: 服务使用的端口号，请分配一个未被使用的端口号。
- `MYSQL_ROOT_PASSWORD`: 数据库`root`用户的密码。
- `MYSQL_INITIAL_USER`: 数据库初始用户名。
- `MYSQL_INITIAL_PASSWORD`: 数据库初始用户的密码。

### 3 启动
```bash
docker-compose up -d
```

如果使用的是的docker-compose-plugin请尝试使用：

```bash
docker compose up -d
```

*ps: 系统初始化需要60s左右，请耐心等待。*

### 4 访问
在浏览器输入`URL`进行访问：
```bash
http://192.168.0.100:8220
```
如果修改了`SERVER_HOST_DNS`或`SERVER_HOST_PORT`，此处的`URL`也需要相应地修改。


一切完成，开始工作吧！🍻🍻🍻
<p align="right">(<a href="#readme-top">返回顶部</a>)</p>

