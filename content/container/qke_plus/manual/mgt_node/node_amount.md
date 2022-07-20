---
title: "调整节点数量"
description: 介绍如何新增及删除 QKE 集群节点。
draft: false
enableToc: false
keyword: 云计算, QKE, 横向扩容, 伸缩, 节点
weight: 10
---

QKE 集群支持通过新增或删除节点来进行集群横向扩缩容。

> **说明**
>
> 您可以通过**自动伸缩**功能来自动调整节点数量。具体操作请参见[节点弹性伸缩](../auto_node/)。

## 新增节点

您可以通过新增节点来应对应用逐步增多带来的压力。

1. 登录管理控制台。

2. 在控制台顶部的导航菜单中，选择**产品与服务** > **容器服务** > **容器引擎 QKE**，进入 QKE 集群列表页面。

3. 在集群列表，点击待查看集群的名称，进入**集群概览**页面。

4. 在左侧导航栏，选择**资源管理** > **节点管理**，进入**节点管理**页面。

4. 点击**新增节点**，弹出**新增节点**页面。

   ![](/container/qke_plus/_images/add_node.png)

6. 选择新增节点类型，并配置节点信息：节点规格（即云服务实例规格）、硬盘大小、节点数量、节点名称。

   > **说明**
   >
   > - 不支持新增主节点。
   > - 基础型节点只能选择基础型实例，企业型节点只能选择企业型实例。
   > - 若增加当前集群已存在的节点类型，则只能增加节点数量，不可选择同类型下其他规格。例如，当前集群中基础型工作节点已存在性能型 4核8G 的节点，则增加基础型工作节点时，只能选择性能型 4核8G 的规格，不支持增加其他规格的实例。

7. 点击**确定**。

## 删除节点

当集群服务能力过剩时，您也可以删除多余的节点，以节省资源和费用。

> **注意**
>
> - 删除前请确保 QKE 集群内有足够资源容纳迁移的 Pod。
> - 删除节点不可恢复，请谨慎操作。
> - 集群至少需要有 3 个工作节点。
> - 不支持删除主节点。

1. 登录管理控制台。

2. 在控制台顶部的导航菜单中，选择**产品与服务** > **容器服务** > **容器引擎 QKE**，进入 QKE 集群列表页面。

3. 在集群列表，点击待查看集群的名称，进入**集群概览**页面。

4. 在左侧导航栏，选择**资源管理** > **节点管理**，进入**节点管理**页面。

5. 在节点列表，点击**操作**列的**删除**，弹出提示框。

   若需删除多个节点，则勾选多个节点，然后点击**批量删除**。

   ![](/container/qke_plus/_images/delete_node.png)

6. 确认无误后，点击**删除**。
