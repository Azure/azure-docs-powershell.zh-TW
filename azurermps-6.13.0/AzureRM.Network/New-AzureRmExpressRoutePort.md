---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
ms.openlocfilehash: 8d3b204815fc273f97a549582a193002f5f4a48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448345"
---
# <span data-ttu-id="cb11a-101">New-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cb11a-101">New-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="cb11a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb11a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb11a-103">建立 Azure ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="cb11a-103">Creates an Azure ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb11a-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb11a-104">SYNTAX</span></span>

### <span data-ttu-id="cb11a-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cb11a-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb11a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb11a-106">ResourceIdParameterSet</span></span>
```
New-AzureRmExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb11a-107">說明</span><span class="sxs-lookup"><span data-stu-id="cb11a-107">DESCRIPTION</span></span>
<span data-ttu-id="cb11a-108">**新的-AzureRmExpressRoutePort** Cmdlet 會建立 Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cb11a-108">The **New-AzureRmExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="cb11a-109">示例</span><span class="sxs-lookup"><span data-stu-id="cb11a-109">EXAMPLES</span></span>

### <span data-ttu-id="cb11a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="cb11a-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

### <span data-ttu-id="cb11a-111">範例2</span><span class="sxs-lookup"><span data-stu-id="cb11a-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

## <span data-ttu-id="cb11a-112">參數</span><span class="sxs-lookup"><span data-stu-id="cb11a-112">PARAMETERS</span></span>

### <span data-ttu-id="cb11a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb11a-113">-AsJob</span></span>
<span data-ttu-id="cb11a-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb11a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb11a-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="cb11a-115">-BandwidthInGbps</span></span>
<span data-ttu-id="cb11a-116">Gbps 中的採購埠頻寬</span><span class="sxs-lookup"><span data-stu-id="cb11a-116">Bandwidth of procured ports in Gbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb11a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb11a-117">-DefaultProfile</span></span>
<span data-ttu-id="cb11a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb11a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb11a-119">-封裝</span><span class="sxs-lookup"><span data-stu-id="cb11a-119">-Encapsulation</span></span>
<span data-ttu-id="cb11a-120">物理埠上的封裝方法。</span><span class="sxs-lookup"><span data-stu-id="cb11a-120">Encapsulation method on physical ports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb11a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cb11a-121">-Force</span></span>
<span data-ttu-id="cb11a-122">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="cb11a-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cb11a-123">-連結</span><span class="sxs-lookup"><span data-stu-id="cb11a-123">-Link</span></span>
<span data-ttu-id="cb11a-124">ExpressRoutePort 資源的物理連結集</span><span class="sxs-lookup"><span data-stu-id="cb11a-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb11a-125">-位置</span><span class="sxs-lookup"><span data-stu-id="cb11a-125">-Location</span></span>
<span data-ttu-id="cb11a-126">位置。</span><span class="sxs-lookup"><span data-stu-id="cb11a-126">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb11a-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb11a-127">-Name</span></span>
<span data-ttu-id="cb11a-128">ExpressRoutePort 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb11a-128">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb11a-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="cb11a-129">-PeeringLocation</span></span>
<span data-ttu-id="cb11a-130">ExpressRoutePort 對應至實際的對等位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb11a-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb11a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb11a-131">-ResourceGroupName</span></span>
<span data-ttu-id="cb11a-132">ExpressRoutePort 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cb11a-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb11a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb11a-133">-ResourceId</span></span>
<span data-ttu-id="cb11a-134">快速路由埠的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="cb11a-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb11a-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="cb11a-135">-Tag</span></span>
<span data-ttu-id="cb11a-136">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="cb11a-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb11a-137">-確認</span><span class="sxs-lookup"><span data-stu-id="cb11a-137">-Confirm</span></span>
<span data-ttu-id="cb11a-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb11a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb11a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb11a-139">-WhatIf</span></span>
<span data-ttu-id="cb11a-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb11a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb11a-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb11a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb11a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb11a-142">CommonParameters</span></span>
<span data-ttu-id="cb11a-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb11a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb11a-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb11a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb11a-145">輸入</span><span class="sxs-lookup"><span data-stu-id="cb11a-145">INPUTS</span></span>

### <span data-ttu-id="cb11a-146">System.object</span><span class="sxs-lookup"><span data-stu-id="cb11a-146">System.String</span></span>

### <span data-ttu-id="cb11a-147">System.object</span><span class="sxs-lookup"><span data-stu-id="cb11a-147">System.Int32</span></span>

### <span data-ttu-id="cb11a-148">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cb11a-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cb11a-149">[System.object]. 清單 ' 1 [PSExpressRouteLink，6.3.0.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="cb11a-149">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink, Microsoft.Azure.Commands.Network, Version=6.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cb11a-150">輸出</span><span class="sxs-lookup"><span data-stu-id="cb11a-150">OUTPUTS</span></span>

### <span data-ttu-id="cb11a-151">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cb11a-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="cb11a-152">筆記</span><span class="sxs-lookup"><span data-stu-id="cb11a-152">NOTES</span></span>

## <span data-ttu-id="cb11a-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb11a-153">RELATED LINKS</span></span>
