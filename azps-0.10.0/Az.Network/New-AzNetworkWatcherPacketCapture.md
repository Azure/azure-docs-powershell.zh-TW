---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 6844db506ee8a55c7d0c16f54946e35349059ae4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794245"
---
# <span data-ttu-id="220ba-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="220ba-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="220ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="220ba-102">SYNOPSIS</span></span>
<span data-ttu-id="220ba-103">建立新的 [資料包捕獲] 資源，並啟動 VM 上的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="220ba-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="220ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="220ba-104">SYNTAX</span></span>

### <span data-ttu-id="220ba-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="220ba-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="220ba-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="220ba-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="220ba-107">說明</span><span class="sxs-lookup"><span data-stu-id="220ba-107">DESCRIPTION</span></span>
<span data-ttu-id="220ba-108">New-AzNetworkWatcherPacketCapture Cmdlet 會建立新的 [資料包捕獲資源]，並啟動 VM 上的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="220ba-108">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="220ba-109">您可以透過時間限制或大小限制來設定資料包捕獲會話的長度。</span><span class="sxs-lookup"><span data-stu-id="220ba-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="220ba-110">您也可以設定為每個資料包捕獲的資料量。</span><span class="sxs-lookup"><span data-stu-id="220ba-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="220ba-111">篩選可套用到特定的資料包捕獲會話，讓您自訂捕獲的資料包類型。</span><span class="sxs-lookup"><span data-stu-id="220ba-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="220ba-112">篩選可限制本機和遠端 IP 位址上的資料包，& 位址範圍、本機和遠端埠 & 埠範圍，以及要捕獲的工作階段層級通訊協定。</span><span class="sxs-lookup"><span data-stu-id="220ba-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="220ba-113">篩選是可組合的，而且可以套用多個篩選，以提供捕獲細微性。</span><span class="sxs-lookup"><span data-stu-id="220ba-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="220ba-114">示例</span><span class="sxs-lookup"><span data-stu-id="220ba-114">EXAMPLES</span></span>

### <span data-ttu-id="220ba-115">---範例1：使用多個篩選器建立資料包捕獲---</span><span class="sxs-lookup"><span data-stu-id="220ba-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="220ba-116">在這個範例中，我們會建立名為 "PacketCaptureTest" 的資料包捕獲，並提供多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="220ba-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="220ba-117">會話完成後，就會將它儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="220ba-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="220ba-118">注意：必須在目標虛擬機器上安裝 Azure 網路觀察程式延伸，才能建立資料包捕獲。</span><span class="sxs-lookup"><span data-stu-id="220ba-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="220ba-119">參數</span><span class="sxs-lookup"><span data-stu-id="220ba-119">PARAMETERS</span></span>

### <span data-ttu-id="220ba-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="220ba-120">-AsJob</span></span>
<span data-ttu-id="220ba-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="220ba-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="220ba-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="220ba-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="220ba-123">每個資料包要捕獲的位元組數。</span><span class="sxs-lookup"><span data-stu-id="220ba-123">Bytes to capture per packet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220ba-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220ba-124">-DefaultProfile</span></span>
<span data-ttu-id="220ba-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="220ba-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="220ba-126">-篩選</span><span class="sxs-lookup"><span data-stu-id="220ba-126">-Filter</span></span>
<span data-ttu-id="220ba-127">針對 [資料包捕獲] 會話的篩選。</span><span class="sxs-lookup"><span data-stu-id="220ba-127">Filters for packet capture session.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220ba-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="220ba-128">-LocalFilePath</span></span>
<span data-ttu-id="220ba-129">本機檔路徑。</span><span class="sxs-lookup"><span data-stu-id="220ba-129">Local file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220ba-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="220ba-130">-NetworkWatcher</span></span>
<span data-ttu-id="220ba-131">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="220ba-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="220ba-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="220ba-132">-NetworkWatcherName</span></span>
<span data-ttu-id="220ba-133">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="220ba-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="220ba-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="220ba-134">-PacketCaptureName</span></span>
<span data-ttu-id="220ba-135">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="220ba-135">The packet capture name.</span></span>

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

### <span data-ttu-id="220ba-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="220ba-136">-ResourceGroupName</span></span>
<span data-ttu-id="220ba-137">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="220ba-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="220ba-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="220ba-138">-StorageAccountId</span></span>
<span data-ttu-id="220ba-139">儲存空間帳戶 Id。</span><span class="sxs-lookup"><span data-stu-id="220ba-139">Storage account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220ba-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="220ba-140">-StoragePath</span></span>
<span data-ttu-id="220ba-141">儲存路徑。</span><span class="sxs-lookup"><span data-stu-id="220ba-141">Storage path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220ba-142">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="220ba-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="220ba-143">目標虛擬機器 ID。</span><span class="sxs-lookup"><span data-stu-id="220ba-143">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="220ba-144">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="220ba-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="220ba-145">時間限制（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="220ba-145">Time limit in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220ba-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="220ba-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="220ba-147">每個會話的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="220ba-147">Total bytes per session.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220ba-148">-確認</span><span class="sxs-lookup"><span data-stu-id="220ba-148">-Confirm</span></span>
<span data-ttu-id="220ba-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="220ba-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="220ba-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="220ba-150">-WhatIf</span></span>
<span data-ttu-id="220ba-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="220ba-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="220ba-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="220ba-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="220ba-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220ba-153">CommonParameters</span></span>
<span data-ttu-id="220ba-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="220ba-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220ba-155">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="220ba-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220ba-156">輸入</span><span class="sxs-lookup"><span data-stu-id="220ba-156">INPUTS</span></span>

### <span data-ttu-id="220ba-157">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="220ba-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="220ba-158">System.object System。 Nullable \` \[ \[ 、mscorlib、Version = 4.0.0.0、Culture = 中性、PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="220ba-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="220ba-159">輸出</span><span class="sxs-lookup"><span data-stu-id="220ba-159">OUTPUTS</span></span>

### <span data-ttu-id="220ba-160">PSPacketCapture 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="220ba-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="220ba-161">筆記</span><span class="sxs-lookup"><span data-stu-id="220ba-161">NOTES</span></span>
<span data-ttu-id="220ba-162">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="220ba-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="220ba-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="220ba-163">RELATED LINKS</span></span>

[<span data-ttu-id="220ba-164">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="220ba-164">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="220ba-165">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="220ba-165">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="220ba-166">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="220ba-166">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="220ba-167">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="220ba-167">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="220ba-168">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="220ba-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="220ba-169">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="220ba-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="220ba-170">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="220ba-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="220ba-171">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="220ba-171">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="220ba-172">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="220ba-172">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="220ba-173">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="220ba-173">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="220ba-174">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="220ba-174">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="220ba-175">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="220ba-175">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)


