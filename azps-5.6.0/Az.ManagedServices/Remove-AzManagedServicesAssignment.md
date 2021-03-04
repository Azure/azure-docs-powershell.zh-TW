---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: f63b27c19b2ba1366b1418360a731829041f5247
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909694"
---
# <span data-ttu-id="186d7-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="186d7-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="186d7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="186d7-102">SYNOPSIS</span></span>
<span data-ttu-id="186d7-103">刪除註冊作業。</span><span class="sxs-lookup"><span data-stu-id="186d7-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="186d7-104">語法</span><span class="sxs-lookup"><span data-stu-id="186d7-104">SYNTAX</span></span>

### <span data-ttu-id="186d7-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="186d7-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [-Scope <String>] -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186d7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="186d7-106">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="186d7-107">描述</span><span class="sxs-lookup"><span data-stu-id="186d7-107">DESCRIPTION</span></span>
<span data-ttu-id="186d7-108">刪除註冊作業。</span><span class="sxs-lookup"><span data-stu-id="186d7-108">Deletes a registration assignment.</span></span>

## <span data-ttu-id="186d7-109">例子</span><span class="sxs-lookup"><span data-stu-id="186d7-109">EXAMPLES</span></span>

### <span data-ttu-id="186d7-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="186d7-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80
PS C:\>
```

<span data-ttu-id="186d7-111">刪除預設範圍中按名稱的註冊工作分派。</span><span class="sxs-lookup"><span data-stu-id="186d7-111">Deletes the registration assignment by name at the default scope.</span></span>

### <span data-ttu-id="186d7-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="186d7-112">Example 2</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 12b05f0f-3426-48da-9e67-738e1dbf775f
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
PS C:\>
```

<span data-ttu-id="186d7-113">使用提供的輸入物件刪除註冊指派。</span><span class="sxs-lookup"><span data-stu-id="186d7-113">Deletes the registration assignment using the input object provided.</span></span>

### <span data-ttu-id="186d7-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="186d7-114">Example 3</span></span>
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


PS C:\> Remove-AzManagedServicesAssignment -Name b279ec53-b42f-4952-bd62-cd49982e9572 -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8
PS C:\>
```

<span data-ttu-id="186d7-115">刪除指定範圍中按名稱的註冊作業。</span><span class="sxs-lookup"><span data-stu-id="186d7-115">Deletes the registration assignment by name at the given scope.</span></span>

## <span data-ttu-id="186d7-116">參數</span><span class="sxs-lookup"><span data-stu-id="186d7-116">PARAMETERS</span></span>

### <span data-ttu-id="186d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="186d7-117">-DefaultProfile</span></span>
<span data-ttu-id="186d7-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="186d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="186d7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="186d7-119">-InputObject</span></span>
<span data-ttu-id="186d7-120">註冊指派物件。</span><span class="sxs-lookup"><span data-stu-id="186d7-120">The registration assignment object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="186d7-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="186d7-121">-Name</span></span>
<span data-ttu-id="186d7-122">註冊作業的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="186d7-122">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186d7-123">-範圍</span><span class="sxs-lookup"><span data-stu-id="186d7-123">-Scope</span></span>
<span data-ttu-id="186d7-124">註冊作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="186d7-124">The scope of the registration assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186d7-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="186d7-125">-AsJob</span></span>
<span data-ttu-id="186d7-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="186d7-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="186d7-127">-確認</span><span class="sxs-lookup"><span data-stu-id="186d7-127">-Confirm</span></span>
<span data-ttu-id="186d7-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="186d7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="186d7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="186d7-129">-WhatIf</span></span>
<span data-ttu-id="186d7-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="186d7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="186d7-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="186d7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="186d7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186d7-132">CommonParameters</span></span>
<span data-ttu-id="186d7-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="186d7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186d7-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="186d7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186d7-135">輸入</span><span class="sxs-lookup"><span data-stu-id="186d7-135">INPUTS</span></span>

### <span data-ttu-id="186d7-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="186d7-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="186d7-137">輸出</span><span class="sxs-lookup"><span data-stu-id="186d7-137">OUTPUTS</span></span>

### <span data-ttu-id="186d7-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="186d7-138">System.Void</span></span>
## <span data-ttu-id="186d7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="186d7-139">NOTES</span></span>

## <span data-ttu-id="186d7-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="186d7-140">RELATED LINKS</span></span>
