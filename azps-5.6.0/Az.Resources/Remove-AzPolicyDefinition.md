---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: a65892efce36490d256c99935f6cbe8a96f5ff98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911314"
---
# <span data-ttu-id="eb604-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eb604-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="eb604-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb604-102">SYNOPSIS</span></span>
<span data-ttu-id="eb604-103">移除一個策略定義。</span><span class="sxs-lookup"><span data-stu-id="eb604-103">Removes a policy definition.</span></span>

## <span data-ttu-id="eb604-104">語法</span><span class="sxs-lookup"><span data-stu-id="eb604-104">SYNTAX</span></span>

### <span data-ttu-id="eb604-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="eb604-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb604-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb604-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb604-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb604-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb604-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb604-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb604-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb604-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb604-110">描述</span><span class="sxs-lookup"><span data-stu-id="eb604-110">DESCRIPTION</span></span>
<span data-ttu-id="eb604-111">**Remove-AzPolicyDefinition** Cmdlet 會移除一個策略定義。</span><span class="sxs-lookup"><span data-stu-id="eb604-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="eb604-112">例子</span><span class="sxs-lookup"><span data-stu-id="eb604-112">EXAMPLES</span></span>

### <span data-ttu-id="eb604-113">範例 1：根據名稱移除策略定義</span><span class="sxs-lookup"><span data-stu-id="eb604-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="eb604-114">此命令會移除指定的策略定義。</span><span class="sxs-lookup"><span data-stu-id="eb604-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="eb604-115">範例 2：根據資源識別碼移除策略定義</span><span class="sxs-lookup"><span data-stu-id="eb604-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="eb604-116">第一個命令會使用 Get-AzPolicyDefinition Cmdlet，獲得名為 VMPolicyDefinitionGet-AzPolicyDefinition定義。</span><span class="sxs-lookup"><span data-stu-id="eb604-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="eb604-117">命令會儲存在$PolicyDefinition變數中。</span><span class="sxs-lookup"><span data-stu-id="eb604-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="eb604-118">第二個命令會移除 **由 resourceId** 屬性識別$PolicyDefinition。</span><span class="sxs-lookup"><span data-stu-id="eb604-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="eb604-119">參數</span><span class="sxs-lookup"><span data-stu-id="eb604-119">PARAMETERS</span></span>

### <span data-ttu-id="eb604-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="eb604-120">-ApiVersion</span></span>
<span data-ttu-id="eb604-121">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="eb604-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="eb604-122">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="eb604-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="eb604-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb604-123">-DefaultProfile</span></span>
<span data-ttu-id="eb604-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="eb604-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb604-125">-強制</span><span class="sxs-lookup"><span data-stu-id="eb604-125">-Force</span></span>
<span data-ttu-id="eb604-126">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="eb604-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eb604-127">-Id</span><span class="sxs-lookup"><span data-stu-id="eb604-127">-Id</span></span>
<span data-ttu-id="eb604-128">指定此 Cmdlet 移除之策略定義之完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb604-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eb604-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb604-129">-InputObject</span></span>
<span data-ttu-id="eb604-130">移除來自另一個 Cmdlet 之命令定義物件。</span><span class="sxs-lookup"><span data-stu-id="eb604-130">The policy definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb604-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="eb604-131">-ManagementGroupName</span></span>
<span data-ttu-id="eb604-132">要刪除之策略定義的管理組名。</span><span class="sxs-lookup"><span data-stu-id="eb604-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="eb604-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb604-133">-Name</span></span>
<span data-ttu-id="eb604-134">指定此 Cmdlet 移除之策略定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb604-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb604-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="eb604-135">-Pre</span></span>
<span data-ttu-id="eb604-136">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="eb604-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="eb604-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb604-137">-SubscriptionId</span></span>
<span data-ttu-id="eb604-138">要刪除之策略定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb604-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="eb604-139">-確認</span><span class="sxs-lookup"><span data-stu-id="eb604-139">-Confirm</span></span>
<span data-ttu-id="eb604-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eb604-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb604-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb604-141">-WhatIf</span></span>
<span data-ttu-id="eb604-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb604-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb604-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb604-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb604-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb604-144">CommonParameters</span></span>
<span data-ttu-id="eb604-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb604-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb604-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb604-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb604-147">輸入</span><span class="sxs-lookup"><span data-stu-id="eb604-147">INPUTS</span></span>

### <span data-ttu-id="eb604-148">System.String</span><span class="sxs-lookup"><span data-stu-id="eb604-148">System.String</span></span>

### <span data-ttu-id="eb604-149">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eb604-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="eb604-150">輸出</span><span class="sxs-lookup"><span data-stu-id="eb604-150">OUTPUTS</span></span>

### <span data-ttu-id="eb604-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eb604-151">System.Boolean</span></span>

## <span data-ttu-id="eb604-152">筆記</span><span class="sxs-lookup"><span data-stu-id="eb604-152">NOTES</span></span>

## <span data-ttu-id="eb604-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb604-153">RELATED LINKS</span></span>

[<span data-ttu-id="eb604-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eb604-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="eb604-155">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eb604-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="eb604-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eb604-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


