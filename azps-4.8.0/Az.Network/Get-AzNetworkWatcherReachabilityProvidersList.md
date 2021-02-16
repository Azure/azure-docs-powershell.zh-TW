---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 028af170e73397178dfe3b81ff216b7fdb0ecfe6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402502"
---
# <span data-ttu-id="d6bea-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d6bea-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="d6bea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d6bea-102">SYNOPSIS</span></span>
<span data-ttu-id="d6bea-103">列出指定 Azure 區域的所有可用網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="d6bea-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="d6bea-104">語法</span><span class="sxs-lookup"><span data-stu-id="d6bea-104">SYNTAX</span></span>

### <span data-ttu-id="d6bea-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="d6bea-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6bea-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d6bea-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6bea-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d6bea-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6bea-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6bea-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6bea-109">描述</span><span class="sxs-lookup"><span data-stu-id="d6bea-109">DESCRIPTION</span></span>
<span data-ttu-id="d6bea-110">此Get-AzNetworkWatcherReachabilityProvidersList列出指定 Azure 區域的所有可用網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="d6bea-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="d6bea-111">例子</span><span class="sxs-lookup"><span data-stu-id="d6bea-111">EXAMPLES</span></span>

### <span data-ttu-id="d6bea-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="d6bea-112">Example 1</span></span>
```powershell
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="d6bea-113">列出美國西部華盛頓州西雅圖 Azure 資料中心的所有可用提供者。</span><span class="sxs-lookup"><span data-stu-id="d6bea-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="d6bea-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="d6bea-114">Example 2</span></span>

<span data-ttu-id="d6bea-115">列出指定 Azure 區域的所有可用網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="d6bea-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="d6bea-116"> (自動) </span><span class="sxs-lookup"><span data-stu-id="d6bea-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="d6bea-117">參數</span><span class="sxs-lookup"><span data-stu-id="d6bea-117">PARAMETERS</span></span>

### <span data-ttu-id="d6bea-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6bea-118">-AsJob</span></span>
<span data-ttu-id="d6bea-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d6bea-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6bea-120">-縣/市</span><span class="sxs-lookup"><span data-stu-id="d6bea-120">-City</span></span>
<span data-ttu-id="d6bea-121">縣/市名稱。</span><span class="sxs-lookup"><span data-stu-id="d6bea-121">The name of the city.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bea-122">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="d6bea-122">-Country</span></span>
<span data-ttu-id="d6bea-123">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6bea-123">The name of the country.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bea-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6bea-124">-DefaultProfile</span></span>
<span data-ttu-id="d6bea-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6bea-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6bea-126">-位置</span><span class="sxs-lookup"><span data-stu-id="d6bea-126">-Location</span></span>
<span data-ttu-id="d6bea-127">選擇性的 Azure 區域，以將查詢範圍縮小到範圍。</span><span class="sxs-lookup"><span data-stu-id="d6bea-127">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bea-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6bea-128">-NetworkWatcher</span></span>
<span data-ttu-id="d6bea-129">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="d6bea-129">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bea-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="d6bea-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="d6bea-131">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="d6bea-131">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bea-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d6bea-132">-NetworkWatcherName</span></span>
<span data-ttu-id="d6bea-133">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6bea-133">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bea-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6bea-134">-ResourceGroupName</span></span>
<span data-ttu-id="d6bea-135">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6bea-135">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bea-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6bea-136">-ResourceId</span></span>
<span data-ttu-id="d6bea-137">網路監視資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6bea-137">The Id of network watcher resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bea-138">-State</span><span class="sxs-lookup"><span data-stu-id="d6bea-138">-State</span></span>
<span data-ttu-id="d6bea-139">州名。</span><span class="sxs-lookup"><span data-stu-id="d6bea-139">The name of the state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6bea-140">CommonParameters</span></span>
<span data-ttu-id="d6bea-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d6bea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6bea-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6bea-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6bea-143">輸入</span><span class="sxs-lookup"><span data-stu-id="d6bea-143">INPUTS</span></span>

### <span data-ttu-id="d6bea-144">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6bea-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d6bea-145">System.String</span><span class="sxs-lookup"><span data-stu-id="d6bea-145">System.String</span></span>

## <span data-ttu-id="d6bea-146">輸出</span><span class="sxs-lookup"><span data-stu-id="d6bea-146">OUTPUTS</span></span>

### <span data-ttu-id="d6bea-147">Microsoft.Azure.Commands.Network.models.PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="d6bea-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="d6bea-148">筆記</span><span class="sxs-lookup"><span data-stu-id="d6bea-148">NOTES</span></span>
<span data-ttu-id="d6bea-149">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路、網路監視者、下一個、躍點</span><span class="sxs-lookup"><span data-stu-id="d6bea-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="d6bea-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6bea-150">RELATED LINKS</span></span>

[<span data-ttu-id="d6bea-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6bea-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d6bea-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6bea-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d6bea-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6bea-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d6bea-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d6bea-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d6bea-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d6bea-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d6bea-156">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="d6bea-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d6bea-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d6bea-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d6bea-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6bea-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6bea-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d6bea-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d6bea-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6bea-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6bea-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6bea-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6bea-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6bea-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6bea-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6bea-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d6bea-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d6bea-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d6bea-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d6bea-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d6bea-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6bea-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d6bea-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6bea-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d6bea-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6bea-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d6bea-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d6bea-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d6bea-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6bea-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d6bea-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6bea-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d6bea-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d6bea-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d6bea-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d6bea-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d6bea-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d6bea-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d6bea-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d6bea-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d6bea-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d6bea-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d6bea-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d6bea-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
