---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 7ec4ebbe9e1224e47605a35f7f21feb2dfbcf045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451435"
---
# <span data-ttu-id="7e380-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7e380-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="7e380-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e380-102">SYNOPSIS</span></span>
<span data-ttu-id="7e380-103">取得從指定位置到 Azure 區域的 internet 服務提供者相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="7e380-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e380-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e380-104">SYNTAX</span></span>

### <span data-ttu-id="7e380-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="7e380-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e380-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7e380-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e380-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e380-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e380-108">說明</span><span class="sxs-lookup"><span data-stu-id="7e380-108">DESCRIPTION</span></span>
<span data-ttu-id="7e380-109">Get-AzureRmNetworkWatcherReachabilityReport 會取得從指定位置到 Azure 區域的 internet 服務提供者相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="7e380-109">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="7e380-110">示例</span><span class="sxs-lookup"><span data-stu-id="7e380-110">EXAMPLES</span></span>

### <span data-ttu-id="7e380-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7e380-111">Example 1</span></span>
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

<span data-ttu-id="7e380-112">在美國境內2017-10-10 到2017-10-12 的 Microsoft 西部中，取得對 Azure 資料中心的相對延遲。</span><span class="sxs-lookup"><span data-stu-id="7e380-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="7e380-113">參數</span><span class="sxs-lookup"><span data-stu-id="7e380-113">PARAMETERS</span></span>

### <span data-ttu-id="7e380-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e380-114">-AsJob</span></span>
<span data-ttu-id="7e380-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e380-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e380-116">-城市</span><span class="sxs-lookup"><span data-stu-id="7e380-116">-City</span></span>
<span data-ttu-id="7e380-117">城市的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e380-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e380-118">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="7e380-118">-Country</span></span>
<span data-ttu-id="7e380-119">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e380-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e380-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e380-120">-DefaultProfile</span></span>
<span data-ttu-id="7e380-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e380-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e380-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7e380-122">-EndTime</span></span>
<span data-ttu-id="7e380-123">Azure 可存取性報告的結束時間。</span><span class="sxs-lookup"><span data-stu-id="7e380-123">The end time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e380-124">-位置</span><span class="sxs-lookup"><span data-stu-id="7e380-124">-Location</span></span>
<span data-ttu-id="7e380-125">要將查詢範圍限定在其中的選用 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="7e380-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="7e380-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7e380-126">-NetworkWatcher</span></span>
<span data-ttu-id="7e380-127">網路觀察程式資源</span><span class="sxs-lookup"><span data-stu-id="7e380-127">The network watcher resource</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e380-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7e380-128">-NetworkWatcherName</span></span>
<span data-ttu-id="7e380-129">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e380-129">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e380-130">-提供者</span><span class="sxs-lookup"><span data-stu-id="7e380-130">-Provider</span></span>
<span data-ttu-id="7e380-131">網際網路服務提供者清單。</span><span class="sxs-lookup"><span data-stu-id="7e380-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="7e380-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e380-132">-ResourceGroupName</span></span>
<span data-ttu-id="7e380-133">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e380-133">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e380-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e380-134">-ResourceId</span></span>
<span data-ttu-id="7e380-135">網路觀察程式資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e380-135">The Id of network watcher resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e380-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7e380-136">-StartTime</span></span>
<span data-ttu-id="7e380-137">Azure 可存取性報告的開始時間。</span><span class="sxs-lookup"><span data-stu-id="7e380-137">The start time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e380-138">-State</span><span class="sxs-lookup"><span data-stu-id="7e380-138">-State</span></span>
<span data-ttu-id="7e380-139">狀態的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e380-139">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e380-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e380-140">CommonParameters</span></span>
<span data-ttu-id="7e380-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e380-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e380-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7e380-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e380-143">輸入</span><span class="sxs-lookup"><span data-stu-id="7e380-143">INPUTS</span></span>

### <span data-ttu-id="7e380-144">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7e380-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7e380-145">System.object</span><span class="sxs-lookup"><span data-stu-id="7e380-145">System.String</span></span>

## <span data-ttu-id="7e380-146">輸出</span><span class="sxs-lookup"><span data-stu-id="7e380-146">OUTPUTS</span></span>

### <span data-ttu-id="7e380-147">PSAzureReachabilityReport 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7e380-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="7e380-148">筆記</span><span class="sxs-lookup"><span data-stu-id="7e380-148">NOTES</span></span>
<span data-ttu-id="7e380-149">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，可存取性，報告</span><span class="sxs-lookup"><span data-stu-id="7e380-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="7e380-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e380-150">RELATED LINKS</span></span>

[<span data-ttu-id="7e380-151">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7e380-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7e380-152">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7e380-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7e380-153">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7e380-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7e380-154">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7e380-154">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7e380-155">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7e380-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7e380-156">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7e380-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7e380-157">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7e380-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7e380-158">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7e380-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7e380-159">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7e380-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7e380-160">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7e380-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7e380-161">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7e380-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7e380-162">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7e380-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)