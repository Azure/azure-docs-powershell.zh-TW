---
title: 使用 Azure PowerShell 來建立 Azure 服務主體
description: 了解如何使用 Azure PowerShell 來為應用程式或服務建立服務主體。
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594703"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="8dbda-104">使用 Azure PowerShell 來建立 Azure 服務主體</span><span class="sxs-lookup"><span data-stu-id="8dbda-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="8dbda-105">如果您打算使用 Azure PowerShell 來管理應用程式或服務，請根據 Azure Active Directory (AAD) 服務主體 (而非您自己的認證) 來執行它。</span><span class="sxs-lookup"><span data-stu-id="8dbda-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="8dbda-106">本文會逐步引導您使用 Azure PowerShell 建立安全性主體。</span><span class="sxs-lookup"><span data-stu-id="8dbda-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="8dbda-107">何謂服務主體？</span><span class="sxs-lookup"><span data-stu-id="8dbda-107">What is a service principal?</span></span>

<span data-ttu-id="8dbda-108">Azure 服務主體是一項安全性身分識別，可供使用者所建立的應用程式、服務和自動化工具用來存取特定 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="8dbda-108">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="8dbda-109">服務主體會獲派與其工作相關的特定權限，以便讓您獲得更好的安全性控制能力。</span><span class="sxs-lookup"><span data-stu-id="8dbda-109">Service principals are assigned specific permissions related to their tasks, giving you better security control.</span></span> <span data-ttu-id="8dbda-110">這與一般的使用者身分識別不同，後者通常會獲得進行任何變更的授權。</span><span class="sxs-lookup"><span data-stu-id="8dbda-110">This is unlike a general user identity, which is usually authorized to make any changes.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="8dbda-111">確認您自己的權限等級</span><span class="sxs-lookup"><span data-stu-id="8dbda-111">Verify your own permission level</span></span>

<span data-ttu-id="8dbda-112">首先，您在 Azure Active Directory 和 Azure 訂用帳戶中都必須有足夠的權限。</span><span class="sxs-lookup"><span data-stu-id="8dbda-112">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="8dbda-113">您必須能夠在 Active Directory 中建立應用程式，並將角色指派給服務主體。</span><span class="sxs-lookup"><span data-stu-id="8dbda-113">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="8dbda-114">要檢查您的帳戶是否具有正確的權限，最簡單的方式是透過入口網站。</span><span class="sxs-lookup"><span data-stu-id="8dbda-114">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="8dbda-115">請參閱[在入口網站中檢查必要的權限](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)。</span><span class="sxs-lookup"><span data-stu-id="8dbda-115">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="8dbda-116">建立應用程式的服務主體</span><span class="sxs-lookup"><span data-stu-id="8dbda-116">Create a service principal for your app</span></span>

<span data-ttu-id="8dbda-117">在登入 Azure 帳戶之後，您便可以建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="8dbda-117">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="8dbda-118">您必須具備下列其中一種用來識別已部署之應用程式的方式︰</span><span class="sxs-lookup"><span data-stu-id="8dbda-118">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="8dbda-119">已部署之應用程式的唯一名稱，例如下列範例的「MyDemoWebApp」</span><span class="sxs-lookup"><span data-stu-id="8dbda-119">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples</span></span>
* <span data-ttu-id="8dbda-120">應用程式識別碼、與您已部署的應用程式、服務或物件相關聯的唯一 GUID</span><span class="sxs-lookup"><span data-stu-id="8dbda-120">The Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="8dbda-121">取得應用程式的相關資訊</span><span class="sxs-lookup"><span data-stu-id="8dbda-121">Get information about your application</span></span>

<span data-ttu-id="8dbda-122">`Get-AzADApplication` Cmdlet 可用來取得應用程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8dbda-122">The `Get-AzADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
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

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="8dbda-123">建立應用程式的服務主體</span><span class="sxs-lookup"><span data-stu-id="8dbda-123">Create a service principal for your application</span></span>

