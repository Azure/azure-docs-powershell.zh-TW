---
title: 使用 Azure PowerShell 來建立 Azure 服務主體
description: 了解如何使用 Azure PowerShell 來為應用程式或服務建立服務主體。
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 433a638187f024883c177457e420a759968fed9a
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001434"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="cd3fa-104">使用 Azure PowerShell 來建立 Azure 服務主體</span><span class="sxs-lookup"><span data-stu-id="cd3fa-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="cd3fa-105">如果您打算使用 Azure PowerShell 來管理應用程式或服務，請根據 Azure Active Directory (AAD) 服務主體 (而非您自己的認證) 來執行它。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="cd3fa-106">本文會逐步引導您使用 Azure PowerShell 建立安全性主體。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="cd3fa-107">您也可以透過 Azure 入口網站來建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="cd3fa-108">如需詳細資訊，請閱讀[使用入口網站來建立可存取資源的 Active Directory 應用程式和服務主體](/azure/azure-resource-manager/resource-group-create-service-principal-portal)。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="cd3fa-109">何謂「服務主體」？</span><span class="sxs-lookup"><span data-stu-id="cd3fa-109">What is a 'service principal'?</span></span>

<span data-ttu-id="cd3fa-110">Azure 服務主體是一項安全性身分識別，可供使用者所建立的應用程式、服務和自動化工具用來存取特定 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="cd3fa-111">您可以把它想成是具有特定角色及嚴格控制權限的「使用者身分識別」(使用者名稱和密碼或憑證)。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="cd3fa-112">不同於一般的使用者身分識別，服務主體只需要執行特定動作。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-112">A service principal should only need to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="cd3fa-113">如果您只對服務主體授與它為了執行管理工作所需要的最低權限等級，它就能提高安全性。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="cd3fa-114">確認您自己的權限等級</span><span class="sxs-lookup"><span data-stu-id="cd3fa-114">Verify your own permission level</span></span>

