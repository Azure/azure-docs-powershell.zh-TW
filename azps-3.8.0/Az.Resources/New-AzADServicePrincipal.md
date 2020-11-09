---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: f921cceb3692032f61f99db825efeea074773faa
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/05/2020
ms.locfileid: "94288468"
---
# <span data-ttu-id="1465d-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1465d-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="1465d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1465d-102">SYNOPSIS</span></span>
<span data-ttu-id="1465d-103">建立新的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1465d-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="1465d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1465d-104">SYNTAX</span></span>

### <span data-ttu-id="1465d-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1465d-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1465d-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1465d-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1465d-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1465d-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1465d-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1465d-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1465d-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1465d-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1465d-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1465d-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1465d-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1465d-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1465d-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-118">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1465d-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="1465d-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1465d-120">說明</span><span class="sxs-lookup"><span data-stu-id="1465d-120">DESCRIPTION</span></span>
<span data-ttu-id="1465d-121">建立新的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1465d-121">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="1465d-122">如果使用者沒有提供參數的預設參數集，則它會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="1465d-122">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="1465d-123">如需使用預設值的詳細資訊，請參閱下列指定參數的描述。</span><span class="sxs-lookup"><span data-stu-id="1465d-123">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="1465d-124">這個 Cmdlet 能夠使用 and 參數將角色指派給服務主體 `Role` `Scope` ; 如果沒有提供這些參數，就不會將任何角色指派給服務主體。</span><span class="sxs-lookup"><span data-stu-id="1465d-124">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="1465d-125">與參數的預設值 `Role` `Scope` 分別是「參與者」和目前的訂閱， ( _注意_ ：只有當使用者提供其中一個參數的值，而不是其他) 時，才會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="1465d-125">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="1465d-126">如果沒有提供 ApplicationId，該 Cmdlet 也會以隱含方式建立應用程式，並將其屬性 () 。</span><span class="sxs-lookup"><span data-stu-id="1465d-126">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="1465d-127">若要更新應用程式的特定參數，請使用 Set-AzADApplication Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1465d-127">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="1465d-128">當您使用 **新的-AzADServicePrincipal** 命令建立服務主體時，輸出會包含您必須受到保護的認證。</span><span class="sxs-lookup"><span data-stu-id="1465d-128">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="1465d-129">請確定您的程式碼中不包含這些認證，或者請將認證核取到您的來源控制中。</span><span class="sxs-lookup"><span data-stu-id="1465d-129">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="1465d-130">或者，請考慮使用 [受管理](/azure/active-directory/managed-identities-azure-resources/overview) 的身分識別，以避免需要使用認證。</span><span class="sxs-lookup"><span data-stu-id="1465d-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="1465d-131">根據預設， **新-AzADServicePrincipal** 會將 [參與者](/azure/role-based-access-control/built-in-roles#contributor) 角色指派給訂閱範圍中的服務主體。</span><span class="sxs-lookup"><span data-stu-id="1465d-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="1465d-132">若要降低受到危害的服務主體的風險，請指派更明確的角色，並將範圍縮小至資源或資源群組。</span><span class="sxs-lookup"><span data-stu-id="1465d-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="1465d-133">如需詳細資訊，請參閱 [新增角色分派的步驟](/azure/role-based-access-control/role-assignments-steps) 。</span><span class="sxs-lookup"><span data-stu-id="1465d-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="1465d-134">示例</span><span class="sxs-lookup"><span data-stu-id="1465d-134">EXAMPLES</span></span>

