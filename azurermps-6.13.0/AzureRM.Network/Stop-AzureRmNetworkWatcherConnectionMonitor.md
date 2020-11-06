---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 3cb69a6dbf2a08c242d0a49e6d023692663b7f19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450216"
---
# <span data-ttu-id="d25e4-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d25e4-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="d25e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d25e4-102">SYNOPSIS</span></span>
<span data-ttu-id="d25e4-103">停止連線監視器</span><span class="sxs-lookup"><span data-stu-id="d25e4-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d25e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="d25e4-104">SYNTAX</span></span>

### <span data-ttu-id="d25e4-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="d25e4-105">SetByName (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d25e4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d25e4-106">SetByResource</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d25e4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d25e4-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d25e4-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d25e4-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d25e4-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="d25e4-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d25e4-110">說明</span><span class="sxs-lookup"><span data-stu-id="d25e4-110">DESCRIPTION</span></span>
<span data-ttu-id="d25e4-111">Stop-AzureRmNetworkWatcherConnectionMonitor Cmdlet 會停止指定的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="d25e4-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="d25e4-112">示例</span><span class="sxs-lookup"><span data-stu-id="d25e4-112">EXAMPLES</span></span>

### <span data-ttu-id="d25e4-113">範例1：停止連線監視器</span><span class="sxs-lookup"><span data-stu-id="d25e4-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="d25e4-114">在這個範例中，我們會停止由名稱和網路觀察程式指定的連線監視器</span><span class="sxs-lookup"><span data-stu-id="d25e4-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="d25e4-115">參數</span><span class="sxs-lookup"><span data-stu-id="d25e4-115">PARAMETERS</span></span>

### <span data-ttu-id="d25e4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d25e4-116">-AsJob</span></span>
<span data-ttu-id="d25e4-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d25e4-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25e4-118">-DefaultProfile</span></span>
<span data-ttu-id="d25e4-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d25e4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d25e4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d25e4-120">-InputObject</span></span>
<span data-ttu-id="d25e4-121">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="d25e4-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d25e4-122">-位置</span><span class="sxs-lookup"><span data-stu-id="d25e4-122">-Location</span></span>
<span data-ttu-id="d25e4-123">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="d25e4-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d25e4-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d25e4-124">-Name</span></span>
<span data-ttu-id="d25e4-125">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="d25e4-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25e4-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d25e4-126">-NetworkWatcher</span></span>
<span data-ttu-id="d25e4-127">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="d25e4-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="d25e4-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d25e4-128">-NetworkWatcherName</span></span>
<span data-ttu-id="d25e4-129">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d25e4-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="d25e4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d25e4-130">-PassThru</span></span>
<span data-ttu-id="d25e4-131">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="d25e4-131">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25e4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d25e4-132">-ResourceGroupName</span></span>
<span data-ttu-id="d25e4-133">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d25e4-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d25e4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d25e4-134">-ResourceId</span></span>
<span data-ttu-id="d25e4-135">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d25e4-135">Resource ID.</span></span>

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

### <span data-ttu-id="d25e4-136">-確認</span><span class="sxs-lookup"><span data-stu-id="d25e4-136">-Confirm</span></span>
<span data-ttu-id="d25e4-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d25e4-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25e4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d25e4-138">-WhatIf</span></span>
<span data-ttu-id="d25e4-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d25e4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d25e4-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d25e4-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25e4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25e4-141">CommonParameters</span></span>
<span data-ttu-id="d25e4-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d25e4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25e4-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d25e4-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25e4-144">輸入</span><span class="sxs-lookup"><span data-stu-id="d25e4-144">INPUTS</span></span>

### <span data-ttu-id="d25e4-145">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d25e4-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d25e4-146">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="d25e4-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="d25e4-147">System.object</span><span class="sxs-lookup"><span data-stu-id="d25e4-147">System.String</span></span>

### <span data-ttu-id="d25e4-148">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d25e4-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="d25e4-149">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="d25e4-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d25e4-150">輸出</span><span class="sxs-lookup"><span data-stu-id="d25e4-150">OUTPUTS</span></span>

### <span data-ttu-id="d25e4-151">System.object</span><span class="sxs-lookup"><span data-stu-id="d25e4-151">System.Boolean</span></span>

## <span data-ttu-id="d25e4-152">筆記</span><span class="sxs-lookup"><span data-stu-id="d25e4-152">NOTES</span></span>
<span data-ttu-id="d25e4-153">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="d25e4-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="d25e4-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="d25e4-154">RELATED LINKS</span></span>

[<span data-ttu-id="d25e4-155">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d25e4-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="d25e4-156">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d25e4-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="d25e4-157">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d25e4-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="d25e4-158">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d25e4-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="d25e4-159">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d25e4-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="d25e4-160">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d25e4-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="d25e4-161">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d25e4-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="d25e4-162">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d25e4-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d25e4-163">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d25e4-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="d25e4-164">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d25e4-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d25e4-165">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d25e4-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d25e4-166">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d25e4-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="d25e4-167">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d25e4-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d25e4-168">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d25e4-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="d25e4-169">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d25e4-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d25e4-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d25e4-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d25e4-171">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d25e4-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d25e4-172">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d25e4-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d25e4-173">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d25e4-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="d25e4-174">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d25e4-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="d25e4-175">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d25e4-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="d25e4-176">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d25e4-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="d25e4-177">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d25e4-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="d25e4-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d25e4-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="d25e4-179">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d25e4-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="d25e4-180">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d25e4-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="d25e4-181">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d25e4-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
