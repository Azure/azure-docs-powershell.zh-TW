---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 380061134c94cdbd618aaa4d18ef39b0b3a11359
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910434"
---
# <span data-ttu-id="091f6-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="091f6-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="091f6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="091f6-102">SYNOPSIS</span></span>
<span data-ttu-id="091f6-103">建立 Azure ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="091f6-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="091f6-104">語法</span><span class="sxs-lookup"><span data-stu-id="091f6-104">SYNTAX</span></span>

### <span data-ttu-id="091f6-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="091f6-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="091f6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="091f6-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="091f6-107">描述</span><span class="sxs-lookup"><span data-stu-id="091f6-107">DESCRIPTION</span></span>
<span data-ttu-id="091f6-108">**New-AzExpressRoutePort** Cmdlet 會建立 Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="091f6-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="091f6-109">例子</span><span class="sxs-lookup"><span data-stu-id="091f6-109">EXAMPLES</span></span>

### <span data-ttu-id="091f6-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="091f6-110">Example 1</span></span>
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

### <span data-ttu-id="091f6-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="091f6-111">Example 2</span></span>
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

## <span data-ttu-id="091f6-112">參數</span><span class="sxs-lookup"><span data-stu-id="091f6-112">PARAMETERS</span></span>

### <span data-ttu-id="091f6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="091f6-113">-AsJob</span></span>
<span data-ttu-id="091f6-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="091f6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="091f6-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="091f6-115">-BandwidthInGbps</span></span>
<span data-ttu-id="091f6-116">以百分位為單位的已延遲埠頻寬</span><span class="sxs-lookup"><span data-stu-id="091f6-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="091f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="091f6-117">-DefaultProfile</span></span>
<span data-ttu-id="091f6-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="091f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="091f6-119">-封裝</span><span class="sxs-lookup"><span data-stu-id="091f6-119">-Encapsulation</span></span>
<span data-ttu-id="091f6-120">實體埠上的封裝方法。</span><span class="sxs-lookup"><span data-stu-id="091f6-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="091f6-121">-強制</span><span class="sxs-lookup"><span data-stu-id="091f6-121">-Force</span></span>
<span data-ttu-id="091f6-122">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="091f6-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="091f6-123">-身分識別</span><span class="sxs-lookup"><span data-stu-id="091f6-123">-Identity</span></span>
<span data-ttu-id="091f6-124">讀取 MacSec 組配置的已指派使用者身分識別</span><span class="sxs-lookup"><span data-stu-id="091f6-124">User Assigned Identity for reading MacSec configuration</span></span>

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

### <span data-ttu-id="091f6-125">-連結</span><span class="sxs-lookup"><span data-stu-id="091f6-125">-Link</span></span>
<span data-ttu-id="091f6-126">ExpressRoutePort 資源實體連結集</span><span class="sxs-lookup"><span data-stu-id="091f6-126">The set of physical links of the ExpressRoutePort resource</span></span>

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

### <span data-ttu-id="091f6-127">-位置</span><span class="sxs-lookup"><span data-stu-id="091f6-127">-Location</span></span>
<span data-ttu-id="091f6-128">位置。</span><span class="sxs-lookup"><span data-stu-id="091f6-128">The location.</span></span>

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

### <span data-ttu-id="091f6-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="091f6-129">-Name</span></span>
<span data-ttu-id="091f6-130">ExpressRoutePort 的名稱。</span><span class="sxs-lookup"><span data-stu-id="091f6-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="091f6-131">-對等位置</span><span class="sxs-lookup"><span data-stu-id="091f6-131">-PeeringLocation</span></span>
<span data-ttu-id="091f6-132">ExpressRoutePort 實際對應到的對等位置名稱。</span><span class="sxs-lookup"><span data-stu-id="091f6-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="091f6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="091f6-133">-ResourceGroupName</span></span>
<span data-ttu-id="091f6-134">ExpressRoutePort 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="091f6-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="091f6-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="091f6-135">-ResourceId</span></span>
<span data-ttu-id="091f6-136">Express 路由埠的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="091f6-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="091f6-137">-標記</span><span class="sxs-lookup"><span data-stu-id="091f6-137">-Tag</span></span>
<span data-ttu-id="091f6-138">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="091f6-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="091f6-139">-確認</span><span class="sxs-lookup"><span data-stu-id="091f6-139">-Confirm</span></span>
<span data-ttu-id="091f6-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="091f6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="091f6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="091f6-141">-WhatIf</span></span>
<span data-ttu-id="091f6-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="091f6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="091f6-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="091f6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="091f6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="091f6-144">CommonParameters</span></span>
<span data-ttu-id="091f6-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="091f6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="091f6-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="091f6-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="091f6-147">輸入</span><span class="sxs-lookup"><span data-stu-id="091f6-147">INPUTS</span></span>

### <span data-ttu-id="091f6-148">System.String</span><span class="sxs-lookup"><span data-stu-id="091f6-148">System.String</span></span>

### <span data-ttu-id="091f6-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="091f6-149">System.Int32</span></span>

### <span data-ttu-id="091f6-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="091f6-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="091f6-151">Microsoft.Azure.Commands.Network.models.PSExpressRouteLink[]</span><span class="sxs-lookup"><span data-stu-id="091f6-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="091f6-152">輸出</span><span class="sxs-lookup"><span data-stu-id="091f6-152">OUTPUTS</span></span>

### <span data-ttu-id="091f6-153">Microsoft.Azure.Commands.Network.models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="091f6-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="091f6-154">筆記</span><span class="sxs-lookup"><span data-stu-id="091f6-154">NOTES</span></span>

## <span data-ttu-id="091f6-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="091f6-155">RELATED LINKS</span></span>

[<span data-ttu-id="091f6-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="091f6-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="091f6-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="091f6-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="091f6-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="091f6-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
