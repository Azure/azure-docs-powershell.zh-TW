---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: f8d2eded01e4816b99b71475aca896c697dd5ae0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132750"
---
# <span data-ttu-id="b50bb-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="b50bb-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="b50bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b50bb-102">SYNOPSIS</span></span>
<span data-ttu-id="b50bb-103">建立或更新註冊定義。</span><span class="sxs-lookup"><span data-stu-id="b50bb-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="b50bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="b50bb-104">SYNTAX</span></span>

### <span data-ttu-id="b50bb-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="b50bb-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b50bb-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="b50bb-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b50bb-107">ByAuthorization</span><span class="sxs-lookup"><span data-stu-id="b50bb-107">ByAuthorization</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b50bb-108">說明</span><span class="sxs-lookup"><span data-stu-id="b50bb-108">DESCRIPTION</span></span>
<span data-ttu-id="b50bb-109">建立或更新註冊定義。</span><span class="sxs-lookup"><span data-stu-id="b50bb-109">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="b50bb-110">示例</span><span class="sxs-lookup"><span data-stu-id="b50bb-110">EXAMPLES</span></span>

### <span data-ttu-id="b50bb-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b50bb-111">Example 1</span></span>
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

<span data-ttu-id="b50bb-112">透過 roleDefinitionId 並直接指定的 principalId 值來建立註冊定義。</span><span class="sxs-lookup"><span data-stu-id="b50bb-112">Creates a registration definition by roleDefinitionId and principalId values given directly.</span></span>

### <span data-ttu-id="b50bb-113">範例2</span><span class="sxs-lookup"><span data-stu-id="b50bb-113">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\>
```

<span data-ttu-id="b50bb-114">使用授權詳細資料建立或更新註冊定義。</span><span class="sxs-lookup"><span data-stu-id="b50bb-114">Creates or updates a registration definition with authorization details.</span></span>

### <span data-ttu-id="b50bb-115">範例3</span><span class="sxs-lookup"><span data-stu-id="b50bb-115">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" },
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "9980e02c-c2be-4d73-94e8-173b1dc7cf3c"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7


PS C:\> $definition.Name
55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths -Name 55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7
714160ec-87d5-42bb-8b17-287c0dd7417d 9980e02c-c2be-4d73-94e8-173b1dc7cf3c

PS C:\>
```

<span data-ttu-id="b50bb-116">使用授權詳細資料和註冊定義的名稱來更新註冊定義。</span><span class="sxs-lookup"><span data-stu-id="b50bb-116">Updates a registration definition with authorization details and name of the registration definition.</span></span>

## <span data-ttu-id="b50bb-117">參數</span><span class="sxs-lookup"><span data-stu-id="b50bb-117">PARAMETERS</span></span>

### <span data-ttu-id="b50bb-118">-授權</span><span class="sxs-lookup"><span data-stu-id="b50bb-118">-Authorization</span></span>
<span data-ttu-id="b50bb-119">含 principalId-roleDefinitionId 的授權對應清單。</span><span class="sxs-lookup"><span data-stu-id="b50bb-119">The authorization mapping list with principalId - roleDefinitionId.</span></span>

```yaml
Type: Microsoft.Azure.Management.ManagedServices.Models.Authorization[]
Parameter Sets: ByPlan, ByAuthorization
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b50bb-120">-DefaultProfile</span></span>
<span data-ttu-id="b50bb-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b50bb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b50bb-122">-描述</span><span class="sxs-lookup"><span data-stu-id="b50bb-122">-Description</span></span>
<span data-ttu-id="b50bb-123">註冊定義的描述。</span><span class="sxs-lookup"><span data-stu-id="b50bb-123">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="b50bb-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b50bb-124">-DisplayName</span></span>
<span data-ttu-id="b50bb-125">註冊定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b50bb-125">The display name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50bb-126">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="b50bb-126">-ManagedByTenantId</span></span>
<span data-ttu-id="b50bb-127">ManagedBy 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="b50bb-127">The ManagedBy Tenant Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50bb-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="b50bb-128">-Name</span></span>
<span data-ttu-id="b50bb-129">註冊定義的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="b50bb-129">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="b50bb-130">-PlanName</span><span class="sxs-lookup"><span data-stu-id="b50bb-130">-PlanName</span></span>
<span data-ttu-id="b50bb-131">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="b50bb-131">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50bb-132">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="b50bb-132">-PlanProduct</span></span>
<span data-ttu-id="b50bb-133">產品名稱。</span><span class="sxs-lookup"><span data-stu-id="b50bb-133">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50bb-134">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="b50bb-134">-PlanPublisher</span></span>
<span data-ttu-id="b50bb-135">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="b50bb-135">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50bb-136">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="b50bb-136">-PlanVersion</span></span>
<span data-ttu-id="b50bb-137">方案的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="b50bb-137">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50bb-138">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="b50bb-138">-PrincipalId</span></span>
<span data-ttu-id="b50bb-139">ManagedBy 主體識別碼。</span><span class="sxs-lookup"><span data-stu-id="b50bb-139">The ManagedBy Principal Identifier.</span></span>

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

### <span data-ttu-id="b50bb-140">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b50bb-140">-RoleDefinitionId</span></span>
<span data-ttu-id="b50bb-141">角色定義識別碼，用於授與主體識別碼的許可權。</span><span class="sxs-lookup"><span data-stu-id="b50bb-141">The role definition identifier to grant permissions to principal identifier.</span></span>

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

### <span data-ttu-id="b50bb-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b50bb-142">-AsJob</span></span>
<span data-ttu-id="b50bb-143">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b50bb-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b50bb-144">-確認</span><span class="sxs-lookup"><span data-stu-id="b50bb-144">-Confirm</span></span>
<span data-ttu-id="b50bb-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b50bb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b50bb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b50bb-146">-WhatIf</span></span>
<span data-ttu-id="b50bb-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b50bb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b50bb-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b50bb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b50bb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b50bb-149">CommonParameters</span></span>
<span data-ttu-id="b50bb-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b50bb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b50bb-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b50bb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b50bb-152">輸入</span><span class="sxs-lookup"><span data-stu-id="b50bb-152">INPUTS</span></span>

### <span data-ttu-id="b50bb-153">所有</span><span class="sxs-lookup"><span data-stu-id="b50bb-153">None</span></span>
## <span data-ttu-id="b50bb-154">輸出</span><span class="sxs-lookup"><span data-stu-id="b50bb-154">OUTPUTS</span></span>

### <span data-ttu-id="b50bb-155">PSRegistrationDefinition （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="b50bb-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="b50bb-156">筆記</span><span class="sxs-lookup"><span data-stu-id="b50bb-156">NOTES</span></span>

## <span data-ttu-id="b50bb-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="b50bb-157">RELATED LINKS</span></span>
