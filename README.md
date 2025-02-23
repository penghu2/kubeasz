fork 于https://github.com/easzlab/kubeasz, 自立为分支项目，后续独立维护
# ![kubeasz](pics/kubeasz.png)

`kubeasz`致力于提供快速部署高可用`k8s`集群的工具, 同时也努力成为`k8s`实践、使用的参考书；基于二进制方式部署和利用`ansible-playbook`实现自动化；既提供一键安装脚本, 也可以根据[指南](docs/setup/00-planning_and_overall_intro.md)分步执行安装各个组件。

- **集群特性** `TLS`双向认证、`RBAC`授权、多`Master`高可用、支持`Network Policy`、备份恢复
- **集群版本** kubernetes v1.8, v1.9, v1.10, v1.11, v1.12, v1.13, v1.14
- **操作系统** Ubuntu 16.04+, CentOS/RedHat 7
- **运行时** docker 17.03.x-ce, 18.06.x-ce, 18.09.x, [containerd](docs/guide/containerd.md) 1.2.6
- **网络** [calico](docs/setup/network-plugin/calico.md), [cilium](docs/setup/network-plugin/cilium.md), [flannel](docs/setup/network-plugin/flannel.md), [kube-ovn](docs/setup/network-plugin/kube-ovn.md), [kube-router](docs/setup/network-plugin/kube-router.md)

## 快速指南

单机快速体验k8s集群的测试、开发环境--[AllinOne部署](docs/setup/quickStart.md)

- 注：集群用到的所有二进制文件已打包好供下载 [https://pan.baidu.com/s/1c4RFaA](https://pan.baidu.com/s/1c4RFaA)

## 安装指南

<table border="0">
    <tr>
        <td><a href="docs/setup/00-planning_and_overall_intro.md">00-规划集群和安装概览</a></td>
        <td><a href="docs/setup/02-install_etcd.md">02-安装etcd集群</a></td>
        <td><a href="docs/setup/04-install_kube_master.md">04-安装master节点</a></td>
        <td><a href="docs/setup/06-install_network_plugin.md">06-安装集群网络</a></td>
    </tr>
    <tr>
        <td><a href="docs/setup/01-CA_and_prerequisite.md">01-创建证书和安装准备</a></td>
        <td><a href="docs/setup/03-install_docker.md">03-安装docker服务</a></td>
        <td><a href="docs/setup/05-install_kube_node.md">05-安装node节点</a></td>
        <td><a href="docs/setup/07-install_cluster_addon.md">07-安装集群插件</a></td>
    </tr>
</table>

- 命令行工具 [easzctl介绍](docs/setup/easzctl_cmd.md)
- 公有云自建集群 [部署指南](docs/setup/kubeasz_on_public_cloud.md) [阿里云](docs/setup/kubeasz_on_aliyun.md) [腾讯云](docs/setup/kubeasz_on_tencent_cloud.md) [百度云](docs/setup/kubeasz_on_baidu_cloud.md) [AWS](docs/setup/kubeasz_on_aws_cloud.md)
- 容器部署集群 [使用kubeasz容器创建k8s集群（测试）](docs/setup/docker_kubeasz.md)

## 使用指南

<table border="0">
    <tr>
        <td><strong>常用插件</strong><a href="docs/guide/index.md">+</a></td>
        <td><a href="docs/guide/kubedns.md">DNS</a></td>
        <td><a href="docs/guide/dashboard.md">dashboard</a></td>
        <td><a href="docs/guide/metrics-server.md">metrics-server</a></td>
        <td><a href="docs/guide/prometheus.md">prometheus</a></td>
        <td><a href="docs/guide/efk.md">efk</a></td>
        <td><a href="docs/guide/ingress.md">ingress</a></td>
    </tr>
    <tr>
        <td><strong>集群管理</strong><a href="docs/op/op-index.md">+</a></td>
        <td><a href="docs/op/AddNode.md">增加node节点</a></td>
        <td><a href="docs/op/AddMaster.md">增加master节点</a></td>
        <td><a href="docs/op/op-etcd.md">管理etcd集群</a></td>
        <td><a href="docs/op/clean_one_node.md">删除节点</a></td>
        <td><a href="docs/op/upgrade.md">升级集群</a></td>
        <td><a href="docs/op/cluster_restore.md">备份恢复</a></td>
    </tr>
    <tr>
        <td><strong>特性实验</strong></td>
        <td><a href="docs/guide/networkpolicy.md">NetworkPolicy</a></td>
        <td><a href="docs/guide/rollingupdateWithZeroDowntime.md">RollingUpdate</a></td>
        <td><a href="docs/guide/hpa.md">HPA</a></td>
        <td><a href=""></a></td>
        <td><a href=""></a></td>
        <td><a href=""></a></td>
    </tr>
    <tr>
        <td><strong>周边生态</strong></td>
        <td><a href="docs/guide/harbor.md">harbor</a></td>
        <td><a href="docs/guide/helm.md">helm</a></td>
        <td><a href="docs/guide/jenkins.md">jenkins</a></td>
        <td><a href="docs/guide/gitlab/readme.md">gitlab</a></td>
        <td><a href=""></a></td>
        <td><a href=""></a></td>
    </tr>
    <tr>
        <td><strong>应用实践</strong></td>
        <td><a href="docs/practice/java_war_app.md">java应用部署</a></td>
        <td><a href="docs/practice/es_cluster.md">elasticsearch集群</a></td>
        <td><a href="docs/practice/mariadb_cluster.md">mariadb集群</a></td>
        <td><a href=""></a></td>
        <td><a href=""></a></td>
        <td><a href=""></a></td>
    </tr>
</table>

## 沟通交流

- 微信群：k8s&kubeasz实践, 搜索微信号`badtobone`, 请备注（城市-github用户名）, 验证通过会加入群聊。
- 推荐阅读：[feisky-Kubernetes指南](https://github.com/feiskyer/kubernetes-handbook/blob/master/SUMMARY.md) [rootsongjc-Kubernetes指南](https://github.com/rootsongjc/kubernetes-handbook) [opsnull-安装教程](https://github.com/opsnull/follow-me-install-kubernetes-cluster)

## 贡献&致谢

请阅读[项目分支说明](docs/mixes/branch.md), 欢迎提[Issues](https://github.com/easzlab/kubeasz/issues)和[PRs](docs/mixes/HowToContribute.md)参与维护项目！感谢您的关注与支持！

- [如何 PR](docs/mixes/HowToContribute.md)
- [如何捐赠](docs/mixes/donate.md)

Copyright 2017 gjmzj (jmgaozz@163.com) Apache License 2.0, 详情见 [LICENSE](docs/mixes/LICENSE) 文件。
