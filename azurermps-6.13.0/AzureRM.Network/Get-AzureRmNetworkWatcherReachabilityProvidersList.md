---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 4cb80bec513459797790ae04c3e26a2f25fe95db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451143"
---
# <span data-ttu-id="7615f-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7615f-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="7615f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7615f-102">SYNOPSIS</span></span>
<span data-ttu-id="7615f-103">列出指定 Azure 區域所有可用的網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="7615f-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7615f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7615f-104">SYNTAX</span></span>

### <span data-ttu-id="7615f-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="7615f-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7615f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7615f-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7615f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7615f-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7615f-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7615f-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7615f-109">說明</span><span class="sxs-lookup"><span data-stu-id="7615f-109">DESCRIPTION</span></span>
<span data-ttu-id="7615f-110">Get-AzureRmNetworkWatcherReachabilityProvidersList 會列出指定 Azure 區域所有可用的網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="7615f-110">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="7615f-111">示例</span><span class="sxs-lookup"><span data-stu-id="7615f-111">EXAMPLES</span></span>

### <span data-ttu-id="7615f-112">範例1</span><span class="sxs-lookup"><span data-stu-id="7615f-112">Example 1</span></span>
```
PS C:\> $nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

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

<span data-ttu-id="7615f-113">在華盛頓州的 [北京] 中，列出所有在西雅圖、適用于 Azure 資料中心的可用提供者。</span><span class="sxs-lookup"><span data-stu-id="7615f-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="7615f-114">參數</span><span class="sxs-lookup"><span data-stu-id="7615f-114">PARAMETERS</span></span>

### <span data-ttu-id="7615f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7615f-115">-AsJob</span></span>
<span data-ttu-id="7615f-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7615f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7615f-117">-城市</span><span class="sxs-lookup"><span data-stu-id="7615f-117">-City</span></span>
<span data-ttu-id="7615f-118">城市的名稱。</span><span class="sxs-lookup"><span data-stu-id="7615f-118">The name of the city.</span></span>

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

### <span data-ttu-id="7615f-119">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="7615f-119">-Country</span></span>
<span data-ttu-id="7615f-120">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="7615f-120">The name of the country.</span></span>

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

### <span data-ttu-id="7615f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7615f-121">-DefaultProfile</span></span>
<span data-ttu-id="7615f-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7615f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7615f-123">-位置</span><span class="sxs-lookup"><span data-stu-id="7615f-123">-Location</span></span>
<span data-ttu-id="7615f-124">要將查詢範圍限定在其中的選用 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="7615f-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="7615f-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7615f-125">-NetworkWatcher</span></span>
<span data-ttu-id="7615f-126">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="7615f-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="7615f-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="7615f-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="7615f-128">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="7615f-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7615f-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7615f-129">-NetworkWatcherName</span></span>
<span data-ttu-id="7615f-130">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="7615f-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="7615f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7615f-131">-ResourceGroupName</span></span>
<span data-ttu-id="7615f-132">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7615f-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7615f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7615f-133">-ResourceId</span></span>
<span data-ttu-id="7615f-134">網路觀察程式資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7615f-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="7615f-135">-State</span><span class="sxs-lookup"><span data-stu-id="7615f-135">-State</span></span>
<span data-ttu-id="7615f-136">狀態的名稱。</span><span class="sxs-lookup"><span data-stu-id="7615f-136">The name of the state.</span></span>

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

### <span data-ttu-id="7615f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7615f-137">CommonParameters</span></span>
<span data-ttu-id="7615f-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7615f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7615f-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7615f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7615f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7615f-140">INPUTS</span></span>

### <span data-ttu-id="7615f-141">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7615f-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7615f-142">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="7615f-142">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="7615f-143">System.object</span><span class="sxs-lookup"><span data-stu-id="7615f-143">System.String</span></span>

## <span data-ttu-id="7615f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="7615f-144">OUTPUTS</span></span>

### <span data-ttu-id="7615f-145">PSAvailableProvidersList 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7615f-145">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="7615f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="7615f-146">NOTES</span></span>
<span data-ttu-id="7615f-147">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，下一步，hop</span><span class="sxs-lookup"><span data-stu-id="7615f-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="7615f-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="7615f-148">RELATED LINKS</span></span>

[<span data-ttu-id="7615f-149">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7615f-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7615f-150">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7615f-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7615f-151">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7615f-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7615f-152">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7615f-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="7615f-153">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7615f-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7615f-154">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7615f-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7615f-155">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7615f-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7615f-156">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7615f-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7615f-157">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7615f-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7615f-158">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7615f-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7615f-159">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7615f-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7615f-160">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7615f-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7615f-161">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7615f-161">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7615f-162">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7615f-162">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7615f-163">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7615f-163">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="7615f-164">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7615f-164">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7615f-165">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7615f-165">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7615f-166">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7615f-166">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7615f-167">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7615f-167">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7615f-168">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7615f-168">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7615f-169">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7615f-169">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7615f-170">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7615f-170">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7615f-171">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7615f-171">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7615f-172">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7615f-172">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7615f-173">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7615f-173">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7615f-174">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7615f-174">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="7615f-175">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7615f-175">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
