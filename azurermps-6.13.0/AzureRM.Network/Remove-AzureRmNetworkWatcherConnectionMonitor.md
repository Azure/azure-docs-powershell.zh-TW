---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 01e8a41c8d8854527037c447545f3d0601d4daf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625778"
---
# <span data-ttu-id="46887-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46887-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="46887-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46887-102">SYNOPSIS</span></span>
<span data-ttu-id="46887-103">移除 [連接監視器]。</span><span class="sxs-lookup"><span data-stu-id="46887-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46887-104">句法</span><span class="sxs-lookup"><span data-stu-id="46887-104">SYNTAX</span></span>

### <span data-ttu-id="46887-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="46887-105">SetByName (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46887-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="46887-106">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46887-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="46887-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46887-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="46887-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46887-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="46887-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46887-110">說明</span><span class="sxs-lookup"><span data-stu-id="46887-110">DESCRIPTION</span></span>
<span data-ttu-id="46887-111">AzureRmNetworkWatcherConnectionMonitor Cmdlet 會移除指定的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="46887-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="46887-112">示例</span><span class="sxs-lookup"><span data-stu-id="46887-112">EXAMPLES</span></span>

### <span data-ttu-id="46887-113">範例1：移除指定的連接監視器</span><span class="sxs-lookup"><span data-stu-id="46887-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="46887-114">在這個範例中，我們會刪除由位置和名稱指定的連線監視器。</span><span class="sxs-lookup"><span data-stu-id="46887-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="46887-115">參數</span><span class="sxs-lookup"><span data-stu-id="46887-115">PARAMETERS</span></span>

### <span data-ttu-id="46887-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46887-116">-AsJob</span></span>
<span data-ttu-id="46887-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46887-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46887-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46887-118">-DefaultProfile</span></span>
<span data-ttu-id="46887-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46887-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46887-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46887-120">-InputObject</span></span>
<span data-ttu-id="46887-121">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="46887-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="46887-122">-位置</span><span class="sxs-lookup"><span data-stu-id="46887-122">-Location</span></span>
<span data-ttu-id="46887-123">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="46887-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="46887-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="46887-124">-Name</span></span>
<span data-ttu-id="46887-125">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="46887-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="46887-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46887-126">-NetworkWatcher</span></span>
<span data-ttu-id="46887-127">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="46887-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="46887-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="46887-128">-NetworkWatcherName</span></span>
<span data-ttu-id="46887-129">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="46887-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="46887-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46887-130">-PassThru</span></span>
<span data-ttu-id="46887-131">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="46887-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="46887-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46887-132">-ResourceGroupName</span></span>
<span data-ttu-id="46887-133">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="46887-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="46887-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46887-134">-ResourceId</span></span>
<span data-ttu-id="46887-135">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="46887-135">Resource ID.</span></span>

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

### <span data-ttu-id="46887-136">-確認</span><span class="sxs-lookup"><span data-stu-id="46887-136">-Confirm</span></span>
<span data-ttu-id="46887-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46887-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46887-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46887-138">-WhatIf</span></span>
<span data-ttu-id="46887-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46887-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46887-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46887-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46887-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46887-141">CommonParameters</span></span>
<span data-ttu-id="46887-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46887-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46887-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46887-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46887-144">輸入</span><span class="sxs-lookup"><span data-stu-id="46887-144">INPUTS</span></span>

### <span data-ttu-id="46887-145">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="46887-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="46887-146">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="46887-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="46887-147">System.object</span><span class="sxs-lookup"><span data-stu-id="46887-147">System.String</span></span>

### <span data-ttu-id="46887-148">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="46887-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="46887-149">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="46887-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="46887-150">輸出</span><span class="sxs-lookup"><span data-stu-id="46887-150">OUTPUTS</span></span>

### <span data-ttu-id="46887-151">System.object</span><span class="sxs-lookup"><span data-stu-id="46887-151">System.Boolean</span></span>

## <span data-ttu-id="46887-152">筆記</span><span class="sxs-lookup"><span data-stu-id="46887-152">NOTES</span></span>
<span data-ttu-id="46887-153">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="46887-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="46887-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="46887-154">RELATED LINKS</span></span>

[<span data-ttu-id="46887-155">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46887-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="46887-156">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46887-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="46887-157">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46887-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="46887-158">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="46887-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="46887-159">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="46887-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="46887-160">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="46887-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="46887-161">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="46887-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="46887-162">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46887-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="46887-163">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="46887-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="46887-164">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46887-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="46887-165">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46887-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="46887-166">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46887-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="46887-167">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46887-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="46887-168">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="46887-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="46887-169">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46887-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="46887-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46887-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="46887-171">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46887-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="46887-172">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46887-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="46887-173">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="46887-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="46887-174">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="46887-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="46887-175">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="46887-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="46887-176">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="46887-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="46887-177">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46887-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="46887-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="46887-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="46887-179">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="46887-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="46887-180">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="46887-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="46887-181">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="46887-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
