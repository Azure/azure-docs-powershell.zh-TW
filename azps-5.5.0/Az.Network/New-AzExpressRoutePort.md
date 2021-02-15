---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142171"
---
# <span data-ttu-id="71a83-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71a83-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="71a83-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71a83-102">SYNOPSIS</span></span>
<span data-ttu-id="71a83-103">建立 Azure ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="71a83-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="71a83-104">句法</span><span class="sxs-lookup"><span data-stu-id="71a83-104">SYNTAX</span></span>

### <span data-ttu-id="71a83-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="71a83-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71a83-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71a83-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71a83-107">說明</span><span class="sxs-lookup"><span data-stu-id="71a83-107">DESCRIPTION</span></span>
<span data-ttu-id="71a83-108">**新的-AzExpressRoutePort** Cmdlet 會建立 Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71a83-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="71a83-109">示例</span><span class="sxs-lookup"><span data-stu-id="71a83-109">EXAMPLES</span></span>

### <span data-ttu-id="71a83-110">範例1</span><span class="sxs-lookup"><span data-stu-id="71a83-110">Example 1</span></span>
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

### <span data-ttu-id="71a83-111">範例2</span><span class="sxs-lookup"><span data-stu-id="71a83-111">Example 2</span></span>
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

## <span data-ttu-id="71a83-112">參數</span><span class="sxs-lookup"><span data-stu-id="71a83-112">PARAMETERS</span></span>

### <span data-ttu-id="71a83-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71a83-113">-AsJob</span></span>
<span data-ttu-id="71a83-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="71a83-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71a83-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="71a83-115">-BandwidthInGbps</span></span>
<span data-ttu-id="71a83-116">Gbps 中的採購埠頻寬</span><span class="sxs-lookup"><span data-stu-id="71a83-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="71a83-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a83-117">-DefaultProfile</span></span>
<span data-ttu-id="71a83-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71a83-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71a83-119">-封裝</span><span class="sxs-lookup"><span data-stu-id="71a83-119">-Encapsulation</span></span>
<span data-ttu-id="71a83-120">物理埠上的封裝方法。</span><span class="sxs-lookup"><span data-stu-id="71a83-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="71a83-121">-Force</span><span class="sxs-lookup"><span data-stu-id="71a83-121">-Force</span></span>
<span data-ttu-id="71a83-122">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="71a83-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="71a83-123">身分識別</span><span class="sxs-lookup"><span data-stu-id="71a83-123">-Identity</span></span>
<span data-ttu-id="71a83-124">用來讀取 MacSec 設定的使用者指派身分識別</span><span class="sxs-lookup"><span data-stu-id="71a83-124">User Assigned Identity for reading MacSec configuration</span></span>

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

### <span data-ttu-id="71a83-125">-連結</span><span class="sxs-lookup"><span data-stu-id="71a83-125">-Link</span></span>
<span data-ttu-id="71a83-126">ExpressRoutePort 資源的物理連結集</span><span class="sxs-lookup"><span data-stu-id="71a83-126">The set of physical links of the ExpressRoutePort resource</span></span>

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

### <span data-ttu-id="71a83-127">-位置</span><span class="sxs-lookup"><span data-stu-id="71a83-127">-Location</span></span>
<span data-ttu-id="71a83-128">位置。</span><span class="sxs-lookup"><span data-stu-id="71a83-128">The location.</span></span>

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

### <span data-ttu-id="71a83-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="71a83-129">-Name</span></span>
<span data-ttu-id="71a83-130">ExpressRoutePort 的名稱。</span><span class="sxs-lookup"><span data-stu-id="71a83-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="71a83-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="71a83-131">-PeeringLocation</span></span>
<span data-ttu-id="71a83-132">ExpressRoutePort 對應至實際的對等位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="71a83-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="71a83-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71a83-133">-ResourceGroupName</span></span>
<span data-ttu-id="71a83-134">ExpressRoutePort 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="71a83-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="71a83-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71a83-135">-ResourceId</span></span>
<span data-ttu-id="71a83-136">快速路由埠的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="71a83-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="71a83-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="71a83-137">-Tag</span></span>
<span data-ttu-id="71a83-138">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="71a83-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="71a83-139">-確認</span><span class="sxs-lookup"><span data-stu-id="71a83-139">-Confirm</span></span>
<span data-ttu-id="71a83-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71a83-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71a83-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71a83-141">-WhatIf</span></span>
<span data-ttu-id="71a83-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71a83-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71a83-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71a83-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71a83-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a83-144">CommonParameters</span></span>
<span data-ttu-id="71a83-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71a83-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a83-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71a83-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a83-147">輸入</span><span class="sxs-lookup"><span data-stu-id="71a83-147">INPUTS</span></span>

### <span data-ttu-id="71a83-148">System.object</span><span class="sxs-lookup"><span data-stu-id="71a83-148">System.String</span></span>

### <span data-ttu-id="71a83-149">System.object</span><span class="sxs-lookup"><span data-stu-id="71a83-149">System.Int32</span></span>

### <span data-ttu-id="71a83-150">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="71a83-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="71a83-151">PSExpressRouteLink [] （[]）</span><span class="sxs-lookup"><span data-stu-id="71a83-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="71a83-152">輸出</span><span class="sxs-lookup"><span data-stu-id="71a83-152">OUTPUTS</span></span>

### <span data-ttu-id="71a83-153">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="71a83-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="71a83-154">筆記</span><span class="sxs-lookup"><span data-stu-id="71a83-154">NOTES</span></span>

## <span data-ttu-id="71a83-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="71a83-155">RELATED LINKS</span></span>

[<span data-ttu-id="71a83-156">AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71a83-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="71a83-157">移除-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71a83-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="71a83-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71a83-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
