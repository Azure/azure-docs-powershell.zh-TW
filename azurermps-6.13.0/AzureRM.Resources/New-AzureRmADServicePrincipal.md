---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: 50f4a277461e81e26d1e553ad24f817415d5b267
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623899"
---
# <span data-ttu-id="0d91e-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0d91e-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="0d91e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d91e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d91e-103">建立新的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="0d91e-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d91e-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d91e-104">SYNTAX</span></span>

### <span data-ttu-id="0d91e-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0d91e-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d91e-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d91e-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91e-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d91e-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d91e-121">說明</span><span class="sxs-lookup"><span data-stu-id="0d91e-121">DESCRIPTION</span></span>
<span data-ttu-id="0d91e-122">建立新的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="0d91e-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="0d91e-123">如果使用者沒有提供參數的預設參數集，則它會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="0d91e-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="0d91e-124">如需使用預設值的詳細資訊，請參閱下列指定參數的描述。</span><span class="sxs-lookup"><span data-stu-id="0d91e-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="0d91e-125">這個 Cmdlet 能夠使用 and 參數將角色指派給服務主體 `Role` `Scope` ; 如果沒有提供這些參數，就不會將任何角色指派給服務主體。</span><span class="sxs-lookup"><span data-stu-id="0d91e-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="0d91e-126">與參數的預設值 `Role` `Scope` 分別是「參與者」和目前的訂閱， ( _注意_ ：只有當使用者提供其中一個參數的值，而不是其他) 時，才會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="0d91e-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="0d91e-127">如果沒有提供 ApplicationId，該 Cmdlet 也會以隱含方式建立應用程式，並將其屬性 () 。</span><span class="sxs-lookup"><span data-stu-id="0d91e-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="0d91e-128">若要更新應用程式的特定參數，請使用 Set-AzureRmADApplication Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d91e-128">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="0d91e-129">示例</span><span class="sxs-lookup"><span data-stu-id="0d91e-129">EXAMPLES</span></span>

