---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 8023dde9253ccb4a1f7ff223c4dfdddf773a4728
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132751"
---
# <span data-ttu-id="1c681-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="1c681-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="1c681-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c681-102">SYNOPSIS</span></span>
<span data-ttu-id="1c681-103">建立或更新註冊作業。</span><span class="sxs-lookup"><span data-stu-id="1c681-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="1c681-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c681-104">SYNTAX</span></span>

### <span data-ttu-id="1c681-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="1c681-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c681-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1c681-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c681-107">說明</span><span class="sxs-lookup"><span data-stu-id="1c681-107">DESCRIPTION</span></span>
<span data-ttu-id="1c681-108">建立或更新註冊作業。</span><span class="sxs-lookup"><span data-stu-id="1c681-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="1c681-109">示例</span><span class="sxs-lookup"><span data-stu-id="1c681-109">EXAMPLES</span></span>

### <span data-ttu-id="1c681-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1c681-110">Example 1</span></span>
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

<span data-ttu-id="1c681-111">使用註冊定義識別碼，在預設範圍建立註冊作業。</span><span class="sxs-lookup"><span data-stu-id="1c681-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="1c681-112">範例2</span><span class="sxs-lookup"><span data-stu-id="1c681-112">Example 2</span></span>
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

<span data-ttu-id="1c681-113">建立具有註冊定義物件作為輸入的註冊作業。</span><span class="sxs-lookup"><span data-stu-id="1c681-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="1c681-114">範例3</span><span class="sxs-lookup"><span data-stu-id="1c681-114">Example 3</span></span>
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

<span data-ttu-id="1c681-115">使用註冊定義識別碼和名稱更新註冊作業。</span><span class="sxs-lookup"><span data-stu-id="1c681-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="1c681-116">參數</span><span class="sxs-lookup"><span data-stu-id="1c681-116">PARAMETERS</span></span>

### <span data-ttu-id="1c681-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c681-117">-DefaultProfile</span></span>
<span data-ttu-id="1c681-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c681-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c681-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c681-119">-Name</span></span>
<span data-ttu-id="1c681-120">註冊作業的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="1c681-120">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="1c681-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="1c681-121">-RegistrationDefinition</span></span>
<span data-ttu-id="1c681-122">註冊定義輸入物件。</span><span class="sxs-lookup"><span data-stu-id="1c681-122">The registration definition input object.</span></span>

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

### <span data-ttu-id="1c681-123">-RegistrationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1c681-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="1c681-124">註冊定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c681-124">The fully qualified resource id of the registration definition.</span></span>

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

### <span data-ttu-id="1c681-125">-範圍</span><span class="sxs-lookup"><span data-stu-id="1c681-125">-Scope</span></span>
<span data-ttu-id="1c681-126">應建立註冊作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="1c681-126">The scope where the registration assignment should be created.</span></span>

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

### <span data-ttu-id="1c681-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c681-127">-AsJob</span></span>
<span data-ttu-id="1c681-128">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1c681-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c681-129">-確認</span><span class="sxs-lookup"><span data-stu-id="1c681-129">-Confirm</span></span>
<span data-ttu-id="1c681-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1c681-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c681-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c681-131">-WhatIf</span></span>
<span data-ttu-id="1c681-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1c681-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c681-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c681-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c681-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c681-134">CommonParameters</span></span>
<span data-ttu-id="1c681-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c681-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c681-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1c681-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c681-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1c681-137">INPUTS</span></span>

### <span data-ttu-id="1c681-138">PSRegistrationDefinition （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="1c681-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="1c681-139">System.object</span><span class="sxs-lookup"><span data-stu-id="1c681-139">System.String</span></span>
## <span data-ttu-id="1c681-140">輸出</span><span class="sxs-lookup"><span data-stu-id="1c681-140">OUTPUTS</span></span>

### <span data-ttu-id="1c681-141">PSRegistrationAssignment （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="1c681-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="1c681-142">筆記</span><span class="sxs-lookup"><span data-stu-id="1c681-142">NOTES</span></span>

## <span data-ttu-id="1c681-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c681-143">RELATED LINKS</span></span>
