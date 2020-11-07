---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: c4d31de526132974defc6b3d28542e1ec8de4c67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795360"
---
# <span data-ttu-id="845f9-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="845f9-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="845f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="845f9-102">SYNOPSIS</span></span>
<span data-ttu-id="845f9-103">停止執行中的 [資料包捕獲] 會話</span><span class="sxs-lookup"><span data-stu-id="845f9-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="845f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="845f9-104">SYNTAX</span></span>

### <span data-ttu-id="845f9-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="845f9-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="845f9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="845f9-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="845f9-107">說明</span><span class="sxs-lookup"><span data-stu-id="845f9-107">DESCRIPTION</span></span>
<span data-ttu-id="845f9-108">Stop-AzNetworkWatcherPacketCapture 會停止執行中的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="845f9-108">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="845f9-109">會話停止之後，就會根據其設定，將資料包捕獲檔案上傳到儲存空間和/或儲存在 VM 的本機。</span><span class="sxs-lookup"><span data-stu-id="845f9-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="845f9-110">示例</span><span class="sxs-lookup"><span data-stu-id="845f9-110">EXAMPLES</span></span>

### <span data-ttu-id="845f9-111">---範例1：停止 [資料包捕獲] 會話---</span><span class="sxs-lookup"><span data-stu-id="845f9-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="845f9-112">在這個範例中，我們會停止一個名為「PacketCaptureTest」的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="845f9-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="845f9-113">會話停止之後，就會根據其設定，將資料包捕獲檔案上傳到儲存空間和/或儲存在 VM 的本機。</span><span class="sxs-lookup"><span data-stu-id="845f9-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="845f9-114">參數</span><span class="sxs-lookup"><span data-stu-id="845f9-114">PARAMETERS</span></span>

### <span data-ttu-id="845f9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="845f9-115">-AsJob</span></span>
<span data-ttu-id="845f9-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="845f9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="845f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="845f9-117">-DefaultProfile</span></span>
<span data-ttu-id="845f9-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="845f9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="845f9-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="845f9-119">-NetworkWatcher</span></span>
<span data-ttu-id="845f9-120">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="845f9-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="845f9-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="845f9-121">-NetworkWatcherName</span></span>
<span data-ttu-id="845f9-122">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="845f9-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="845f9-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="845f9-123">-PacketCaptureName</span></span>
<span data-ttu-id="845f9-124">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="845f9-124">The packet capture name.</span></span>

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

### <span data-ttu-id="845f9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="845f9-125">-PassThru</span></span>
<span data-ttu-id="845f9-126">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="845f9-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="845f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="845f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="845f9-128">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="845f9-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="845f9-129">-確認</span><span class="sxs-lookup"><span data-stu-id="845f9-129">-Confirm</span></span>
<span data-ttu-id="845f9-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="845f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="845f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="845f9-131">-WhatIf</span></span>
<span data-ttu-id="845f9-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="845f9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="845f9-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="845f9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="845f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="845f9-134">CommonParameters</span></span>
<span data-ttu-id="845f9-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="845f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="845f9-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="845f9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="845f9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="845f9-137">INPUTS</span></span>

### <span data-ttu-id="845f9-138">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="845f9-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="845f9-139">System.object</span><span class="sxs-lookup"><span data-stu-id="845f9-139">System.String</span></span>

## <span data-ttu-id="845f9-140">輸出</span><span class="sxs-lookup"><span data-stu-id="845f9-140">OUTPUTS</span></span>

### <span data-ttu-id="845f9-141">System.object</span><span class="sxs-lookup"><span data-stu-id="845f9-141">System.Boolean</span></span>

## <span data-ttu-id="845f9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="845f9-142">NOTES</span></span>
<span data-ttu-id="845f9-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="845f9-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="845f9-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="845f9-144">RELATED LINKS</span></span>

[<span data-ttu-id="845f9-145">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="845f9-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="845f9-146">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="845f9-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="845f9-147">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="845f9-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="845f9-148">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="845f9-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="845f9-149">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="845f9-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="845f9-150">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="845f9-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="845f9-151">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="845f9-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="845f9-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="845f9-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="845f9-153">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="845f9-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="845f9-154">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="845f9-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="845f9-155">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="845f9-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="845f9-156">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="845f9-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
