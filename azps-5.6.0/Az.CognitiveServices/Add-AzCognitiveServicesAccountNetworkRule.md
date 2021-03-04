---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: fe2f405e07bc20437b9c0b47b8e551039b90b500
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905185"
---
# <span data-ttu-id="408dc-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="408dc-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="408dc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="408dc-102">SYNOPSIS</span></span>
<span data-ttu-id="408dc-103">新增 IpRules 或 VirtualNetworkRules 至認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="408dc-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="408dc-104">語法</span><span class="sxs-lookup"><span data-stu-id="408dc-104">SYNTAX</span></span>

### <span data-ttu-id="408dc-105">NetWorkRuleString (預設) </span><span class="sxs-lookup"><span data-stu-id="408dc-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="408dc-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="408dc-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="408dc-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="408dc-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="408dc-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="408dc-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="408dc-109">描述</span><span class="sxs-lookup"><span data-stu-id="408dc-109">DESCRIPTION</span></span>
<span data-ttu-id="408dc-110">**Add-AzCognitiveServicesAccountNetworkRule** Cmdlet 會將 IpRules 或 VirtualNetworkRules 新增到認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="408dc-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="408dc-111">例子</span><span class="sxs-lookup"><span data-stu-id="408dc-111">EXAMPLES</span></span>

### <span data-ttu-id="408dc-112">範例 1：使用 IpAddressOrRange 新增多個 IpRules</span><span class="sxs-lookup"><span data-stu-id="408dc-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="408dc-113">此命令會使用 IpAddressOrRange 新增數個 IpRules。</span><span class="sxs-lookup"><span data-stu-id="408dc-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="408dc-114">範例 2：使用 VirtualNetworkResourceID 新增 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="408dc-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="408dc-115">此命令會新增 VirtualNetworkRule 與 VirtualNetworkResourceID。</span><span class="sxs-lookup"><span data-stu-id="408dc-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="408dc-116">範例 3：使用 VirtualNetworkRule Objects 從另一個帳戶新增 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="408dc-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="408dc-117">此命令會使用 VirtualNetworkRule Objects 從另一個帳戶新增 VirtualNetworkRules。</span><span class="sxs-lookup"><span data-stu-id="408dc-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="408dc-118">範例 4：使用 IpRule 物件新增多個 IpRule，使用 JSON 輸入</span><span class="sxs-lookup"><span data-stu-id="408dc-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="408dc-119">此命令會使用 IpRule 物件新增數個 IpRule，並輸入 JSON。</span><span class="sxs-lookup"><span data-stu-id="408dc-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="408dc-120">參數</span><span class="sxs-lookup"><span data-stu-id="408dc-120">PARAMETERS</span></span>

### <span data-ttu-id="408dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408dc-121">-DefaultProfile</span></span>
<span data-ttu-id="408dc-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="408dc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="408dc-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="408dc-123">-IpAddressOrRange</span></span>
<span data-ttu-id="408dc-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span><span class="sxs-lookup"><span data-stu-id="408dc-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="408dc-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="408dc-125">-IpRule</span></span>
<span data-ttu-id="408dc-126">認知服務帳戶 NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="408dc-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="408dc-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="408dc-127">-Name</span></span>
<span data-ttu-id="408dc-128">認知服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="408dc-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="408dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="408dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="408dc-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="408dc-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="408dc-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="408dc-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="408dc-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span><span class="sxs-lookup"><span data-stu-id="408dc-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="408dc-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="408dc-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="408dc-134">認知服務帳戶 NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="408dc-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="408dc-135">-確認</span><span class="sxs-lookup"><span data-stu-id="408dc-135">-Confirm</span></span>
<span data-ttu-id="408dc-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="408dc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="408dc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="408dc-137">-WhatIf</span></span>
<span data-ttu-id="408dc-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="408dc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="408dc-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="408dc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="408dc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408dc-140">CommonParameters</span></span>
<span data-ttu-id="408dc-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="408dc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408dc-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="408dc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408dc-143">輸入</span><span class="sxs-lookup"><span data-stu-id="408dc-143">INPUTS</span></span>

### <span data-ttu-id="408dc-144">System.String</span><span class="sxs-lookup"><span data-stu-id="408dc-144">System.String</span></span>

### <span data-ttu-id="408dc-145">Microsoft.Azure.Commands.management.CognitiveServices.models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="408dc-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="408dc-146">Microsoft.Azure.Commands.management.CognitiveServices.models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="408dc-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="408dc-147">輸出</span><span class="sxs-lookup"><span data-stu-id="408dc-147">OUTPUTS</span></span>

### <span data-ttu-id="408dc-148">Microsoft.Azure.Commands.management.CognitiveServices.models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="408dc-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="408dc-149">Microsoft.Azure.Commands.management.CognitiveServices.models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="408dc-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="408dc-150">筆記</span><span class="sxs-lookup"><span data-stu-id="408dc-150">NOTES</span></span>

## <span data-ttu-id="408dc-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="408dc-151">RELATED LINKS</span></span>
