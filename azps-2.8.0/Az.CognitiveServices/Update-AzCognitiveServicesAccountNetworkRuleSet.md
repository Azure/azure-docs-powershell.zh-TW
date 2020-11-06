---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 114163bdae16d73f490f0110186ccd43bee7d43c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613476"
---
# <span data-ttu-id="7bcc6-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7bcc6-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="7bcc6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bcc6-102">SYNOPSIS</span></span>
<span data-ttu-id="7bcc6-103">更新認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="7bcc6-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="7bcc6-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bcc6-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bcc6-105">說明</span><span class="sxs-lookup"><span data-stu-id="7bcc6-105">DESCRIPTION</span></span>
<span data-ttu-id="7bcc6-106">**AzCognitiveServicesAccountNetworkRuleSet** Cmdlet 會更新認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="7bcc6-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="7bcc6-107">示例</span><span class="sxs-lookup"><span data-stu-id="7bcc6-107">EXAMPLES</span></span>

### <span data-ttu-id="7bcc6-108">範例1：使用 JSON 更新 NetworkRule 的所有屬性、輸入規則</span><span class="sxs-lookup"><span data-stu-id="7bcc6-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="7bcc6-109">這個命令會以 JSON 更新 NetworkRule、輸入規則的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="7bcc6-110">範例2： NetworkRule 的更新旁路屬性</span><span class="sxs-lookup"><span data-stu-id="7bcc6-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="7bcc6-111">此命令會更新 NetworkRule 的旁路屬性 (其他屬性不會變更) 。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="7bcc6-112">範例3：清除認知服務帳戶 NetworkRule 的規則</span><span class="sxs-lookup"><span data-stu-id="7bcc6-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="7bcc6-113">這個命令會清理 NetworkRule 的認知服務帳戶規則， (其他屬性不會變更) 。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="7bcc6-114">參數</span><span class="sxs-lookup"><span data-stu-id="7bcc6-114">PARAMETERS</span></span>

### <span data-ttu-id="7bcc6-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="7bcc6-115">-DefaultAction</span></span>
<span data-ttu-id="7bcc6-116">認知服務帳戶 NetworkRule DefaultAction。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-116">Cognitive Services Account NetworkRule DefaultAction.</span></span>

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

### <span data-ttu-id="7bcc6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bcc6-117">-DefaultProfile</span></span>
<span data-ttu-id="7bcc6-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bcc6-119">-IpRule</span><span class="sxs-lookup"><span data-stu-id="7bcc6-119">-IpRule</span></span>
<span data-ttu-id="7bcc6-120">認知服務帳戶 NetworkRule IpRules。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-120">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="7bcc6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7bcc6-121">-Name</span></span>
<span data-ttu-id="7bcc6-122">認知服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-122">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="7bcc6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bcc6-123">-ResourceGroupName</span></span>
<span data-ttu-id="7bcc6-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="7bcc6-125">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7bcc6-125">-VirtualNetworkRule</span></span>
<span data-ttu-id="7bcc6-126">認知服務帳戶 NetworkRule VirtualNetworkRules。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-126">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="7bcc6-127">-確認</span><span class="sxs-lookup"><span data-stu-id="7bcc6-127">-Confirm</span></span>
<span data-ttu-id="7bcc6-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bcc6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bcc6-129">-WhatIf</span></span>
<span data-ttu-id="7bcc6-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bcc6-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bcc6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bcc6-132">CommonParameters</span></span>
<span data-ttu-id="7bcc6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bcc6-134">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bcc6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="7bcc6-135">INPUTS</span></span>

### <span data-ttu-id="7bcc6-136">System.object</span><span class="sxs-lookup"><span data-stu-id="7bcc6-136">System.String</span></span>

### <span data-ttu-id="7bcc6-137">PSIpRule []. CognitiveServices. []</span><span class="sxs-lookup"><span data-stu-id="7bcc6-137">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="7bcc6-138">PSVirtualNetworkRule []. CognitiveServices. []</span><span class="sxs-lookup"><span data-stu-id="7bcc6-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="7bcc6-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7bcc6-139">OUTPUTS</span></span>

### <span data-ttu-id="7bcc6-140">PSNetworkRuleSet （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="7bcc6-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="7bcc6-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7bcc6-141">NOTES</span></span>

## <span data-ttu-id="7bcc6-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bcc6-142">RELATED LINKS</span></span>