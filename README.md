# 🌦️基于机器学习的天气预测及可视化 WeatherNow


[![Contributors][contributors-shield]][contributors-url][![Forks][forks-shield]][forks-url][![Stargazers][stars-shield]][stars-url][![Issues][issues-shield]][issues-url][![MIT License][license-shield]][license-url][![LinkedIn][linkedin-shield]][linkedin-url]
<!-- 项目 LOGO -->
<br />
<div align="center">
  <a href="https://github.com/admin1025/WeatherNow">
    <img src="images/logo/trans_bg.png" alt="Logo" width="300" height="300">
  </a>

  <h3 align="center"><img src="https://user-images.githubusercontent.com/74038190/213844263-a8897a51-32f4-4b3b-b5c2-e1528b89f6f3.png" width="50px" /> &nbsp;Weather Now   <img src="https://user-images.githubusercontent.com/74038190/213844263-a8897a51-32f4-4b3b-b5c2-e1528b89f6f3.png" width="50px" /> &nbsp;</h3>

  <p align="center">
    基于机器学习的天气预测及可视化模型！
    <br />
    <a href="https://github.com/admin1025/WeatherNow"><strong>浏览文档 »</strong></a>
    <br />
    <br />
    <a href="https://weathernow-android.streamlit.app/">🔗查看 Demo</a>
    ·
    <a href="https://github.com/admin1025/WeatherNow/issues">反馈 Bug</a>
    ·
    <a href="https://github.com/admin1025/WeatherNow/issues">请求新功能</a>
  </p>
</div>


<div align="center">


