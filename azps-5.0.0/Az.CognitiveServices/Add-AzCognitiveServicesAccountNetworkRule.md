---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140649"
---
# <span data-ttu-id="5741a-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5741a-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="5741a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5741a-102">SYNOPSIS</span></span>
<span data-ttu-id="5741a-103">在認知服務帳戶的 NetworkRule 屬性中新增 IpRules 或 VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="5741a-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="5741a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5741a-104">SYNTAX</span></span>

### <span data-ttu-id="5741a-105">NetWorkRuleString (預設) </span><span class="sxs-lookup"><span data-stu-id="5741a-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5741a-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="5741a-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5741a-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="5741a-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5741a-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="5741a-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5741a-109">說明</span><span class="sxs-lookup"><span data-stu-id="5741a-109">DESCRIPTION</span></span>
<span data-ttu-id="5741a-110">**AzCognitiveServicesAccountNetworkRule** Cmdlet 會將 IpRules 或 VirtualNetworkRules 新增至認知服務帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="5741a-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="5741a-111">示例</span><span class="sxs-lookup"><span data-stu-id="5741a-111">EXAMPLES</span></span>

### <span data-ttu-id="5741a-112">範例1：在 IpAddressOrRange 中新增數個 IpRules</span><span class="sxs-lookup"><span data-stu-id="5741a-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="5741a-113">這個命令在 IpAddressOrRange 中新增數個 IpRules。</span><span class="sxs-lookup"><span data-stu-id="5741a-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="5741a-114">範例2：使用 VirtualNetworkResourceID 新增 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5741a-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="5741a-115">這個命令會在 VirtualNetworkResourceID 中新增 VirtualNetworkRule。</span><span class="sxs-lookup"><span data-stu-id="5741a-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="5741a-116">範例3：從另一個帳戶新增 VirtualNetworkRules 與 VirtualNetworkRule 物件</span><span class="sxs-lookup"><span data-stu-id="5741a-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="5741a-117">這個命令會從另一個帳戶新增 VirtualNetworkRules 與 VirtualNetworkRule 物件。</span><span class="sxs-lookup"><span data-stu-id="5741a-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="5741a-118">範例4：使用 IpRule 物件新增多個 IpRule，並以 JSON 輸入</span><span class="sxs-lookup"><span data-stu-id="5741a-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="5741a-119">這個命令會在多個 IpRule 物件中新增數個 IpRule，並以 JSON 進行輸入。</span><span class="sxs-lookup"><span data-stu-id="5741a-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="5741a-120">參數</span><span class="sxs-lookup"><span data-stu-id="5741a-120">PARAMETERS</span></span>

### <span data-ttu-id="5741a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5741a-121">-DefaultProfile</span></span>
<span data-ttu-id="5741a-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5741a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5741a-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5741a-123">-IpAddressOrRange</span></span>
<span data-ttu-id="5741a-124">認知服務帳戶在字串中 NetworkRule IpRules IpAddressOrRange。</span><span class="sxs-lookup"><span data-stu-id="5741a-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="5741a-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="5741a-125">-IpRule</span></span>
<span data-ttu-id="5741a-126">認知服務帳戶 NetworkRule IpRules。</span><span class="sxs-lookup"><span data-stu-id="5741a-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="5741a-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="5741a-127">-Name</span></span>
<span data-ttu-id="5741a-128">認知服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5741a-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="5741a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5741a-129">-ResourceGroupName</span></span>
<span data-ttu-id="5741a-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5741a-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="5741a-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5741a-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="5741a-132">認知服務帳戶在字串中 NetworkRule VirtualNetworkRules VirtualNetworkResourceId。</span><span class="sxs-lookup"><span data-stu-id="5741a-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="5741a-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5741a-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="5741a-134">認知服務帳戶 NetworkRule VirtualNetworkRules。</span><span class="sxs-lookup"><span data-stu-id="5741a-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="5741a-135">-確認</span><span class="sxs-lookup"><span data-stu-id="5741a-135">-Confirm</span></span>
<span data-ttu-id="5741a-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5741a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5741a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5741a-137">-WhatIf</span></span>
<span data-ttu-id="5741a-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5741a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5741a-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5741a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5741a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5741a-140">CommonParameters</span></span>
<span data-ttu-id="5741a-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5741a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5741a-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5741a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5741a-143">輸入</span><span class="sxs-lookup"><span data-stu-id="5741a-143">INPUTS</span></span>

### <span data-ttu-id="5741a-144">System.object</span><span class="sxs-lookup"><span data-stu-id="5741a-144">System.String</span></span>

### <span data-ttu-id="5741a-145">PSIpRule []. CognitiveServices. []</span><span class="sxs-lookup"><span data-stu-id="5741a-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="5741a-146">PSVirtualNetworkRule []. CognitiveServices. []</span><span class="sxs-lookup"><span data-stu-id="5741a-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="5741a-147">輸出</span><span class="sxs-lookup"><span data-stu-id="5741a-147">OUTPUTS</span></span>

### <span data-ttu-id="5741a-148">PSVirtualNetworkRule （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="5741a-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="5741a-149">PSIpRule （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="5741a-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="5741a-150">筆記</span><span class="sxs-lookup"><span data-stu-id="5741a-150">NOTES</span></span>

## <span data-ttu-id="5741a-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="5741a-151">RELATED LINKS</span></span>
