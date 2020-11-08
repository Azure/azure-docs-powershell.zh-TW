---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 3fe26c99dd92afb65105008524908a10dec02e0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127013"
---
# <span data-ttu-id="dffac-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="dffac-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="dffac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dffac-102">SYNOPSIS</span></span>
<span data-ttu-id="dffac-103">取得從指定位置到 Azure 區域的 internet 服務提供者相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="dffac-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="dffac-104">句法</span><span class="sxs-lookup"><span data-stu-id="dffac-104">SYNTAX</span></span>

### <span data-ttu-id="dffac-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="dffac-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dffac-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dffac-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dffac-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dffac-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dffac-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="dffac-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dffac-109">說明</span><span class="sxs-lookup"><span data-stu-id="dffac-109">DESCRIPTION</span></span>
<span data-ttu-id="dffac-110">Get-AzNetworkWatcherReachabilityReport 會取得從指定位置到 Azure 區域的 internet 服務提供者相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="dffac-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="dffac-111">示例</span><span class="sxs-lookup"><span data-stu-id="dffac-111">EXAMPLES</span></span>

### <span data-ttu-id="dffac-112">範例1</span><span class="sxs-lookup"><span data-stu-id="dffac-112">Example 1</span></span>
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

<span data-ttu-id="dffac-113">在美國境內2017-10-10 到2017-10-12 的 Microsoft 西部中，取得對 Azure 資料中心的相對延遲。</span><span class="sxs-lookup"><span data-stu-id="dffac-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="dffac-114">範例2</span><span class="sxs-lookup"><span data-stu-id="dffac-114">Example 2</span></span>

<span data-ttu-id="dffac-115">取得從指定位置到 Azure 區域的 internet 服務提供者相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="dffac-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="dffac-116"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="dffac-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="dffac-117">參數</span><span class="sxs-lookup"><span data-stu-id="dffac-117">PARAMETERS</span></span>

### <span data-ttu-id="dffac-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dffac-118">-AsJob</span></span>
<span data-ttu-id="dffac-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dffac-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dffac-120">-城市</span><span class="sxs-lookup"><span data-stu-id="dffac-120">-City</span></span>
<span data-ttu-id="dffac-121">城市的名稱。</span><span class="sxs-lookup"><span data-stu-id="dffac-121">The name of the city.</span></span>

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

### <span data-ttu-id="dffac-122">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="dffac-122">-Country</span></span>
<span data-ttu-id="dffac-123">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="dffac-123">The name of the country.</span></span>

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

### <span data-ttu-id="dffac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dffac-124">-DefaultProfile</span></span>
<span data-ttu-id="dffac-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dffac-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dffac-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dffac-126">-EndTime</span></span>
<span data-ttu-id="dffac-127">Azure 可存取性報告的結束時間。</span><span class="sxs-lookup"><span data-stu-id="dffac-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="dffac-128">-位置</span><span class="sxs-lookup"><span data-stu-id="dffac-128">-Location</span></span>
<span data-ttu-id="dffac-129">要將查詢範圍限定在其中的選用 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="dffac-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="dffac-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dffac-130">-NetworkWatcher</span></span>
<span data-ttu-id="dffac-131">網路觀察程式資源</span><span class="sxs-lookup"><span data-stu-id="dffac-131">The network watcher resource</span></span>

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

### <span data-ttu-id="dffac-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="dffac-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="dffac-133">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="dffac-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="dffac-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dffac-134">-NetworkWatcherName</span></span>
<span data-ttu-id="dffac-135">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="dffac-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="dffac-136">-提供者</span><span class="sxs-lookup"><span data-stu-id="dffac-136">-Provider</span></span>
<span data-ttu-id="dffac-137">網際網路服務提供者清單。</span><span class="sxs-lookup"><span data-stu-id="dffac-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="dffac-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dffac-138">-ResourceGroupName</span></span>
<span data-ttu-id="dffac-139">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dffac-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="dffac-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dffac-140">-ResourceId</span></span>
<span data-ttu-id="dffac-141">網路觀察程式資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dffac-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="dffac-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dffac-142">-StartTime</span></span>
<span data-ttu-id="dffac-143">Azure 可存取性報告的開始時間。</span><span class="sxs-lookup"><span data-stu-id="dffac-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="dffac-144">-State</span><span class="sxs-lookup"><span data-stu-id="dffac-144">-State</span></span>
<span data-ttu-id="dffac-145">狀態的名稱。</span><span class="sxs-lookup"><span data-stu-id="dffac-145">The name of the state.</span></span>

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

### <span data-ttu-id="dffac-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dffac-146">CommonParameters</span></span>
<span data-ttu-id="dffac-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dffac-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dffac-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dffac-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dffac-149">輸入</span><span class="sxs-lookup"><span data-stu-id="dffac-149">INPUTS</span></span>

### <span data-ttu-id="dffac-150">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dffac-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="dffac-151">System.object</span><span class="sxs-lookup"><span data-stu-id="dffac-151">System.String</span></span>

## <span data-ttu-id="dffac-152">輸出</span><span class="sxs-lookup"><span data-stu-id="dffac-152">OUTPUTS</span></span>

### <span data-ttu-id="dffac-153">PSAzureReachabilityReport 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dffac-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="dffac-154">筆記</span><span class="sxs-lookup"><span data-stu-id="dffac-154">NOTES</span></span>
<span data-ttu-id="dffac-155">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，可存取性，報告</span><span class="sxs-lookup"><span data-stu-id="dffac-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="dffac-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="dffac-156">RELATED LINKS</span></span>

[<span data-ttu-id="dffac-157">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dffac-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="dffac-158">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dffac-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="dffac-159">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dffac-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="dffac-160">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dffac-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="dffac-161">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dffac-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dffac-162">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dffac-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="dffac-163">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dffac-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="dffac-164">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dffac-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dffac-165">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dffac-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="dffac-166">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dffac-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dffac-167">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dffac-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dffac-168">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dffac-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dffac-169">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="dffac-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="dffac-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dffac-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="dffac-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="dffac-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="dffac-172">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dffac-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dffac-173">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dffac-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dffac-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dffac-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dffac-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="dffac-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="dffac-176">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dffac-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dffac-177">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dffac-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dffac-178">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="dffac-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="dffac-179">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="dffac-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="dffac-180">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="dffac-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="dffac-181">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="dffac-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="dffac-182">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="dffac-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="dffac-183">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dffac-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
