云原生架构是当前构建现代化应用系统的主流方法，它强调在云环境中构建和运行应用，具有以下基本特质：组件化、可观察、可独立部署/测试、可动态升级/替换、可配置管理等。云原生是一套技术体系和方法论，主要构成包括微服务、DevOps、持续交付和容器化。

UBSI（Unified Basic Service Infrastructure）是一个轻量级的微服务架构平台，旨在提供快速、简单且易于使用的微服务开发和治理解决方案。与 SpringCloud 相比，UBSI同样构建了一套完备的微服务开发/治理体系，旨在简化微服务的开发流程，提高开发效率和系统的可维护性。

## 快速开始

1. ### **域名访问配置**：

   - 需要保证您的域名服务器/本机 hosts 能解析 rewin.ubsi.admin.com。

2. ### **安装扩展组件**：

   - 安装后，在 KubeSphere 平台的左上角点击`ubsi-admin`按钮进入 UBSI-admin 控制台。
   - 初次进入可能需要几分钟加载组件。

3. ### **初始账户设置**：

   - 超级管理员账户：`admin`
   - 初始密码：`abcde321`

4. ### **开发文档**：

   - 在开始UBSI的探索之旅之前，不妨先花些时间深入阅读其官方开发文档，这将为您后续的开发工作打下坚实的基础。文档可通过以下链接获取：[UBSI开发文档](https://ubsi-home.github.io/docs/index.html)。

## 高级配置

1. ### **扩展组件配置调整**：

   - 在“扩展组件配置”界面，针对`redis`和`mongodb`组，根据生产需求调整`architecture`和`replicaCount`字段。
     - `architecture` 默认为`standalone`（单节点），适合开发环境。
     - `replicaCount` 默认为1，可根据企业级需求调整副本数量。

2. ### **存储组件配置**：

   - 在UBSI中需要有相应的存储（MongoDB, Redis, Nexus等）。
   - 在安装前需配置 Kubernetes 的 StorageClass ，确保支持 PVC（Persistent Volume Claim）的自动创建，实现数据持久化。

3. ### **安装后操作**：

   - 所有Pod安装完毕后，重启 `ubsi-admin-container` 和 `ubsi-webapi` 容器，确保最新配置生效。
   - 随后即可开始开发工作。

## 获取 License

1. ### **版本说明**：

   - UBSI-admin分为企业版和开发版。
   - 开发版无需 license，可在开发/测试环境中免费使用。
   - 生产环境中部署需申请 license，将开发版升级为企业版。

2. ### **获取 License 步骤**：

   - 点击“订阅”，选择对应版本，购买扩展组件。
   - 购买成功后，发送部署的 redis 和 mongodb svc的IP地址到邮箱：`ubsi@rewin.com.cn`。
   - 收到 license 文件后，将内容修改到名称为`ubsi-admin-license`的配置字典里。
   - 修改完 `ubsi-admin-license` 的配置字典，需要重启`ubsi-admin-container`容器，确保最新配置生效。

## 商务咨询

更多信息请访问公司网站：[UBSI微服务架构平台主页](https://ubsi-home.github.io/)，或通过邮件进行商务咨询：`ubsi@rewin.com.cn`。

希望这份安装指南能帮助您顺利部署 UBSI平台。如果有任何问题，请随时联系我们获取支持。