### <span data-ttu-id="0d91e-130">範例 1-簡單的廣告服務主體建立</span><span class="sxs-lookup"><span data-stu-id="0d91e-130">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzureRmADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="0d91e-131">上述命令會使用未提供參數的預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="0d91e-131">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="0d91e-132">因為未提供應用程式識別碼，所以已為服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="0d91e-132">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="0d91e-133">由於未提供或的值 `Role` `Scope` ，因此建立的服務主體不具備任何許可權。</span><span class="sxs-lookup"><span data-stu-id="0d91e-133">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="0d91e-134">範例 2-使用指定角色和預設作用中的簡單 AD 服務主體建立</span><span class="sxs-lookup"><span data-stu-id="0d91e-134">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="0d91e-135">上述命令會使用未提供的參數預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="0d91e-135">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="0d91e-136">因為未提供應用程式識別碼，所以已為服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="0d91e-136">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="0d91e-137">由於沒有為參數) 提供任何值，因此已使用 [Reader] 許可權在目前的訂閱上建立服務主體 (`Scope` 。</span><span class="sxs-lookup"><span data-stu-id="0d91e-137">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="0d91e-138">範例 3-以指定的範圍和預設角色建立簡單的 AD 服務主體建立</span><span class="sxs-lookup"><span data-stu-id="0d91e-138">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="0d91e-139">上述命令會使用未提供的參數預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="0d91e-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="0d91e-140">因為未提供應用程式識別碼，所以已為服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="0d91e-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="0d91e-141">服務主體是由「參與者」 (許可權所建立，因為沒有為參數提供任何值， `Role`) 超出提供的資源群組範圍。</span><span class="sxs-lookup"><span data-stu-id="0d91e-141">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="0d91e-142">範例 4-使用指定範圍和角色的簡單 AD 服務主體建立</span><span class="sxs-lookup"><span data-stu-id="0d91e-142">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="0d91e-143">上述命令會使用未提供的參數預設值來建立 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="0d91e-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="0d91e-144">因為未提供應用程式識別碼，所以已為服務主體建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="0d91e-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="0d91e-145">服務主體是由提供的資源群組範圍的「Reader」許可權所建立。</span><span class="sxs-lookup"><span data-stu-id="0d91e-145">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="0d91e-146">範例 5-使用含角色指派的應用程式識別碼，建立新的廣告服務主體</span><span class="sxs-lookup"><span data-stu-id="0d91e-146">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="0d91e-147">針對應用程式 id 為 ' 34a28ad2-dec4-4a41-bc3b-d22ddf90000e」的應用程式建立新的廣告服務主體。</span><span class="sxs-lookup"><span data-stu-id="0d91e-147">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="0d91e-148">由於未提供或的值 `Role` `Scope` ，因此建立的服務主體不具備任何許可權。</span><span class="sxs-lookup"><span data-stu-id="0d91e-148">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="0d91e-149">範例 6-使用管道建立新的廣告服務主體</span><span class="sxs-lookup"><span data-stu-id="0d91e-149">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzureRmADServicePrincipal
```

<span data-ttu-id="0d91e-150">取得 3ede3c26-b443-4e0b-9efc-b05e68338dc3 Cmdlet 之物件 id 為「」和管道 New-AzureRmADServicePrincipal 的應用程式，以為該應用程式建立新的廣告服務主體。</span><span class="sxs-lookup"><span data-stu-id="0d91e-150">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzureRmADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="0d91e-151">參數</span><span class="sxs-lookup"><span data-stu-id="0d91e-151">PARAMETERS</span></span>

### <span data-ttu-id="0d91e-152">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0d91e-152">-ApplicationId</span></span>
<span data-ttu-id="0d91e-153">租使用者中服務主體的唯一應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d91e-153">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="0d91e-154">建立之後，就無法變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0d91e-154">Once created this property cannot be changed.</span></span>
<span data-ttu-id="0d91e-155">如果沒有指定應用程式識別碼，就會產生一個。</span><span class="sxs-lookup"><span data-stu-id="0d91e-155">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="0d91e-156">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="0d91e-156">-ApplicationObject</span></span>
<span data-ttu-id="0d91e-157">代表建立服務主體之應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="0d91e-157">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d91e-158">-CertValue</span><span class="sxs-lookup"><span data-stu-id="0d91e-158">-CertValue</span></span>
<span data-ttu-id="0d91e-159">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="0d91e-159">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="0d91e-160">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="0d91e-160">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="0d91e-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d91e-161">-DefaultProfile</span></span>
<span data-ttu-id="0d91e-162">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0d91e-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d91e-163">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0d91e-163">-DisplayName</span></span>
<span data-ttu-id="0d91e-164">服務主體的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="0d91e-164">The friendly name of the service principal.</span></span> <span data-ttu-id="0d91e-165">如果未提供顯示名稱，此值會預設為「azure-powershell-MM-HH-HH-mm-ss」，其中尾碼是應用程式的建立時間。</span><span class="sxs-lookup"><span data-stu-id="0d91e-165">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="0d91e-166">-結束日期</span><span class="sxs-lookup"><span data-stu-id="0d91e-166">-EndDate</span></span>
<span data-ttu-id="0d91e-167">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="0d91e-167">The effective end date of the credential usage.</span></span>
<span data-ttu-id="0d91e-168">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="0d91e-168">The default end date value is one year from today.</span></span> <span data-ttu-id="0d91e-169">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="0d91e-169">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="0d91e-170">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="0d91e-170">-KeyCredential</span></span>
<span data-ttu-id="0d91e-171">與應用程式相關聯的主要認證集合。</span><span class="sxs-lookup"><span data-stu-id="0d91e-171">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d91e-172">-Password</span><span class="sxs-lookup"><span data-stu-id="0d91e-172">-Password</span></span>
<span data-ttu-id="0d91e-173">要與服務主體相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="0d91e-173">The password to be associated with the service principal.</span></span> <span data-ttu-id="0d91e-174">如果未提供密碼，則會產生隨機 GUID 並將它當作密碼使用。</span><span class="sxs-lookup"><span data-stu-id="0d91e-174">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d91e-175">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="0d91e-175">-PasswordCredential</span></span>
<span data-ttu-id="0d91e-176">與應用程式相關聯的密碼認證集合。</span><span class="sxs-lookup"><span data-stu-id="0d91e-176">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d91e-177">-角色</span><span class="sxs-lookup"><span data-stu-id="0d91e-177">-Role</span></span>
<span data-ttu-id="0d91e-178">服務主體在範圍上擁有的角色。</span><span class="sxs-lookup"><span data-stu-id="0d91e-178">The role that the service principal has over the scope.</span></span> <span data-ttu-id="0d91e-179">如果提供的值為 `Scope` 已提供，但未提供任何值 `Role` ，則 `Role` 預設為「參與者」角色。</span><span class="sxs-lookup"><span data-stu-id="0d91e-179">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="0d91e-180">-範圍</span><span class="sxs-lookup"><span data-stu-id="0d91e-180">-Scope</span></span>
<span data-ttu-id="0d91e-181">服務主體擁有許可權的範圍。</span><span class="sxs-lookup"><span data-stu-id="0d91e-181">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="0d91e-182">如果 `Role` 已提供值，但未提供任何值 `Scope` ，則 `Scope` 會預設為目前的訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d91e-182">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="0d91e-183">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="0d91e-183">-SkipAssignment</span></span>
<span data-ttu-id="0d91e-184">如果設定，將會略過為服務主體建立預設角色指派。</span><span class="sxs-lookup"><span data-stu-id="0d91e-184">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="0d91e-185">-開始日期</span><span class="sxs-lookup"><span data-stu-id="0d91e-185">-StartDate</span></span>
<span data-ttu-id="0d91e-186">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="0d91e-186">The effective start date of the credential usage.</span></span>
<span data-ttu-id="0d91e-187">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="0d91e-187">The default start date value is today.</span></span> <span data-ttu-id="0d91e-188">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="0d91e-188">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="0d91e-189">-確認</span><span class="sxs-lookup"><span data-stu-id="0d91e-189">-Confirm</span></span>
<span data-ttu-id="0d91e-190">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d91e-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d91e-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d91e-191">-WhatIf</span></span>
<span data-ttu-id="0d91e-192">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d91e-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d91e-193">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d91e-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d91e-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d91e-194">CommonParameters</span></span>
<span data-ttu-id="0d91e-195">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d91e-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d91e-196">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d91e-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d91e-197">輸入</span><span class="sxs-lookup"><span data-stu-id="0d91e-197">INPUTS</span></span>

### <span data-ttu-id="0d91e-198">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="0d91e-198">System.Guid</span></span>

### <span data-ttu-id="0d91e-199">System.object</span><span class="sxs-lookup"><span data-stu-id="0d91e-199">System.String</span></span>

### <span data-ttu-id="0d91e-200">Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication</span><span class="sxs-lookup"><span data-stu-id="0d91e-200">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="0d91e-201">參數： ApplicationObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="0d91e-201">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="0d91e-202">PSADPasswordCredential [] Microsoft.Azure.Graph.RBAC.Version1_6</span><span class="sxs-lookup"><span data-stu-id="0d91e-202">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="0d91e-203">PSADKeyCredential [] Microsoft.Azure.Graph.RBAC.Version1_6</span><span class="sxs-lookup"><span data-stu-id="0d91e-203">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="0d91e-204">SecureString</span><span class="sxs-lookup"><span data-stu-id="0d91e-204">System.Security.SecureString</span></span>

### <span data-ttu-id="0d91e-205">System.object</span><span class="sxs-lookup"><span data-stu-id="0d91e-205">System.DateTime</span></span>

## <span data-ttu-id="0d91e-206">輸出</span><span class="sxs-lookup"><span data-stu-id="0d91e-206">OUTPUTS</span></span>

### <span data-ttu-id="0d91e-207">Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0d91e-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="0d91e-208">PSADServicePrincipalWrapper 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="0d91e-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="0d91e-209">筆記</span><span class="sxs-lookup"><span data-stu-id="0d91e-209">NOTES</span></span>
<span data-ttu-id="0d91e-210">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="0d91e-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0d91e-211">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d91e-211">RELATED LINKS</span></span>

[<span data-ttu-id="0d91e-212">移除-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0d91e-212">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="0d91e-213">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0d91e-213">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="0d91e-214">新-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0d91e-214">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="0d91e-215">移除-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0d91e-215">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="0d91e-216">AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0d91e-216">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="0d91e-217">新-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0d91e-217">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="0d91e-218">移除-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0d91e-218">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