### <span data-ttu-id="1465d-135">範例 1-簡單的廣告服務主體建立</span><span class="sxs-lookup"><span data-stu-id="1465d-135">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="1465d-136">上述命令會使用未提供參數的預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1465d-136">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="1465d-137">因為未提供應用程式識別碼，所以已為服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="1465d-137">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="1465d-138">由於未提供或的值 `Role` `Scope` ，因此建立的服務主體不具備任何許可權。</span><span class="sxs-lookup"><span data-stu-id="1465d-138">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="1465d-139">範例 2-使用指定角色和預設作用中的簡單 AD 服務主體建立</span><span class="sxs-lookup"><span data-stu-id="1465d-139">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="1465d-140">上述命令會使用未提供的參數預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1465d-140">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="1465d-141">因為未提供應用程式識別碼，所以已為服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="1465d-141">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="1465d-142">由於沒有為參數) 提供任何值，因此已使用 [Reader] 許可權在目前的訂閱上建立服務主體 (`Scope` 。</span><span class="sxs-lookup"><span data-stu-id="1465d-142">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="1465d-143">範例 3-以指定的範圍和預設角色建立簡單的 AD 服務主體建立</span><span class="sxs-lookup"><span data-stu-id="1465d-143">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="1465d-144">上述命令會使用未提供的參數預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1465d-144">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="1465d-145">因為未提供應用程式識別碼，所以已為服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="1465d-145">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="1465d-146">服務主體是由「參與者」 (許可權所建立，因為沒有為參數提供任何值， `Role`) 超出提供的資源群組範圍。</span><span class="sxs-lookup"><span data-stu-id="1465d-146">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="1465d-147">範例 4-使用指定範圍和角色的簡單 AD 服務主體建立</span><span class="sxs-lookup"><span data-stu-id="1465d-147">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="1465d-148">上述命令會使用未提供的參數預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="1465d-148">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="1465d-149">因為未提供應用程式識別碼，所以已為服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="1465d-149">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="1465d-150">服務主體是由提供的資源群組範圍的「Reader」許可權所建立。</span><span class="sxs-lookup"><span data-stu-id="1465d-150">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="1465d-151">範例 5-使用含角色指派的應用程式識別碼，建立新的廣告服務主體</span><span class="sxs-lookup"><span data-stu-id="1465d-151">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="1465d-152">針對應用程式 id 為 ' 34a28ad2-dec4-4a41-bc3b-d22ddf90000e」的應用程式建立新的廣告服務主體。</span><span class="sxs-lookup"><span data-stu-id="1465d-152">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="1465d-153">由於未提供或的值 `Role` `Scope` ，因此建立的服務主體不具備任何許可權。</span><span class="sxs-lookup"><span data-stu-id="1465d-153">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="1465d-154">範例 6-使用管道建立新的廣告服務主體</span><span class="sxs-lookup"><span data-stu-id="1465d-154">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="1465d-155">取得 3ede3c26-b443-4e0b-9efc-b05e68338dc3 Cmdlet 之物件 id 為「」和管道 New-AzADServicePrincipal 的應用程式，以為該應用程式建立新的廣告服務主體。</span><span class="sxs-lookup"><span data-stu-id="1465d-155">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

### <span data-ttu-id="1465d-156">範例 7-使用 DisplayName 及密碼認證建立新的廣告服務主體</span><span class="sxs-lookup"><span data-stu-id="1465d-156">Example 7 - Create a new AD service principal using DisplayName and password credential</span></span>

```
PS C:\> $credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password="StrongPassworld!23"}
PS C:\> $sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials

ServicePrincipalNames : {exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc, http://ServicePrincipalName}
ApplicationId         : exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxcc
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 6xxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxb
Type                  :
```

<span data-ttu-id="1465d-157">建立名為 "ServicePrincipalName" 且密碼為 "StrongPassworld！ 23" 的新應用程式，並根據剛剛建立的應用程式建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="1465d-157">Creates a new application with name "ServicePrincipalName" and password "StrongPassworld!23" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="1465d-158">[開始日期] 和 [結束日期] 會新增至 [密碼認證]。</span><span class="sxs-lookup"><span data-stu-id="1465d-158">The start date and end date are added to password credential.</span></span>

### <span data-ttu-id="1465d-159">範例 8-使用 DisplayName 和 [一般] 金鑰認證建立新的廣告服務主體</span><span class="sxs-lookup"><span data-stu-id="1465d-159">Example 8 - Create a new AD service principal using DisplayName and plain key credential</span></span>

```
PS C:\> $cert = <public certificate as base64-encoded string>
PS C:\> $sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate "2021-01-01"

ServicePrincipalNames : {cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6, http://ServicePrincipalName}
ApplicationId         : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc
Type                  :
```

<span data-ttu-id="1465d-160">建立名為 "ServicePrincipalName" 的新應用程式，並 certifcate "$cert"，並根據剛建立的應用程式建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="1465d-160">Creates a new application with name "ServicePrincipalName" and certifcate "$cert" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="1465d-161">[結束日期] 會新增到 [金鑰認證] 中。</span><span class="sxs-lookup"><span data-stu-id="1465d-161">The end date is added to key credential.</span></span>

## <span data-ttu-id="1465d-162">參數</span><span class="sxs-lookup"><span data-stu-id="1465d-162">PARAMETERS</span></span>

