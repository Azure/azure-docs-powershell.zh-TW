---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a4e9c9a928d3a6c3ddeb7afa754cc957089a2283
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137859"
---
# <span data-ttu-id="1a309-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1a309-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="1a309-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a309-102">SYNOPSIS</span></span>
<span data-ttu-id="1a309-103">列出指定 Azure 區域所有可用的網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="1a309-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="1a309-104">句法</span><span class="sxs-lookup"><span data-stu-id="1a309-104">SYNTAX</span></span>

### <span data-ttu-id="1a309-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="1a309-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a309-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1a309-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a309-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1a309-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a309-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a309-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a309-109">說明</span><span class="sxs-lookup"><span data-stu-id="1a309-109">DESCRIPTION</span></span>
<span data-ttu-id="1a309-110">Get-AzNetworkWatcherReachabilityProvidersList 會列出指定 Azure 區域所有可用的網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="1a309-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="1a309-111">示例</span><span class="sxs-lookup"><span data-stu-id="1a309-111">EXAMPLES</span></span>

### <span data-ttu-id="1a309-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1a309-112">Example 1</span></span>
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

<span data-ttu-id="1a309-113">在華盛頓州的 [北京] 中，列出所有在西雅圖、適用于 Azure 資料中心的可用提供者。</span><span class="sxs-lookup"><span data-stu-id="1a309-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="1a309-114">範例2</span><span class="sxs-lookup"><span data-stu-id="1a309-114">Example 2</span></span>

<span data-ttu-id="1a309-115">列出指定 Azure 區域所有可用的網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="1a309-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="1a309-116"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="1a309-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="1a309-117">參數</span><span class="sxs-lookup"><span data-stu-id="1a309-117">PARAMETERS</span></span>

### <span data-ttu-id="1a309-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a309-118">-AsJob</span></span>
<span data-ttu-id="1a309-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1a309-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a309-120">-城市</span><span class="sxs-lookup"><span data-stu-id="1a309-120">-City</span></span>
<span data-ttu-id="1a309-121">城市的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a309-121">The name of the city.</span></span>

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

### <span data-ttu-id="1a309-122">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="1a309-122">-Country</span></span>
<span data-ttu-id="1a309-123">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a309-123">The name of the country.</span></span>

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

### <span data-ttu-id="1a309-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a309-124">-DefaultProfile</span></span>
<span data-ttu-id="1a309-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a309-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a309-126">-位置</span><span class="sxs-lookup"><span data-stu-id="1a309-126">-Location</span></span>
<span data-ttu-id="1a309-127">要將查詢範圍限定在其中的選用 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="1a309-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="1a309-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a309-128">-NetworkWatcher</span></span>
<span data-ttu-id="1a309-129">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="1a309-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="1a309-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="1a309-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="1a309-131">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="1a309-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1a309-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1a309-132">-NetworkWatcherName</span></span>
<span data-ttu-id="1a309-133">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a309-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="1a309-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a309-134">-ResourceGroupName</span></span>
<span data-ttu-id="1a309-135">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a309-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1a309-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a309-136">-ResourceId</span></span>
<span data-ttu-id="1a309-137">網路觀察程式資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a309-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="1a309-138">-State</span><span class="sxs-lookup"><span data-stu-id="1a309-138">-State</span></span>
<span data-ttu-id="1a309-139">狀態的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a309-139">The name of the state.</span></span>

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

### <span data-ttu-id="1a309-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a309-140">CommonParameters</span></span>
<span data-ttu-id="1a309-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a309-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a309-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1a309-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a309-143">輸入</span><span class="sxs-lookup"><span data-stu-id="1a309-143">INPUTS</span></span>

### <span data-ttu-id="1a309-144">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1a309-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1a309-145">System.object</span><span class="sxs-lookup"><span data-stu-id="1a309-145">System.String</span></span>

## <span data-ttu-id="1a309-146">輸出</span><span class="sxs-lookup"><span data-stu-id="1a309-146">OUTPUTS</span></span>

### <span data-ttu-id="1a309-147">PSAvailableProvidersList 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1a309-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="1a309-148">筆記</span><span class="sxs-lookup"><span data-stu-id="1a309-148">NOTES</span></span>
<span data-ttu-id="1a309-149">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，下一步，hop</span><span class="sxs-lookup"><span data-stu-id="1a309-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="1a309-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a309-150">RELATED LINKS</span></span>

[<span data-ttu-id="1a309-151">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a309-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1a309-152">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a309-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1a309-153">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a309-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1a309-154">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1a309-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1a309-155">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1a309-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1a309-156">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1a309-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1a309-157">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1a309-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1a309-158">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a309-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a309-159">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1a309-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1a309-160">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a309-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a309-161">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a309-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a309-162">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a309-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a309-163">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a309-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1a309-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1a309-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1a309-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1a309-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1a309-166">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a309-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a309-167">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a309-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a309-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a309-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a309-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1a309-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1a309-170">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a309-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a309-171">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a309-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a309-172">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1a309-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1a309-173">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1a309-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1a309-174">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1a309-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1a309-175">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1a309-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1a309-176">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1a309-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1a309-177">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a309-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
