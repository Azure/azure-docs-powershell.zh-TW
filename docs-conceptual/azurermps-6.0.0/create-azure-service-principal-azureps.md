---
title: 使用 Azure PowerShell 來建立 Azure 服務主體
description: 了解如何使用 Azure PowerShell 來為應用程式或服務建立服務主體。
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 4866ee6fa4d88f1e3143c4e4b5df7fa3cc80eeee
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/08/2018
ms.locfileid: "33911896"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>使用 Azure PowerShell 來建立 Azure 服務主體

如果您打算使用 Azure PowerShell 來管理應用程式或服務，請根據 Azure Active Directory (AAD) 服務主體 (而非您自己的認證) 來執行它。 本主題會逐步引導您使用 Azure PowerShell 來建立安全性主體。

> [!NOTE]
> 您也可以透過 Azure 入口網站來建立服務主體。 如需詳細資訊，請閱讀[使用入口網站來建立可存取資源的 Active Directory 應用程式和服務主體](/azure/azure-resource-manager/resource-group-create-service-principal-portal)。

## <a name="what-is-a-service-principal"></a>何謂「服務主體」？

Azure 服務主體是一項安全性身分識別，可供使用者所建立的應用程式、服務和自動化工具用來存取特定 Azure 資源。 您可以把它想成是具有特定角色及嚴格控制權限的「使用者身分識別」(使用者名稱和密碼或憑證)。 不同於一般的使用者識別，服務主體只需要能夠執行特定動作。 如果您只對服務主體授與它為了執行管理工作所需要的最低權限等級，它就能提高安全性。

## <a name="verify-your-own-permission-level"></a>確認您自己的權限等級

首先，您在 Azure Active Directory 和 Azure 訂用帳戶中都必須有足夠的權限。 具體來說，您必須能夠在 Active Directory 中建立應用程式，並將角色指派給服務主體。

檢查您的帳戶是否具有足夠的權限，最簡單的方式是透過入口網站。 請參閱[在入口網站中檢查必要的權限](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)。

## <a name="create-a-service-principal-for-your-app"></a>建立應用程式的服務主體

在登入 Azure 帳戶之後，您便可以建立服務主體。 您必須具備下列其中一種用來識別已部署之應用程式的方式︰

* 已部署之應用程式的唯一名稱，例如下列範例的「MyDemoWebApp」，或是
* 應用程式識別碼、與您已部署的應用程式、服務或物件相關聯的唯一 GUID

### <a name="get-information-about-your-application"></a>取得應用程式的相關資訊

`Get-AzureRmADApplication` Cmdlet 可用來探索應用程式的相關資訊。

```powershell
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a>建立應用程式的服務主體

`New-AzureRmADServicePrincipal` Cmdlet 可用來建立服務主體。

```powershell
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
$securePassword = ConvertTo-SecureString -Force -AsPlainText -String $password
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $securePassword
```

```
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a>取得服務主體的相關資訊

```powershell
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a>使用服務主體來登入

您現在可以使用您提供的「應用程式識別碼」和「密碼」，來登入成為應用程式的新服務主體。 您需要提供帳戶的租用戶識別碼。 當您使用個人認證來登入 Azure 時，系統會顯示您的租用戶識別碼。

```powershell
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

從新的 PowerShell 工作階段執行此命令。 成功登入之後，您會看到如下所示的輸出︰

```
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

恭喜！ 您可以使用這些認證來執行應用程式了。 接下來，您需要調整服務主體的權限。

## <a name="managing-roles"></a>管理角色

> [!NOTE]
> Azure 角色型存取控制 (RBAC) 是一種可定義及管理使用者和服務主體角色的模型。 角色會有一組相關聯的權限，以決定主體可以讀取、存取、寫入或管理的資源。 如需 RBAC 和角色的詳細資訊，請參閱 [RBAC：內建角色](/azure/active-directory/role-based-access-built-in-roles)。

Azure PowerShell 提供下列 Cmdlet 以供您管理角色指派︰

* [Get-AzureRmRoleAssignment](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [New-AzureRmRoleAssignment](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [Remove-AzureRmRoleAssignment](/powershell/module/azurerm.resources/remove-azurermroleassignment)

服務主體的預設角色是**參與者**。 視應用程式與 Azure 服務的互動範圍而定，此角色可能並非最佳選擇，因為它所提供的權限很廣泛。
角色的權限較為侷限，因此很適合唯讀應用程式使用。 您可以透過 Azure 入口網站來檢視角色專屬權限的詳細資料或建立自訂角色。

在此範例中，我們會對先前的範例新增**讀取者**角色，並刪除**參與者**角色︰

```powershell
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```powershell
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

若要檢視目前已指派的角色︰

```powershell
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

可用來管理角色的其他 Azure PowerShell Cmdlet：

* [Get-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleDefinition](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>變更安全性主體的認證

定期檢閱權限並更新密碼是很好的安全性作法。 您也可能會想要在應用程式變更時，管理及修改安全性認證。 例如，我們可以藉由建立新密碼並移除舊密碼，來變更服務主體的密碼。

### <a name="add-a-new-password-for-the-service-principal"></a>為服務主體新增密碼

```powershell
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>取得服務主體的認證清單

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>從服務主體移除舊密碼

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>確認服務主體的認證清單

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
