---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 7f9417fe4ad6e115e73502e953dfcab965ccd17b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446717"
---
# <span data-ttu-id="107d1-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="107d1-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="107d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="107d1-102">SYNOPSIS</span></span>
<span data-ttu-id="107d1-103">移除 [資料包捕獲資源]。</span><span class="sxs-lookup"><span data-stu-id="107d1-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="107d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="107d1-104">SYNTAX</span></span>

### <span data-ttu-id="107d1-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="107d1-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="107d1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="107d1-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="107d1-107">說明</span><span class="sxs-lookup"><span data-stu-id="107d1-107">DESCRIPTION</span></span>
<span data-ttu-id="107d1-108">Remove-AzureRmNetworkWatcherPacketCapture 會移除 [資料包捕獲資源]。</span><span class="sxs-lookup"><span data-stu-id="107d1-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="107d1-109">建議您先呼叫 Stop-AzureRmNetworkWatcherPacketCapture，然後再呼叫 AzureRmNetworkWatcherPacketCapture。</span><span class="sxs-lookup"><span data-stu-id="107d1-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="107d1-110">如果 Remove-AzureRmNetworkWatcherPacketCapture 稱為 [資料包捕獲會話]，則可能無法儲存 [資料包捕獲]。</span><span class="sxs-lookup"><span data-stu-id="107d1-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="107d1-111">如果在移除前停止會話，則不會移除內含捕獲資料的 .cap 檔案。</span><span class="sxs-lookup"><span data-stu-id="107d1-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="107d1-112">示例</span><span class="sxs-lookup"><span data-stu-id="107d1-112">EXAMPLES</span></span>

### <span data-ttu-id="107d1-113">---範例1：移除資料包捕獲會話--</span><span class="sxs-lookup"><span data-stu-id="107d1-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="107d1-114">在這個範例中，我們會移除名為 "PacketCaptureTest" 的現有資料包捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="107d1-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="107d1-115">參數</span><span class="sxs-lookup"><span data-stu-id="107d1-115">PARAMETERS</span></span>

### <span data-ttu-id="107d1-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="107d1-116">-NetworkWatcher</span></span>
<span data-ttu-id="107d1-117">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="107d1-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="107d1-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="107d1-118">-NetworkWatcherName</span></span>
<span data-ttu-id="107d1-119">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="107d1-119">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="107d1-120">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="107d1-120">-PacketCaptureName</span></span>
<span data-ttu-id="107d1-121">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="107d1-121">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107d1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="107d1-122">-PassThru</span></span>
<span data-ttu-id="107d1-123">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="107d1-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="107d1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107d1-124">-ResourceGroupName</span></span>
<span data-ttu-id="107d1-125">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="107d1-125">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107d1-126">-確認</span><span class="sxs-lookup"><span data-stu-id="107d1-126">-Confirm</span></span>
<span data-ttu-id="107d1-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="107d1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="107d1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="107d1-128">-WhatIf</span></span>
<span data-ttu-id="107d1-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="107d1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="107d1-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="107d1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="107d1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107d1-131">-DefaultProfile</span></span>
<span data-ttu-id="107d1-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="107d1-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="107d1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107d1-133">CommonParameters</span></span>
<span data-ttu-id="107d1-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="107d1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107d1-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="107d1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107d1-136">輸入</span><span class="sxs-lookup"><span data-stu-id="107d1-136">INPUTS</span></span>

### <span data-ttu-id="107d1-137">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="107d1-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="107d1-138">System.object</span><span class="sxs-lookup"><span data-stu-id="107d1-138">System.String</span></span>

## <span data-ttu-id="107d1-139">輸出</span><span class="sxs-lookup"><span data-stu-id="107d1-139">OUTPUTS</span></span>

### <span data-ttu-id="107d1-140">System.object</span><span class="sxs-lookup"><span data-stu-id="107d1-140">System.Object</span></span>

## <span data-ttu-id="107d1-141">筆記</span><span class="sxs-lookup"><span data-stu-id="107d1-141">NOTES</span></span>
<span data-ttu-id="107d1-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量，移除</span><span class="sxs-lookup"><span data-stu-id="107d1-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="107d1-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="107d1-143">RELATED LINKS</span></span>

[<span data-ttu-id="107d1-144">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="107d1-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="107d1-145">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="107d1-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="107d1-146">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="107d1-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="107d1-147">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="107d1-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="107d1-148">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="107d1-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="107d1-149">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="107d1-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="107d1-150">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="107d1-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="107d1-151">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="107d1-151">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="107d1-152">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="107d1-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="107d1-153">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="107d1-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="107d1-154">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="107d1-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="107d1-155">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="107d1-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
