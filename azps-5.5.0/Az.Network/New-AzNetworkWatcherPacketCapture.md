---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 9825562ad5f0bec36da0efd14f2e06b93a3ad588
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398048"
---
# <span data-ttu-id="99c71-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99c71-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="99c71-102">簡介</span><span class="sxs-lookup"><span data-stu-id="99c71-102">SYNOPSIS</span></span>
<span data-ttu-id="99c71-103">建立新的封包捕獲資源，並啟動 VM 上的封包捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="99c71-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="99c71-104">語法</span><span class="sxs-lookup"><span data-stu-id="99c71-104">SYNTAX</span></span>

### <span data-ttu-id="99c71-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="99c71-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99c71-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="99c71-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99c71-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="99c71-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99c71-108">描述</span><span class="sxs-lookup"><span data-stu-id="99c71-108">DESCRIPTION</span></span>
<span data-ttu-id="99c71-109">Cmdlet New-AzNetworkWatcherPacketCapture建立新的封包捕獲資源，並啟動 VM 上的封包捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="99c71-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="99c71-110">封包捕獲會話的長度可以透過時間限制或大小限制來進行。</span><span class="sxs-lookup"><span data-stu-id="99c71-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="99c71-111">也可以針對每個封包的捕獲資料量進行配置。</span><span class="sxs-lookup"><span data-stu-id="99c71-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="99c71-112">篩選可以適用于特定封包捕獲會話，讓您自訂所捕獲的封包類型。</span><span class="sxs-lookup"><span data-stu-id="99c71-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="99c71-113">篩選可以限制本地和遠端 IP 位址的封包&位址範圍、&埠範圍，以及要捕獲的工作階段層級通訊協定。</span><span class="sxs-lookup"><span data-stu-id="99c71-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="99c71-114">篩選可撰寫，而且可以應用多個篩選，提供您捕獲的細微度。</span><span class="sxs-lookup"><span data-stu-id="99c71-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="99c71-115">例子</span><span class="sxs-lookup"><span data-stu-id="99c71-115">EXAMPLES</span></span>

### <span data-ttu-id="99c71-116">範例 1：建立包含多個篩選的封包捕獲</span><span class="sxs-lookup"><span data-stu-id="99c71-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="99c71-117">在此範例中，我們建立名為「PacketCaptureTest」的封包捕獲，具有多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="99c71-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="99c71-118">會話完成之後，就會儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="99c71-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="99c71-119">注意：Azure 網路監視程式擴充功能必須安裝在目標虛擬機器上，以建立封包捕獲。</span><span class="sxs-lookup"><span data-stu-id="99c71-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="99c71-120">參數</span><span class="sxs-lookup"><span data-stu-id="99c71-120">PARAMETERS</span></span>

### <span data-ttu-id="99c71-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99c71-121">-AsJob</span></span>
<span data-ttu-id="99c71-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="99c71-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99c71-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="99c71-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="99c71-124">每個封包要捕獲的位元組。</span><span class="sxs-lookup"><span data-stu-id="99c71-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="99c71-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c71-125">-DefaultProfile</span></span>
<span data-ttu-id="99c71-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="99c71-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99c71-127">-篩選</span><span class="sxs-lookup"><span data-stu-id="99c71-127">-Filter</span></span>
<span data-ttu-id="99c71-128">封包捕獲會話的篩選。</span><span class="sxs-lookup"><span data-stu-id="99c71-128">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="99c71-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="99c71-129">-LocalFilePath</span></span>
<span data-ttu-id="99c71-130">本地檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="99c71-130">Local file path.</span></span>

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

### <span data-ttu-id="99c71-131">-位置</span><span class="sxs-lookup"><span data-stu-id="99c71-131">-Location</span></span>
<span data-ttu-id="99c71-132">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="99c71-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="99c71-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="99c71-133">-NetworkWatcher</span></span>
<span data-ttu-id="99c71-134">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="99c71-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="99c71-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="99c71-135">-NetworkWatcherName</span></span>
<span data-ttu-id="99c71-136">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="99c71-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="99c71-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="99c71-137">-PacketCaptureName</span></span>
<span data-ttu-id="99c71-138">封包捕獲名稱。</span><span class="sxs-lookup"><span data-stu-id="99c71-138">The packet capture name.</span></span>

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

### <span data-ttu-id="99c71-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99c71-139">-ResourceGroupName</span></span>
<span data-ttu-id="99c71-140">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99c71-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="99c71-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="99c71-141">-StorageAccountId</span></span>
<span data-ttu-id="99c71-142">儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="99c71-142">Storage account Id.</span></span>

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

### <span data-ttu-id="99c71-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="99c71-143">-StoragePath</span></span>
<span data-ttu-id="99c71-144">儲存路徑。</span><span class="sxs-lookup"><span data-stu-id="99c71-144">Storage path.</span></span>

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

### <span data-ttu-id="99c71-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="99c71-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="99c71-146">目標虛擬機器識別碼。</span><span class="sxs-lookup"><span data-stu-id="99c71-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="99c71-147">-TimeLimitIn以秒為單位</span><span class="sxs-lookup"><span data-stu-id="99c71-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="99c71-148">以碼錶示的時間限制。</span><span class="sxs-lookup"><span data-stu-id="99c71-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="99c71-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="99c71-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="99c71-150">每個會話的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="99c71-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="99c71-151">-確認</span><span class="sxs-lookup"><span data-stu-id="99c71-151">-Confirm</span></span>
<span data-ttu-id="99c71-152">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="99c71-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99c71-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99c71-153">-WhatIf</span></span>
<span data-ttu-id="99c71-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99c71-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99c71-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99c71-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99c71-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c71-156">CommonParameters</span></span>
<span data-ttu-id="99c71-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="99c71-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c71-158">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="99c71-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c71-159">輸入</span><span class="sxs-lookup"><span data-stu-id="99c71-159">INPUTS</span></span>

### <span data-ttu-id="99c71-160">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="99c71-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="99c71-161">System.String</span><span class="sxs-lookup"><span data-stu-id="99c71-161">System.String</span></span>

### <span data-ttu-id="99c71-162">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="99c71-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="99c71-163">輸出</span><span class="sxs-lookup"><span data-stu-id="99c71-163">OUTPUTS</span></span>

### <span data-ttu-id="99c71-164">Microsoft.Azure.Commands.Network.models.PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="99c71-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="99c71-165">筆記</span><span class="sxs-lookup"><span data-stu-id="99c71-165">NOTES</span></span>
<span data-ttu-id="99c71-166">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路、網路監視者、封包、捕獲、流量</span><span class="sxs-lookup"><span data-stu-id="99c71-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="99c71-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="99c71-167">RELATED LINKS</span></span>

[<span data-ttu-id="99c71-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="99c71-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="99c71-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="99c71-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="99c71-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="99c71-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="99c71-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="99c71-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="99c71-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="99c71-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="99c71-173">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="99c71-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="99c71-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="99c71-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="99c71-175">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99c71-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="99c71-176">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="99c71-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="99c71-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99c71-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="99c71-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99c71-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="99c71-179">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99c71-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="99c71-180">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="99c71-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="99c71-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="99c71-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="99c71-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="99c71-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="99c71-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="99c71-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="99c71-184">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="99c71-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="99c71-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="99c71-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="99c71-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="99c71-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="99c71-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="99c71-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="99c71-188">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="99c71-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="99c71-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="99c71-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="99c71-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="99c71-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="99c71-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="99c71-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="99c71-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="99c71-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="99c71-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="99c71-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="99c71-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="99c71-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)


