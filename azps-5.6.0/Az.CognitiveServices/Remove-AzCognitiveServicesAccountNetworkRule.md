---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 0b50a6b7d7dd3b762f00b292e421f981dddd3740
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906321"
---
# <span data-ttu-id="643d3-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="643d3-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="643d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="643d3-102">SYNOPSIS</span></span>
<span data-ttu-id="643d3-103">從認知服務帳戶的 NetWorkRule 屬性移除 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="643d3-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="643d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="643d3-104">SYNTAX</span></span>

### <span data-ttu-id="643d3-105">NetWorkRuleString (預設) </span><span class="sxs-lookup"><span data-stu-id="643d3-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="643d3-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="643d3-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="643d3-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="643d3-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="643d3-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="643d3-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="643d3-109">描述</span><span class="sxs-lookup"><span data-stu-id="643d3-109">DESCRIPTION</span></span>
<span data-ttu-id="643d3-110">**Remove-AzCognitiveServicesAccountNetworkRule** Cmdlet 會從認知服務帳戶的 NetWorkRule 屬性移除 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="643d3-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="643d3-111">例子</span><span class="sxs-lookup"><span data-stu-id="643d3-111">EXAMPLES</span></span>

### <span data-ttu-id="643d3-112">範例 1：使用 IPAddressOrRange 移除多個 IpRules</span><span class="sxs-lookup"><span data-stu-id="643d3-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="643d3-113">此命令會使用 IPAddressOrRange 移除多個 IpRules。</span><span class="sxs-lookup"><span data-stu-id="643d3-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="643d3-114">範例 2：使用 JSON 移除 VirtualNetworkRule 與 VirtualNetworkRule 物件輸入</span><span class="sxs-lookup"><span data-stu-id="643d3-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="643d3-115">此命令會移除 VirtualNetworkRule 與 VirtualNetworkRule 物件輸入 JSON。</span><span class="sxs-lookup"><span data-stu-id="643d3-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="643d3-116">範例 3：使用管線移除第一個 IpRule</span><span class="sxs-lookup"><span data-stu-id="643d3-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="643d3-117">此命令會移除第一個具有管線的 IpRule。</span><span class="sxs-lookup"><span data-stu-id="643d3-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="643d3-118">範例 4：使用 VirtualNetworkResourceID 移除多個 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="643d3-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="643d3-119">此命令會使用 VirtualNetworkResourceID 移除多個 VirtualNetworkRules。</span><span class="sxs-lookup"><span data-stu-id="643d3-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="643d3-120">參數</span><span class="sxs-lookup"><span data-stu-id="643d3-120">PARAMETERS</span></span>

### <span data-ttu-id="643d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643d3-121">-DefaultProfile</span></span>
<span data-ttu-id="643d3-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="643d3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="643d3-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="643d3-123">-IpAddressOrRange</span></span>
<span data-ttu-id="643d3-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span><span class="sxs-lookup"><span data-stu-id="643d3-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="643d3-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="643d3-125">-IpRule</span></span>
<span data-ttu-id="643d3-126">認知服務帳戶 NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="643d3-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="643d3-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="643d3-127">-Name</span></span>
<span data-ttu-id="643d3-128">認知服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="643d3-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="643d3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="643d3-129">-ResourceGroupName</span></span>
<span data-ttu-id="643d3-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="643d3-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="643d3-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="643d3-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="643d3-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span><span class="sxs-lookup"><span data-stu-id="643d3-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="643d3-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="643d3-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="643d3-134">認知服務帳戶 NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="643d3-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="643d3-135">-確認</span><span class="sxs-lookup"><span data-stu-id="643d3-135">-Confirm</span></span>
<span data-ttu-id="643d3-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="643d3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="643d3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="643d3-137">-WhatIf</span></span>
<span data-ttu-id="643d3-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="643d3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="643d3-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="643d3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="643d3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643d3-140">CommonParameters</span></span>
<span data-ttu-id="643d3-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="643d3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643d3-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="643d3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643d3-143">輸入</span><span class="sxs-lookup"><span data-stu-id="643d3-143">INPUTS</span></span>

### <span data-ttu-id="643d3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="643d3-144">System.String</span></span>

### <span data-ttu-id="643d3-145">Microsoft.Azure.Commands.management.CognitiveServices.models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="643d3-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="643d3-146">Microsoft.Azure.Commands.management.CognitiveServices.models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="643d3-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="643d3-147">輸出</span><span class="sxs-lookup"><span data-stu-id="643d3-147">OUTPUTS</span></span>

### <span data-ttu-id="643d3-148">Microsoft.Azure.Commands.management.CognitiveServices.models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="643d3-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="643d3-149">Microsoft.Azure.Commands.management.CognitiveServices.models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="643d3-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="643d3-150">筆記</span><span class="sxs-lookup"><span data-stu-id="643d3-150">NOTES</span></span>

## <span data-ttu-id="643d3-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="643d3-151">RELATED LINKS</span></span>