[:page_with_curl:更新日志](https://github.com/admin1025/WeatherNow/blob/main/docs/%7Flog.md)[:clipboard:项目规范](https://github.com/admin1025/WeatherNow/blob/main/docs/project-guidelines.md)

</div>
<div id="top"></div>

**关于本项目**


![image](https://github.com/admin1025/WeatherNow/main/images/loading.gif)
GitHub 上有很多优秀的关于天气预测的 Repository ，但都是基于本地化和网络爬虫进行的，所以我创建了这个Repository。我们的项目基于机器学习的随机森林模型对天气进行预测，并且通过Streamlit Cloud 部署到服务器端。
<!---->


当然，没有一个Repository可以满足所有人的要求，因为你的需求可能与众不同。所以我们会在未来添加更多内容。你也可以通过复刻（fork）本仓库并且创建一个拉取请求（pull request）或者创建议题（issue）来向我们提出建议。感谢所有帮助我们扩充本仓库的贡献者！


如果你对我的网站感兴趣，欢迎访问我的线上网站[🌦️Weather Now](https://weathernow-android.streamlit.app/) 来开始。

[toc]

## 功能
* **实时天气查询**：获取全球各城市的当前天气。
* **机器学习预测**：使用随机森林算法训练模型并拟合数据
* **天气详细信息**：显示温度、湿度、气压、风速等。
* **简洁易用**：友好的用户界面和交互体验。

## 技术栈
* **前端**：HTML, CSS, JavaScript
* **后端**：Python
* **API**：Streamlit API 
  
<!-- 使用方法 示例 -->
## 项目架构

### 软件结构规范
WeatherNow 项目符合现代 Web 开发的最佳实践，结构简洁清晰、模块化设计良好、易于扩展和维护。通过分离关注点、合理的 API 密钥管理以及清晰的文档，项目不仅具备高可用性和安全性，同时也便于开发者扩展和社区贡献。

本项目大体上采用了分层系统风格架构。
总体分为**表示层**，**应用层**，**服务层**，**数据访问层**。
层与层之前不能直接进行互通，非相邻分层之间不可以进行数据互通，只可以进行迭代访问。
```
表示层： 负责处理用户界面和用户交互。例如，网页或移动应用的前端界面。
应用层： 包含系统的业务逻辑，处理用户请求并执行相关的操作。
服务层： 提供应用层所需的特定服务，如认证或数据转换服务。
数据访问层： 负责与数据库或其他持久性存储进行交互。
```


_转到 [SoftwareArchitecture](docs/SoftwareArchitecture.md) 查看更多介绍_

### 文件规范
我们遵循了 Github 项目：[pythonic-project-guidelines](https://github.com/pyloong/pythonic-project-guidelines)的规范要求，对项目文件结构构成如下：
> WeatherNow/
├── db              
├── src  
├ &emsp;    ├──lib  
├ &emsp;    ├──main\.py  
├── images        
├── test       
├── README\.md    
├── VISUALIZATION\.py

_转到 [project-guidelines](/docs/project-guidelines.md) 查看更多介绍_





## 构建工具

如果你尝试本地部署本项目，请确保你正确安装了以下这些模块，你可以通过pip来安装这些模块。
```python
$ pip install moudelname
```


* [Streamlit](https://nextjs.org/)
* [Requests](https://reactjs.org/)
* [Sklearn](https://vuejs.org/)





<!-- 开始 -->
## 开始

这是一份在本地构建项目的指导的例子。
要获取本地副本并且配置运行，你可以按照下面的示例步骤操作。

### 依赖

本项目完全由Python构建，请你确保正确安装了Python。
为避免Pypi兼容性，你的Python版本应在**3.9及以上**。
你可以通过以下方式查看你的Python版本
* Power Shell
  ```sh
  python --version​
  ```
* Python
  ```sh
  import sys
  #sys模块提供了一系列有关Python运行环境的变量和函数。
  print(sys.version)
  ```

### 安装

_下面是一个指导你如何安装和配置你的应用的例子。这个模板不需要任何外部依赖或服务。_

1. 在 [`Streamlit Could`](https://share.streamlit.io/) 获取一个免费的 API Key。
2. 克隆本仓库
   ```sh
   git clone https://github.com/admin1025/WeatherNow.git
   ```
3. 在 `Streamlit Could` 中填写你的 API
   ```js
   const API_KEY = 'API';
   ```
4. 使用命令行工具启动项目
   ```js
   streamlit run /yourpath/src/main.py
   ```








<!-- 路线图 -->
## 项目更新

- [x] 添加更新日志
- [x] 使用 Radom Frost 进行模型训练
- [x] 使用Streamlit进行数据可视化
- [X] 使用Streamlit Cloud进行服务器部署
- [ ] 进一步优化可视化界面
    - [x] 增加侧边栏控件
    - [x] 增加开屏动画
    - [ ] 增加多种数据展示图样
- [ ] 优化模型超参数


到 [open issues](https://github.com/admin1025/WeatherNow/issues) 页查看所有请求的功能 （以及已知的问题）。



<!-- 贡献 -->
## 贡献

贡献让开源社区成为了一个非常适合学习、启发和创新的地方。你所做出的任何贡献都是**受人尊敬**的。

如果你有好的建议，请复刻（fork）本仓库并且创建一个拉取请求（pull request）。你也可以简单地创建一个议题（issue），并且添加标签「enhancement」。不要忘记给项目点一个 star！再次感谢！

1. 复刻（Fork）本项目
2. 创建你的 Feature 分支 (`git checkout -b feature/AmazingFeature`)
3. 提交你的变更 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到该分支 (`git push origin feature/AmazingFeature`)
5. 创建一个拉取请求（Pull Request）


<!-- 许可证 -->
## 许可证

根据 MIT 许可证分发。打开 [LICENSE.txt](LICENSE.txt) 查看更多内容。

<!-- 联系我们 -->
## 联系我们

<div align=center>

<a herf="https://github.com/admin1025"><img src="https://avatars.githubusercontent.com/u/116926526?s=96&v=4">

@author:R  

<div align=center><img src="https://workspace.google.com/lp/static/images/logo-gmail.png?fingerprint=c2eaf4aae389c3f885e97081bb197b97" alt="tian5784879@gmail.com"  width="15" height="15">tian5784879@gmail.com</div>

项目链接: [https://github.com/admin1025/WeatherNow](https://github.com/admin1025/WeatherNow)
</div>



<!-- 致谢 -->
## 致谢

此项目的可视化模板和对streamlit部署环境处理主要灵感来源于作者`JuneWaySue`
此项目的可视化界面的大部分组件主要来源于[Streamlit Gallery](https://streamlit.io/gallery)，感谢为开源做出贡献的作者。

* [GW Quickview](https://gw-quickview.streamlit.app/)
* [30Day of Streamlit](https://30days.streamlit.app/)
* [JuneWaySue](https://github.com/JuneWaySue)
* [Streamlit中文文档](https://www.streamlit.org.cn/)


<p align="right">(<a href="#top">返回顶部</a>)</p>



<!-- MARKDOWN 链接 & 图片 -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/admin1025/WeatherNow.svg?style=for-the-badge
[contributors-url]: https://github.com/admin1025/WeatherNow/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/admin1025/WeatherNow.svg?style=for-the-badge
[forks-url]: https://github.com/Badmin1025/WeatherNow/network/members
[stars-shield]: https://img.shields.io/github/stars/admin1025/WeatherNow.svg?style=for-the-badge
[stars-url]: https://github.com/admin1025/WeatherNow/stargazers
[issues-shield]: https://img.shields.io/github/issues/admin1025/WeatherNow.svg?style=for-the-badge
[issues-url]: https://github.com/admin1025/WeatherNow/issues
[license-shield]: https://img.shields.io/github/license/admin1025/WeatherNow.svg?style=for-the-badge
[license-url]: https://github.com/admin1025/WeatherNow/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[product-screenshot]: images/screenshot.png
[linkedin-url]: https://linkedin.com/in/othneildrew
