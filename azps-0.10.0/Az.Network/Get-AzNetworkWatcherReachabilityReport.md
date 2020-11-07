---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 6da0a36ee5e394008ea1d1de4a16f7982227ca06
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794383"
---
# <span data-ttu-id="10257-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="10257-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="10257-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10257-102">SYNOPSIS</span></span>
<span data-ttu-id="10257-103">取得從指定位置到 Azure 區域的 internet 服務提供者相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="10257-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="10257-104">句法</span><span class="sxs-lookup"><span data-stu-id="10257-104">SYNTAX</span></span>

### <span data-ttu-id="10257-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="10257-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10257-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="10257-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10257-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="10257-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10257-108">說明</span><span class="sxs-lookup"><span data-stu-id="10257-108">DESCRIPTION</span></span>
<span data-ttu-id="10257-109">Get-AzNetworkWatcherReachabilityReport 會取得從指定位置到 Azure 區域的 internet 服務提供者相對延遲分數。</span><span class="sxs-lookup"><span data-stu-id="10257-109">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="10257-110">示例</span><span class="sxs-lookup"><span data-stu-id="10257-110">EXAMPLES</span></span>

### <span data-ttu-id="10257-111">範例1</span><span class="sxs-lookup"><span data-stu-id="10257-111">Example 1</span></span>
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

<span data-ttu-id="10257-112">在美國境內2017-10-10 到2017-10-12 的 Microsoft 西部中，取得對 Azure 資料中心的相對延遲。</span><span class="sxs-lookup"><span data-stu-id="10257-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="10257-113">參數</span><span class="sxs-lookup"><span data-stu-id="10257-113">PARAMETERS</span></span>

### <span data-ttu-id="10257-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10257-114">-AsJob</span></span>
<span data-ttu-id="10257-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="10257-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10257-116">-城市</span><span class="sxs-lookup"><span data-stu-id="10257-116">-City</span></span>
<span data-ttu-id="10257-117">城市的名稱。</span><span class="sxs-lookup"><span data-stu-id="10257-117">The name of the city.</span></span>

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

### <span data-ttu-id="10257-118">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="10257-118">-Country</span></span>
<span data-ttu-id="10257-119">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="10257-119">The name of the country.</span></span>

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

### <span data-ttu-id="10257-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10257-120">-DefaultProfile</span></span>
<span data-ttu-id="10257-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10257-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10257-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="10257-122">-EndTime</span></span>
<span data-ttu-id="10257-123">Azure 可存取性報告的結束時間。</span><span class="sxs-lookup"><span data-stu-id="10257-123">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="10257-124">-位置</span><span class="sxs-lookup"><span data-stu-id="10257-124">-Location</span></span>
<span data-ttu-id="10257-125">要將查詢範圍限定在其中的選用 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="10257-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="10257-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="10257-126">-NetworkWatcher</span></span>
<span data-ttu-id="10257-127">網路觀察程式資源</span><span class="sxs-lookup"><span data-stu-id="10257-127">The network watcher resource</span></span>

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

### <span data-ttu-id="10257-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="10257-128">-NetworkWatcherName</span></span>
<span data-ttu-id="10257-129">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="10257-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="10257-130">-提供者</span><span class="sxs-lookup"><span data-stu-id="10257-130">-Provider</span></span>
<span data-ttu-id="10257-131">網際網路服務提供者清單。</span><span class="sxs-lookup"><span data-stu-id="10257-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="10257-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10257-132">-ResourceGroupName</span></span>
<span data-ttu-id="10257-133">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="10257-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="10257-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10257-134">-ResourceId</span></span>
<span data-ttu-id="10257-135">網路觀察程式資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="10257-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="10257-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="10257-136">-StartTime</span></span>
<span data-ttu-id="10257-137">Azure 可存取性報告的開始時間。</span><span class="sxs-lookup"><span data-stu-id="10257-137">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="10257-138">-State</span><span class="sxs-lookup"><span data-stu-id="10257-138">-State</span></span>
<span data-ttu-id="10257-139">狀態的名稱。</span><span class="sxs-lookup"><span data-stu-id="10257-139">The name of the state.</span></span>

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

### <span data-ttu-id="10257-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10257-140">CommonParameters</span></span>
<span data-ttu-id="10257-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10257-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10257-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10257-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10257-143">輸入</span><span class="sxs-lookup"><span data-stu-id="10257-143">INPUTS</span></span>

### <span data-ttu-id="10257-144">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="10257-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="10257-145">System.object</span><span class="sxs-lookup"><span data-stu-id="10257-145">System.String</span></span>

## <span data-ttu-id="10257-146">輸出</span><span class="sxs-lookup"><span data-stu-id="10257-146">OUTPUTS</span></span>

### <span data-ttu-id="10257-147">PSAzureReachabilityReport 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="10257-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="10257-148">筆記</span><span class="sxs-lookup"><span data-stu-id="10257-148">NOTES</span></span>
<span data-ttu-id="10257-149">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，可存取性，報告</span><span class="sxs-lookup"><span data-stu-id="10257-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="10257-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="10257-150">RELATED LINKS</span></span>

[<span data-ttu-id="10257-151">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="10257-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="10257-152">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="10257-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="10257-153">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="10257-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="10257-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="10257-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="10257-155">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="10257-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="10257-156">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="10257-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="10257-157">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="10257-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="10257-158">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="10257-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="10257-159">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="10257-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="10257-160">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="10257-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="10257-161">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="10257-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="10257-162">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="10257-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
