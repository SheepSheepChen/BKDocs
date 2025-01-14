# 软件包简介

解压 `bkce-src-6.2.0.tgz` 安装包后，`src` 即为软件包目录，存放了蓝鲸基础平台、官方 SaaS 包、开源组件等内容，`install` 则为蓝鲸部署脚本。

## 软件包目录结构

请按照目录结构检查对应文件目录是否存在，版本号会随着每次更新而变更，请以官网下载的实际版本号为准：

### 基础套餐

```bash
[root@VM-0-1 src]# pwd
/data/src
[root@VM-0-1 src]# tree -F -L 1
.
|-- bkapi_check-1.1.19.tgz
|-- bk_apigateway_ee-1.11.3.tgz
|-- bkauth_ce-0.0.13.tgz
|-- bkiam_ce-v1.12.6.tgz
|-- bkiam_search_engine-1.1.2.tgz
|-- bklog_ce-4.6.4.tgz
|-- bkmonitorv3_ce-3.8.2.tgz
|-- bknodeman_ee-2.4.1.tgz
|-- bkssm_ce-1.0.12.tgz
|-- blueking.env
|-- cmdb_ce-3.10.28.tgz
|-- COMMON_MD5
|-- COMMON_VERSION
|-- etcd-v3.5.4-linux-amd64.tar.gz
|-- gse_agent_ce-v2.1.2-beta.20.tgz
|-- gse_ce-v2.1.2-beta.20.tgz
|-- gse_plugins/
|-- image/
|-- java11.tgz
|-- java8.tgz
|-- job_ce-3.8.1-beta.5.tgz
|-- MD5
|-- node-v14.17.0-linux-x64.tar.gz
|-- official_saas/
|-- open_paas_ce-2.14.57.tgz
|-- paas_agent_ce-3.2.4.tgz
|-- paas_plugins_ee-2.5.7.tgz
|-- python/
|-- usermgr_ce-2.5.4-beta.8.tar.gz
|-- VERSION
`-- yum/
```

这里重点说明各产品下的 `support-files/` 目录，以权限中心的为例：

- **bkiam**: 存放初始化权限文件。
- **pkgs**： 存放依赖包，比如 Python 工程的 pip 包。
- **sql**： 存放初始化或升级时用到的 sql 文件。
- **templates**： 存放模块的模板文件，安装时会替换里面的 类似 `__VAR_NAME__`： 形式的变量。

## 软件包内容说明

蓝鲸基础平台及 SaaS 详细说明请参考 [产品白皮书](https://bk.tencent.com/docs/)，开源组件版本和配置方式可参考版本日志。

- **bkiam：** 权限中心后台
- **bklog：** 日志平台后台
- **bkmonitorv3：** 监控平台后台
- **bknodeman：** 节点管理后台
- **bkssm：** 凭证管理后台
- **blueking.env：** 证书环境变量
- **cert：** 证书文件目录
- **cmdb：** 配置平台后台
- **COMMON_VERSION：** 开源组件包版本号
- **gse：** 管控平台后台
- **gse_plugins：** 官方采集器插件目录
- **image：** SaaS 基础镜像目录
- **java8.tgz：** JDK 安装包
- **job：** 作业平台后台
- **license：** 鉴权服务
- **MD5：** MD5 校验文件
- **official_saas：** 官方 SaaS 包
- **open_paas：** PaaS 后台
- **paas_agent：** PaaS Agent 后台
- **python：** 蓝鲸定制 Python 解释器目录
- **usermgr：** 用户管理后台
- **VERSION：** 社区版版本号
- **yum：** 开源组件 RPM 包目录
- **bk_apigateway：** 蓝鲸 API 网关
