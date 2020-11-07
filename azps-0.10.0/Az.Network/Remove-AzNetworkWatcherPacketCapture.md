---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b3095aace7fa8e1959e51ef64aa92b6d2bcaffba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795499"
---
# <span data-ttu-id="029a5-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="029a5-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="029a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="029a5-102">SYNOPSIS</span></span>
<span data-ttu-id="029a5-103">移除 [資料包捕獲資源]。</span><span class="sxs-lookup"><span data-stu-id="029a5-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="029a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="029a5-104">SYNTAX</span></span>

### <span data-ttu-id="029a5-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="029a5-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="029a5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="029a5-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="029a5-107">說明</span><span class="sxs-lookup"><span data-stu-id="029a5-107">DESCRIPTION</span></span>
<span data-ttu-id="029a5-108">Remove-AzNetworkWatcherPacketCapture 會移除 [資料包捕獲資源]。</span><span class="sxs-lookup"><span data-stu-id="029a5-108">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="029a5-109">建議您先呼叫 Stop-AzNetworkWatcherPacketCapture，然後再呼叫 AzNetworkWatcherPacketCapture。</span><span class="sxs-lookup"><span data-stu-id="029a5-109">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="029a5-110">如果 Remove-AzNetworkWatcherPacketCapture 稱為 [資料包捕獲會話]，則可能無法儲存 [資料包捕獲]。</span><span class="sxs-lookup"><span data-stu-id="029a5-110">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="029a5-111">如果在移除前停止會話，則不會移除內含捕獲資料的 .cap 檔案。</span><span class="sxs-lookup"><span data-stu-id="029a5-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="029a5-112">示例</span><span class="sxs-lookup"><span data-stu-id="029a5-112">EXAMPLES</span></span>

### <span data-ttu-id="029a5-113">---範例1：移除資料包捕獲會話--</span><span class="sxs-lookup"><span data-stu-id="029a5-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="029a5-114">在這個範例中，我們會移除名為 "PacketCaptureTest" 的現有資料包捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="029a5-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="029a5-115">參數</span><span class="sxs-lookup"><span data-stu-id="029a5-115">PARAMETERS</span></span>

### <span data-ttu-id="029a5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="029a5-116">-AsJob</span></span>
<span data-ttu-id="029a5-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="029a5-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="029a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="029a5-118">-DefaultProfile</span></span>
<span data-ttu-id="029a5-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="029a5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="029a5-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="029a5-120">-NetworkWatcher</span></span>
<span data-ttu-id="029a5-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="029a5-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="029a5-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="029a5-122">-NetworkWatcherName</span></span>
<span data-ttu-id="029a5-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="029a5-123">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="029a5-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="029a5-124">-PacketCaptureName</span></span>
<span data-ttu-id="029a5-125">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="029a5-125">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="029a5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="029a5-126">-PassThru</span></span>
<span data-ttu-id="029a5-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="029a5-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="029a5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="029a5-128">-ResourceGroupName</span></span>
<span data-ttu-id="029a5-129">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="029a5-129">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="029a5-130">-確認</span><span class="sxs-lookup"><span data-stu-id="029a5-130">-Confirm</span></span>
<span data-ttu-id="029a5-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="029a5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="029a5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="029a5-132">-WhatIf</span></span>
<span data-ttu-id="029a5-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="029a5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="029a5-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="029a5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="029a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="029a5-135">CommonParameters</span></span>
<span data-ttu-id="029a5-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="029a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="029a5-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="029a5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="029a5-138">輸入</span><span class="sxs-lookup"><span data-stu-id="029a5-138">INPUTS</span></span>

### <span data-ttu-id="029a5-139">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="029a5-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="029a5-140">System.object</span><span class="sxs-lookup"><span data-stu-id="029a5-140">System.String</span></span>

## <span data-ttu-id="029a5-141">輸出</span><span class="sxs-lookup"><span data-stu-id="029a5-141">OUTPUTS</span></span>

### <span data-ttu-id="029a5-142">System.object</span><span class="sxs-lookup"><span data-stu-id="029a5-142">System.Object</span></span>

## <span data-ttu-id="029a5-143">筆記</span><span class="sxs-lookup"><span data-stu-id="029a5-143">NOTES</span></span>
<span data-ttu-id="029a5-144">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量，移除</span><span class="sxs-lookup"><span data-stu-id="029a5-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="029a5-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="029a5-145">RELATED LINKS</span></span>

[<span data-ttu-id="029a5-146">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="029a5-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="029a5-147">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="029a5-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="029a5-148">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="029a5-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="029a5-149">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="029a5-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="029a5-150">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="029a5-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="029a5-151">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="029a5-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="029a5-152">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="029a5-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="029a5-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="029a5-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="029a5-154">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="029a5-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="029a5-155">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="029a5-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="029a5-156">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="029a5-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="029a5-157">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="029a5-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
