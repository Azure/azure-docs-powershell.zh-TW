---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: bd374f19a282ccafc3201a2965c33d4e8a3007ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957702"
---
# <span data-ttu-id="0cea9-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0cea9-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="0cea9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0cea9-102">SYNOPSIS</span></span>
<span data-ttu-id="0cea9-103">移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="0cea9-103">Removes a policy definition.</span></span>

## <span data-ttu-id="0cea9-104">句法</span><span class="sxs-lookup"><span data-stu-id="0cea9-104">SYNTAX</span></span>

### <span data-ttu-id="0cea9-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0cea9-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cea9-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cea9-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cea9-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cea9-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cea9-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cea9-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cea9-109">說明</span><span class="sxs-lookup"><span data-stu-id="0cea9-109">DESCRIPTION</span></span>
<span data-ttu-id="0cea9-110">**AzPolicyDefinition** Cmdlet 會移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="0cea9-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="0cea9-111">示例</span><span class="sxs-lookup"><span data-stu-id="0cea9-111">EXAMPLES</span></span>

### <span data-ttu-id="0cea9-112">範例1：依名稱移除原則定義</span><span class="sxs-lookup"><span data-stu-id="0cea9-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="0cea9-113">這個命令會移除指定的原則定義。</span><span class="sxs-lookup"><span data-stu-id="0cea9-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="0cea9-114">範例2：依資源識別碼移除原則定義</span><span class="sxs-lookup"><span data-stu-id="0cea9-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="0cea9-115">第一個命令會使用 Get-AzPolicyDefinition Cmdlet 來取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="0cea9-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="0cea9-116">該命令會將它儲存在 $PolicyDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="0cea9-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="0cea9-117">第二個命令會移除由 $PolicyDefinition 的 **ResourceId** 屬性所識別的原則定義。</span><span class="sxs-lookup"><span data-stu-id="0cea9-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="0cea9-118">參數</span><span class="sxs-lookup"><span data-stu-id="0cea9-118">PARAMETERS</span></span>

### <span data-ttu-id="0cea9-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0cea9-119">-ApiVersion</span></span>
<span data-ttu-id="0cea9-120">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0cea9-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0cea9-121">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="0cea9-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0cea9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cea9-122">-DefaultProfile</span></span>
<span data-ttu-id="0cea9-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0cea9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cea9-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0cea9-124">-Force</span></span>
<span data-ttu-id="0cea9-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0cea9-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0cea9-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0cea9-126">-Id</span></span>
<span data-ttu-id="0cea9-127">指定此 Cmdlet 移除之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0cea9-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0cea9-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0cea9-128">-ManagementGroupName</span></span>
<span data-ttu-id="0cea9-129">要刪除之原則定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cea9-129">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="0cea9-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="0cea9-130">-Name</span></span>
<span data-ttu-id="0cea9-131">指定此 Cmdlet 移除之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cea9-131">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0cea9-132">-預先</span><span class="sxs-lookup"><span data-stu-id="0cea9-132">-Pre</span></span>
<span data-ttu-id="0cea9-133">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0cea9-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0cea9-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0cea9-134">-SubscriptionId</span></span>
<span data-ttu-id="0cea9-135">要刪除之原則定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="0cea9-135">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="0cea9-136">-確認</span><span class="sxs-lookup"><span data-stu-id="0cea9-136">-Confirm</span></span>
<span data-ttu-id="0cea9-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0cea9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cea9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cea9-138">-WhatIf</span></span>
<span data-ttu-id="0cea9-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0cea9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cea9-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0cea9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cea9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cea9-141">CommonParameters</span></span>
<span data-ttu-id="0cea9-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0cea9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cea9-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0cea9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cea9-144">輸入</span><span class="sxs-lookup"><span data-stu-id="0cea9-144">INPUTS</span></span>

### <span data-ttu-id="0cea9-145">System.object</span><span class="sxs-lookup"><span data-stu-id="0cea9-145">System.String</span></span>

### <span data-ttu-id="0cea9-146">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0cea9-146">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0cea9-147">輸出</span><span class="sxs-lookup"><span data-stu-id="0cea9-147">OUTPUTS</span></span>

### <span data-ttu-id="0cea9-148">System.object</span><span class="sxs-lookup"><span data-stu-id="0cea9-148">System.Boolean</span></span>

## <span data-ttu-id="0cea9-149">筆記</span><span class="sxs-lookup"><span data-stu-id="0cea9-149">NOTES</span></span>

## <span data-ttu-id="0cea9-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="0cea9-150">RELATED LINKS</span></span>

[<span data-ttu-id="0cea9-151">AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0cea9-151">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="0cea9-152">新-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0cea9-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="0cea9-153">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0cea9-153">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


