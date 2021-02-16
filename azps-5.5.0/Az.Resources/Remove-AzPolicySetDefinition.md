---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 551e30077fe1ce836f98c18d3c00976adc779f64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139934"
---
# <span data-ttu-id="0e0cb-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="0e0cb-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="0e0cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e0cb-102">SYNOPSIS</span></span>
<span data-ttu-id="0e0cb-103">移除原則集定義。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="0e0cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e0cb-104">SYNTAX</span></span>

### <span data-ttu-id="0e0cb-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0e0cb-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e0cb-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e0cb-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e0cb-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e0cb-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e0cb-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e0cb-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e0cb-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e0cb-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e0cb-110">說明</span><span class="sxs-lookup"><span data-stu-id="0e0cb-110">DESCRIPTION</span></span>
<span data-ttu-id="0e0cb-111">**AzPolicySetDefinition** Cmdlet 會移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="0e0cb-112">示例</span><span class="sxs-lookup"><span data-stu-id="0e0cb-112">EXAMPLES</span></span>

### <span data-ttu-id="0e0cb-113">範例1：按照資源識別碼移除原則集定義</span><span class="sxs-lookup"><span data-stu-id="0e0cb-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="0e0cb-114">第一個命令會使用 Get-AzPolicySetDefinition Cmdlet 來取得原則集定義。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="0e0cb-115">該命令會將它儲存在 $PolicySetDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="0e0cb-116">第二個命令會移除由 $PolicySetDefinition 的 **ResourceId** 屬性所識別的原則集定義。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="0e0cb-117">參數</span><span class="sxs-lookup"><span data-stu-id="0e0cb-117">PARAMETERS</span></span>

### <span data-ttu-id="0e0cb-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0e0cb-118">-ApiVersion</span></span>
<span data-ttu-id="0e0cb-119">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0e0cb-120">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0e0cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e0cb-121">-DefaultProfile</span></span>
<span data-ttu-id="0e0cb-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0e0cb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e0cb-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0e0cb-123">-Force</span></span>
<span data-ttu-id="0e0cb-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0e0cb-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0e0cb-125">-Id</span></span>
<span data-ttu-id="0e0cb-126">完全限定的原則集定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="0e0cb-127">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="0e0cb-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="0e0cb-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e0cb-128">-InputObject</span></span>
<span data-ttu-id="0e0cb-129">要移除的原則集定義物件，該物件是從另一個 Cmdlet 輸出的。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="0e0cb-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0e0cb-130">-ManagementGroupName</span></span>
<span data-ttu-id="0e0cb-131">要刪除之原則集定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-131">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="0e0cb-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e0cb-132">-Name</span></span>
<span data-ttu-id="0e0cb-133">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="0e0cb-134">-預先</span><span class="sxs-lookup"><span data-stu-id="0e0cb-134">-Pre</span></span>
<span data-ttu-id="0e0cb-135">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0e0cb-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e0cb-136">-SubscriptionId</span></span>
<span data-ttu-id="0e0cb-137">要刪除之原則集定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-137">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="0e0cb-138">-確認</span><span class="sxs-lookup"><span data-stu-id="0e0cb-138">-Confirm</span></span>
<span data-ttu-id="0e0cb-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e0cb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e0cb-140">-WhatIf</span></span>
<span data-ttu-id="0e0cb-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e0cb-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e0cb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e0cb-143">CommonParameters</span></span>
<span data-ttu-id="0e0cb-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e0cb-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0e0cb-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e0cb-146">輸入</span><span class="sxs-lookup"><span data-stu-id="0e0cb-146">INPUTS</span></span>

### <span data-ttu-id="0e0cb-147">System.object</span><span class="sxs-lookup"><span data-stu-id="0e0cb-147">System.String</span></span>

### <span data-ttu-id="0e0cb-148">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0e0cb-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0e0cb-149">輸出</span><span class="sxs-lookup"><span data-stu-id="0e0cb-149">OUTPUTS</span></span>

### <span data-ttu-id="0e0cb-150">System.object</span><span class="sxs-lookup"><span data-stu-id="0e0cb-150">System.Boolean</span></span>

## <span data-ttu-id="0e0cb-151">筆記</span><span class="sxs-lookup"><span data-stu-id="0e0cb-151">NOTES</span></span>

## <span data-ttu-id="0e0cb-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e0cb-152">RELATED LINKS</span></span>
