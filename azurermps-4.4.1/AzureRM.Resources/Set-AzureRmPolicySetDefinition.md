---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: a09dae99d7a2b6e08dd255cc19b859aec89808f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449544"
---
# <span data-ttu-id="b9eb4-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b9eb4-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="b9eb4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="b9eb4-103">修改原則集定義</span><span class="sxs-lookup"><span data-stu-id="b9eb4-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9eb4-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9eb4-104">SYNTAX</span></span>

### <span data-ttu-id="b9eb4-105">已設定原則集定義名稱參數。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="b9eb4-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="b9eb4-106">(Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9eb4-107">已設定原則集定義識別碼參數。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-107">The policy set definition Id parameter set.</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9eb4-108">說明</span><span class="sxs-lookup"><span data-stu-id="b9eb4-108">DESCRIPTION</span></span>
<span data-ttu-id="b9eb4-109">**AzureRmPolicySetDefinition** Cmdlet 會修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-109">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="b9eb4-110">示例</span><span class="sxs-lookup"><span data-stu-id="b9eb4-110">EXAMPLES</span></span>

### <span data-ttu-id="b9eb4-111">範例1：更新原則集定義的描述</span><span class="sxs-lookup"><span data-stu-id="b9eb4-111">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="b9eb4-112">第一個命令會使用 Get-AzureRmPolicySetDefinition Cmdlet 來取得原則集定義。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="b9eb4-113">該命令會將該物件儲存在 $PolicySetDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-113">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="b9eb4-114">第二個命令會更新由 $PolicySetDefinition 的 **ResourceId** 屬性所識別之原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-114">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="b9eb4-115">參數</span><span class="sxs-lookup"><span data-stu-id="b9eb4-115">PARAMETERS</span></span>

### <span data-ttu-id="b9eb4-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b9eb4-116">-ApiVersion</span></span>
<span data-ttu-id="b9eb4-117">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b9eb4-118">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b9eb4-119">-描述</span><span class="sxs-lookup"><span data-stu-id="b9eb4-119">-Description</span></span>
<span data-ttu-id="b9eb4-120">原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-120">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9eb4-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b9eb4-121">-DisplayName</span></span>
<span data-ttu-id="b9eb4-122">原則集定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-122">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9eb4-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b9eb4-123">-Id</span></span>
<span data-ttu-id="b9eb4-124">完全合格的原則定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-124">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="b9eb4-125">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b9eb4-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9eb4-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9eb4-126">-Name</span></span>
<span data-ttu-id="b9eb4-127">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-127">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9eb4-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b9eb4-128">-PolicyDefinition</span></span>
<span data-ttu-id="b9eb4-129">原則集定義。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-129">The policy set definition.</span></span> <span data-ttu-id="b9eb4-130">這可以是包含原則定義的檔案名路徑，或原則集定義（字串）。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9eb4-131">-預先</span><span class="sxs-lookup"><span data-stu-id="b9eb4-131">-Pre</span></span>
<span data-ttu-id="b9eb4-132">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b9eb4-133">-確認</span><span class="sxs-lookup"><span data-stu-id="b9eb4-133">-Confirm</span></span>
<span data-ttu-id="b9eb4-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9eb4-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9eb4-135">-DefaultProfile</span></span>
<span data-ttu-id="b9eb4-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9eb4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9eb4-137">-WhatIf</span></span>
<span data-ttu-id="b9eb4-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9eb4-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9eb4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9eb4-140">CommonParameters</span></span>
<span data-ttu-id="b9eb4-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9eb4-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b9eb4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9eb4-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b9eb4-143">INPUTS</span></span>

### <span data-ttu-id="b9eb4-144">System.object</span><span class="sxs-lookup"><span data-stu-id="b9eb4-144">System.String</span></span>

## <span data-ttu-id="b9eb4-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b9eb4-145">OUTPUTS</span></span>

### <span data-ttu-id="b9eb4-146">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="b9eb4-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b9eb4-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b9eb4-147">NOTES</span></span>

## <span data-ttu-id="b9eb4-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9eb4-148">RELATED LINKS</span></span>

