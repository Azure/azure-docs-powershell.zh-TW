---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: c3d1e7e3a76a2561c77c8d580b7365f8fd2e6fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794380"
---
# <span data-ttu-id="ab785-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ab785-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="ab785-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab785-102">SYNOPSIS</span></span>
<span data-ttu-id="ab785-103">從先前執行或目前正在執行的疑難排解作業中取得疑難排解結果。</span><span class="sxs-lookup"><span data-stu-id="ab785-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="ab785-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab785-104">SYNTAX</span></span>

### <span data-ttu-id="ab785-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="ab785-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab785-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ab785-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab785-107">說明</span><span class="sxs-lookup"><span data-stu-id="ab785-107">DESCRIPTION</span></span>
<span data-ttu-id="ab785-108">Get-AzNetworkWatcherTroubleshootingResult Cmdlet 會從先前執行或目前正在執行的 Start-AzNetworkWatcherResourceTroubleshooting 操作中取得疑難排解結果。</span><span class="sxs-lookup"><span data-stu-id="ab785-108">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="ab785-109">如果正在進行疑難排解作業，則可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="ab785-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="ab785-110">目前支援虛擬網路閘道和連線。</span><span class="sxs-lookup"><span data-stu-id="ab785-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="ab785-111">示例</span><span class="sxs-lookup"><span data-stu-id="ab785-111">EXAMPLES</span></span>

### <span data-ttu-id="ab785-112">---範例1：在虛擬網路閘道開始疑難排解，並取得結果---</span><span class="sxs-lookup"><span data-stu-id="ab785-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="ab785-113">上述範例會在虛擬網路閘道開始進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="ab785-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="ab785-114">作業可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="ab785-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="ab785-115">在疑難排解已開始之後，就會對資源進行 Get-AzNetworkWatcherTroubleshootingResult 呼叫，以取得此通話的結果。</span><span class="sxs-lookup"><span data-stu-id="ab785-115">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="ab785-116">參數</span><span class="sxs-lookup"><span data-stu-id="ab785-116">PARAMETERS</span></span>

### <span data-ttu-id="ab785-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab785-117">-DefaultProfile</span></span>
<span data-ttu-id="ab785-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab785-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab785-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab785-119">-NetworkWatcher</span></span>
<span data-ttu-id="ab785-120">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="ab785-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="ab785-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ab785-121">-NetworkWatcherName</span></span>
<span data-ttu-id="ab785-122">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab785-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="ab785-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab785-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab785-124">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab785-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ab785-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ab785-125">-TargetResourceId</span></span>
<span data-ttu-id="ab785-126">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ab785-126">The target resource ID.</span></span>

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

### <span data-ttu-id="ab785-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab785-127">CommonParameters</span></span>
<span data-ttu-id="ab785-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab785-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab785-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab785-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab785-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ab785-130">INPUTS</span></span>

### <span data-ttu-id="ab785-131">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab785-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ab785-132">System.object</span><span class="sxs-lookup"><span data-stu-id="ab785-132">System.String</span></span>

## <span data-ttu-id="ab785-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ab785-133">OUTPUTS</span></span>

### <span data-ttu-id="ab785-134">PSViewNsgRules 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab785-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="ab785-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ab785-135">NOTES</span></span>
<span data-ttu-id="ab785-136">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，疑難排解，VPN，連線</span><span class="sxs-lookup"><span data-stu-id="ab785-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="ab785-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab785-137">RELATED LINKS</span></span>

[<span data-ttu-id="ab785-138">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ab785-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ab785-139">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab785-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ab785-140">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab785-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ab785-141">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab785-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ab785-142">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab785-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ab785-143">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ab785-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ab785-144">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab785-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ab785-145">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab785-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ab785-146">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab785-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ab785-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ab785-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ab785-148">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ab785-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ab785-149">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ab785-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ab785-150">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ab785-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
