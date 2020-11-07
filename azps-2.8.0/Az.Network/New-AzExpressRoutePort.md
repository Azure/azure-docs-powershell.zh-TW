---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 63fda9c2f5b0231a2072483d4df05f6940b8fef8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789373"
---
# <span data-ttu-id="18e51-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="18e51-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="18e51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18e51-102">SYNOPSIS</span></span>
<span data-ttu-id="18e51-103">建立 Azure ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="18e51-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="18e51-104">句法</span><span class="sxs-lookup"><span data-stu-id="18e51-104">SYNTAX</span></span>

### <span data-ttu-id="18e51-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="18e51-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18e51-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18e51-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18e51-107">說明</span><span class="sxs-lookup"><span data-stu-id="18e51-107">DESCRIPTION</span></span>
<span data-ttu-id="18e51-108">**新的-AzExpressRoutePort** Cmdlet 會建立 Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="18e51-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="18e51-109">示例</span><span class="sxs-lookup"><span data-stu-id="18e51-109">EXAMPLES</span></span>

### <span data-ttu-id="18e51-110">範例1</span><span class="sxs-lookup"><span data-stu-id="18e51-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="18e51-111">範例2</span><span class="sxs-lookup"><span data-stu-id="18e51-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="18e51-112">參數</span><span class="sxs-lookup"><span data-stu-id="18e51-112">PARAMETERS</span></span>

### <span data-ttu-id="18e51-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18e51-113">-AsJob</span></span>
<span data-ttu-id="18e51-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="18e51-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18e51-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="18e51-115">-BandwidthInGbps</span></span>
<span data-ttu-id="18e51-116">Gbps 中的採購埠頻寬</span><span class="sxs-lookup"><span data-stu-id="18e51-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="18e51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18e51-117">-DefaultProfile</span></span>
<span data-ttu-id="18e51-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18e51-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18e51-119">-封裝</span><span class="sxs-lookup"><span data-stu-id="18e51-119">-Encapsulation</span></span>
<span data-ttu-id="18e51-120">物理埠上的封裝方法。</span><span class="sxs-lookup"><span data-stu-id="18e51-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="18e51-121">-Force</span><span class="sxs-lookup"><span data-stu-id="18e51-121">-Force</span></span>
<span data-ttu-id="18e51-122">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="18e51-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="18e51-123">身分識別</span><span class="sxs-lookup"><span data-stu-id="18e51-123">-Identity</span></span>
<span data-ttu-id="18e51-124">用來讀取 MacSec 設定的使用者指派身分識別</span><span class="sxs-lookup"><span data-stu-id="18e51-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18e51-125">-連結</span><span class="sxs-lookup"><span data-stu-id="18e51-125">-Link</span></span>
<span data-ttu-id="18e51-126">ExpressRoutePort 資源的物理連結集</span><span class="sxs-lookup"><span data-stu-id="18e51-126">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e51-127">-位置</span><span class="sxs-lookup"><span data-stu-id="18e51-127">-Location</span></span>
<span data-ttu-id="18e51-128">位置。</span><span class="sxs-lookup"><span data-stu-id="18e51-128">The location.</span></span>

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

### <span data-ttu-id="18e51-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="18e51-129">-Name</span></span>
<span data-ttu-id="18e51-130">ExpressRoutePort 的名稱。</span><span class="sxs-lookup"><span data-stu-id="18e51-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="18e51-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="18e51-131">-PeeringLocation</span></span>
<span data-ttu-id="18e51-132">ExpressRoutePort 對應至實際的對等位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="18e51-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="18e51-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18e51-133">-ResourceGroupName</span></span>
<span data-ttu-id="18e51-134">ExpressRoutePort 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="18e51-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="18e51-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18e51-135">-ResourceId</span></span>
<span data-ttu-id="18e51-136">快速路由埠的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="18e51-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="18e51-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="18e51-137">-Tag</span></span>
<span data-ttu-id="18e51-138">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="18e51-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="18e51-139">-確認</span><span class="sxs-lookup"><span data-stu-id="18e51-139">-Confirm</span></span>
<span data-ttu-id="18e51-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="18e51-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18e51-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18e51-141">-WhatIf</span></span>
<span data-ttu-id="18e51-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18e51-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18e51-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18e51-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18e51-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e51-144">CommonParameters</span></span>
<span data-ttu-id="18e51-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18e51-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e51-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="18e51-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e51-147">輸入</span><span class="sxs-lookup"><span data-stu-id="18e51-147">INPUTS</span></span>

### <span data-ttu-id="18e51-148">System.object</span><span class="sxs-lookup"><span data-stu-id="18e51-148">System.String</span></span>

### <span data-ttu-id="18e51-149">System.object</span><span class="sxs-lookup"><span data-stu-id="18e51-149">System.Int32</span></span>

### <span data-ttu-id="18e51-150">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="18e51-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="18e51-151">PSExpressRouteLink [] （[]）</span><span class="sxs-lookup"><span data-stu-id="18e51-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="18e51-152">輸出</span><span class="sxs-lookup"><span data-stu-id="18e51-152">OUTPUTS</span></span>

### <span data-ttu-id="18e51-153">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="18e51-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="18e51-154">筆記</span><span class="sxs-lookup"><span data-stu-id="18e51-154">NOTES</span></span>

## <span data-ttu-id="18e51-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="18e51-155">RELATED LINKS</span></span>

[<span data-ttu-id="18e51-156">AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="18e51-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="18e51-157">移除-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="18e51-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="18e51-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="18e51-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
