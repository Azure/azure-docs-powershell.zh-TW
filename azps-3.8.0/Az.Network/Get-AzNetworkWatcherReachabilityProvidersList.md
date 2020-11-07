---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a2c66f9e93a26c433c245f87c8506b71ad01c5e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797562"
---
# <span data-ttu-id="cb272-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cb272-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="cb272-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb272-102">SYNOPSIS</span></span>
<span data-ttu-id="cb272-103">列出指定 Azure 區域所有可用的網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="cb272-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="cb272-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb272-104">SYNTAX</span></span>

### <span data-ttu-id="cb272-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="cb272-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb272-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cb272-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb272-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cb272-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb272-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cb272-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb272-109">說明</span><span class="sxs-lookup"><span data-stu-id="cb272-109">DESCRIPTION</span></span>
<span data-ttu-id="cb272-110">Get-AzNetworkWatcherReachabilityProvidersList 會列出指定 Azure 區域所有可用的網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="cb272-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="cb272-111">示例</span><span class="sxs-lookup"><span data-stu-id="cb272-111">EXAMPLES</span></span>

### <span data-ttu-id="cb272-112">範例1</span><span class="sxs-lookup"><span data-stu-id="cb272-112">Example 1</span></span>
```
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

<span data-ttu-id="cb272-113">在華盛頓州的 [北京] 中，列出所有在西雅圖、適用于 Azure 資料中心的可用提供者。</span><span class="sxs-lookup"><span data-stu-id="cb272-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="cb272-114">參數</span><span class="sxs-lookup"><span data-stu-id="cb272-114">PARAMETERS</span></span>

### <span data-ttu-id="cb272-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb272-115">-AsJob</span></span>
<span data-ttu-id="cb272-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb272-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb272-117">-城市</span><span class="sxs-lookup"><span data-stu-id="cb272-117">-City</span></span>
<span data-ttu-id="cb272-118">城市的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb272-118">The name of the city.</span></span>

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

### <span data-ttu-id="cb272-119">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="cb272-119">-Country</span></span>
<span data-ttu-id="cb272-120">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb272-120">The name of the country.</span></span>

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

### <span data-ttu-id="cb272-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb272-121">-DefaultProfile</span></span>
<span data-ttu-id="cb272-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb272-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb272-123">-位置</span><span class="sxs-lookup"><span data-stu-id="cb272-123">-Location</span></span>
<span data-ttu-id="cb272-124">要將查詢範圍限定在其中的選用 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="cb272-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="cb272-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cb272-125">-NetworkWatcher</span></span>
<span data-ttu-id="cb272-126">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="cb272-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="cb272-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="cb272-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="cb272-128">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="cb272-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cb272-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cb272-129">-NetworkWatcherName</span></span>
<span data-ttu-id="cb272-130">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb272-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="cb272-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb272-131">-ResourceGroupName</span></span>
<span data-ttu-id="cb272-132">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb272-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cb272-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb272-133">-ResourceId</span></span>
<span data-ttu-id="cb272-134">網路觀察程式資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb272-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="cb272-135">-State</span><span class="sxs-lookup"><span data-stu-id="cb272-135">-State</span></span>
<span data-ttu-id="cb272-136">狀態的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb272-136">The name of the state.</span></span>

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

### <span data-ttu-id="cb272-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb272-137">CommonParameters</span></span>
<span data-ttu-id="cb272-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb272-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb272-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb272-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb272-140">輸入</span><span class="sxs-lookup"><span data-stu-id="cb272-140">INPUTS</span></span>

### <span data-ttu-id="cb272-141">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cb272-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="cb272-142">System.object</span><span class="sxs-lookup"><span data-stu-id="cb272-142">System.String</span></span>

## <span data-ttu-id="cb272-143">輸出</span><span class="sxs-lookup"><span data-stu-id="cb272-143">OUTPUTS</span></span>

### <span data-ttu-id="cb272-144">PSAvailableProvidersList 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cb272-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="cb272-145">筆記</span><span class="sxs-lookup"><span data-stu-id="cb272-145">NOTES</span></span>
<span data-ttu-id="cb272-146">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，下一步，hop</span><span class="sxs-lookup"><span data-stu-id="cb272-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="cb272-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb272-147">RELATED LINKS</span></span>

[<span data-ttu-id="cb272-148">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cb272-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="cb272-149">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cb272-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="cb272-150">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cb272-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="cb272-151">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cb272-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="cb272-152">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cb272-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cb272-153">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cb272-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="cb272-154">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cb272-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cb272-155">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cb272-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cb272-156">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cb272-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="cb272-157">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cb272-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cb272-158">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cb272-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cb272-159">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cb272-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cb272-160">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb272-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="cb272-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cb272-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="cb272-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="cb272-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="cb272-163">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cb272-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cb272-164">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cb272-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cb272-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cb272-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cb272-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cb272-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="cb272-167">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cb272-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cb272-168">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cb272-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cb272-169">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cb272-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cb272-170">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cb272-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="cb272-171">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cb272-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="cb272-172">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="cb272-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="cb272-173">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cb272-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="cb272-174">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cb272-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
