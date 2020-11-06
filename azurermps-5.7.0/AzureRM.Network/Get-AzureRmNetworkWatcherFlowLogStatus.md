---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 1904e9df565a5f9e8d3738e723348ec96010f97a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449861"
---
# <span data-ttu-id="39464-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="39464-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="39464-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39464-102">SYNOPSIS</span></span>
<span data-ttu-id="39464-103">取得資源的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="39464-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39464-104">句法</span><span class="sxs-lookup"><span data-stu-id="39464-104">SYNTAX</span></span>

### <span data-ttu-id="39464-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="39464-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39464-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="39464-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39464-107">說明</span><span class="sxs-lookup"><span data-stu-id="39464-107">DESCRIPTION</span></span>
<span data-ttu-id="39464-108">Get-AzureRmNetworkWatcherFlowLogStatus Cmdlet 會取得資源的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="39464-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="39464-109">狀態包括是否針對提供的資源、已設定的儲存空間帳戶來傳送記錄，以及記錄的保留原則，都已啟用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="39464-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="39464-110">目前支援資料流程記錄的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="39464-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="39464-111">示例</span><span class="sxs-lookup"><span data-stu-id="39464-111">EXAMPLES</span></span>

### <span data-ttu-id="39464-112">---範例1：取得指定 NSG 的流程記錄狀態---</span><span class="sxs-lookup"><span data-stu-id="39464-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                   }
```

<span data-ttu-id="39464-113">在這個範例中，我們會取得網路安全性群組的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="39464-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="39464-114">指定的 NSG 已啟用流程記錄，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="39464-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="39464-115">參數</span><span class="sxs-lookup"><span data-stu-id="39464-115">PARAMETERS</span></span>

### <span data-ttu-id="39464-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39464-116">-AsJob</span></span>
<span data-ttu-id="39464-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="39464-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39464-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39464-118">-DefaultProfile</span></span>
<span data-ttu-id="39464-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39464-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39464-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39464-120">-NetworkWatcher</span></span>
<span data-ttu-id="39464-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="39464-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="39464-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="39464-122">-NetworkWatcherName</span></span>
<span data-ttu-id="39464-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="39464-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="39464-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39464-124">-ResourceGroupName</span></span>
<span data-ttu-id="39464-125">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="39464-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="39464-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="39464-126">-TargetResourceId</span></span>
<span data-ttu-id="39464-127">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="39464-127">The target resource ID.</span></span>

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

### <span data-ttu-id="39464-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39464-128">CommonParameters</span></span>
<span data-ttu-id="39464-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39464-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39464-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39464-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39464-131">輸入</span><span class="sxs-lookup"><span data-stu-id="39464-131">INPUTS</span></span>

### <span data-ttu-id="39464-132">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="39464-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="39464-133">System.object</span><span class="sxs-lookup"><span data-stu-id="39464-133">System.String</span></span>

## <span data-ttu-id="39464-134">輸出</span><span class="sxs-lookup"><span data-stu-id="39464-134">OUTPUTS</span></span>

### <span data-ttu-id="39464-135">PSFlowLog 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="39464-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="39464-136">筆記</span><span class="sxs-lookup"><span data-stu-id="39464-136">NOTES</span></span>
<span data-ttu-id="39464-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，流程，記錄，flowlog，記錄</span><span class="sxs-lookup"><span data-stu-id="39464-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="39464-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="39464-138">RELATED LINKS</span></span>

[<span data-ttu-id="39464-139">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="39464-139">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="39464-140">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39464-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="39464-141">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39464-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="39464-142">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39464-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="39464-143">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39464-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="39464-144">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="39464-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="39464-145">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39464-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="39464-146">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39464-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="39464-147">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39464-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="39464-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="39464-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="39464-149">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="39464-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="39464-150">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="39464-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="39464-151">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="39464-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="39464-152">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="39464-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="39464-153">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="39464-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
