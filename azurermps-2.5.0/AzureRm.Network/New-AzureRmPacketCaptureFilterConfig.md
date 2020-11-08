---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
ms.openlocfilehash: 1d6054307ad1e499fbb36342f6c81e7e32227f37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800782"
---
# <span data-ttu-id="b5fec-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b5fec-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="b5fec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5fec-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fec-103">建立新的 [資料包捕獲篩選] 物件。</span><span class="sxs-lookup"><span data-stu-id="b5fec-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5fec-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5fec-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5fec-105">說明</span><span class="sxs-lookup"><span data-stu-id="b5fec-105">DESCRIPTION</span></span>
<span data-ttu-id="b5fec-106">New-AzureRmPacketCaptureFilterConfig Cmdlet 會建立新的 [資料包捕獲] 篩選物件。</span><span class="sxs-lookup"><span data-stu-id="b5fec-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="b5fec-107">這個物件是用來限制在資料包捕獲會話期間使用指定準則捕獲的資料包類型。</span><span class="sxs-lookup"><span data-stu-id="b5fec-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="b5fec-108">New-AzureRmNetworkWatcherPacketCapture Cmdlet 可以接受多個篩選物件，以啟用可撰寫的捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="b5fec-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="b5fec-109">示例</span><span class="sxs-lookup"><span data-stu-id="b5fec-109">EXAMPLES</span></span>

### <span data-ttu-id="b5fec-110">---範例1：使用多個篩選器建立資料包捕獲---</span><span class="sxs-lookup"><span data-stu-id="b5fec-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="b5fec-111">在這個範例中，我們會建立名為 "PacketCaptureTest" 的資料包捕獲，並提供多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="b5fec-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="b5fec-112">會話完成後，就會將它儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b5fec-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="b5fec-113">注意：必須在目標虛擬機器上安裝 Azure 網路觀察程式延伸，才能建立資料包捕獲。</span><span class="sxs-lookup"><span data-stu-id="b5fec-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="b5fec-114">參數</span><span class="sxs-lookup"><span data-stu-id="b5fec-114">PARAMETERS</span></span>

### <span data-ttu-id="b5fec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5fec-115">-DefaultProfile</span></span>
<span data-ttu-id="b5fec-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5fec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5fec-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="b5fec-117">-LocalIPAddress</span></span>
<span data-ttu-id="b5fec-118">指定要篩選的本機 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b5fec-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="b5fec-119">[範例] 輸入： [127.0.0.1 "代表單一位址專案。</span><span class="sxs-lookup"><span data-stu-id="b5fec-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="b5fec-120">範圍的 "127.0.0.1-127.0.0.255"。</span><span class="sxs-lookup"><span data-stu-id="b5fec-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="b5fec-121">"127.0.0.1; 127.0.0.5;" 代表多個專案。</span><span class="sxs-lookup"><span data-stu-id="b5fec-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="b5fec-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="b5fec-122">-LocalPort</span></span>
<span data-ttu-id="b5fec-123">指定要篩選的本機 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b5fec-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="b5fec-124">[範例] 輸入： [127.0.0.1 "代表單一位址專案。</span><span class="sxs-lookup"><span data-stu-id="b5fec-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="b5fec-125">範圍的 "127.0.0.1-127.0.0.255"。</span><span class="sxs-lookup"><span data-stu-id="b5fec-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="b5fec-126">"127.0.0.1; 127.0.0.5;" 代表多個專案。</span><span class="sxs-lookup"><span data-stu-id="b5fec-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="b5fec-127">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="b5fec-127">-Protocol</span></span>
<span data-ttu-id="b5fec-128">指定要篩選的 Procotol。</span><span class="sxs-lookup"><span data-stu-id="b5fec-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="b5fec-129">可接受的值 "TCP"，"UDP"，"Any"</span><span class="sxs-lookup"><span data-stu-id="b5fec-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5fec-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="b5fec-130">-RemoteIPAddress</span></span>
<span data-ttu-id="b5fec-131">指定要篩選的遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b5fec-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="b5fec-132">[範例] 輸入： [127.0.0.1 "代表單一位址專案。</span><span class="sxs-lookup"><span data-stu-id="b5fec-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="b5fec-133">範圍的 "127.0.0.1-127.0.0.255"。</span><span class="sxs-lookup"><span data-stu-id="b5fec-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="b5fec-134">"127.0.0.1; 127.0.0.5;" 代表多個專案。</span><span class="sxs-lookup"><span data-stu-id="b5fec-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="b5fec-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="b5fec-135">-RemotePort</span></span>
<span data-ttu-id="b5fec-136">指定要篩選的遠端埠。</span><span class="sxs-lookup"><span data-stu-id="b5fec-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="b5fec-137">遠端埠範例輸入：「80」（適用于單一端口專案）。</span><span class="sxs-lookup"><span data-stu-id="b5fec-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="b5fec-138">範圍的 "80-85"。</span><span class="sxs-lookup"><span data-stu-id="b5fec-138">"80-85" for range.</span></span>
<span data-ttu-id="b5fec-139">"80; 443;" （針對多個專案）。</span><span class="sxs-lookup"><span data-stu-id="b5fec-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="b5fec-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fec-140">CommonParameters</span></span>
<span data-ttu-id="b5fec-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5fec-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5fec-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5fec-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fec-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b5fec-143">INPUTS</span></span>

### <span data-ttu-id="b5fec-144">System.object</span><span class="sxs-lookup"><span data-stu-id="b5fec-144">System.String</span></span>

## <span data-ttu-id="b5fec-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b5fec-145">OUTPUTS</span></span>

### <span data-ttu-id="b5fec-146">PSPacketCaptureFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b5fec-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="b5fec-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b5fec-147">NOTES</span></span>
<span data-ttu-id="b5fec-148">關鍵字： azure、azurerm、arm、資源、管理、管理員、網路、網路、觀察者、資料包、捕獲、流量、篩選器</span><span class="sxs-lookup"><span data-stu-id="b5fec-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="b5fec-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5fec-149">RELATED LINKS</span></span>

[<span data-ttu-id="b5fec-150">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5fec-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b5fec-151">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5fec-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b5fec-152">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5fec-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b5fec-153">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5fec-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b5fec-154">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b5fec-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b5fec-155">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b5fec-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b5fec-156">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b5fec-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b5fec-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b5fec-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="b5fec-158">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b5fec-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="b5fec-159">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b5fec-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b5fec-160">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b5fec-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="b5fec-161">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b5fec-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)