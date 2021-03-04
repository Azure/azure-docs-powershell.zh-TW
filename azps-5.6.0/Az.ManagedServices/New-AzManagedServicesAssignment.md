---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 90ba4f3080f73207430c0751fcc4f90897507819
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904386"
---
# <span data-ttu-id="464bc-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="464bc-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="464bc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="464bc-102">SYNOPSIS</span></span>
<span data-ttu-id="464bc-103">建立或更新註冊作業。</span><span class="sxs-lookup"><span data-stu-id="464bc-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="464bc-104">語法</span><span class="sxs-lookup"><span data-stu-id="464bc-104">SYNTAX</span></span>

### <span data-ttu-id="464bc-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="464bc-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="464bc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="464bc-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="464bc-107">描述</span><span class="sxs-lookup"><span data-stu-id="464bc-107">DESCRIPTION</span></span>
<span data-ttu-id="464bc-108">建立或更新註冊作業。</span><span class="sxs-lookup"><span data-stu-id="464bc-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="464bc-109">例子</span><span class="sxs-lookup"><span data-stu-id="464bc-109">EXAMPLES</span></span>

### <span data-ttu-id="464bc-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="464bc-110">Example 1</span></span>
```
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded

PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\>
```

<span data-ttu-id="464bc-111">使用註冊定義識別碼在預設範圍中建立註冊指派。</span><span class="sxs-lookup"><span data-stu-id="464bc-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="464bc-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="464bc-112">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b279ec53-b42f-4952-bd62-cd49982e9572 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/b279ec53-b42f-4952-bd62-cd49982e9572 Succeeded


PS C:\>
```

<span data-ttu-id="464bc-113">使用註冊定義物件做為輸入來建立註冊指派。</span><span class="sxs-lookup"><span data-stu-id="464bc-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="464bc-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="464bc-114">Example 3</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded

PS C:\>
```

<span data-ttu-id="464bc-115">使用註冊定義識別碼和名稱更新註冊指派。</span><span class="sxs-lookup"><span data-stu-id="464bc-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="464bc-116">參數</span><span class="sxs-lookup"><span data-stu-id="464bc-116">PARAMETERS</span></span>

### <span data-ttu-id="464bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="464bc-117">-DefaultProfile</span></span>
<span data-ttu-id="464bc-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="464bc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="464bc-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="464bc-119">-Name</span></span>
<span data-ttu-id="464bc-120">註冊作業的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="464bc-120">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464bc-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="464bc-121">-RegistrationDefinition</span></span>
<span data-ttu-id="464bc-122">註冊定義輸入物件。</span><span class="sxs-lookup"><span data-stu-id="464bc-122">The registration definition input object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="464bc-123">-RegistrationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="464bc-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="464bc-124">註冊定義之完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="464bc-124">The fully qualified resource id of the registration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="464bc-125">-範圍</span><span class="sxs-lookup"><span data-stu-id="464bc-125">-Scope</span></span>
<span data-ttu-id="464bc-126">應建立註冊工作分派的範圍。</span><span class="sxs-lookup"><span data-stu-id="464bc-126">The scope where the registration assignment should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464bc-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="464bc-127">-AsJob</span></span>
<span data-ttu-id="464bc-128">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="464bc-128">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464bc-129">-確認</span><span class="sxs-lookup"><span data-stu-id="464bc-129">-Confirm</span></span>
<span data-ttu-id="464bc-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="464bc-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464bc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="464bc-131">-WhatIf</span></span>
<span data-ttu-id="464bc-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="464bc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="464bc-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="464bc-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464bc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="464bc-134">CommonParameters</span></span>
<span data-ttu-id="464bc-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="464bc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="464bc-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="464bc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="464bc-137">輸入</span><span class="sxs-lookup"><span data-stu-id="464bc-137">INPUTS</span></span>

### <span data-ttu-id="464bc-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="464bc-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="464bc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="464bc-139">System.String</span></span>
## <span data-ttu-id="464bc-140">輸出</span><span class="sxs-lookup"><span data-stu-id="464bc-140">OUTPUTS</span></span>

### <span data-ttu-id="464bc-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="464bc-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="464bc-142">筆記</span><span class="sxs-lookup"><span data-stu-id="464bc-142">NOTES</span></span>

## <span data-ttu-id="464bc-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="464bc-143">RELATED LINKS</span></span>
