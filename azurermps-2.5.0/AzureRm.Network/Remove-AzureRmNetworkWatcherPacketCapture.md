---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: eb8997025a9fa73c394c2c51c23f00c211604cb2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800057"
---
# <span data-ttu-id="b0135-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b0135-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="b0135-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0135-102">SYNOPSIS</span></span>
<span data-ttu-id="b0135-103">移除 [資料包捕獲資源]。</span><span class="sxs-lookup"><span data-stu-id="b0135-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0135-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0135-104">SYNTAX</span></span>

### <span data-ttu-id="b0135-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b0135-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0135-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b0135-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0135-107">說明</span><span class="sxs-lookup"><span data-stu-id="b0135-107">DESCRIPTION</span></span>
<span data-ttu-id="b0135-108">Remove-AzureRmNetworkWatcherPacketCapture 會移除 [資料包捕獲資源]。</span><span class="sxs-lookup"><span data-stu-id="b0135-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="b0135-109">建議您先呼叫 Stop-AzureRmNetworkWatcherPacketCapture，然後再呼叫 AzureRmNetworkWatcherPacketCapture。</span><span class="sxs-lookup"><span data-stu-id="b0135-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="b0135-110">如果 Remove-AzureRmNetworkWatcherPacketCapture 稱為 [資料包捕獲會話]，則可能無法儲存 [資料包捕獲]。</span><span class="sxs-lookup"><span data-stu-id="b0135-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="b0135-111">如果在移除前停止會話，則不會移除內含捕獲資料的 .cap 檔案。</span><span class="sxs-lookup"><span data-stu-id="b0135-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="b0135-112">示例</span><span class="sxs-lookup"><span data-stu-id="b0135-112">EXAMPLES</span></span>

### <span data-ttu-id="b0135-113">---範例1：移除資料包捕獲會話--</span><span class="sxs-lookup"><span data-stu-id="b0135-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="b0135-114">在這個範例中，我們會移除名為 "PacketCaptureTest" 的現有資料包捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="b0135-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="b0135-115">參數</span><span class="sxs-lookup"><span data-stu-id="b0135-115">PARAMETERS</span></span>

### <span data-ttu-id="b0135-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0135-116">-AsJob</span></span>
<span data-ttu-id="b0135-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b0135-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0135-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0135-118">-DefaultProfile</span></span>
<span data-ttu-id="b0135-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0135-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0135-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b0135-120">-NetworkWatcher</span></span>
<span data-ttu-id="b0135-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="b0135-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="b0135-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b0135-122">-NetworkWatcherName</span></span>
<span data-ttu-id="b0135-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0135-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="b0135-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="b0135-124">-PacketCaptureName</span></span>
<span data-ttu-id="b0135-125">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="b0135-125">The packet capture name.</span></span>

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

### <span data-ttu-id="b0135-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0135-126">-PassThru</span></span>
<span data-ttu-id="b0135-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="b0135-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b0135-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0135-128">-ResourceGroupName</span></span>
<span data-ttu-id="b0135-129">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0135-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b0135-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b0135-130">-Confirm</span></span>
<span data-ttu-id="b0135-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b0135-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0135-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0135-132">-WhatIf</span></span>
<span data-ttu-id="b0135-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0135-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0135-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0135-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0135-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0135-135">CommonParameters</span></span>
<span data-ttu-id="b0135-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0135-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0135-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0135-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0135-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b0135-138">INPUTS</span></span>

### <span data-ttu-id="b0135-139">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b0135-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b0135-140">System.object</span><span class="sxs-lookup"><span data-stu-id="b0135-140">System.String</span></span>

## <span data-ttu-id="b0135-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b0135-141">OUTPUTS</span></span>

### <span data-ttu-id="b0135-142">System.object</span><span class="sxs-lookup"><span data-stu-id="b0135-142">System.Object</span></span>

## <span data-ttu-id="b0135-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b0135-143">NOTES</span></span>
<span data-ttu-id="b0135-144">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量，移除</span><span class="sxs-lookup"><span data-stu-id="b0135-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="b0135-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0135-145">RELATED LINKS</span></span>

[<span data-ttu-id="b0135-146">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b0135-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b0135-147">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b0135-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="b0135-148">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b0135-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b0135-149">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b0135-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b0135-150">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b0135-150">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b0135-151">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b0135-151">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b0135-152">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b0135-152">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b0135-153">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b0135-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="b0135-154">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b0135-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="b0135-155">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b0135-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b0135-156">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b0135-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="b0135-157">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b0135-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
