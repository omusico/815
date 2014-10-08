<properties writer="kathydav" editor="tysonn" manager="jeffreyg" />

#如何创建自定义虚拟机

通过创建自定义虚拟机，您可以选择在使用“快速创建”方法时不可用的选项。这些选项包括连接到虚拟网络、连接到现有云服务以及连接到可用性集。

每台虚拟机都将独自或与位于相同云服务中的其他虚拟机一起与某个云服务相关联。在相同云服务中放置多台虚拟机一般是为了提供应用程序的负载平衡。如果您的应用程序只需要一台虚拟机，或者您要创建第一台虚拟机，则将在创建虚拟机时创建云服务。否则，您需将新的虚拟机添加到现有云服务。

**重要说明**：如果您希望您的虚拟机使用虚拟网络，以便可以按主机名直接连接到它或者设置跨界连接，则请确保在创建虚拟机时指定虚拟网络。仅当创建虚拟机后，才能将该虚拟机配置为加入虚拟网络。有关虚拟网络的更多信息，请参见 [Windows Azure 虚拟网络概述](http://go.microsoft.com/fwlink/p/?LinkID=294063)。

1. 登录到 [Windows Azure 管理门户](http://manage.windowsazure.com)。

2. 在命令栏上，单击“新建”。

3. 依次单击“计算”、“虚拟机”和“从库中”。

4. 从“平台映像”选择想要使用的平台映像，然后单击箭头以继续。
	
5. 如果提供了多个版本的映像，请在“版本发布日期”中，选取您要使用的版本。

6. 在“虚拟机名称”中，键入您要用于该虚拟机的名称。

7. 在“大小”中，选择要用于该虚拟机的大小。所选大小具体取决于您应用程序所需的内核数。

8. 在“新用户名”中，键入要用于管理服务器的管理帐户的名称。

9. 在“新密码”中，为虚拟机上的管理帐户键入要使用的强密码。在“确认密码”中，重新键入相同密码。

10. 单击箭头以继续。

11. 在“云服务”中，执行下列操作之一：
	
- 如果这是云服务中的第一台虚拟机或唯一的一台虚拟机，请选择“新建云服务”。然后，在“云服务 DNS 名称”中，键入使用 3 到 24 个小写字母和数字的名称。此名称将成为用于通过云服务联系虚拟机的 URI 的一部分。
- 如果要将此虚拟机添加到云服务，请在列表中选择它。

	**注意**：有关在相同云服务中放置虚拟机的更多信息，请参见[如何连接云服务中的虚拟机](http://www.windowsazure.com/zh-cn/manage/windows/how-to-guides/connect-to-a-cloud-service/)。

12. 在“区域/地缘组/虚拟网络”中，选择要用于该虚拟机的区域、地缘组或虚拟网络。有关地缘组的更多信息，请参见[关于虚拟网络的地缘组][]。

13. 在“存储帐户”中，选择 VHD 文件的现有存储帐户，或者使用自动生成的存储帐户。每个区域只能自动创建一个存储帐户。使用此设置创建的所有其他虚拟机也位于该存储帐户中。您最多只能创建 20 个存储帐户。

14. 如果您希望虚拟机属于一个可用性集，请在“可用性集”中，选择“创建可用性集”或将虚拟机添加到现有可用性集。

	**注意**：属于可用性集成员的虚拟机将部署到不同的故障域中。在一个可用性集中放置多台虚拟机将帮助确保您的应用程序在出现网络故障、本地磁盘硬件故障以及任何计划内停机时仍然可用。

15. 在“VM 代理”下，确定是否要安装 VM 代理。此代理为您提供安装扩展的环境，可帮助您与虚拟机交互。有关详细信息，请参见[使用扩展](http://go.microsoft.com/FWLink/p/?LinkID=394093)。
	**重要说明**：仅当您创建虚拟机时才能安装 VM 代理。

15. 在“终结点”下，查看为了允许通过远程桌面或安全 Shell (SSH) 客户端等连接到虚拟机而要创建的新终结点。您还可现在添加终结点，或者稍后创建终结点。有关稍后创建终结点的说明，请参见[如何设置与虚拟机的通信](http://www.windowsazure.com/zh-cn/manage/linux/how-to-guides/setup-endpoints/)。


16. 单击箭头以创建虚拟机。


	![成功创建自定义虚拟机](./media/howto-custom-create-vm/VMSuccessWindows.png)


[将虚拟机添加到虚拟网络]：/zh-cn/manage/services/networking/add-a-vm-to-a-virtual-network/

[关于虚拟网络的地缘组]：http://msdn.microsoft.com/zh-cn/library/windowsazure/

[新建虚拟机]：./media/howto-custom-create-vm/Create.png

[新建自定义虚拟机]：./media/howto-custom-create-vm/CreateNew.png


