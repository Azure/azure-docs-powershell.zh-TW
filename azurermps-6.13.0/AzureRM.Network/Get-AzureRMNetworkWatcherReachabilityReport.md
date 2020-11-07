---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 09d75e73cc6139bfa2c3d0d6293b07060a709f15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625791"
---
# <span data-ttu-id="58e55-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="58e55-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="58e55-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58e55-102">SYNOPSIS</span></span>
<span data-ttu-id="58e55-103">取得從指定位置到 Azure 區域的 internet 服務提供者相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="58e55-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58e55-104">句法</span><span class="sxs-lookup"><span data-stu-id="58e55-104">SYNTAX</span></span>

### <span data-ttu-id="58e55-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="58e55-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58e55-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="58e55-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58e55-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="58e55-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58e55-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="58e55-108">SetByLocation</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherLocation <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58e55-109">說明</span><span class="sxs-lookup"><span data-stu-id="58e55-109">DESCRIPTION</span></span>
<span data-ttu-id="58e55-110">Get-AzureRmNetworkWatcherReachabilityReport 會取得從指定位置到 Azure 區域的 internet 服務提供者相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="58e55-110">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="58e55-111">示例</span><span class="sxs-lookup"><span data-stu-id="58e55-111">EXAMPLES</span></span>

### <span data-ttu-id="58e55-112">範例1</span><span class="sxs-lookup"><span data-stu-id="58e55-112">Example 1</span></span>
```
$nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzureRmNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

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

<span data-ttu-id="58e55-113">在美國境內2017-10-10 到2017-10-12 的 Microsoft 西部中，取得對 Azure 資料中心的相對延遲。</span><span class="sxs-lookup"><span data-stu-id="58e55-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="58e55-114">參數</span><span class="sxs-lookup"><span data-stu-id="58e55-114">PARAMETERS</span></span>

### <span data-ttu-id="58e55-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58e55-115">-AsJob</span></span>
<span data-ttu-id="58e55-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="58e55-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58e55-117">-城市</span><span class="sxs-lookup"><span data-stu-id="58e55-117">-City</span></span>
<span data-ttu-id="58e55-118">城市的名稱。</span><span class="sxs-lookup"><span data-stu-id="58e55-118">The name of the city.</span></span>

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

### <span data-ttu-id="58e55-119">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="58e55-119">-Country</span></span>
<span data-ttu-id="58e55-120">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="58e55-120">The name of the country.</span></span>

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

### <span data-ttu-id="58e55-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e55-121">-DefaultProfile</span></span>
<span data-ttu-id="58e55-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58e55-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58e55-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="58e55-123">-EndTime</span></span>
<span data-ttu-id="58e55-124">Azure 可存取性報告的結束時間。</span><span class="sxs-lookup"><span data-stu-id="58e55-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="58e55-125">-位置</span><span class="sxs-lookup"><span data-stu-id="58e55-125">-Location</span></span>
<span data-ttu-id="58e55-126">要將查詢範圍限定在其中的選用 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="58e55-126">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e55-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58e55-127">-NetworkWatcher</span></span>
<span data-ttu-id="58e55-128">網路觀察程式資源</span><span class="sxs-lookup"><span data-stu-id="58e55-128">The network watcher resource</span></span>

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

### <span data-ttu-id="58e55-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="58e55-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="58e55-130">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="58e55-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="58e55-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="58e55-131">-NetworkWatcherName</span></span>
<span data-ttu-id="58e55-132">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="58e55-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="58e55-133">-提供者</span><span class="sxs-lookup"><span data-stu-id="58e55-133">-Provider</span></span>
<span data-ttu-id="58e55-134">網際網路服務提供者清單。</span><span class="sxs-lookup"><span data-stu-id="58e55-134">List of Internet service providers.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e55-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e55-135">-ResourceGroupName</span></span>
<span data-ttu-id="58e55-136">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58e55-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="58e55-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58e55-137">-ResourceId</span></span>
<span data-ttu-id="58e55-138">網路觀察程式資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="58e55-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="58e55-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="58e55-139">-StartTime</span></span>
<span data-ttu-id="58e55-140">Azure 可存取性報告的開始時間。</span><span class="sxs-lookup"><span data-stu-id="58e55-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="58e55-141">-State</span><span class="sxs-lookup"><span data-stu-id="58e55-141">-State</span></span>
<span data-ttu-id="58e55-142">狀態的名稱。</span><span class="sxs-lookup"><span data-stu-id="58e55-142">The name of the state.</span></span>

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

### <span data-ttu-id="58e55-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e55-143">CommonParameters</span></span>
<span data-ttu-id="58e55-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58e55-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e55-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58e55-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e55-146">輸入</span><span class="sxs-lookup"><span data-stu-id="58e55-146">INPUTS</span></span>

### <span data-ttu-id="58e55-147">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="58e55-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="58e55-148">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="58e55-148">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="58e55-149">System.object</span><span class="sxs-lookup"><span data-stu-id="58e55-149">System.String</span></span>

## <span data-ttu-id="58e55-150">輸出</span><span class="sxs-lookup"><span data-stu-id="58e55-150">OUTPUTS</span></span>

### <span data-ttu-id="58e55-151">PSAzureReachabilityReport 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="58e55-151">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="58e55-152">筆記</span><span class="sxs-lookup"><span data-stu-id="58e55-152">NOTES</span></span>
<span data-ttu-id="58e55-153">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，可存取性，報告</span><span class="sxs-lookup"><span data-stu-id="58e55-153">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="58e55-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="58e55-154">RELATED LINKS</span></span>

[<span data-ttu-id="58e55-155">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58e55-155">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="58e55-156">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58e55-156">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="58e55-157">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58e55-157">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="58e55-158">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="58e55-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="58e55-159">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="58e55-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="58e55-160">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="58e55-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="58e55-161">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="58e55-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="58e55-162">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58e55-162">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="58e55-163">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="58e55-163">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="58e55-164">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58e55-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="58e55-165">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58e55-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="58e55-166">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58e55-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="58e55-167">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="58e55-167">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="58e55-168">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="58e55-168">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="58e55-169">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="58e55-169">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="58e55-170">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="58e55-170">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="58e55-171">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="58e55-171">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="58e55-172">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="58e55-172">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="58e55-173">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="58e55-173">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="58e55-174">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="58e55-174">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="58e55-175">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="58e55-175">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="58e55-176">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="58e55-176">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="58e55-177">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="58e55-177">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="58e55-178">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="58e55-178">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="58e55-179">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="58e55-179">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="58e55-180">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="58e55-180">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="58e55-181">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="58e55-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
