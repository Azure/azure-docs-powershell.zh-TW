---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 1c06b6605cfa7d4b7d402dec2fcb0e33136b125c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400276"
---
# <span data-ttu-id="644c8-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="644c8-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="644c8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="644c8-102">SYNOPSIS</span></span>
<span data-ttu-id="644c8-103">取得網際網路服務提供者從指定位置到 Azure 區域的相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="644c8-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="644c8-104">語法</span><span class="sxs-lookup"><span data-stu-id="644c8-104">SYNTAX</span></span>

### <span data-ttu-id="644c8-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="644c8-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="644c8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="644c8-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="644c8-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="644c8-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="644c8-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="644c8-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="644c8-109">描述</span><span class="sxs-lookup"><span data-stu-id="644c8-109">DESCRIPTION</span></span>
<span data-ttu-id="644c8-110">此Get-AzNetworkWatcherReachabilityReport會取得從指定位置到 Azure 區域之網際網路服務提供者的相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="644c8-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="644c8-111">例子</span><span class="sxs-lookup"><span data-stu-id="644c8-111">EXAMPLES</span></span>

### <span data-ttu-id="644c8-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="644c8-112">Example 1</span></span>
```
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="644c8-113">從美國西部的 2017-10-10 到 2017-10-12，獲得美國西部 Azure 資料中心的相對延遲。</span><span class="sxs-lookup"><span data-stu-id="644c8-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="644c8-114">參數</span><span class="sxs-lookup"><span data-stu-id="644c8-114">PARAMETERS</span></span>

### <span data-ttu-id="644c8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="644c8-115">-AsJob</span></span>
<span data-ttu-id="644c8-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="644c8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="644c8-117">-縣/市</span><span class="sxs-lookup"><span data-stu-id="644c8-117">-City</span></span>
<span data-ttu-id="644c8-118">縣/市名稱。</span><span class="sxs-lookup"><span data-stu-id="644c8-118">The name of the city.</span></span>

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

### <span data-ttu-id="644c8-119">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="644c8-119">-Country</span></span>
<span data-ttu-id="644c8-120">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="644c8-120">The name of the country.</span></span>

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

### <span data-ttu-id="644c8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="644c8-121">-DefaultProfile</span></span>
<span data-ttu-id="644c8-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="644c8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="644c8-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="644c8-123">-EndTime</span></span>
<span data-ttu-id="644c8-124">Azure 可及性報告的結束時間。</span><span class="sxs-lookup"><span data-stu-id="644c8-124">The end time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="644c8-125">-位置</span><span class="sxs-lookup"><span data-stu-id="644c8-125">-Location</span></span>
<span data-ttu-id="644c8-126">選擇性的 Azure 區域，以將查詢範圍縮小到範圍。</span><span class="sxs-lookup"><span data-stu-id="644c8-126">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="644c8-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="644c8-127">-NetworkWatcher</span></span>
<span data-ttu-id="644c8-128">網路監視程式資源</span><span class="sxs-lookup"><span data-stu-id="644c8-128">The network watcher resource</span></span>

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

### <span data-ttu-id="644c8-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="644c8-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="644c8-130">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="644c8-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="644c8-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="644c8-131">-NetworkWatcherName</span></span>
<span data-ttu-id="644c8-132">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="644c8-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="644c8-133">-提供者</span><span class="sxs-lookup"><span data-stu-id="644c8-133">-Provider</span></span>
<span data-ttu-id="644c8-134">網際網路服務提供者清單。</span><span class="sxs-lookup"><span data-stu-id="644c8-134">List of Internet service providers.</span></span>

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

### <span data-ttu-id="644c8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="644c8-135">-ResourceGroupName</span></span>
<span data-ttu-id="644c8-136">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="644c8-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="644c8-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="644c8-137">-ResourceId</span></span>
<span data-ttu-id="644c8-138">網路監視資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="644c8-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="644c8-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="644c8-139">-StartTime</span></span>
<span data-ttu-id="644c8-140">Azure 可及性報告的開始時間。</span><span class="sxs-lookup"><span data-stu-id="644c8-140">The start time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="644c8-141">-State</span><span class="sxs-lookup"><span data-stu-id="644c8-141">-State</span></span>
<span data-ttu-id="644c8-142">州名。</span><span class="sxs-lookup"><span data-stu-id="644c8-142">The name of the state.</span></span>

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

### <span data-ttu-id="644c8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="644c8-143">CommonParameters</span></span>
<span data-ttu-id="644c8-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="644c8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="644c8-145">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="644c8-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="644c8-146">輸入</span><span class="sxs-lookup"><span data-stu-id="644c8-146">INPUTS</span></span>

### <span data-ttu-id="644c8-147">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="644c8-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="644c8-148">System.String</span><span class="sxs-lookup"><span data-stu-id="644c8-148">System.String</span></span>

## <span data-ttu-id="644c8-149">輸出</span><span class="sxs-lookup"><span data-stu-id="644c8-149">OUTPUTS</span></span>

### <span data-ttu-id="644c8-150">Microsoft.Azure.Commands.Network.models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="644c8-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="644c8-151">筆記</span><span class="sxs-lookup"><span data-stu-id="644c8-151">NOTES</span></span>
<span data-ttu-id="644c8-152">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路、網路監視者、可聯繫性、報告</span><span class="sxs-lookup"><span data-stu-id="644c8-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="644c8-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="644c8-153">RELATED LINKS</span></span>

[<span data-ttu-id="644c8-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="644c8-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="644c8-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="644c8-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="644c8-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="644c8-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="644c8-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="644c8-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="644c8-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="644c8-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="644c8-159">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="644c8-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="644c8-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="644c8-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="644c8-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="644c8-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="644c8-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="644c8-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="644c8-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="644c8-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="644c8-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="644c8-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="644c8-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="644c8-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="644c8-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="644c8-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="644c8-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="644c8-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="644c8-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="644c8-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="644c8-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="644c8-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="644c8-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="644c8-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="644c8-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="644c8-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="644c8-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="644c8-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="644c8-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="644c8-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="644c8-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="644c8-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="644c8-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="644c8-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="644c8-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="644c8-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="644c8-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="644c8-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="644c8-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="644c8-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="644c8-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="644c8-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="644c8-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="644c8-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
