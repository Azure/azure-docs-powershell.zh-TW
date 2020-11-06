---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 3f1206b79f8e80793106b1e294b591e21b9fb77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446706"
---
# <span data-ttu-id="ab768-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab768-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="ab768-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab768-102">SYNOPSIS</span></span>
<span data-ttu-id="ab768-103">停止執行中的 [資料包捕獲] 會話</span><span class="sxs-lookup"><span data-stu-id="ab768-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab768-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab768-104">SYNTAX</span></span>

### <span data-ttu-id="ab768-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="ab768-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab768-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ab768-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab768-107">說明</span><span class="sxs-lookup"><span data-stu-id="ab768-107">DESCRIPTION</span></span>
<span data-ttu-id="ab768-108">Stop-AzureRmNetworkWatcherPacketCapture 會停止執行中的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="ab768-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="ab768-109">會話停止之後，就會根據其設定，將資料包捕獲檔案上傳到儲存空間和/或儲存在 VM 的本機。</span><span class="sxs-lookup"><span data-stu-id="ab768-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="ab768-110">示例</span><span class="sxs-lookup"><span data-stu-id="ab768-110">EXAMPLES</span></span>

### <span data-ttu-id="ab768-111">---範例1：停止 [資料包捕獲] 會話---</span><span class="sxs-lookup"><span data-stu-id="ab768-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="ab768-112">在這個範例中，我們會停止一個名為「PacketCaptureTest」的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="ab768-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="ab768-113">會話停止之後，就會根據其設定，將資料包捕獲檔案上傳到儲存空間和/或儲存在 VM 的本機。</span><span class="sxs-lookup"><span data-stu-id="ab768-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="ab768-114">參數</span><span class="sxs-lookup"><span data-stu-id="ab768-114">PARAMETERS</span></span>

### <span data-ttu-id="ab768-115">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab768-115">-NetworkWatcher</span></span>
<span data-ttu-id="ab768-116">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="ab768-116">The network watcher resource.</span></span>

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

### <span data-ttu-id="ab768-117">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ab768-117">-NetworkWatcherName</span></span>
<span data-ttu-id="ab768-118">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab768-118">The name of network watcher.</span></span>

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

### <span data-ttu-id="ab768-119">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="ab768-119">-PacketCaptureName</span></span>
<span data-ttu-id="ab768-120">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="ab768-120">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab768-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab768-121">-PassThru</span></span>
<span data-ttu-id="ab768-122">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="ab768-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ab768-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab768-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab768-124">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab768-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ab768-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ab768-125">-Confirm</span></span>
<span data-ttu-id="ab768-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ab768-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab768-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab768-127">-WhatIf</span></span>
<span data-ttu-id="ab768-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab768-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab768-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab768-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab768-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab768-130">-DefaultProfile</span></span>
<span data-ttu-id="ab768-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab768-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab768-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab768-132">CommonParameters</span></span>
<span data-ttu-id="ab768-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab768-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab768-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab768-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab768-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ab768-135">INPUTS</span></span>

### <span data-ttu-id="ab768-136">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab768-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ab768-137">System.object</span><span class="sxs-lookup"><span data-stu-id="ab768-137">System.String</span></span>

## <span data-ttu-id="ab768-138">輸出</span><span class="sxs-lookup"><span data-stu-id="ab768-138">OUTPUTS</span></span>

### <span data-ttu-id="ab768-139">System.object</span><span class="sxs-lookup"><span data-stu-id="ab768-139">System.Boolean</span></span>

## <span data-ttu-id="ab768-140">筆記</span><span class="sxs-lookup"><span data-stu-id="ab768-140">NOTES</span></span>
<span data-ttu-id="ab768-141">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="ab768-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="ab768-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab768-142">RELATED LINKS</span></span>

[<span data-ttu-id="ab768-143">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab768-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ab768-144">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ab768-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ab768-145">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab768-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ab768-146">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab768-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ab768-147">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab768-147">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ab768-148">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab768-148">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ab768-149">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab768-149">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ab768-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ab768-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ab768-151">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ab768-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ab768-152">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ab768-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ab768-153">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ab768-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ab768-154">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ab768-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
