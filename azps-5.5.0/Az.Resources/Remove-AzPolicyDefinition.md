---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: c7d292a983090d8be22e159fbca6e423778b21f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128398"
---
# <span data-ttu-id="f97ea-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f97ea-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="f97ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f97ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f97ea-103">移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="f97ea-103">Removes a policy definition.</span></span>

## <span data-ttu-id="f97ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="f97ea-104">SYNTAX</span></span>

### <span data-ttu-id="f97ea-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f97ea-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f97ea-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f97ea-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f97ea-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f97ea-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f97ea-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f97ea-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f97ea-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f97ea-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f97ea-110">說明</span><span class="sxs-lookup"><span data-stu-id="f97ea-110">DESCRIPTION</span></span>
<span data-ttu-id="f97ea-111">**AzPolicyDefinition** Cmdlet 會移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="f97ea-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="f97ea-112">示例</span><span class="sxs-lookup"><span data-stu-id="f97ea-112">EXAMPLES</span></span>

### <span data-ttu-id="f97ea-113">範例1：依名稱移除原則定義</span><span class="sxs-lookup"><span data-stu-id="f97ea-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="f97ea-114">這個命令會移除指定的原則定義。</span><span class="sxs-lookup"><span data-stu-id="f97ea-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="f97ea-115">範例2：依資源識別碼移除原則定義</span><span class="sxs-lookup"><span data-stu-id="f97ea-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="f97ea-116">第一個命令會使用 Get-AzPolicyDefinition Cmdlet 來取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="f97ea-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="f97ea-117">該命令會將它儲存在 $PolicyDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="f97ea-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="f97ea-118">第二個命令會移除由 $PolicyDefinition 的 **ResourceId** 屬性所識別的原則定義。</span><span class="sxs-lookup"><span data-stu-id="f97ea-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="f97ea-119">參數</span><span class="sxs-lookup"><span data-stu-id="f97ea-119">PARAMETERS</span></span>

### <span data-ttu-id="f97ea-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f97ea-120">-ApiVersion</span></span>
<span data-ttu-id="f97ea-121">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f97ea-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f97ea-122">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="f97ea-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f97ea-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f97ea-123">-DefaultProfile</span></span>
<span data-ttu-id="f97ea-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f97ea-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f97ea-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f97ea-125">-Force</span></span>
<span data-ttu-id="f97ea-126">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f97ea-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f97ea-127">-識別碼</span><span class="sxs-lookup"><span data-stu-id="f97ea-127">-Id</span></span>
<span data-ttu-id="f97ea-128">指定此 Cmdlet 移除之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f97ea-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f97ea-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f97ea-129">-InputObject</span></span>
<span data-ttu-id="f97ea-130">要移除的原則定義物件是從另一個 Cmdlet 輸出的。</span><span class="sxs-lookup"><span data-stu-id="f97ea-130">The policy definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="f97ea-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f97ea-131">-ManagementGroupName</span></span>
<span data-ttu-id="f97ea-132">要刪除之原則定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f97ea-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="f97ea-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="f97ea-133">-Name</span></span>
<span data-ttu-id="f97ea-134">指定此 Cmdlet 移除之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="f97ea-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f97ea-135">-預先</span><span class="sxs-lookup"><span data-stu-id="f97ea-135">-Pre</span></span>
<span data-ttu-id="f97ea-136">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f97ea-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f97ea-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f97ea-137">-SubscriptionId</span></span>
<span data-ttu-id="f97ea-138">要刪除之原則定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f97ea-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="f97ea-139">-確認</span><span class="sxs-lookup"><span data-stu-id="f97ea-139">-Confirm</span></span>
<span data-ttu-id="f97ea-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f97ea-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f97ea-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f97ea-141">-WhatIf</span></span>
<span data-ttu-id="f97ea-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f97ea-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f97ea-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f97ea-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f97ea-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97ea-144">CommonParameters</span></span>
<span data-ttu-id="f97ea-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f97ea-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97ea-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f97ea-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97ea-147">輸入</span><span class="sxs-lookup"><span data-stu-id="f97ea-147">INPUTS</span></span>

### <span data-ttu-id="f97ea-148">System.object</span><span class="sxs-lookup"><span data-stu-id="f97ea-148">System.String</span></span>

### <span data-ttu-id="f97ea-149">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f97ea-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f97ea-150">輸出</span><span class="sxs-lookup"><span data-stu-id="f97ea-150">OUTPUTS</span></span>

### <span data-ttu-id="f97ea-151">System.object</span><span class="sxs-lookup"><span data-stu-id="f97ea-151">System.Boolean</span></span>

## <span data-ttu-id="f97ea-152">筆記</span><span class="sxs-lookup"><span data-stu-id="f97ea-152">NOTES</span></span>

## <span data-ttu-id="f97ea-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="f97ea-153">RELATED LINKS</span></span>

[<span data-ttu-id="f97ea-154">AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f97ea-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="f97ea-155">新-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f97ea-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="f97ea-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f97ea-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


