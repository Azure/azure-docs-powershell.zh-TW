---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: e49245fabd4387c48def797168e1d572a43d6bfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447739"
---
# <span data-ttu-id="c0650-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0650-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="c0650-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0650-102">SYNOPSIS</span></span>
<span data-ttu-id="c0650-103">停止連線監視器</span><span class="sxs-lookup"><span data-stu-id="c0650-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0650-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0650-104">SYNTAX</span></span>

### <span data-ttu-id="c0650-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="c0650-105">SetByName (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0650-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c0650-106">SetByResource</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0650-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c0650-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0650-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0650-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0650-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0650-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0650-110">說明</span><span class="sxs-lookup"><span data-stu-id="c0650-110">DESCRIPTION</span></span>
<span data-ttu-id="c0650-111">Stop-AzureRmNetworkWatcherConnectionMonitor Cmdlet 會停止指定的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="c0650-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="c0650-112">示例</span><span class="sxs-lookup"><span data-stu-id="c0650-112">EXAMPLES</span></span>

### <span data-ttu-id="c0650-113">範例1：停止連線監視器</span><span class="sxs-lookup"><span data-stu-id="c0650-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="c0650-114">在這個範例中，我們會停止由名稱和網路觀察程式指定的連線監視器</span><span class="sxs-lookup"><span data-stu-id="c0650-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="c0650-115">參數</span><span class="sxs-lookup"><span data-stu-id="c0650-115">PARAMETERS</span></span>

### <span data-ttu-id="c0650-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0650-116">-AsJob</span></span>
<span data-ttu-id="c0650-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c0650-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0650-118">-確認</span><span class="sxs-lookup"><span data-stu-id="c0650-118">-Confirm</span></span>
<span data-ttu-id="c0650-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0650-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0650-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0650-120">-DefaultProfile</span></span>
<span data-ttu-id="c0650-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0650-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0650-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0650-122">-InputObject</span></span>
<span data-ttu-id="c0650-123">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="c0650-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0650-124">-位置</span><span class="sxs-lookup"><span data-stu-id="c0650-124">-Location</span></span>
<span data-ttu-id="c0650-125">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="c0650-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0650-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0650-126">-Name</span></span>
<span data-ttu-id="c0650-127">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="c0650-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0650-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0650-128">-NetworkWatcher</span></span>
<span data-ttu-id="c0650-129">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="c0650-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="c0650-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c0650-130">-NetworkWatcherName</span></span>
<span data-ttu-id="c0650-131">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0650-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="c0650-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0650-132">-PassThru</span></span>
<span data-ttu-id="c0650-133">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="c0650-133">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0650-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0650-134">-ResourceGroupName</span></span>
<span data-ttu-id="c0650-135">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0650-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c0650-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0650-136">-ResourceId</span></span>
<span data-ttu-id="c0650-137">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c0650-137">Resource ID.</span></span>

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

### <span data-ttu-id="c0650-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0650-138">-WhatIf</span></span>
<span data-ttu-id="c0650-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0650-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0650-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0650-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0650-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0650-141">CommonParameters</span></span>
<span data-ttu-id="c0650-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0650-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c0650-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0650-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0650-144">輸入</span><span class="sxs-lookup"><span data-stu-id="c0650-144">INPUTS</span></span>

### <span data-ttu-id="c0650-145">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c0650-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c0650-146">PSConnectionMonitorResult 中的 [system.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="c0650-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="c0650-147">輸出</span><span class="sxs-lookup"><span data-stu-id="c0650-147">OUTPUTS</span></span>

### <span data-ttu-id="c0650-148">System.object</span><span class="sxs-lookup"><span data-stu-id="c0650-148">System.Boolean</span></span>

## <span data-ttu-id="c0650-149">筆記</span><span class="sxs-lookup"><span data-stu-id="c0650-149">NOTES</span></span>
<span data-ttu-id="c0650-150">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="c0650-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="c0650-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0650-151">RELATED LINKS</span></span>

[<span data-ttu-id="c0650-152">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0650-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="c0650-153">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0650-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="c0650-154">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0650-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="c0650-155">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c0650-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="c0650-156">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c0650-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="c0650-157">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c0650-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="c0650-158">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c0650-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="c0650-159">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0650-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="c0650-160">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c0650-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="c0650-161">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0650-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="c0650-162">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0650-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="c0650-163">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0650-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="c0650-164">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0650-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c0650-165">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0650-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c0650-166">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c0650-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="c0650-167">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0650-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c0650-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0650-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c0650-169">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0650-169">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
