+++
date = "2016-01-27T16:14:21+08:00"
title = "Elastic-Job-Lite运维平台"
weight=22
+++

# Elastic-Job-Lite运维平台

以`war`包形式提供，可自行部署至`tomcat`或`jetty`等支持`servlet`的`web`容器中。可通过`mvn install`编译或`maven`中央仓库获取。

## 登录

默认用户名和密码是`root/root`，可通过`conf\auth.properties`修改默认登录账户。

## 功能列表

* 登录安全控制

* 注册中心管理

* 作业维度状态查看

* 服务器维度状态查看

* 快捷修改作业设置

* 控制作业暂停，恢复运行，停止和删除

## 设计理念

运维平台和`elastic-job-lite`并无直接关系，是通过读取作业注册中心数据展现作业状态，或更新注册中心数据修改全局配置。

控制台只能控制作业本身是否运行，但不能控制作业进程的启动，因为控制台和作业本身服务器是完全分离的，控制台并不能控制作业服务器。

## 不支持项

* 添加作业。
作业在首次运行时将自动添加。`Elastic-Job-Lite`以`jar`方式启动，并无作业分发功能。如需完全通过运维平台发布作业，请使用`Elastic-Job-Cloud`。

## 主要界面

* 总览页

![总览页](../../../../../img/console/lite_index.png)

* 注册中心管理页

![注册中心管理页](../../../../../img/console/lite_reg_center.png)

* 作业详细信息页

![作业详细信息页](../../../../../img/console/lite_job_details.png)

* 服务器详细信息页

![服务器详细信息页](../../../../../img/console/lite_server_details.png)