### <span data-ttu-id="1465d-163">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1465d-163">-ApplicationId</span></span>
<span data-ttu-id="1465d-164">租使用者中服務主體的唯一應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="1465d-164">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="1465d-165">建立之後，就無法變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1465d-165">Once created this property cannot be changed.</span></span>
<span data-ttu-id="1465d-166">如果沒有指定應用程式識別碼，就會產生一個。</span><span class="sxs-lookup"><span data-stu-id="1465d-166">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="1465d-167">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="1465d-167">-ApplicationObject</span></span>
<span data-ttu-id="1465d-168">代表建立服務主體之應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="1465d-168">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="1465d-169">-CertValue</span><span class="sxs-lookup"><span data-stu-id="1465d-169">-CertValue</span></span>
<span data-ttu-id="1465d-170">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="1465d-170">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="1465d-171">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="1465d-171">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="1465d-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1465d-172">-DefaultProfile</span></span>
<span data-ttu-id="1465d-173">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1465d-173">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1465d-174">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1465d-174">-DisplayName</span></span>
<span data-ttu-id="1465d-175">服務主體的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="1465d-175">The friendly name of the service principal.</span></span> <span data-ttu-id="1465d-176">如果未提供顯示名稱，此值會預設為「azure-powershell-MM-HH-HH-mm-ss」，其中尾碼是應用程式的建立時間。</span><span class="sxs-lookup"><span data-stu-id="1465d-176">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="1465d-177">-結束日期</span><span class="sxs-lookup"><span data-stu-id="1465d-177">-EndDate</span></span>
<span data-ttu-id="1465d-178">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="1465d-178">The effective end date of the credential usage.</span></span>
<span data-ttu-id="1465d-179">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="1465d-179">The default end date value is one year from today.</span></span> <span data-ttu-id="1465d-180">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="1465d-180">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="1465d-181">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="1465d-181">-KeyCredential</span></span>
<span data-ttu-id="1465d-182">與應用程式相關聯的主要認證集合。</span><span class="sxs-lookup"><span data-stu-id="1465d-182">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="1465d-183">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="1465d-183">-PasswordCredential</span></span>
<span data-ttu-id="1465d-184">與應用程式相關聯的密碼認證集合。</span><span class="sxs-lookup"><span data-stu-id="1465d-184">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="1465d-185">-角色</span><span class="sxs-lookup"><span data-stu-id="1465d-185">-Role</span></span>
<span data-ttu-id="1465d-186">服務主體在範圍上擁有的角色。</span><span class="sxs-lookup"><span data-stu-id="1465d-186">The role that the service principal has over the scope.</span></span> <span data-ttu-id="1465d-187">如果提供的值為 `Scope` 已提供，但未提供任何值 `Role` ，則 `Role` 預設為「參與者」角色。</span><span class="sxs-lookup"><span data-stu-id="1465d-187">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="1465d-188">-範圍</span><span class="sxs-lookup"><span data-stu-id="1465d-188">-Scope</span></span>
<span data-ttu-id="1465d-189">服務主體擁有許可權的範圍。</span><span class="sxs-lookup"><span data-stu-id="1465d-189">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="1465d-190">如果 `Role` 已提供值，但未提供任何值 `Scope` ，則 `Scope` 會預設為目前的訂閱。</span><span class="sxs-lookup"><span data-stu-id="1465d-190">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="1465d-191">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="1465d-191">-SkipAssignment</span></span>
<span data-ttu-id="1465d-192">如果設定，將會略過為服務主體建立預設角色指派。</span><span class="sxs-lookup"><span data-stu-id="1465d-192">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="1465d-193">-開始日期</span><span class="sxs-lookup"><span data-stu-id="1465d-193">-StartDate</span></span>
<span data-ttu-id="1465d-194">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="1465d-194">The effective start date of the credential usage.</span></span>
<span data-ttu-id="1465d-195">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="1465d-195">The default start date value is today.</span></span> <span data-ttu-id="1465d-196">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="1465d-196">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="1465d-197">-確認</span><span class="sxs-lookup"><span data-stu-id="1465d-197">-Confirm</span></span>
<span data-ttu-id="1465d-198">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1465d-198">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1465d-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1465d-199">-WhatIf</span></span>
<span data-ttu-id="1465d-200">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1465d-200">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1465d-201">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1465d-201">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1465d-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1465d-202">CommonParameters</span></span>
<span data-ttu-id="1465d-203">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1465d-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1465d-204">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1465d-204">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1465d-205">輸入</span><span class="sxs-lookup"><span data-stu-id="1465d-205">INPUTS</span></span>

### <span data-ttu-id="1465d-206">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="1465d-206">System.Guid</span></span>

### <span data-ttu-id="1465d-207">System.object</span><span class="sxs-lookup"><span data-stu-id="1465d-207">System.String</span></span>

### <span data-ttu-id="1465d-208">PSADApplication （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="1465d-208">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="1465d-209">PSADPasswordCredential [] （[]）</span><span class="sxs-lookup"><span data-stu-id="1465d-209">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="1465d-210">PSADKeyCredential [] （[]）</span><span class="sxs-lookup"><span data-stu-id="1465d-210">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="1465d-211">System.object</span><span class="sxs-lookup"><span data-stu-id="1465d-211">System.DateTime</span></span>

## <span data-ttu-id="1465d-212">輸出</span><span class="sxs-lookup"><span data-stu-id="1465d-212">OUTPUTS</span></span>

### <span data-ttu-id="1465d-213">PSADServicePrincipal （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="1465d-213">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="1465d-214">PSADServicePrincipalWrapper 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="1465d-214">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="1465d-215">筆記</span><span class="sxs-lookup"><span data-stu-id="1465d-215">NOTES</span></span>
<span data-ttu-id="1465d-216">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="1465d-216">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1465d-217">相關連結</span><span class="sxs-lookup"><span data-stu-id="1465d-217">RELATED LINKS</span></span>

[<span data-ttu-id="1465d-218">移除-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1465d-218">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="1465d-219">AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1465d-219">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="1465d-220">新-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1465d-220">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="1465d-221">移除-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="1465d-221">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="1465d-222">AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1465d-222">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="1465d-223">新-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1465d-223">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="1465d-224">移除-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1465d-224">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

