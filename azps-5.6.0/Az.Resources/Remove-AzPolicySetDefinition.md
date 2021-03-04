---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: e4f9164e9cfcb84ed9b8fb2051a732886ca74819
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911309"
---
# <span data-ttu-id="b59e2-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b59e2-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="b59e2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b59e2-102">SYNOPSIS</span></span>
<span data-ttu-id="b59e2-103">移除一個策略集定義。</span><span class="sxs-lookup"><span data-stu-id="b59e2-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="b59e2-104">語法</span><span class="sxs-lookup"><span data-stu-id="b59e2-104">SYNTAX</span></span>

### <span data-ttu-id="b59e2-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b59e2-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b59e2-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b59e2-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b59e2-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b59e2-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b59e2-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b59e2-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b59e2-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b59e2-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b59e2-110">描述</span><span class="sxs-lookup"><span data-stu-id="b59e2-110">DESCRIPTION</span></span>
<span data-ttu-id="b59e2-111">**Remove-AzPolicySetDefinition** Cmdlet 會移除一個策略定義。</span><span class="sxs-lookup"><span data-stu-id="b59e2-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="b59e2-112">例子</span><span class="sxs-lookup"><span data-stu-id="b59e2-112">EXAMPLES</span></span>

### <span data-ttu-id="b59e2-113">範例 1：根據資源識別碼移除策略集定義</span><span class="sxs-lookup"><span data-stu-id="b59e2-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="b59e2-114">第一個命令會使用 Cmdlet Get-AzPolicySetDefinition定義。</span><span class="sxs-lookup"><span data-stu-id="b59e2-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="b59e2-115">命令會儲存在$PolicySetDefinition變數中。</span><span class="sxs-lookup"><span data-stu-id="b59e2-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="b59e2-116">第二個命令會移除由 **resourceId** 屬性識別$PolicySetDefinition。</span><span class="sxs-lookup"><span data-stu-id="b59e2-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="b59e2-117">參數</span><span class="sxs-lookup"><span data-stu-id="b59e2-117">PARAMETERS</span></span>

### <span data-ttu-id="b59e2-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b59e2-118">-ApiVersion</span></span>
<span data-ttu-id="b59e2-119">設定時，表示要使用資源提供者 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="b59e2-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b59e2-120">如果未指定，API 版本會自動判斷為最新可用。</span><span class="sxs-lookup"><span data-stu-id="b59e2-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b59e2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b59e2-121">-DefaultProfile</span></span>
<span data-ttu-id="b59e2-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b59e2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b59e2-123">-強制</span><span class="sxs-lookup"><span data-stu-id="b59e2-123">-Force</span></span>
<span data-ttu-id="b59e2-124">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="b59e2-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b59e2-125">-Id</span><span class="sxs-lookup"><span data-stu-id="b59e2-125">-Id</span></span>
<span data-ttu-id="b59e2-126">完整規定設定定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="b59e2-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="b59e2-127">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b59e2-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59e2-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b59e2-128">-InputObject</span></span>
<span data-ttu-id="b59e2-129">此策略會設定定義物件，以移除從另一個 Cmdlet 輸出的物件。</span><span class="sxs-lookup"><span data-stu-id="b59e2-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b59e2-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b59e2-130">-ManagementGroupName</span></span>
<span data-ttu-id="b59e2-131">要刪除之組定義之管理組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b59e2-131">The name of the management group of the policy set definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59e2-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="b59e2-132">-Name</span></span>
<span data-ttu-id="b59e2-133">該策略集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="b59e2-133">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59e2-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="b59e2-134">-Pre</span></span>
<span data-ttu-id="b59e2-135">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b59e2-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b59e2-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b59e2-136">-SubscriptionId</span></span>
<span data-ttu-id="b59e2-137">要刪除之策略集定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b59e2-137">The subscription ID of the policy set definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59e2-138">-確認</span><span class="sxs-lookup"><span data-stu-id="b59e2-138">-Confirm</span></span>
<span data-ttu-id="b59e2-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b59e2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b59e2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b59e2-140">-WhatIf</span></span>
<span data-ttu-id="b59e2-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b59e2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b59e2-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b59e2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b59e2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59e2-143">CommonParameters</span></span>
<span data-ttu-id="b59e2-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b59e2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59e2-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b59e2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59e2-146">輸入</span><span class="sxs-lookup"><span data-stu-id="b59e2-146">INPUTS</span></span>

### <span data-ttu-id="b59e2-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b59e2-147">System.String</span></span>

### <span data-ttu-id="b59e2-148">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b59e2-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b59e2-149">輸出</span><span class="sxs-lookup"><span data-stu-id="b59e2-149">OUTPUTS</span></span>

### <span data-ttu-id="b59e2-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b59e2-150">System.Boolean</span></span>

## <span data-ttu-id="b59e2-151">筆記</span><span class="sxs-lookup"><span data-stu-id="b59e2-151">NOTES</span></span>

## <span data-ttu-id="b59e2-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b59e2-152">RELATED LINKS</span></span>
