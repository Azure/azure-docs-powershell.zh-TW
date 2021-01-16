---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435465"
---
# <span data-ttu-id="8497c-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8497c-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="8497c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8497c-102">SYNOPSIS</span></span>
<span data-ttu-id="8497c-103">建立新的 Azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="8497c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8497c-104">SYNTAX</span></span>

### <span data-ttu-id="8497c-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8497c-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8497c-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8497c-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8497c-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8497c-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8497c-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8497c-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8497c-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8497c-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8497c-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8497c-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8497c-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8497c-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8497c-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8497c-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8497c-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8497c-120">說明</span><span class="sxs-lookup"><span data-stu-id="8497c-120">DESCRIPTION</span></span>

<span data-ttu-id="8497c-121">建立新的 Azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="8497c-122">如果未提供參數，則預設參數集會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="8497c-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="8497c-123">如需有關預設值的詳細資訊，請參閱每個參數的描述。</span><span class="sxs-lookup"><span data-stu-id="8497c-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="8497c-124">這個 Cmdlet 能夠 **將角色指派** 給服務主體與 **作用域** 參數。</span><span class="sxs-lookup"><span data-stu-id="8497c-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="8497c-125">如果省略兩者，則會將參與者角色指派給服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="8497c-126">[ **角色** ] 與 [ **範圍** ] 參數的預設值是目前訂閱的 **參與者** 。</span><span class="sxs-lookup"><span data-stu-id="8497c-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="8497c-127">如果未提供 ApplicationId，此 Cmdlet 會建立應用程式並設定其屬性。</span><span class="sxs-lookup"><span data-stu-id="8497c-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="8497c-128">若要更新應用程式的特定參數，請使用 [AzADApplication](./update-azadapplication.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8497c-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="8497c-129">當您使用 **新的-AzADServicePrincipal** 命令建立服務主體時，輸出會包含您必須受到保護的認證。</span><span class="sxs-lookup"><span data-stu-id="8497c-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="8497c-130">請確定您的程式碼中不包含這些認證，或者請將認證核取到您的來源控制中。</span><span class="sxs-lookup"><span data-stu-id="8497c-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="8497c-131">或者，請考慮使用 [受管理](/azure/active-directory/managed-identities-azure-resources/overview) 的身分識別，以避免需要使用認證。</span><span class="sxs-lookup"><span data-stu-id="8497c-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="8497c-132">根據預設， **新-AzADServicePrincipal** 會將 [參與者](/azure/role-based-access-control/built-in-roles#contributor) 角色指派給訂閱範圍中的服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="8497c-133">若要降低受到危害的服務主體的風險，請指派更明確的角色，並將範圍縮小至資源或資源群組。</span><span class="sxs-lookup"><span data-stu-id="8497c-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="8497c-134">如需詳細資訊，請參閱 [新增角色分派的步驟](/azure/role-based-access-control/role-assignments-steps) 。</span><span class="sxs-lookup"><span data-stu-id="8497c-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="8497c-135">示例</span><span class="sxs-lookup"><span data-stu-id="8497c-135">EXAMPLES</span></span>

### <span data-ttu-id="8497c-136">範例1：簡單的 AD 服務主體建立</span><span class="sxs-lookup"><span data-stu-id="8497c-136">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="8497c-137">下列範例會使用未指定之參數的預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-137">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="8497c-138">因為未提供應用程式識別碼，所以會為服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="8497c-138">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="8497c-139">由於沒有為 **角色** 或 **範圍** 提供任何值，已建立的服務主體會獲指派目前訂閱的 **參與者** 角色。</span><span class="sxs-lookup"><span data-stu-id="8497c-139">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="8497c-140">範例2：使用指定角色和預設範圍進行簡單的 AD 服務主體建立</span><span class="sxs-lookup"><span data-stu-id="8497c-140">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="8497c-141">下列範例會使用未指定之參數的預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-141">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="8497c-142">因為未提供應用程式識別碼，所以會針對服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="8497c-142">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="8497c-143">由於沒有為 **範圍** 參數提供任何值，因此已建立目前訂閱的 **Reader** 許可權的服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-143">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

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

### <span data-ttu-id="8497c-144">範例3：使用指定的範圍和預設角色來建立簡單的 AD 服務主體</span><span class="sxs-lookup"><span data-stu-id="8497c-144">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="8497c-145">下列範例會使用未指定之參數的預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-145">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="8497c-146">因為未提供應用程式識別碼，所以會針對服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="8497c-146">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="8497c-147">由於沒有為 **Role** 參數提供任何值，因此會針對提供的資源群組範圍建立具有 **參與者** 許可權的服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-147">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

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

### <span data-ttu-id="8497c-148">範例4：使用指定的範圍和角色來建立簡單的 AD 服務主體</span><span class="sxs-lookup"><span data-stu-id="8497c-148">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="8497c-149">下列範例會使用未指定之參數的預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-149">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="8497c-150">因為未提供應用程式識別碼，所以會針對服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="8497c-150">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="8497c-151">服務主體是由所提供資源群組範圍的 **Reader** 許可權所建立。</span><span class="sxs-lookup"><span data-stu-id="8497c-151">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

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

### <span data-ttu-id="8497c-152">範例5：使用應用程式識別碼與角色指派來建立新的廣告服務主體</span><span class="sxs-lookup"><span data-stu-id="8497c-152">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="8497c-153">下列範例會在應用程式 ID 為 ' 00000000-0000-0000-0000-000000000000」的應用程式中建立新的廣告服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-153">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="8497c-154">由於沒有為 **角色** 或 **範圍** 提供任何值，已建立的服務主體會獲指派目前訂閱的 **參與者** 角色。</span><span class="sxs-lookup"><span data-stu-id="8497c-154">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="8497c-155">範例6：使用管道建立新的廣告服務主體</span><span class="sxs-lookup"><span data-stu-id="8497c-155">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="8497c-156">下列範例會使用 [AzADApplication](./get-azadapplication.md) Cmdlet 來檢索物件識別碼 為 ' 3ede3c26-b443-4e0b-9efc-b05e68338dc3」的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8497c-156">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="8497c-157">結果會以管道傳送到 `New-AzADServicePrincipal` Cmdlet，以為該應用程式建立新的廣告服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-157">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="8497c-158">範例7：使用 DisplayName 及密碼認證建立新的廣告服務主體</span><span class="sxs-lookup"><span data-stu-id="8497c-158">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="8497c-159">下列範例會使用名稱 **ServicePrincipalName** 及密碼 **StrongPassworld！ 23** 來建立新的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8497c-159">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="8497c-160">它會根據已建立的應用程式建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-160">It creates the service principal based on the created application.</span></span> <span data-ttu-id="8497c-161">[開始日期] 和 [結束日期] 會新增至密碼認證。</span><span class="sxs-lookup"><span data-stu-id="8497c-161">The start date and end date are added to the password credential.</span></span>

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

### <span data-ttu-id="8497c-162">範例8：使用 [DisplayName] 和 [普通金鑰] 認證建立新的廣告服務主體</span><span class="sxs-lookup"><span data-stu-id="8497c-162">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="8497c-163">下列範例會使用名稱 **ServicePrincipalName** 與憑證 **$cert** 建立新的應用程式。它會根據建立的應用程式來建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="8497c-163">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="8497c-164">[結束日期] 會新增到 [金鑰認證] 中。</span><span class="sxs-lookup"><span data-stu-id="8497c-164">The end date is added to key credential.</span></span>

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

## <span data-ttu-id="8497c-165">參數</span><span class="sxs-lookup"><span data-stu-id="8497c-165">PARAMETERS</span></span>

### <span data-ttu-id="8497c-166">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8497c-166">-ApplicationId</span></span>

<span data-ttu-id="8497c-167">租使用者中服務主體的唯一應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="8497c-167">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="8497c-168">建立之後，就無法變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8497c-168">Once created this property cannot be changed.</span></span> <span data-ttu-id="8497c-169">如果沒有指定現有應用程式的應用程式識別碼，就會建立一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="8497c-169">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="8497c-170">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="8497c-170">-ApplicationObject</span></span>

<span data-ttu-id="8497c-171">代表建立服務主體之應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="8497c-171">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="8497c-172">-CertValue</span><span class="sxs-lookup"><span data-stu-id="8497c-172">-CertValue</span></span>

<span data-ttu-id="8497c-173">非對稱認證類型的值。</span><span class="sxs-lookup"><span data-stu-id="8497c-173">The value of the asymmetric credential type.</span></span> <span data-ttu-id="8497c-174">它代表 Base64 編碼的憑證。</span><span class="sxs-lookup"><span data-stu-id="8497c-174">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="8497c-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8497c-175">-DefaultProfile</span></span>

<span data-ttu-id="8497c-176">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8497c-176">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8497c-177">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8497c-177">-DisplayName</span></span>

<span data-ttu-id="8497c-178">服務主體的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="8497c-178">The friendly name of the service principal.</span></span> <span data-ttu-id="8497c-179">如果未提供顯示名稱，此值會預設為 **azure--mm-yyyy-HH-HH-mm-ss** ，其中尾碼是應用程式的建立時間。</span><span class="sxs-lookup"><span data-stu-id="8497c-179">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="8497c-180">-結束日期</span><span class="sxs-lookup"><span data-stu-id="8497c-180">-EndDate</span></span>

<span data-ttu-id="8497c-181">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="8497c-181">The effective end date of the credential usage.</span></span> <span data-ttu-id="8497c-182">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="8497c-182">The default end date value is one year from today.</span></span>
<span data-ttu-id="8497c-183">針對非對稱類型認證，此狀態必須設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="8497c-183">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="8497c-184">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="8497c-184">-KeyCredential</span></span>

<span data-ttu-id="8497c-185">與應用程式相關聯的主要認證集合。</span><span class="sxs-lookup"><span data-stu-id="8497c-185">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="8497c-186">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="8497c-186">-PasswordCredential</span></span>

<span data-ttu-id="8497c-187">與應用程式相關聯的密碼認證集合。</span><span class="sxs-lookup"><span data-stu-id="8497c-187">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="8497c-188">-角色</span><span class="sxs-lookup"><span data-stu-id="8497c-188">-Role</span></span>

<span data-ttu-id="8497c-189">服務主體在範圍上擁有的角色。</span><span class="sxs-lookup"><span data-stu-id="8497c-189">The role that the service principal has over the scope.</span></span> <span data-ttu-id="8497c-190">如果未提供任何值， **角色** 預設為 [ **參與者** ] 角色。</span><span class="sxs-lookup"><span data-stu-id="8497c-190">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="8497c-191">-範圍</span><span class="sxs-lookup"><span data-stu-id="8497c-191">-Scope</span></span>

<span data-ttu-id="8497c-192">服務主體擁有許可權的範圍。</span><span class="sxs-lookup"><span data-stu-id="8497c-192">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="8497c-193">如果未提供任何值，則會將 **範圍** 預設值設為目前的訂閱。</span><span class="sxs-lookup"><span data-stu-id="8497c-193">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="8497c-194">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="8497c-194">-SkipAssignment</span></span>

<span data-ttu-id="8497c-195">如果設定，請跳過為服務主體建立預設角色指派。</span><span class="sxs-lookup"><span data-stu-id="8497c-195">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="8497c-196">-開始日期</span><span class="sxs-lookup"><span data-stu-id="8497c-196">-StartDate</span></span>

<span data-ttu-id="8497c-197">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="8497c-197">The effective start date of the credential usage.</span></span> <span data-ttu-id="8497c-198">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="8497c-198">The default start date value is today.</span></span> <span data-ttu-id="8497c-199">針對非對稱類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證生效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="8497c-199">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="8497c-200">-確認</span><span class="sxs-lookup"><span data-stu-id="8497c-200">-Confirm</span></span>

<span data-ttu-id="8497c-201">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8497c-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8497c-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8497c-202">-WhatIf</span></span>

<span data-ttu-id="8497c-203">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8497c-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8497c-204">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8497c-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8497c-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8497c-205">CommonParameters</span></span>
<span data-ttu-id="8497c-206">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8497c-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8497c-207">如需詳細資訊，請參閱 [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)。</span><span class="sxs-lookup"><span data-stu-id="8497c-207">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="8497c-208">輸入</span><span class="sxs-lookup"><span data-stu-id="8497c-208">INPUTS</span></span>

### <span data-ttu-id="8497c-209">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="8497c-209">System.Guid</span></span>

### <span data-ttu-id="8497c-210">System.object</span><span class="sxs-lookup"><span data-stu-id="8497c-210">System.String</span></span>

### <span data-ttu-id="8497c-211">PSADApplication （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="8497c-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="8497c-212">PSADPasswordCredential [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8497c-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="8497c-213">PSADKeyCredential [] （[]）</span><span class="sxs-lookup"><span data-stu-id="8497c-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="8497c-214">System.object</span><span class="sxs-lookup"><span data-stu-id="8497c-214">System.DateTime</span></span>

## <span data-ttu-id="8497c-215">輸出</span><span class="sxs-lookup"><span data-stu-id="8497c-215">OUTPUTS</span></span>

### <span data-ttu-id="8497c-216">PSADServicePrincipal （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="8497c-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="8497c-217">PSADServicePrincipalWrapper 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="8497c-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="8497c-218">筆記</span><span class="sxs-lookup"><span data-stu-id="8497c-218">NOTES</span></span>

<span data-ttu-id="8497c-219">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="8497c-219">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8497c-220">相關連結</span><span class="sxs-lookup"><span data-stu-id="8497c-220">RELATED LINKS</span></span>

[<span data-ttu-id="8497c-221">移除-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8497c-221">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="8497c-222">AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8497c-222">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="8497c-223">新-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8497c-223">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="8497c-224">移除-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8497c-224">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="8497c-225">AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8497c-225">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="8497c-226">新-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8497c-226">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="8497c-227">移除-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8497c-227">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)