<span data-ttu-id="cd3fa-115">首先，您在 Azure Active Directory 和 Azure 訂用帳戶中都必須有足夠的權限。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="cd3fa-116">您必須能夠在 Active Directory 中建立應用程式，並將角色指派給服務主體。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-116">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="cd3fa-117">要檢查您的帳戶是否具有正確的權限，最簡單的方式是透過入口網站。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-117">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="cd3fa-118">請參閱[在入口網站中檢查必要的權限](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="cd3fa-119">建立應用程式的服務主體</span><span class="sxs-lookup"><span data-stu-id="cd3fa-119">Create a service principal for your app</span></span>

<span data-ttu-id="cd3fa-120">在登入 Azure 帳戶之後，您便可以建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-120">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="cd3fa-121">您必須具備下列其中一種用來識別已部署之應用程式的方式︰</span><span class="sxs-lookup"><span data-stu-id="cd3fa-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="cd3fa-122">已部署之應用程式的唯一名稱，例如下列範例的「MyDemoWebApp」，或是</span><span class="sxs-lookup"><span data-stu-id="cd3fa-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="cd3fa-123">應用程式識別碼、與您已部署的應用程式、服務或物件相關聯的唯一 GUID</span><span class="sxs-lookup"><span data-stu-id="cd3fa-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="cd3fa-124">取得應用程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="cd3fa-124">Get information about your application</span></span>

<span data-ttu-id="cd3fa-125">`Get-AzureRmADApplication` Cmdlet 可用來取得應用程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-125">The `Get-AzureRmADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
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

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="cd3fa-126">建立應用程式的服務主體</span><span class="sxs-lookup"><span data-stu-id="cd3fa-126">Create a service principal for your application</span></span>

<span data-ttu-id="cd3fa-127">`New-AzureRmADServicePrincipal` Cmdlet 可用來建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
$securePassword = ConvertTo-SecureString -Force -AsPlainText -String $password
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $securePassword
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="cd3fa-128">取得服務主體的相關資訊</span><span class="sxs-lookup"><span data-stu-id="cd3fa-128">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="cd3fa-129">使用服務主體來登入</span><span class="sxs-lookup"><span data-stu-id="cd3fa-129">Sign in using the service principal</span></span>

<span data-ttu-id="cd3fa-130">您現在可以使用您提供的「應用程式識別碼」和「密碼」，來登入成為應用程式的新服務主體。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-130">You can now sign in as the new service principal for your app using the *appId* and *password* you provided.</span></span> <span data-ttu-id="cd3fa-131">您的服務主體也需要租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-131">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="cd3fa-132">當您使用個人認證來登入 Azure 時，系統會顯示您的租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-132">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="cd3fa-133">若要使用服務主體登入，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="cd3fa-133">To sign in with a service principal, use the following commands:</span></span>

```azurepowershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="cd3fa-134">成功登入後，您會看到如下的輸出︰</span><span class="sxs-lookup"><span data-stu-id="cd3fa-134">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="cd3fa-135">恭喜！</span><span class="sxs-lookup"><span data-stu-id="cd3fa-135">Congratulations!</span></span> <span data-ttu-id="cd3fa-136">您可以使用這些認證來執行應用程式了。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="cd3fa-137">接下來，您需要調整服務主體的權限。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="cd3fa-138">管理角色</span><span class="sxs-lookup"><span data-stu-id="cd3fa-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="cd3fa-139">Azure 角色型存取控制 (RBAC) 是一種可定義及管理使用者和服務主體角色的模型。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="cd3fa-140">角色會有一組相關聯的權限，以決定主體可以讀取、存取、寫入或管理的資源。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="cd3fa-141">如需 RBAC 和角色的詳細資訊，請參閱 [RBAC：內建角色](/azure/active-directory/role-based-access-built-in-roles)。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="cd3fa-142">Azure PowerShell 提供下列 Cmdlet 以供您管理角色指派︰</span><span class="sxs-lookup"><span data-stu-id="cd3fa-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="cd3fa-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cd3fa-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="cd3fa-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cd3fa-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="cd3fa-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cd3fa-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="cd3fa-146">服務主體的預設角色是**參與者**。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="cd3fa-147">視應用程式與 Azure 服務的互動範圍而定，此角色可能並非最佳選擇，因為它所提供的權限很廣泛。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="cd3fa-148">角色的權限較為侷限，因此很適合唯讀應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="cd3fa-149">您可以透過 Azure 入口網站來檢視角色專屬權限的詳細資料或建立自訂角色。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="cd3fa-150">在此範例中，我們會對先前的範例新增**讀取者**角色，並刪除**參與者**角色︰</span><span class="sxs-lookup"><span data-stu-id="cd3fa-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="cd3fa-151">若要檢視目前已指派的角色︰</span><span class="sxs-lookup"><span data-stu-id="cd3fa-151">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="cd3fa-152">可用來管理角色的其他 Azure PowerShell Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cd3fa-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="cd3fa-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cd3fa-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="cd3fa-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cd3fa-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="cd3fa-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cd3fa-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="cd3fa-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cd3fa-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="cd3fa-157">變更安全性主體的認證</span><span class="sxs-lookup"><span data-stu-id="cd3fa-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="cd3fa-158">定期檢閱權限並更新密碼是很好的安全性作法。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="cd3fa-159">您也可能會想要在應用程式變更時，管理及修改安全性認證。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="cd3fa-160">例如，我們可以藉由建立新密碼並移除舊密碼，來變更服務主體的密碼。</span><span class="sxs-lookup"><span data-stu-id="cd3fa-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="cd3fa-161">為服務主體新增密碼</span><span class="sxs-lookup"><span data-stu-id="cd3fa-161">Add a new password for the service principal</span></span>

```azurepowershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="cd3fa-162">取得服務主體的認證清單</span><span class="sxs-lookup"><span data-stu-id="cd3fa-162">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="cd3fa-163">從服務主體移除舊密碼</span><span class="sxs-lookup"><span data-stu-id="cd3fa-163">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="cd3fa-164">確認服務主體的認證清單</span><span class="sxs-lookup"><span data-stu-id="cd3fa-164">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