<span data-ttu-id="8dbda-124">`New-AzADServicePrincipal` Cmdlet 可用來建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="8dbda-124">The `New-AzADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

<span data-ttu-id="8dbda-125">從這裡開始，您可以直接使用 `$servicePrincipal.Secret` 屬性作為 `Connect-AzAccount` 的引數 (請參閱「使用服務主體登入」)，也可以將此 `SecureString` 轉換為純文字字串：</span><span class="sxs-lookup"><span data-stu-id="8dbda-125">From here, you can either directly use the `$servicePrincipal.Secret` property as an argument to `Connect-AzAccount` (see "Sign in using the service principal"), or you can convert this `SecureString` to a plain text string:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="8dbda-126">使用服務主體來登入</span><span class="sxs-lookup"><span data-stu-id="8dbda-126">Sign in using the service principal</span></span>

<span data-ttu-id="8dbda-127">您現在可以使用您提供的 `appId` 和產生的 `password`，以應用程式的新服務主體身分來登入。</span><span class="sxs-lookup"><span data-stu-id="8dbda-127">You can now sign in as the new service principal for your app using the `appId` you provided and `password` that was</span></span>  
generated. <span data-ttu-id="8dbda-129">您的服務主體也需要租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="8dbda-129">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="8dbda-130">當您使用個人認證來登入 Azure 時，系統會顯示您的租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="8dbda-130">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="8dbda-131">若要使用服務主體登入，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="8dbda-131">To sign in with a service principal, use the commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="8dbda-132">成功登入後，您會看到如下的輸出︰</span><span class="sxs-lookup"><span data-stu-id="8dbda-132">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="8dbda-133">恭喜！</span><span class="sxs-lookup"><span data-stu-id="8dbda-133">Congratulations!</span></span> <span data-ttu-id="8dbda-134">您可以使用這些認證來執行應用程式了。</span><span class="sxs-lookup"><span data-stu-id="8dbda-134">You can use these credentials to run your app.</span></span> <span data-ttu-id="8dbda-135">接下來，您需要調整服務主體的權限。</span><span class="sxs-lookup"><span data-stu-id="8dbda-135">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="8dbda-136">管理角色</span><span class="sxs-lookup"><span data-stu-id="8dbda-136">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="8dbda-137">Azure 角色型存取控制 (RBAC) 是一種可定義及管理使用者和服務主體角色的模型。</span><span class="sxs-lookup"><span data-stu-id="8dbda-137">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="8dbda-138">角色會有一組相關聯的權限，以決定主體可以讀取、存取、寫入或管理的資源。</span><span class="sxs-lookup"><span data-stu-id="8dbda-138">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="8dbda-139">如需 RBAC 和角色的詳細資訊，請參閱 [RBAC：內建角色](/azure/active-directory/role-based-access-built-in-roles)</span><span class="sxs-lookup"><span data-stu-id="8dbda-139">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="8dbda-140">Azure PowerShell 提供下列 Cmdlet 以供您管理角色指派︰</span><span class="sxs-lookup"><span data-stu-id="8dbda-140">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="8dbda-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8dbda-141">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="8dbda-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8dbda-142">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="8dbda-143">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8dbda-143">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="8dbda-144">服務主體的預設角色是**參與者**。</span><span class="sxs-lookup"><span data-stu-id="8dbda-144">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="8dbda-145">視應用程式與 Azure 服務的互動範圍而定，此角色可能並非最佳選擇，因為它所提供的權限很廣泛。</span><span class="sxs-lookup"><span data-stu-id="8dbda-145">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="8dbda-146">角色的權限較為侷限，因此很適合唯讀應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="8dbda-146">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="8dbda-147">您可以透過 Azure 入口網站來檢視角色專屬權限的詳細資料或建立自訂角色。</span><span class="sxs-lookup"><span data-stu-id="8dbda-147">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="8dbda-148">在此範例中，我們會對先前的範例新增**讀取者**角色，並刪除**參與者**角色︰</span><span class="sxs-lookup"><span data-stu-id="8dbda-148">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
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
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="8dbda-149">若要檢視目前已指派的角色︰</span><span class="sxs-lookup"><span data-stu-id="8dbda-149">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
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

<span data-ttu-id="8dbda-150">可用來管理角色的其他 Azure PowerShell Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8dbda-150">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="8dbda-151">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8dbda-151">Get-AzRoleDefinition</span></span>](/powershell/module/az.resources/Get-azRoleDefinition)
* [<span data-ttu-id="8dbda-152">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8dbda-152">New-AzRoleDefinition</span></span>](/powershell/module/az.resources/New-azRoleDefinition)
* [<span data-ttu-id="8dbda-153">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8dbda-153">Remove-AzRoleDefinition</span></span>](/powershell/module/az.resources/Remove-azRoleDefinition)
* [<span data-ttu-id="8dbda-154">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8dbda-154">Set-AzRoleDefinition</span></span>](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="8dbda-155">變更安全性主體的認證</span><span class="sxs-lookup"><span data-stu-id="8dbda-155">Change the credentials of the security principal</span></span>

<span data-ttu-id="8dbda-156">定期檢閱權限並更新密碼是很好的安全性作法。</span><span class="sxs-lookup"><span data-stu-id="8dbda-156">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="8dbda-157">您也可能會想要在應用程式變更時，管理及修改安全性認證。</span><span class="sxs-lookup"><span data-stu-id="8dbda-157">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="8dbda-158">例如，我們可以藉由建立新密碼並移除舊密碼，來變更服務主體的密碼。</span><span class="sxs-lookup"><span data-stu-id="8dbda-158">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="8dbda-159">為服務主體新增密碼</span><span class="sxs-lookup"><span data-stu-id="8dbda-159">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="8dbda-160">取得服務主體的認證清單</span><span class="sxs-lookup"><span data-stu-id="8dbda-160">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="8dbda-161">從服務主體移除舊密碼</span><span class="sxs-lookup"><span data-stu-id="8dbda-161">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="8dbda-162">確認服務主體的認證清單</span><span class="sxs-lookup"><span data-stu-id="8dbda-162">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="8dbda-163">取得服務主體的相關資訊</span><span class="sxs-lookup"><span data-stu-id="8dbda-163">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
