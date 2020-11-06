---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: ef730b8ee6e6c35408b9d57d9dc23b0ab51a63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447063"
---
# <span data-ttu-id="5db81-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5db81-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="5db81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5db81-102">SYNOPSIS</span></span>
<span data-ttu-id="5db81-103">從先前執行或目前正在執行的疑難排解作業中取得疑難排解結果。</span><span class="sxs-lookup"><span data-stu-id="5db81-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5db81-104">句法</span><span class="sxs-lookup"><span data-stu-id="5db81-104">SYNTAX</span></span>

### <span data-ttu-id="5db81-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="5db81-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5db81-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5db81-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5db81-107">說明</span><span class="sxs-lookup"><span data-stu-id="5db81-107">DESCRIPTION</span></span>
<span data-ttu-id="5db81-108">Get-AzureRmNetworkWatcherTroubleshootingResult Cmdlet 會從先前執行或目前正在執行的 Start-AzureRmNetworkWatcherResourceTroubleshooting 操作中取得疑難排解結果。</span><span class="sxs-lookup"><span data-stu-id="5db81-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="5db81-109">如果正在進行疑難排解作業，則可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="5db81-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="5db81-110">目前支援虛擬網路閘道和連線。</span><span class="sxs-lookup"><span data-stu-id="5db81-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="5db81-111">示例</span><span class="sxs-lookup"><span data-stu-id="5db81-111">EXAMPLES</span></span>

### <span data-ttu-id="5db81-112">---範例1：在虛擬網路閘道開始疑難排解，並取得結果---</span><span class="sxs-lookup"><span data-stu-id="5db81-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="5db81-113">上述範例會在虛擬網路閘道開始進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="5db81-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="5db81-114">作業可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="5db81-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="5db81-115">在疑難排解已開始之後，就會對資源進行 Get-AzureRmNetworkWatcherTroubleshootingResult 呼叫，以取得此通話的結果。</span><span class="sxs-lookup"><span data-stu-id="5db81-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="5db81-116">參數</span><span class="sxs-lookup"><span data-stu-id="5db81-116">PARAMETERS</span></span>

### <span data-ttu-id="5db81-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db81-117">-DefaultProfile</span></span>
<span data-ttu-id="5db81-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5db81-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5db81-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5db81-119">-NetworkWatcher</span></span>
<span data-ttu-id="5db81-120">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="5db81-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="5db81-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5db81-121">-NetworkWatcherName</span></span>
<span data-ttu-id="5db81-122">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="5db81-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="5db81-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db81-123">-ResourceGroupName</span></span>
<span data-ttu-id="5db81-124">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5db81-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5db81-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="5db81-125">-TargetResourceId</span></span>
<span data-ttu-id="5db81-126">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5db81-126">The target resource ID.</span></span>

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

### <span data-ttu-id="5db81-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db81-127">CommonParameters</span></span>
<span data-ttu-id="5db81-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5db81-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db81-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5db81-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db81-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5db81-130">INPUTS</span></span>

### <span data-ttu-id="5db81-131">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5db81-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5db81-132">System.object</span><span class="sxs-lookup"><span data-stu-id="5db81-132">System.String</span></span>

## <span data-ttu-id="5db81-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5db81-133">OUTPUTS</span></span>

### <span data-ttu-id="5db81-134">PSViewNsgRules 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5db81-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="5db81-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5db81-135">NOTES</span></span>
<span data-ttu-id="5db81-136">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，疑難排解，VPN，連線</span><span class="sxs-lookup"><span data-stu-id="5db81-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="5db81-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="5db81-137">RELATED LINKS</span></span>

[<span data-ttu-id="5db81-138">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5db81-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5db81-139">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5db81-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5db81-140">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5db81-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5db81-141">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5db81-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5db81-142">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5db81-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5db81-143">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5db81-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5db81-144">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5db81-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5db81-145">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5db81-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5db81-146">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5db81-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5db81-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5db81-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5db81-148">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5db81-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5db81-149">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5db81-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5db81-150">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5db81-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
