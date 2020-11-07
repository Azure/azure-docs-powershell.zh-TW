---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: a72f494518b3a511eac3e4b1a92330f666bbca64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795366"
---
# <span data-ttu-id="dacb0-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dacb0-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="dacb0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dacb0-102">SYNOPSIS</span></span>
<span data-ttu-id="dacb0-103">開始針對 Azure 中的網路資源進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="dacb0-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="dacb0-104">句法</span><span class="sxs-lookup"><span data-stu-id="dacb0-104">SYNTAX</span></span>

### <span data-ttu-id="dacb0-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="dacb0-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dacb0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="dacb0-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dacb0-107">說明</span><span class="sxs-lookup"><span data-stu-id="dacb0-107">DESCRIPTION</span></span>
<span data-ttu-id="dacb0-108">Start-AzNetworkWatcherResourceTroubleshooting Cmdlet 會針對 Azure 中的網路資源開始疑難排解，並傳回潛在問題與緩解措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dacb0-108">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="dacb0-109">目前支援虛擬網路閘道和連線。</span><span class="sxs-lookup"><span data-stu-id="dacb0-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="dacb0-110">示例</span><span class="sxs-lookup"><span data-stu-id="dacb0-110">EXAMPLES</span></span>

### <span data-ttu-id="dacb0-111">---範例1：啟動虛擬網路閘道的疑難排解---</span><span class="sxs-lookup"><span data-stu-id="dacb0-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="dacb0-112">上述範例會在虛擬網路閘道開始進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="dacb0-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="dacb0-113">作業可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="dacb0-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="dacb0-114">參數</span><span class="sxs-lookup"><span data-stu-id="dacb0-114">PARAMETERS</span></span>

### <span data-ttu-id="dacb0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dacb0-115">-DefaultProfile</span></span>
<span data-ttu-id="dacb0-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dacb0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dacb0-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dacb0-117">-NetworkWatcher</span></span>
<span data-ttu-id="dacb0-118">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="dacb0-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="dacb0-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dacb0-119">-NetworkWatcherName</span></span>
<span data-ttu-id="dacb0-120">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="dacb0-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="dacb0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dacb0-121">-ResourceGroupName</span></span>
<span data-ttu-id="dacb0-122">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dacb0-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="dacb0-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="dacb0-123">-StorageId</span></span>
<span data-ttu-id="dacb0-124">[儲存空間識別碼]。</span><span class="sxs-lookup"><span data-stu-id="dacb0-124">The storage ID.</span></span>

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

### <span data-ttu-id="dacb0-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="dacb0-125">-StoragePath</span></span>
<span data-ttu-id="dacb0-126">儲存路徑。</span><span class="sxs-lookup"><span data-stu-id="dacb0-126">The storage path.</span></span>

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

### <span data-ttu-id="dacb0-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="dacb0-127">-TargetResourceId</span></span>
<span data-ttu-id="dacb0-128">指定要進行疑難排解之資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dacb0-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="dacb0-129">範例格式： "/subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="dacb0-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="dacb0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dacb0-130">CommonParameters</span></span>
<span data-ttu-id="dacb0-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dacb0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dacb0-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dacb0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dacb0-133">輸入</span><span class="sxs-lookup"><span data-stu-id="dacb0-133">INPUTS</span></span>

### <span data-ttu-id="dacb0-134">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dacb0-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="dacb0-135">System.object</span><span class="sxs-lookup"><span data-stu-id="dacb0-135">System.String</span></span>

## <span data-ttu-id="dacb0-136">輸出</span><span class="sxs-lookup"><span data-stu-id="dacb0-136">OUTPUTS</span></span>

### <span data-ttu-id="dacb0-137">PSViewNsgRules 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dacb0-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="dacb0-138">筆記</span><span class="sxs-lookup"><span data-stu-id="dacb0-138">NOTES</span></span>
<span data-ttu-id="dacb0-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，疑難排解，VPN，連線</span><span class="sxs-lookup"><span data-stu-id="dacb0-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="dacb0-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="dacb0-140">RELATED LINKS</span></span>

[<span data-ttu-id="dacb0-141">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="dacb0-141">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="dacb0-142">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dacb0-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="dacb0-143">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dacb0-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="dacb0-144">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dacb0-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="dacb0-145">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dacb0-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dacb0-146">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dacb0-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="dacb0-147">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dacb0-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dacb0-148">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dacb0-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dacb0-149">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dacb0-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dacb0-150">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dacb0-150">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="dacb0-151">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dacb0-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="dacb0-152">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dacb0-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dacb0-153">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dacb0-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
