---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 3174f56a0488b196dc3dc330cfa6435def73476c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620782"
---
# <span data-ttu-id="bdb4b-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="bdb4b-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="bdb4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bdb4b-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb4b-103">移除原則集定義。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="bdb4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="bdb4b-104">SYNTAX</span></span>

### <span data-ttu-id="bdb4b-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bdb4b-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdb4b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdb4b-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdb4b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdb4b-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdb4b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdb4b-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdb4b-109">說明</span><span class="sxs-lookup"><span data-stu-id="bdb4b-109">DESCRIPTION</span></span>
<span data-ttu-id="bdb4b-110">**AzPolicySetDefinition** Cmdlet 會移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-110">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="bdb4b-111">示例</span><span class="sxs-lookup"><span data-stu-id="bdb4b-111">EXAMPLES</span></span>

### <span data-ttu-id="bdb4b-112">範例1：按照資源識別碼移除原則集定義</span><span class="sxs-lookup"><span data-stu-id="bdb4b-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="bdb4b-113">第一個命令會使用 Get-AzPolicySetDefinition Cmdlet 來取得原則集定義。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="bdb4b-114">該命令會將它儲存在 $PolicySetDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="bdb4b-115">第二個命令會移除由 $PolicySetDefinition 的 **ResourceId** 屬性所識別的原則集定義。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="bdb4b-116">參數</span><span class="sxs-lookup"><span data-stu-id="bdb4b-116">PARAMETERS</span></span>

### <span data-ttu-id="bdb4b-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bdb4b-117">-ApiVersion</span></span>
<span data-ttu-id="bdb4b-118">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="bdb4b-119">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="bdb4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb4b-120">-DefaultProfile</span></span>
<span data-ttu-id="bdb4b-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bdb4b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdb4b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bdb4b-122">-Force</span></span>
<span data-ttu-id="bdb4b-123">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bdb4b-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="bdb4b-124">-Id</span></span>
<span data-ttu-id="bdb4b-125">完全限定的原則集定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="bdb4b-126">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="bdb4b-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="bdb4b-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb4b-127">-ManagementGroupName</span></span>
<span data-ttu-id="bdb4b-128">要刪除之原則集定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-128">The name of the management group of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="bdb4b-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="bdb4b-129">-Name</span></span>
<span data-ttu-id="bdb4b-130">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-130">The policy set definition name.</span></span>

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

### <span data-ttu-id="bdb4b-131">-預先</span><span class="sxs-lookup"><span data-stu-id="bdb4b-131">-Pre</span></span>
<span data-ttu-id="bdb4b-132">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bdb4b-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bdb4b-133">-SubscriptionId</span></span>
<span data-ttu-id="bdb4b-134">要刪除之原則集定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-134">The subscription ID of the policy set definition to delete.</span></span>

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

### <span data-ttu-id="bdb4b-135">-確認</span><span class="sxs-lookup"><span data-stu-id="bdb4b-135">-Confirm</span></span>
<span data-ttu-id="bdb4b-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdb4b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdb4b-137">-WhatIf</span></span>
<span data-ttu-id="bdb4b-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdb4b-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdb4b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb4b-140">CommonParameters</span></span>
<span data-ttu-id="bdb4b-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb4b-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bdb4b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb4b-143">輸入</span><span class="sxs-lookup"><span data-stu-id="bdb4b-143">INPUTS</span></span>

### <span data-ttu-id="bdb4b-144">System.object</span><span class="sxs-lookup"><span data-stu-id="bdb4b-144">System.String</span></span>

### <span data-ttu-id="bdb4b-145">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bdb4b-145">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bdb4b-146">輸出</span><span class="sxs-lookup"><span data-stu-id="bdb4b-146">OUTPUTS</span></span>

### <span data-ttu-id="bdb4b-147">System.object</span><span class="sxs-lookup"><span data-stu-id="bdb4b-147">System.Boolean</span></span>

## <span data-ttu-id="bdb4b-148">筆記</span><span class="sxs-lookup"><span data-stu-id="bdb4b-148">NOTES</span></span>

## <span data-ttu-id="bdb4b-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="bdb4b-149">RELATED LINKS</span></span>
