---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
ms.openlocfilehash: 4e9c99f2985be335f2750e500ee0c01394195c39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625702"
---
# <span data-ttu-id="ebc3b-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ebc3b-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="ebc3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebc3b-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc3b-103">傳回指定來源 VM 與目的地的連線資訊。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebc3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebc3b-104">SYNTAX</span></span>

### <span data-ttu-id="ebc3b-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="ebc3b-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebc3b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ebc3b-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebc3b-107">說明</span><span class="sxs-lookup"><span data-stu-id="ebc3b-107">DESCRIPTION</span></span>
<span data-ttu-id="ebc3b-108">Test-AzureRmNetworkWatcherConnectivity Cmdlet 會傳回指定來源 VM 與目的地的連線資訊。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-108">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="ebc3b-109">如果無法建立來源與目的地之間的連線，此 Cmdlet 會傳回問題的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="ebc3b-110">示例</span><span class="sxs-lookup"><span data-stu-id="ebc3b-110">EXAMPLES</span></span>

### <span data-ttu-id="ebc3b-111">---------------範例1：測試從 VM 到網站---------------的網路觀察程式連線能力</span><span class="sxs-lookup"><span data-stu-id="ebc3b-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
<span data-ttu-id="ebc3b-112">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="ebc3b-112">@{paragraph=PS C:\\\>}</span></span>










```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="ebc3b-113">在這個範例中，我們會測試 Azure 中 VM 的連線性與 www.bing.com。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="ebc3b-114">參數</span><span class="sxs-lookup"><span data-stu-id="ebc3b-114">PARAMETERS</span></span>

### <span data-ttu-id="ebc3b-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ebc3b-115">-DestinationAddress</span></span>
<span data-ttu-id="ebc3b-116">要建立連線之資源的 IP 位址或 URI。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-116">The IP address or URI the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc3b-117">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="ebc3b-117">-DestinationId</span></span>
<span data-ttu-id="ebc3b-118">要進行連線嘗試的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-118">The ID of the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc3b-119">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ebc3b-119">-DestinationPort</span></span>
<span data-ttu-id="ebc3b-120">將在其上執行檢查連線的埠。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-120">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc3b-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ebc3b-121">-NetworkWatcher</span></span>
<span data-ttu-id="ebc3b-122">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="ebc3b-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ebc3b-123">-NetworkWatcherName</span></span>
<span data-ttu-id="ebc3b-124">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-124">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc3b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc3b-125">-ResourceGroupName</span></span>
<span data-ttu-id="ebc3b-126">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ebc3b-127">-SourceId</span><span class="sxs-lookup"><span data-stu-id="ebc3b-127">-SourceId</span></span>
<span data-ttu-id="ebc3b-128">將啟動連線檢查的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-128">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="ebc3b-129">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="ebc3b-129">-SourcePort</span></span>
<span data-ttu-id="ebc3b-130">將執行連線檢查的來源埠。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-130">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc3b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc3b-131">-DefaultProfile</span></span>
<span data-ttu-id="ebc3b-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebc3b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc3b-133">CommonParameters</span></span>
<span data-ttu-id="ebc3b-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc3b-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ebc3b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc3b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ebc3b-136">INPUTS</span></span>

### <span data-ttu-id="ebc3b-137">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ebc3b-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ebc3b-138">字串 System.object （system.object）</span><span class="sxs-lookup"><span data-stu-id="ebc3b-138">System.String System.Int32</span></span>

## <span data-ttu-id="ebc3b-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ebc3b-139">OUTPUTS</span></span>

### <span data-ttu-id="ebc3b-140">PSConnectivityInformation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ebc3b-140">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="ebc3b-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ebc3b-141">NOTES</span></span>
<span data-ttu-id="ebc3b-142">關鍵字： azure、azurerm、arm、資源、連線性、管理、管理員、網路、網路、網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="ebc3b-142">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="ebc3b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebc3b-143">RELATED LINKS</span></span>

<span data-ttu-id="ebc3b-144">[新-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
[AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
[移除-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="ebc3b-144">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="ebc3b-145">[AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
[AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
[AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
[AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="ebc3b-145">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="ebc3b-146">[新-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
[新-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
[AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
[移除-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
[停止 AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="ebc3b-146">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>
