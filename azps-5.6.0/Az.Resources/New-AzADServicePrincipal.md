---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: f826ecbde81bc301cc51e031b2047bc7a9f284e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911317"
---
# <span data-ttu-id="1b58b-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1b58b-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="1b58b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1b58b-102">SYNOPSIS</span></span>
<span data-ttu-id="1b58b-103">建立新的 Azure Active Directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1b58b-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="1b58b-104">語法</span><span class="sxs-lookup"><span data-stu-id="1b58b-104">SYNTAX</span></span>

### <span data-ttu-id="1b58b-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1b58b-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b58b-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b58b-107">ApplicationWithPasswordP有ParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b58b-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b58b-109">ApplicationWithKeyP有ParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b58b-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b58b-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b58b-112">DisplayNameWithPasswordP有ParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b58b-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b58b-114">DisplayNameWithKeyP區ParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b58b-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b58b-116">ApplicationObjectWithPasswordPectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b58b-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b58b-118">ApplicationObjectWithKeyP區ParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b58b-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b58b-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b58b-120">描述</span><span class="sxs-lookup"><span data-stu-id="1b58b-120">DESCRIPTION</span></span>

<span data-ttu-id="1b58b-121">建立新的 Azure Active Directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1b58b-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="1b58b-122">如果沒有提供參數，預設參數集會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="1b58b-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="1b58b-123">有關預設值的資訊，請參閱每個參數的描述。</span><span class="sxs-lookup"><span data-stu-id="1b58b-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="1b58b-124">此 Cmdlet 能夠使用角色和範圍參數，將角色指派給 **服務主體。**</span><span class="sxs-lookup"><span data-stu-id="1b58b-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="1b58b-125">如果兩者都省略，參與者角色會指派給服務主體。</span><span class="sxs-lookup"><span data-stu-id="1b58b-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="1b58b-126">角色和範圍參數的 **預設值為\*\*\*\*目前** 訂閱的投稿者。</span><span class="sxs-lookup"><span data-stu-id="1b58b-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="1b58b-127">如果沒有提供 ApplicationId，Cmdlet 會建立應用程式並設定其屬性。</span><span class="sxs-lookup"><span data-stu-id="1b58b-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="1b58b-128">若要更新應用程式特定的參數，請使用 [Update-AzADApplication](./update-azadapplication.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b58b-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="1b58b-129">當您使用 **New-AzADServicePrincipal** 命令建立服務主體時，輸出會包含您必須保護的認證。</span><span class="sxs-lookup"><span data-stu-id="1b58b-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="1b58b-130">或者，請考慮使用 [受管理的身分](/azure/active-directory/managed-identities-azure-resources/overview) ，以避免使用認證。</span><span class="sxs-lookup"><span data-stu-id="1b58b-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="1b58b-131">根據預設 **，New-AzADServicePrincipal** 會指派 [](/azure/role-based-access-control/built-in-roles#contributor)訂閱範圍的服務主體參與者角色。</span><span class="sxs-lookup"><span data-stu-id="1b58b-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="1b58b-132">若要降低服務主體遭到入侵的風險，請指派更特定的角色，並將範圍縮小到資源或資源群組。</span><span class="sxs-lookup"><span data-stu-id="1b58b-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="1b58b-133">請參閱 [新增角色指派的步驟](/azure/role-based-access-control/role-assignments-steps) 以瞭解更多資訊。</span><span class="sxs-lookup"><span data-stu-id="1b58b-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="1b58b-134">例子</span><span class="sxs-lookup"><span data-stu-id="1b58b-134">EXAMPLES</span></span>

### <span data-ttu-id="1b58b-135">範例 1：簡單的 AD 服務主體建立</span><span class="sxs-lookup"><span data-stu-id="1b58b-135">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="1b58b-136">下列範例會針對未指定的參數使用預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1b58b-136">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="1b58b-137">由於未提供應用程式識別碼，因此會針對服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b58b-137">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="1b58b-138">由於未提供 **角色或範圍** 的值，因此已建立的服務主體會 **指派目前訂閱** 的參與者角色。</span><span class="sxs-lookup"><span data-stu-id="1b58b-138">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="1b58b-139">範例 2：使用指定角色和預設範圍建立簡易 AD 服務主體</span><span class="sxs-lookup"><span data-stu-id="1b58b-139">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="1b58b-140">下列範例會針對未指定的參數使用預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1b58b-140">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="1b58b-141">由於未提供應用程式識別碼，因此會針對服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b58b-141">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="1b58b-142">服務主體是使用目前訂閱 **的讀取** 者許可權所建立，因為 Scope 參數未 **提供** 值。</span><span class="sxs-lookup"><span data-stu-id="1b58b-142">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### <span data-ttu-id="1b58b-143">範例 3：使用指定範圍和預設角色建立簡易 AD 服務主體</span><span class="sxs-lookup"><span data-stu-id="1b58b-143">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="1b58b-144">下列範例會針對未指定的參數使用預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1b58b-144">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="1b58b-145">由於未提供應用程式識別碼，因此會針對服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b58b-145">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="1b58b-146">服務主體是使用提供的資源群組範圍之參與者許可權所建立，因為角色參數未 **提供值**。</span><span class="sxs-lookup"><span data-stu-id="1b58b-146">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="1b58b-147">範例 4：使用指定範圍和角色建立簡易 AD 服務主體</span><span class="sxs-lookup"><span data-stu-id="1b58b-147">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="1b58b-148">下列範例會針對未指定的參數使用預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1b58b-148">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="1b58b-149">由於未提供應用程式識別碼，因此會針對服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b58b-149">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="1b58b-150">服務主體是 **使用所提供的資源** 群組範圍之讀取者許可權所建立。</span><span class="sxs-lookup"><span data-stu-id="1b58b-150">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="1b58b-151">範例 5：使用角色指派的應用程式識別碼建立新 AD 服務主體</span><span class="sxs-lookup"><span data-stu-id="1b58b-151">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="1b58b-152">下列範例會針對具有應用程式識別碼 '00000000-0000-0000-0000-000000-0000000000"的應用程式建立新的 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1b58b-152">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="1b58b-153">由於未提供 **角色或範圍** 的值，因此已建立的服務主體會 **指派目前訂閱** 的參與者角色。</span><span class="sxs-lookup"><span data-stu-id="1b58b-153">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="1b58b-154">範例 6：使用管線建立新 AD 服務主體</span><span class="sxs-lookup"><span data-stu-id="1b58b-154">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="1b58b-155">下列範例使用 [Get-AzADApplication](./get-azadapplication.md) Cmdlet 來取得具有物件識別碼 '3ede3c26-b443-4e0b-9efc-b05e68338dc3' 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b58b-155">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="1b58b-156">結果會移轉至 `New-AzADServicePrincipal` Cmdlet，為該應用程式建立新的 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1b58b-156">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="1b58b-157">範例 7：使用 DisplayName 和密碼認證建立新 AD 服務主體</span><span class="sxs-lookup"><span data-stu-id="1b58b-157">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="1b58b-158">下列範例會建立名稱 **為 ServicePrincipalName** 和 **StrongPassworld！23 密碼的新應用程式**。</span><span class="sxs-lookup"><span data-stu-id="1b58b-158">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="1b58b-159">它會根據所建立的應用程式建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="1b58b-159">It creates the service principal based on the created application.</span></span> <span data-ttu-id="1b58b-160">開始日期和結束日期會新增到密碼認證中。</span><span class="sxs-lookup"><span data-stu-id="1b58b-160">The start date and end date are added to the password credential.</span></span>

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### <span data-ttu-id="1b58b-161">範例 8：使用 DisplayName 和純金鑰認證建立新 AD 服務主體</span><span class="sxs-lookup"><span data-stu-id="1b58b-161">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="1b58b-162">下列範例會建立名稱 **為 ServicePrincipalName** 的新應用程式， **以及一個**$cert。它會根據建立的應用程式建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="1b58b-162">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="1b58b-163">結束日期會新增到金鑰認證。</span><span class="sxs-lookup"><span data-stu-id="1b58b-163">The end date is added to key credential.</span></span>

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## <span data-ttu-id="1b58b-164">參數</span><span class="sxs-lookup"><span data-stu-id="1b58b-164">PARAMETERS</span></span>

### <span data-ttu-id="1b58b-165">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1b58b-165">-ApplicationId</span></span>

<span data-ttu-id="1b58b-166">租使用者中服務主體的唯一應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="1b58b-166">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="1b58b-167">此屬性建立之後即無法變更。</span><span class="sxs-lookup"><span data-stu-id="1b58b-167">Once created this property cannot be changed.</span></span> <span data-ttu-id="1b58b-168">如果未指定現有應用程式的應用程式識別碼，即會建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b58b-168">If an application ID for an existing application is not specified, an application is created.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-169">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="1b58b-169">-ApplicationObject</span></span>

<span data-ttu-id="1b58b-170">代表建立服務主體之應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="1b58b-170">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-171">-CertValue</span><span class="sxs-lookup"><span data-stu-id="1b58b-171">-CertValue</span></span>

<span data-ttu-id="1b58b-172">非對稱認證類型的值。</span><span class="sxs-lookup"><span data-stu-id="1b58b-172">The value of the asymmetric credential type.</span></span> <span data-ttu-id="1b58b-173">它代表 Base64 編碼憑證。</span><span class="sxs-lookup"><span data-stu-id="1b58b-173">It represents the Base64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b58b-174">-DefaultProfile</span></span>

<span data-ttu-id="1b58b-175">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b58b-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-176">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1b58b-176">-DisplayName</span></span>

<span data-ttu-id="1b58b-177">服務主體的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="1b58b-177">The friendly name of the service principal.</span></span> <span data-ttu-id="1b58b-178">如果沒有提供顯示名稱，此值會預設為 **azure-powershell-MM-dd-yyyy-HH-mm-ss，** 其中後稱是應用程式建立的時間。</span><span class="sxs-lookup"><span data-stu-id="1b58b-178">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-179">-EndDate</span><span class="sxs-lookup"><span data-stu-id="1b58b-179">-EndDate</span></span>

<span data-ttu-id="1b58b-180">認證使用量的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="1b58b-180">The effective end date of the credential usage.</span></span> <span data-ttu-id="1b58b-181">預設結束日期為自今天起一年。</span><span class="sxs-lookup"><span data-stu-id="1b58b-181">The default end date value is one year from today.</span></span>
<span data-ttu-id="1b58b-182">對於非對稱類型認證，這必須設定為 X509 憑證有效日期當天或之前。</span><span class="sxs-lookup"><span data-stu-id="1b58b-182">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-183">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="1b58b-183">-KeyCredential</span></span>

<span data-ttu-id="1b58b-184">與應用程式相關聯的金鑰認證集合。</span><span class="sxs-lookup"><span data-stu-id="1b58b-184">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-185">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="1b58b-185">-PasswordCredential</span></span>

<span data-ttu-id="1b58b-186">與應用程式相關聯的密碼認證集合。</span><span class="sxs-lookup"><span data-stu-id="1b58b-186">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-187">-角色</span><span class="sxs-lookup"><span data-stu-id="1b58b-187">-Role</span></span>

<span data-ttu-id="1b58b-188">服務主體在範圍中的角色。</span><span class="sxs-lookup"><span data-stu-id="1b58b-188">The role that the service principal has over the scope.</span></span> <span data-ttu-id="1b58b-189">如果沒有提供值， **角色** 會 **預設為參與者** 角色。</span><span class="sxs-lookup"><span data-stu-id="1b58b-189">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-190">-範圍</span><span class="sxs-lookup"><span data-stu-id="1b58b-190">-Scope</span></span>

<span data-ttu-id="1b58b-191">服務主體具有許可權的範圍。</span><span class="sxs-lookup"><span data-stu-id="1b58b-191">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="1b58b-192">如果沒有提供值， **範圍** 會預設為目前的訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b58b-192">If no value is provided, **Scope** defaults to the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-193">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="1b58b-193">-SkipAssignment</span></span>

<span data-ttu-id="1b58b-194">如果設定完成，請略過建立服務主體的預設角色指派。</span><span class="sxs-lookup"><span data-stu-id="1b58b-194">If set, skip creating the default role assignment for the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-195">-StartDate</span><span class="sxs-lookup"><span data-stu-id="1b58b-195">-StartDate</span></span>

<span data-ttu-id="1b58b-196">認證使用量的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="1b58b-196">The effective start date of the credential usage.</span></span> <span data-ttu-id="1b58b-197">預設的開始日期值是今天。</span><span class="sxs-lookup"><span data-stu-id="1b58b-197">The default start date value is today.</span></span> <span data-ttu-id="1b58b-198">對於非對稱類型認證，這必須設定為 X509 憑證的有效日期當天或之後。</span><span class="sxs-lookup"><span data-stu-id="1b58b-198">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-199">-確認</span><span class="sxs-lookup"><span data-stu-id="1b58b-199">-Confirm</span></span>

<span data-ttu-id="1b58b-200">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1b58b-200">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b58b-201">-WhatIf</span></span>

<span data-ttu-id="1b58b-202">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1b58b-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b58b-203">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b58b-203">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b58b-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b58b-204">CommonParameters</span></span>
<span data-ttu-id="1b58b-205">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1b58b-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b58b-206">詳細資訊[請參閱about_CommonParameters。](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="1b58b-206">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="1b58b-207">輸入</span><span class="sxs-lookup"><span data-stu-id="1b58b-207">INPUTS</span></span>

### <span data-ttu-id="1b58b-208">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1b58b-208">System.Guid</span></span>

### <span data-ttu-id="1b58b-209">System.String</span><span class="sxs-lookup"><span data-stu-id="1b58b-209">System.String</span></span>

### <span data-ttu-id="1b58b-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="1b58b-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="1b58b-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="1b58b-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="1b58b-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="1b58b-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="1b58b-213">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="1b58b-213">System.DateTime</span></span>

## <span data-ttu-id="1b58b-214">輸出</span><span class="sxs-lookup"><span data-stu-id="1b58b-214">OUTPUTS</span></span>

### <span data-ttu-id="1b58b-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1b58b-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="1b58b-216">Microsoft.Azure.Commands.Resources.models.Authorization.PSADServicePrincipal方apper</span><span class="sxs-lookup"><span data-stu-id="1b58b-216">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="1b58b-217">筆記</span><span class="sxs-lookup"><span data-stu-id="1b58b-217">NOTES</span></span>

<span data-ttu-id="1b58b-218">關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="1b58b-218">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1b58b-219">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b58b-219">RELATED LINKS</span></span>

[<span data-ttu-id="1b58b-220">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1b58b-220">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="1b58b-221">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1b58b-221">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="1b58b-222">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1b58b-222">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="1b58b-223">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1b58b-223">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="1b58b-224">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1b58b-224">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="1b58b-225">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1b58b-225">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="1b58b-226">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1b58b-226">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)