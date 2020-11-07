---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: 5f2b2bf738c4e83f8f8f3854e831601ea23c7d8e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800334"
---
# <span data-ttu-id="1d600-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d600-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="1d600-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d600-102">SYNOPSIS</span></span>
<span data-ttu-id="1d600-103">停止執行中的 [資料包捕獲] 會話</span><span class="sxs-lookup"><span data-stu-id="1d600-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d600-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d600-104">SYNTAX</span></span>

### <span data-ttu-id="1d600-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="1d600-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d600-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1d600-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d600-107">說明</span><span class="sxs-lookup"><span data-stu-id="1d600-107">DESCRIPTION</span></span>
<span data-ttu-id="1d600-108">Stop-AzureRmNetworkWatcherPacketCapture 會停止執行中的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="1d600-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="1d600-109">會話停止之後，就會根據其設定，將資料包捕獲檔案上傳到儲存空間和/或儲存在 VM 的本機。</span><span class="sxs-lookup"><span data-stu-id="1d600-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="1d600-110">示例</span><span class="sxs-lookup"><span data-stu-id="1d600-110">EXAMPLES</span></span>

### <span data-ttu-id="1d600-111">---範例1：停止 [資料包捕獲] 會話---</span><span class="sxs-lookup"><span data-stu-id="1d600-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="1d600-112">在這個範例中，我們會停止一個名為「PacketCaptureTest」的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="1d600-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="1d600-113">會話停止之後，就會根據其設定，將資料包捕獲檔案上傳到儲存空間和/或儲存在 VM 的本機。</span><span class="sxs-lookup"><span data-stu-id="1d600-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="1d600-114">參數</span><span class="sxs-lookup"><span data-stu-id="1d600-114">PARAMETERS</span></span>

### <span data-ttu-id="1d600-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d600-115">-AsJob</span></span>
<span data-ttu-id="1d600-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1d600-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d600-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d600-117">-DefaultProfile</span></span>
<span data-ttu-id="1d600-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d600-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d600-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d600-119">-NetworkWatcher</span></span>
<span data-ttu-id="1d600-120">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="1d600-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="1d600-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1d600-121">-NetworkWatcherName</span></span>
<span data-ttu-id="1d600-122">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d600-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="1d600-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="1d600-123">-PacketCaptureName</span></span>
<span data-ttu-id="1d600-124">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="1d600-124">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d600-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d600-125">-PassThru</span></span>
<span data-ttu-id="1d600-126">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="1d600-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1d600-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d600-127">-ResourceGroupName</span></span>
<span data-ttu-id="1d600-128">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d600-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1d600-129">-確認</span><span class="sxs-lookup"><span data-stu-id="1d600-129">-Confirm</span></span>
<span data-ttu-id="1d600-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1d600-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d600-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d600-131">-WhatIf</span></span>
<span data-ttu-id="1d600-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1d600-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d600-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d600-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d600-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d600-134">CommonParameters</span></span>
<span data-ttu-id="1d600-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d600-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d600-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1d600-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d600-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1d600-137">INPUTS</span></span>

### <span data-ttu-id="1d600-138">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1d600-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1d600-139">System.object</span><span class="sxs-lookup"><span data-stu-id="1d600-139">System.String</span></span>

## <span data-ttu-id="1d600-140">輸出</span><span class="sxs-lookup"><span data-stu-id="1d600-140">OUTPUTS</span></span>

### <span data-ttu-id="1d600-141">System.object</span><span class="sxs-lookup"><span data-stu-id="1d600-141">System.Boolean</span></span>

## <span data-ttu-id="1d600-142">筆記</span><span class="sxs-lookup"><span data-stu-id="1d600-142">NOTES</span></span>
<span data-ttu-id="1d600-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="1d600-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="1d600-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d600-144">RELATED LINKS</span></span>

[<span data-ttu-id="1d600-145">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d600-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1d600-146">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1d600-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="1d600-147">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d600-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1d600-148">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d600-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1d600-149">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d600-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1d600-150">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d600-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1d600-151">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d600-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1d600-152">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1d600-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="1d600-153">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1d600-153">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="1d600-154">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1d600-154">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1d600-155">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1d600-155">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="1d600-156">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1d600-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
