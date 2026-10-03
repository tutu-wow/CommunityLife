# CommunityLife
社区生活服务小程序  亮点：WebSocket聊天结合语音交互、Echarts数据可视化分析、社区服务集中办理、便民服务形成业务闭环、可配置的居民信用体系、居民与访客通行管理；  角色：用户、商户、管理员；

所有源码均本人开发，项目是前后端分离的，所有的项目都具备了完整的业务逻辑，不仅仅局限于基础的增删改查（CRUD）操作，系统亮点众多。

本文注重于计算机毕业设计选题指导，列出题目均有源码， 大家可以去【公众号】(毕业终点站)获取或者加我【qq】(2112698948)提意见(别忘记Star哟)。备注：git

声明：仅用于学习使用，请勿用于任何商业行为！

1.系统非商用，非开源，非无偿。

2.由本人开发，如需源码，请联系以下方式，qq:2112698948。

3.项目有很多，并未全部上传，如果未找到想要的，可直接咨询。


# DX6006 社区生活服务小程序

> 面向社区居民、商户与社区管理员三类角色的社区生活服务平台，整合报修、账单缴费、公告查看、访客通行与便民服务预约等社区事务到统一入口，减少居民线下办理与多平台切换的成本。系统基于 uni-app 微信小程序端 + Vue 3 管理后台的前后端分离架构，以 WebSocket 实时聊天结合语音交互支撑邻里沟通，借助 ECharts 完成报修、预约、帖子与商户运营的统计分析，并通过可配置的居民信用体系、居民与访客通行管理，构建起覆盖「服务浏览—在线预约—商户接单—服务完成—评价反馈」的完整链路。

## 一、技术架构

| 类别 | 技术 |
| :--- | :--- |
| 架构 | MVC、前后端分离、微信小程序端+管理后台、管理员/商户/居民多角色管理 |
| 系统环境 | Windows |
| 开发环境 | IDEA、JDK17、Maven、MySQL、Node.js、HBuilderX、微信开发者工具 |
| 后端技术 | Java、Spring Boot 3.3.1、Spring MVC、MyBatis-Plus、MySQL、JWT、WebSocket、微信小程序授权登录 |
| 后台技术 | Vue 3、Vite、Element Plus、Vue Router、Pinia、Axios、ECharts |
| 小程序技术 | uni-app、Vue 3、Pinia、微信小程序 API、uni-ui 组件 |

## 二、系统亮点

1. **WebSocket聊天结合语音交互**：基于 WebSocket 实现实时消息推送，同时提供语音转文字、文字转语音能力，丰富社区沟通方式。
2. **Echarts数据可视化分析**：提供报修、预约、社区帖子等统计分析及商户运营看板，帮助管理人员了解业务量与服务运行情况。
3. **社区服务集中办理**：将报修、账单缴费、公告查看、访客通行和便民服务预约整合到统一入口，减少居民线下办理和多平台切换的成本。
4. **便民服务形成完整业务链路**：支持服务浏览、在线预约、商户接单、服务完成、居民评价与商户回复，让服务过程可跟踪、服务质量可反馈。
5. **可配置的居民信用体系**：设置独立的信用规则、信用等级和信用变动记录模块，支持信用信息查询与管理，为社区信用管理提供基础。
6. **居民与访客通行管理**：将居民门禁通行、访客申请、通行证管理和通行记录纳入平台，便于统一管理与记录查询。

## 三、功能模块与截图

> 截图存放于仓库 `images/` 目录，不依赖外部图床。

### 3.0 平台总览

<p align="center"><img src="images/01-system-overview.png" width="78%"></p>

**图 1 · 平台总览**：小程序整体界面概览，涵盖居民端、商户端与管理端入口。


### 3.1 用户端

<p align="center"><img src="images/02-home.png" width="78%"></p>

**图 2 · 首页**：社区居民首页，整合报修、缴费、公告与便民服务入口。

<p align="center"><img src="images/03-repair.png" width="78%"></p>

**图 3 · 报事报修**：居民报修工单提交与进度跟踪。

<p align="center"><img src="images/04-payment.png" width="78%"></p>

**图 4 · 费用缴纳**：物业费、水电等账单查询与在线缴费。

<p align="center"><img src="images/05-guide-safety.png" width="78%"></p>

**图 5 · 办事指南/社区安全**：办事指南与社区安全信息浏览。

<p align="center"><img src="images/06-merchants.png" width="78%"></p>

**图 6 · 周边商户**：周边便民商户浏览与服务预约。

<p align="center"><img src="images/07-square.png" width="78%"></p>

**图 7 · 邻里广场**：社区邻里互动帖子广场。

<p align="center"><img src="images/08-chat.png" width="78%"></p>

**图 8 · 聊天**：WebSocket 实时聊天，支持语音转文字与文字转语音。

<p align="center"><img src="images/09-profile.png" width="78%"></p>

**图 9 · 个人中心**：居民个人信息、信用与账户管理。


### 3.2 商户端

<p align="center"><img src="images/10-merchant-analysis.png" width="78%"></p>

**图 10 · 数据分析**：商户运营数据看板与分析。

<p align="center"><img src="images/11-services.png" width="78%"></p>

**图 11 · 服务项目**：商户便民服务项目维护。

<p align="center"><img src="images/12-merchant-reviews.png" width="78%"></p>

**图 12 · 服务评价**：商户收到的服务评价与回复。

<p align="center"><img src="images/13-merchant-orders.png" width="78%"></p>

**图 13 · 预约订单**：商户便民服务预约订单处理。


### 3.3 管理员端

<p align="center"><img src="images/14-houses.png" width="78%"></p>

**图 14 · 房屋信息**：社区房屋基础信息管理。

<p align="center"><img src="images/15-notices.png" width="78%"></p>

**图 15 · 社区公告**：平台公告发布与维护。

<p align="center"><img src="images/16-posts.png" width="78%"></p>

**图 16 · 社区帖子**：社区帖子审核与管理。

<p align="center"><img src="images/17-passes.png" width="78%"></p>

**图 17 · 访客通行证**：居民门禁通行、访客申请与通行证管理。

<p align="center"><img src="images/18-admin-merchants.png" width="78%"></p>

**图 18 · 社区商户**：入驻商户审核与管理。

<p align="center"><img src="images/19-admin-reviews.png" width="78%"></p>

**图 19 · 服务评价**：全平台服务评价监管。

<p align="center"><img src="images/20-admin-orders.png" width="78%"></p>

**图 20 · 预约订单**：全平台预约订单监管。

<p align="center"><img src="images/21-work-orders.png" width="78%"></p>

**图 21 · 保修工单**：报修工单统一分派与管理。

<p align="center"><img src="images/22-bills.png" width="78%"></p>

**图 22 · 费用账单**：社区费用账单统一管理。


## 说明

- 本文档中的界面截图均来自项目演示环境，仅用于功能展示与学习参考。
- 本项目仅用于学习交流，非开源、非无偿。
- 文档展示 22 张截图，需要了解更多，请联系我。
