UBSI-Admin for k8s 治理工具的安装包

安装前的准备：

- k8s 环境
- k8s环境中安装了 ingress 控制器
- 安装 helm 工具包
- 安装 ksbuilder 工具包

下载安装包：

`git clone https://github.com/ubsi-home/ubsi-for-k8s-extension`

执行安装命令：

  ```
  cd ubsi-admin-all
  ksbuilder package .
  ksbuilder publish ubsipaas-1.0.2.tgz
  在 kubesphere 扩展市场中找到推送的安装包，点击安装
  注意在安装之前仔细阅读安装界面的readme.md
  ```

