---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969327"
---
# <span data-ttu-id="ed6e8-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed6e8-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="ed6e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed6e8-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6e8-103">從認知服務帳戶的 NetWorkRule 屬性移除 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="ed6e8-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="ed6e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed6e8-104">SYNTAX</span></span>

### <span data-ttu-id="ed6e8-105">NetWorkRuleString (預設) </span><span class="sxs-lookup"><span data-stu-id="ed6e8-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed6e8-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="ed6e8-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed6e8-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="ed6e8-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed6e8-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="ed6e8-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed6e8-109">說明</span><span class="sxs-lookup"><span data-stu-id="ed6e8-109">DESCRIPTION</span></span>
<span data-ttu-id="ed6e8-110">**AzCognitiveServicesAccountNetworkRule** Cmdlet 會從認知服務帳戶的 NetWorkRule 屬性中移除 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="ed6e8-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="ed6e8-111">示例</span><span class="sxs-lookup"><span data-stu-id="ed6e8-111">EXAMPLES</span></span>

### <span data-ttu-id="ed6e8-112">範例1：使用 IPAddressOrRange 移除數個 IpRules</span><span class="sxs-lookup"><span data-stu-id="ed6e8-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="ed6e8-113">這個命令會以 IPAddressOrRange 移除數個 IpRules。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="ed6e8-114">範例2：使用 JSON VirtualNetworkRule 物件輸入來移除 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed6e8-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="ed6e8-115">這個命令會移除具有 VirtualNetworkRule 物件輸入的 VirtualNetworkRule，並使用 JSON。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="ed6e8-116">範例3：移除使用管線的第一個 IpRule</span><span class="sxs-lookup"><span data-stu-id="ed6e8-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="ed6e8-117">這個命令會將第一個 IpRule 移除為管線。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="ed6e8-118">範例4：使用 VirtualNetworkResourceID 移除多個 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="ed6e8-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="ed6e8-119">這個命令會以 VirtualNetworkResourceID 移除數個 VirtualNetworkRules。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="ed6e8-120">參數</span><span class="sxs-lookup"><span data-stu-id="ed6e8-120">PARAMETERS</span></span>

### <span data-ttu-id="ed6e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed6e8-121">-DefaultProfile</span></span>
<span data-ttu-id="ed6e8-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed6e8-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ed6e8-123">-IpAddressOrRange</span></span>
<span data-ttu-id="ed6e8-124">認知服務帳戶在字串中 NetworkRule IpRules IpAddressOrRange。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed6e8-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="ed6e8-125">-IpRule</span></span>
<span data-ttu-id="ed6e8-126">認知服務帳戶 NetworkRule IpRules。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-126">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6e8-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed6e8-127">-Name</span></span>
<span data-ttu-id="ed6e8-128">認知服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="ed6e8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed6e8-129">-ResourceGroupName</span></span>
<span data-ttu-id="ed6e8-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ed6e8-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ed6e8-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="ed6e8-132">認知服務帳戶在字串中 NetworkRule VirtualNetworkRules VirtualNetworkResourceId。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed6e8-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed6e8-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="ed6e8-134">認知服務帳戶 NetworkRule VirtualNetworkRules。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6e8-135">-確認</span><span class="sxs-lookup"><span data-stu-id="ed6e8-135">-Confirm</span></span>
<span data-ttu-id="ed6e8-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed6e8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed6e8-137">-WhatIf</span></span>
<span data-ttu-id="ed6e8-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed6e8-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed6e8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6e8-140">CommonParameters</span></span>
<span data-ttu-id="ed6e8-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed6e8-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6e8-143">輸入</span><span class="sxs-lookup"><span data-stu-id="ed6e8-143">INPUTS</span></span>

### <span data-ttu-id="ed6e8-144">System.object</span><span class="sxs-lookup"><span data-stu-id="ed6e8-144">System.String</span></span>

### <span data-ttu-id="ed6e8-145">PSIpRule []. CognitiveServices. []</span><span class="sxs-lookup"><span data-stu-id="ed6e8-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="ed6e8-146">PSVirtualNetworkRule []. CognitiveServices. []</span><span class="sxs-lookup"><span data-stu-id="ed6e8-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="ed6e8-147">輸出</span><span class="sxs-lookup"><span data-stu-id="ed6e8-147">OUTPUTS</span></span>

### <span data-ttu-id="ed6e8-148">PSVirtualNetworkRule （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="ed6e8-149">PSIpRule （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="ed6e8-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="ed6e8-150">筆記</span><span class="sxs-lookup"><span data-stu-id="ed6e8-150">NOTES</span></span>

## <span data-ttu-id="ed6e8-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed6e8-151">RELATED LINKS</span></span>
