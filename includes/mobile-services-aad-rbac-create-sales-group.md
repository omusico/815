﻿在本节中，将两个新用户添加到您的目录以及新销售组。其中一个用户将被授予销售组成员身份。另一个用户将不会被授予该组成员身份。 

### 创建用户


1. 在 [Azure 管理门户]中，浏览到您完成[身份验证入门]教程时先前为身份验证配置的目录。
2. 单击页面顶部的**用户**。然后单击底部的**添加用户**按钮。 
3. 完成"新建用户"对话框，该对话框创建来创建名为 **Bob** 的用户。请注意用户的临时密码。 
4. 创建名为 **Dave** 的另一个用户。请注意用户的临时密码。
5. 新用户应类似于以下显示的内容。

    ![](./media/mobile-services-aad-rbac-create-sales-group/users.png)    


### 创建销售组


1. 在目录页上，单击页面顶部的**组**。然后单击底部的**添加组**按钮。 
2. 输入**销售**作为组名称，然后按对话框上的"完成"按钮以创建组。 

    ![](./media/mobile-services-aad-rbac-create-sales-group/sales-group.png)

### 将用户成员身份添加到销售组。


1. 单击目录页面顶部的**组**。然后单击**销售**组以转到销售组页面。 
2. 在销售组页上，单击**添加成员**。将名为 **Bob** 的用户添加到销售组。名为 **Dave** 的用户不应是该组的成员。

    ![](./media/mobile-services-aad-rbac-create-sales-group/group-membership.png)

3. 在销售组页上，单击**配置**，然后，请注意销售组的**对象 ID**。本教程实际使用 Graph API 来查找组对象 ID。因此，您不需要此 ID。但是，在某些情况下,不使用组名称会更好，因为该名称可能会更改，其中 ID 保持不变。如果您想要将组 ID 作为应用设置存储在移动服务中，或将其硬编码将您的代码中，这是您找到它的位置。

    ![](./media/mobile-services-aad-rbac-create-sales-group/sales-group-id.png)

