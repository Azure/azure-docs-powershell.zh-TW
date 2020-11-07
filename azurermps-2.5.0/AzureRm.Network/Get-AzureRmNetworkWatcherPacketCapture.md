---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: aeadada7c6e2e2d7cb94a484e7ca3223e03b4426
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800110"
---
# <span data-ttu-id="2b703-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b703-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="2b703-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b703-102">SYNOPSIS</span></span>
<span data-ttu-id="2b703-103">取得資料包捕獲資源的資訊和屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="2b703-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b703-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b703-104">SYNTAX</span></span>

### <span data-ttu-id="2b703-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="2b703-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b703-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2b703-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b703-107">說明</span><span class="sxs-lookup"><span data-stu-id="2b703-107">DESCRIPTION</span></span>
<span data-ttu-id="2b703-108">Get-AzureRmNetworkWatcherPacketCapture 會取得資料包捕獲資源的屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="2b703-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="2b703-109">示例</span><span class="sxs-lookup"><span data-stu-id="2b703-109">EXAMPLES</span></span>

### <span data-ttu-id="2b703-110">---範例1：使用多個篩選建立資料包捕獲並檢索其狀態---</span><span class="sxs-lookup"><span data-stu-id="2b703-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="2b703-111">在這個範例中，我們會建立名為 "PacketCaptureTest" 的資料包捕獲，並提供多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="2b703-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="2b703-112">會話完成後，就會將它儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2b703-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="2b703-113">接著，我們會呼叫 Get-AzureRmNetworkWatcherPacketCapture 來取得捕獲會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="2b703-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="2b703-114">注意：必須在目標虛擬機器上安裝 Azure 網路觀察程式延伸，才能建立資料包捕獲。</span><span class="sxs-lookup"><span data-stu-id="2b703-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="2b703-115">參數</span><span class="sxs-lookup"><span data-stu-id="2b703-115">PARAMETERS</span></span>

### <span data-ttu-id="2b703-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b703-116">-AsJob</span></span>
<span data-ttu-id="2b703-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b703-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b703-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b703-118">-DefaultProfile</span></span>
<span data-ttu-id="2b703-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b703-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b703-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b703-120">-NetworkWatcher</span></span>
<span data-ttu-id="2b703-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="2b703-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="2b703-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2b703-122">-NetworkWatcherName</span></span>
<span data-ttu-id="2b703-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b703-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="2b703-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="2b703-124">-PacketCaptureName</span></span>
<span data-ttu-id="2b703-125">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="2b703-125">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b703-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b703-126">-ResourceGroupName</span></span>
<span data-ttu-id="2b703-127">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b703-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2b703-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b703-128">CommonParameters</span></span>
<span data-ttu-id="2b703-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b703-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b703-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b703-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b703-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2b703-131">INPUTS</span></span>

### <span data-ttu-id="2b703-132">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2b703-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2b703-133">System.object</span><span class="sxs-lookup"><span data-stu-id="2b703-133">System.String</span></span>

## <span data-ttu-id="2b703-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2b703-134">OUTPUTS</span></span>

### <span data-ttu-id="2b703-135">PSGetPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2b703-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="2b703-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2b703-136">NOTES</span></span>
<span data-ttu-id="2b703-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="2b703-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="2b703-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b703-138">RELATED LINKS</span></span>

[<span data-ttu-id="2b703-139">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b703-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b703-140">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2b703-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2b703-141">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b703-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b703-142">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b703-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b703-143">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b703-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2b703-144">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b703-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2b703-145">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b703-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2b703-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2b703-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2b703-147">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2b703-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="2b703-148">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2b703-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2b703-149">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2b703-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2b703-150">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2b703-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

