---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermnetworkwatcherresourcetroubleshooting
schema: 2.0.0
ms.openlocfilehash: 411b70fb6018b71b1c1c7fbf67816d0c86e6d3b6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800342"
---
# <span data-ttu-id="8efd7-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8efd7-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="8efd7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8efd7-102">SYNOPSIS</span></span>
<span data-ttu-id="8efd7-103">開始針對 Azure 中的網路資源進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="8efd7-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8efd7-104">句法</span><span class="sxs-lookup"><span data-stu-id="8efd7-104">SYNTAX</span></span>

### <span data-ttu-id="8efd7-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="8efd7-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8efd7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8efd7-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8efd7-107">說明</span><span class="sxs-lookup"><span data-stu-id="8efd7-107">DESCRIPTION</span></span>
<span data-ttu-id="8efd7-108">Start-AzureRmNetworkWatcherResourceTroubleshooting Cmdlet 會針對 Azure 中的網路資源開始疑難排解，並傳回潛在問題與緩解措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8efd7-108">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="8efd7-109">目前支援虛擬網路閘道和連線。</span><span class="sxs-lookup"><span data-stu-id="8efd7-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="8efd7-110">示例</span><span class="sxs-lookup"><span data-stu-id="8efd7-110">EXAMPLES</span></span>

### <span data-ttu-id="8efd7-111">---範例1：啟動虛擬網路閘道的疑難排解---</span><span class="sxs-lookup"><span data-stu-id="8efd7-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="8efd7-112">上述範例會在虛擬網路閘道開始進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="8efd7-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="8efd7-113">作業可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="8efd7-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="8efd7-114">參數</span><span class="sxs-lookup"><span data-stu-id="8efd7-114">PARAMETERS</span></span>

### <span data-ttu-id="8efd7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8efd7-115">-DefaultProfile</span></span>
<span data-ttu-id="8efd7-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8efd7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8efd7-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8efd7-117">-NetworkWatcher</span></span>
<span data-ttu-id="8efd7-118">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="8efd7-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="8efd7-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8efd7-119">-NetworkWatcherName</span></span>
<span data-ttu-id="8efd7-120">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="8efd7-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="8efd7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8efd7-121">-ResourceGroupName</span></span>
<span data-ttu-id="8efd7-122">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8efd7-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8efd7-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="8efd7-123">-StorageId</span></span>
<span data-ttu-id="8efd7-124">[儲存空間識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8efd7-124">The storage ID.</span></span>

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

### <span data-ttu-id="8efd7-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="8efd7-125">-StoragePath</span></span>
<span data-ttu-id="8efd7-126">儲存路徑。</span><span class="sxs-lookup"><span data-stu-id="8efd7-126">The storage path.</span></span>

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

### <span data-ttu-id="8efd7-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8efd7-127">-TargetResourceId</span></span>
<span data-ttu-id="8efd7-128">指定要進行疑難排解之資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8efd7-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="8efd7-129">範例格式： "/subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="8efd7-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="8efd7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8efd7-130">CommonParameters</span></span>
<span data-ttu-id="8efd7-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8efd7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8efd7-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8efd7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8efd7-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8efd7-133">INPUTS</span></span>

### <span data-ttu-id="8efd7-134">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8efd7-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8efd7-135">System.object</span><span class="sxs-lookup"><span data-stu-id="8efd7-135">System.String</span></span>

## <span data-ttu-id="8efd7-136">輸出</span><span class="sxs-lookup"><span data-stu-id="8efd7-136">OUTPUTS</span></span>

### <span data-ttu-id="8efd7-137">PSViewNsgRules 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8efd7-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="8efd7-138">筆記</span><span class="sxs-lookup"><span data-stu-id="8efd7-138">NOTES</span></span>
<span data-ttu-id="8efd7-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，疑難排解，VPN，連線</span><span class="sxs-lookup"><span data-stu-id="8efd7-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="8efd7-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="8efd7-140">RELATED LINKS</span></span>

[<span data-ttu-id="8efd7-141">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8efd7-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8efd7-142">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8efd7-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8efd7-143">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8efd7-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8efd7-144">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8efd7-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8efd7-145">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8efd7-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8efd7-146">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8efd7-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="8efd7-147">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8efd7-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8efd7-148">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8efd7-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8efd7-149">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8efd7-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8efd7-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8efd7-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="8efd7-151">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8efd7-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="8efd7-152">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8efd7-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8efd7-153">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8efd7-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
