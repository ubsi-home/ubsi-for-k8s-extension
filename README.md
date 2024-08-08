UBSI-Admin for k8s 治理工具的安装包

安装前的准备：

- k8s 环境
- k8s环境中安装了 ingress 控制器
- 安装 helm 工具包
- 安装 ksbuilder 工具包

下载安装包：

`git clone https://github.com/ubsi-home/ubsi-for-k8s-extension.git`

执行安装命令：

  ```
  helm install ubsipaas ./ubsipaas-1.0.2.tgz \
  --namespace extension-ubsipaas \
  --set base.domain=rewin.ubsi.admin.com \
  --set base.ingressPort=30888 \
  --set mongodb.replicaCount=1 \
  --set mongodb.architecture=standalone \
  --set redis.replicaCount=1 \
  --set redis.architecture=standalone
  ```
卸载命令：
  ```
  helm delete  ubsipaas -n extension-ubsipaas

  ```
注意事项：
   安装程序的命名空间可以改动，但是需要修改应用程序所用的配置文件，具体修改事项请联系我们：`ubsi@rewin.com.cn`



