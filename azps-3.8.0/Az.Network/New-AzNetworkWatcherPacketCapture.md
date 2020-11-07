---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 348767f145c2dd407fc277549f89c44386c8a564
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957722"
---
# <span data-ttu-id="f7090-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7090-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="f7090-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7090-102">SYNOPSIS</span></span>
<span data-ttu-id="f7090-103">建立新的 [資料包捕獲] 資源，並啟動 VM 上的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="f7090-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="f7090-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7090-104">SYNTAX</span></span>

### <span data-ttu-id="f7090-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f7090-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7090-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f7090-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7090-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f7090-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7090-108">說明</span><span class="sxs-lookup"><span data-stu-id="f7090-108">DESCRIPTION</span></span>
<span data-ttu-id="f7090-109">New-AzNetworkWatcherPacketCapture Cmdlet 會建立新的 [資料包捕獲資源]，並啟動 VM 上的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="f7090-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="f7090-110">您可以透過時間限制或大小限制來設定資料包捕獲會話的長度。</span><span class="sxs-lookup"><span data-stu-id="f7090-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="f7090-111">您也可以設定為每個資料包捕獲的資料量。</span><span class="sxs-lookup"><span data-stu-id="f7090-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="f7090-112">篩選可套用到特定的資料包捕獲會話，讓您自訂捕獲的資料包類型。</span><span class="sxs-lookup"><span data-stu-id="f7090-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="f7090-113">篩選可限制本機和遠端 IP 位址上的資料包，& 位址範圍、本機和遠端埠 & 埠範圍，以及要捕獲的工作階段層級通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f7090-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="f7090-114">篩選是可組合的，而且可以套用多個篩選，以提供捕獲細微性。</span><span class="sxs-lookup"><span data-stu-id="f7090-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="f7090-115">示例</span><span class="sxs-lookup"><span data-stu-id="f7090-115">EXAMPLES</span></span>

### <span data-ttu-id="f7090-116">範例1：使用多個篩選建立資料包捕獲</span><span class="sxs-lookup"><span data-stu-id="f7090-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="f7090-117">在這個範例中，我們會建立名為 "PacketCaptureTest" 的資料包捕獲，並提供多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="f7090-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="f7090-118">會話完成後，就會將它儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="f7090-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="f7090-119">注意：必須在目標虛擬機器上安裝 Azure 網路觀察程式延伸，才能建立資料包捕獲。</span><span class="sxs-lookup"><span data-stu-id="f7090-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="f7090-120">參數</span><span class="sxs-lookup"><span data-stu-id="f7090-120">PARAMETERS</span></span>

### <span data-ttu-id="f7090-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7090-121">-AsJob</span></span>
<span data-ttu-id="f7090-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f7090-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7090-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="f7090-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="f7090-124">每個資料包要捕獲的位元組數。</span><span class="sxs-lookup"><span data-stu-id="f7090-124">Bytes to capture per packet.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7090-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7090-125">-DefaultProfile</span></span>
<span data-ttu-id="f7090-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7090-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7090-127">-篩選</span><span class="sxs-lookup"><span data-stu-id="f7090-127">-Filter</span></span>
<span data-ttu-id="f7090-128">針對 [資料包捕獲] 會話的篩選。</span><span class="sxs-lookup"><span data-stu-id="f7090-128">Filters for packet capture session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7090-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="f7090-129">-LocalFilePath</span></span>
<span data-ttu-id="f7090-130">本機檔路徑。</span><span class="sxs-lookup"><span data-stu-id="f7090-130">Local file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7090-131">-位置</span><span class="sxs-lookup"><span data-stu-id="f7090-131">-Location</span></span>
<span data-ttu-id="f7090-132">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="f7090-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f7090-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7090-133">-NetworkWatcher</span></span>
<span data-ttu-id="f7090-134">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="f7090-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="f7090-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f7090-135">-NetworkWatcherName</span></span>
<span data-ttu-id="f7090-136">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7090-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="f7090-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="f7090-137">-PacketCaptureName</span></span>
<span data-ttu-id="f7090-138">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="f7090-138">The packet capture name.</span></span>

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

### <span data-ttu-id="f7090-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7090-139">-ResourceGroupName</span></span>
<span data-ttu-id="f7090-140">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7090-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f7090-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f7090-141">-StorageAccountId</span></span>
<span data-ttu-id="f7090-142">儲存空間帳戶 Id。</span><span class="sxs-lookup"><span data-stu-id="f7090-142">Storage account Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7090-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="f7090-143">-StoragePath</span></span>
<span data-ttu-id="f7090-144">儲存路徑。</span><span class="sxs-lookup"><span data-stu-id="f7090-144">Storage path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7090-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f7090-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="f7090-146">目標虛擬機器 ID。</span><span class="sxs-lookup"><span data-stu-id="f7090-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="f7090-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="f7090-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="f7090-148">時間限制（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f7090-148">Time limit in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7090-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="f7090-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="f7090-150">每個會話的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="f7090-150">Total bytes per session.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7090-151">-確認</span><span class="sxs-lookup"><span data-stu-id="f7090-151">-Confirm</span></span>
<span data-ttu-id="f7090-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7090-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7090-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7090-153">-WhatIf</span></span>
<span data-ttu-id="f7090-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7090-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7090-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7090-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7090-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7090-156">CommonParameters</span></span>
<span data-ttu-id="f7090-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7090-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7090-158">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7090-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7090-159">輸入</span><span class="sxs-lookup"><span data-stu-id="f7090-159">INPUTS</span></span>

### <span data-ttu-id="f7090-160">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f7090-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f7090-161">System.object</span><span class="sxs-lookup"><span data-stu-id="f7090-161">System.String</span></span>

### <span data-ttu-id="f7090-162">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f7090-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f7090-163">輸出</span><span class="sxs-lookup"><span data-stu-id="f7090-163">OUTPUTS</span></span>

### <span data-ttu-id="f7090-164">PSPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f7090-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="f7090-165">筆記</span><span class="sxs-lookup"><span data-stu-id="f7090-165">NOTES</span></span>
<span data-ttu-id="f7090-166">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="f7090-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="f7090-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7090-167">RELATED LINKS</span></span>

[<span data-ttu-id="f7090-168">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7090-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f7090-169">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7090-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f7090-170">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7090-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f7090-171">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f7090-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f7090-172">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f7090-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f7090-173">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f7090-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f7090-174">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f7090-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f7090-175">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7090-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7090-176">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f7090-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f7090-177">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7090-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7090-178">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7090-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7090-179">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7090-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7090-180">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7090-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f7090-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f7090-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f7090-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f7090-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f7090-183">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f7090-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f7090-184">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f7090-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f7090-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f7090-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f7090-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f7090-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f7090-187">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f7090-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f7090-188">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f7090-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f7090-189">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f7090-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f7090-190">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f7090-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f7090-191">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f7090-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f7090-192">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f7090-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f7090-193">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f7090-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="f7090-194">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f7090-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)


