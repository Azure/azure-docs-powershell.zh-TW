---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: f29ab593ffac847ec6b089efdc39bc594ad1d785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412838"
---
# <span data-ttu-id="075ee-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="075ee-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="075ee-102">簡介</span><span class="sxs-lookup"><span data-stu-id="075ee-102">SYNOPSIS</span></span>
<span data-ttu-id="075ee-103">取得網際網路服務提供者從指定位置到 Azure 區域的相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="075ee-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="075ee-104">語法</span><span class="sxs-lookup"><span data-stu-id="075ee-104">SYNTAX</span></span>

### <span data-ttu-id="075ee-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="075ee-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="075ee-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="075ee-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="075ee-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="075ee-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="075ee-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="075ee-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="075ee-109">描述</span><span class="sxs-lookup"><span data-stu-id="075ee-109">DESCRIPTION</span></span>
<span data-ttu-id="075ee-110">此Get-AzNetworkWatcherReachabilityReport會取得從指定位置到 Azure 區域之網際網路服務提供者的相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="075ee-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="075ee-111">例子</span><span class="sxs-lookup"><span data-stu-id="075ee-111">EXAMPLES</span></span>

### <span data-ttu-id="075ee-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="075ee-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="075ee-113">從美國西部的 2017-10-10 到 2017-10-10-12，獲得美國西部 Azure 資料中心的相對延遲。</span><span class="sxs-lookup"><span data-stu-id="075ee-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="075ee-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="075ee-114">Example 2</span></span>

<span data-ttu-id="075ee-115">取得網際網路服務提供者從指定位置到 Azure 區域的相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="075ee-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="075ee-116"> (自動) </span><span class="sxs-lookup"><span data-stu-id="075ee-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="075ee-117">參數</span><span class="sxs-lookup"><span data-stu-id="075ee-117">PARAMETERS</span></span>

### <span data-ttu-id="075ee-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="075ee-118">-AsJob</span></span>
<span data-ttu-id="075ee-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="075ee-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="075ee-120">-縣/市</span><span class="sxs-lookup"><span data-stu-id="075ee-120">-City</span></span>
<span data-ttu-id="075ee-121">縣/市名稱。</span><span class="sxs-lookup"><span data-stu-id="075ee-121">The name of the city.</span></span>

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

### <span data-ttu-id="075ee-122">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="075ee-122">-Country</span></span>
<span data-ttu-id="075ee-123">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="075ee-123">The name of the country.</span></span>

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

### <span data-ttu-id="075ee-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="075ee-124">-DefaultProfile</span></span>
<span data-ttu-id="075ee-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="075ee-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="075ee-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="075ee-126">-EndTime</span></span>
<span data-ttu-id="075ee-127">Azure 可及性報告的結束時間。</span><span class="sxs-lookup"><span data-stu-id="075ee-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="075ee-128">-位置</span><span class="sxs-lookup"><span data-stu-id="075ee-128">-Location</span></span>
<span data-ttu-id="075ee-129">選擇性的 Azure 區域，以將查詢範圍縮小到範圍。</span><span class="sxs-lookup"><span data-stu-id="075ee-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="075ee-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="075ee-130">-NetworkWatcher</span></span>
<span data-ttu-id="075ee-131">網路監視程式資源</span><span class="sxs-lookup"><span data-stu-id="075ee-131">The network watcher resource</span></span>

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

### <span data-ttu-id="075ee-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="075ee-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="075ee-133">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="075ee-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="075ee-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="075ee-134">-NetworkWatcherName</span></span>
<span data-ttu-id="075ee-135">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="075ee-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="075ee-136">-提供者</span><span class="sxs-lookup"><span data-stu-id="075ee-136">-Provider</span></span>
<span data-ttu-id="075ee-137">網際網路服務提供者清單。</span><span class="sxs-lookup"><span data-stu-id="075ee-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="075ee-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="075ee-138">-ResourceGroupName</span></span>
<span data-ttu-id="075ee-139">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="075ee-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="075ee-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="075ee-140">-ResourceId</span></span>
<span data-ttu-id="075ee-141">網路監視資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="075ee-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="075ee-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="075ee-142">-StartTime</span></span>
<span data-ttu-id="075ee-143">Azure 可及性報告的開始時間。</span><span class="sxs-lookup"><span data-stu-id="075ee-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="075ee-144">-State</span><span class="sxs-lookup"><span data-stu-id="075ee-144">-State</span></span>
<span data-ttu-id="075ee-145">州名。</span><span class="sxs-lookup"><span data-stu-id="075ee-145">The name of the state.</span></span>

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

### <span data-ttu-id="075ee-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="075ee-146">CommonParameters</span></span>
<span data-ttu-id="075ee-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="075ee-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="075ee-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="075ee-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="075ee-149">輸入</span><span class="sxs-lookup"><span data-stu-id="075ee-149">INPUTS</span></span>

### <span data-ttu-id="075ee-150">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="075ee-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="075ee-151">System.String</span><span class="sxs-lookup"><span data-stu-id="075ee-151">System.String</span></span>

## <span data-ttu-id="075ee-152">輸出</span><span class="sxs-lookup"><span data-stu-id="075ee-152">OUTPUTS</span></span>

### <span data-ttu-id="075ee-153">Microsoft.Azure.Commands.Network.models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="075ee-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="075ee-154">筆記</span><span class="sxs-lookup"><span data-stu-id="075ee-154">NOTES</span></span>
<span data-ttu-id="075ee-155">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路、網路監視者、可聯繫性、報告</span><span class="sxs-lookup"><span data-stu-id="075ee-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="075ee-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="075ee-156">RELATED LINKS</span></span>

[<span data-ttu-id="075ee-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="075ee-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="075ee-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="075ee-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="075ee-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="075ee-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="075ee-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="075ee-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="075ee-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="075ee-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="075ee-162">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="075ee-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="075ee-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="075ee-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="075ee-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="075ee-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="075ee-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="075ee-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="075ee-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="075ee-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="075ee-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="075ee-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="075ee-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="075ee-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="075ee-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="075ee-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="075ee-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="075ee-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="075ee-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="075ee-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="075ee-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="075ee-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="075ee-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="075ee-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="075ee-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="075ee-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="075ee-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="075ee-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="075ee-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="075ee-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="075ee-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="075ee-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="075ee-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="075ee-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="075ee-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="075ee-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="075ee-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="075ee-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="075ee-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="075ee-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="075ee-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="075ee-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="075ee-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="075ee-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
