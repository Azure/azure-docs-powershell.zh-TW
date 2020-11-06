---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 71227c2e351e12381a857dcf9cd66767f00265cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621964"
---
# <span data-ttu-id="6bde1-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6bde1-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="6bde1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6bde1-102">SYNOPSIS</span></span>
<span data-ttu-id="6bde1-103">取得從指定位置到 Azure 區域的 internet 服務提供者相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="6bde1-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="6bde1-104">句法</span><span class="sxs-lookup"><span data-stu-id="6bde1-104">SYNTAX</span></span>

### <span data-ttu-id="6bde1-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="6bde1-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bde1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6bde1-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bde1-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bde1-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bde1-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6bde1-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bde1-109">說明</span><span class="sxs-lookup"><span data-stu-id="6bde1-109">DESCRIPTION</span></span>
<span data-ttu-id="6bde1-110">Get-AzNetworkWatcherReachabilityReport 會取得從指定位置到 Azure 區域的 internet 服務提供者相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="6bde1-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="6bde1-111">示例</span><span class="sxs-lookup"><span data-stu-id="6bde1-111">EXAMPLES</span></span>

### <span data-ttu-id="6bde1-112">範例1</span><span class="sxs-lookup"><span data-stu-id="6bde1-112">Example 1</span></span>
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

<span data-ttu-id="6bde1-113">在美國境內2017-10-10 到2017-10-12 的 Microsoft 西部中，取得對 Azure 資料中心的相對延遲。</span><span class="sxs-lookup"><span data-stu-id="6bde1-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="6bde1-114">參數</span><span class="sxs-lookup"><span data-stu-id="6bde1-114">PARAMETERS</span></span>

### <span data-ttu-id="6bde1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bde1-115">-AsJob</span></span>
<span data-ttu-id="6bde1-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6bde1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6bde1-117">-城市</span><span class="sxs-lookup"><span data-stu-id="6bde1-117">-City</span></span>
<span data-ttu-id="6bde1-118">城市的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bde1-118">The name of the city.</span></span>

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

### <span data-ttu-id="6bde1-119">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="6bde1-119">-Country</span></span>
<span data-ttu-id="6bde1-120">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bde1-120">The name of the country.</span></span>

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

### <span data-ttu-id="6bde1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bde1-121">-DefaultProfile</span></span>
<span data-ttu-id="6bde1-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6bde1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bde1-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="6bde1-123">-EndTime</span></span>
<span data-ttu-id="6bde1-124">Azure 可存取性報告的結束時間。</span><span class="sxs-lookup"><span data-stu-id="6bde1-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="6bde1-125">-位置</span><span class="sxs-lookup"><span data-stu-id="6bde1-125">-Location</span></span>
<span data-ttu-id="6bde1-126">要將查詢範圍限定在其中的選用 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="6bde1-126">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="6bde1-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6bde1-127">-NetworkWatcher</span></span>
<span data-ttu-id="6bde1-128">網路觀察程式資源</span><span class="sxs-lookup"><span data-stu-id="6bde1-128">The network watcher resource</span></span>

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

### <span data-ttu-id="6bde1-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="6bde1-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="6bde1-130">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="6bde1-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6bde1-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6bde1-131">-NetworkWatcherName</span></span>
<span data-ttu-id="6bde1-132">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bde1-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="6bde1-133">-提供者</span><span class="sxs-lookup"><span data-stu-id="6bde1-133">-Provider</span></span>
<span data-ttu-id="6bde1-134">網際網路服務提供者清單。</span><span class="sxs-lookup"><span data-stu-id="6bde1-134">List of Internet service providers.</span></span>

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

### <span data-ttu-id="6bde1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bde1-135">-ResourceGroupName</span></span>
<span data-ttu-id="6bde1-136">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bde1-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6bde1-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bde1-137">-ResourceId</span></span>
<span data-ttu-id="6bde1-138">網路觀察程式資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6bde1-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="6bde1-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6bde1-139">-StartTime</span></span>
<span data-ttu-id="6bde1-140">Azure 可存取性報告的開始時間。</span><span class="sxs-lookup"><span data-stu-id="6bde1-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="6bde1-141">-State</span><span class="sxs-lookup"><span data-stu-id="6bde1-141">-State</span></span>
<span data-ttu-id="6bde1-142">狀態的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bde1-142">The name of the state.</span></span>

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

### <span data-ttu-id="6bde1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bde1-143">CommonParameters</span></span>
<span data-ttu-id="6bde1-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6bde1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bde1-145">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6bde1-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bde1-146">輸入</span><span class="sxs-lookup"><span data-stu-id="6bde1-146">INPUTS</span></span>

### <span data-ttu-id="6bde1-147">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6bde1-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="6bde1-148">System.object</span><span class="sxs-lookup"><span data-stu-id="6bde1-148">System.String</span></span>

## <span data-ttu-id="6bde1-149">輸出</span><span class="sxs-lookup"><span data-stu-id="6bde1-149">OUTPUTS</span></span>

### <span data-ttu-id="6bde1-150">PSAzureReachabilityReport 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6bde1-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="6bde1-151">筆記</span><span class="sxs-lookup"><span data-stu-id="6bde1-151">NOTES</span></span>
<span data-ttu-id="6bde1-152">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，可存取性，報告</span><span class="sxs-lookup"><span data-stu-id="6bde1-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="6bde1-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bde1-153">RELATED LINKS</span></span>

[<span data-ttu-id="6bde1-154">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6bde1-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6bde1-155">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6bde1-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6bde1-156">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6bde1-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6bde1-157">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6bde1-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6bde1-158">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6bde1-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6bde1-159">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6bde1-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6bde1-160">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6bde1-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6bde1-161">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6bde1-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6bde1-162">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6bde1-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6bde1-163">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6bde1-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6bde1-164">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6bde1-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6bde1-165">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6bde1-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6bde1-166">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bde1-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6bde1-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6bde1-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6bde1-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6bde1-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="6bde1-169">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6bde1-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6bde1-170">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6bde1-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6bde1-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6bde1-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6bde1-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6bde1-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6bde1-173">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6bde1-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6bde1-174">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6bde1-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6bde1-175">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6bde1-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6bde1-176">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6bde1-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6bde1-177">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6bde1-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6bde1-178">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6bde1-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6bde1-179">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6bde1-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="6bde1-180">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6bde1-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)