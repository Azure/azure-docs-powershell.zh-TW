---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 4c5cd8caef4499d8d603b1947c1fa1dd8a9d5cf6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908318"
---
# <span data-ttu-id="4982f-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4982f-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="4982f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4982f-102">SYNOPSIS</span></span>
<span data-ttu-id="4982f-103">更新認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="4982f-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="4982f-104">語法</span><span class="sxs-lookup"><span data-stu-id="4982f-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4982f-105">描述</span><span class="sxs-lookup"><span data-stu-id="4982f-105">DESCRIPTION</span></span>
<span data-ttu-id="4982f-106">**Update-AzCognitiveServicesAccountNetworkRuleSet** Cmdlet 會更新認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="4982f-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="4982f-107">例子</span><span class="sxs-lookup"><span data-stu-id="4982f-107">EXAMPLES</span></span>

### <span data-ttu-id="4982f-108">範例 1：更新 NetworkRule 的所有屬性，使用 JSON 輸入規則</span><span class="sxs-lookup"><span data-stu-id="4982f-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="4982f-109">此命令會更新 NetworkRule 的所有屬性，以及使用 JSON 輸入規則。</span><span class="sxs-lookup"><span data-stu-id="4982f-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="4982f-110">範例 2：NetworkRule 的更新旁路屬性</span><span class="sxs-lookup"><span data-stu-id="4982f-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="4982f-111">此命令更新 NetworkRule 的 Bypass 屬性 (不會變更其他屬性) 。</span><span class="sxs-lookup"><span data-stu-id="4982f-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="4982f-112">範例 3：清理認知服務帳戶的 NetworkRule 規則</span><span class="sxs-lookup"><span data-stu-id="4982f-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="4982f-113">此命令會清除認知服務帳戶的 NetworkRule 規則， (不會變更) 。</span><span class="sxs-lookup"><span data-stu-id="4982f-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="4982f-114">參數</span><span class="sxs-lookup"><span data-stu-id="4982f-114">PARAMETERS</span></span>

### <span data-ttu-id="4982f-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="4982f-115">-DefaultAction</span></span>
<span data-ttu-id="4982f-116">認知服務帳戶 NetworkRule DefaultAction。</span><span class="sxs-lookup"><span data-stu-id="4982f-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="4982f-117">預設值 `Deny` 。</span><span class="sxs-lookup"><span data-stu-id="4982f-117">Default value `Deny`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4982f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4982f-118">-DefaultProfile</span></span>
<span data-ttu-id="4982f-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4982f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4982f-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="4982f-120">-IpRule</span></span>
<span data-ttu-id="4982f-121">認知服務帳戶 NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="4982f-121">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4982f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4982f-122">-Name</span></span>
<span data-ttu-id="4982f-123">認知服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4982f-123">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4982f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4982f-124">-ResourceGroupName</span></span>
<span data-ttu-id="4982f-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4982f-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4982f-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4982f-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="4982f-127">認知服務帳戶 NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="4982f-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4982f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="4982f-128">-Confirm</span></span>
<span data-ttu-id="4982f-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4982f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4982f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4982f-130">-WhatIf</span></span>
<span data-ttu-id="4982f-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4982f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4982f-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4982f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4982f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4982f-133">CommonParameters</span></span>
<span data-ttu-id="4982f-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4982f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4982f-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4982f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4982f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4982f-136">INPUTS</span></span>

### <span data-ttu-id="4982f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4982f-137">System.String</span></span>

### <span data-ttu-id="4982f-138">Microsoft.Azure.Commands.management.CognitiveServices.models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="4982f-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="4982f-139">Microsoft.Azure.Commands.management.CognitiveServices.models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="4982f-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="4982f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="4982f-140">OUTPUTS</span></span>

### <span data-ttu-id="4982f-141">Microsoft.Azure.Commands.management.CognitiveServices.models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4982f-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="4982f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4982f-142">NOTES</span></span>

## <span data-ttu-id="4982f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="4982f-143">RELATED LINKS</span></span>
