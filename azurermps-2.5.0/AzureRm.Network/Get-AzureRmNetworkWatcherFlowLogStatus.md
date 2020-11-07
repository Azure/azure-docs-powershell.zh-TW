---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
ms.openlocfilehash: 96d3bea781b0c595b54387a9b07b085f173d7b0a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800433"
---
# <span data-ttu-id="2afcf-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2afcf-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="2afcf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2afcf-102">SYNOPSIS</span></span>
<span data-ttu-id="2afcf-103">取得資源的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="2afcf-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2afcf-104">句法</span><span class="sxs-lookup"><span data-stu-id="2afcf-104">SYNTAX</span></span>

### <span data-ttu-id="2afcf-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="2afcf-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2afcf-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2afcf-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2afcf-107">說明</span><span class="sxs-lookup"><span data-stu-id="2afcf-107">DESCRIPTION</span></span>
<span data-ttu-id="2afcf-108">Get-AzureRmNetworkWatcherFlowLogStatus Cmdlet 會取得資源的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="2afcf-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="2afcf-109">狀態包括是否針對提供的資源、已設定的儲存空間帳戶來傳送記錄，以及記錄的保留原則，都已啟用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="2afcf-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="2afcf-110">目前支援資料流程記錄的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="2afcf-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="2afcf-111">示例</span><span class="sxs-lookup"><span data-stu-id="2afcf-111">EXAMPLES</span></span>

### <span data-ttu-id="2afcf-112">---範例1：取得指定 NSG 的流程記錄狀態---</span><span class="sxs-lookup"><span data-stu-id="2afcf-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
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

<span data-ttu-id="2afcf-113">在這個範例中，我們會取得網路安全性群組的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="2afcf-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="2afcf-114">指定的 NSG 已啟用流程記錄，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="2afcf-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="2afcf-115">參數</span><span class="sxs-lookup"><span data-stu-id="2afcf-115">PARAMETERS</span></span>

### <span data-ttu-id="2afcf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2afcf-116">-AsJob</span></span>
<span data-ttu-id="2afcf-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2afcf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2afcf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2afcf-118">-DefaultProfile</span></span>
<span data-ttu-id="2afcf-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2afcf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2afcf-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2afcf-120">-NetworkWatcher</span></span>
<span data-ttu-id="2afcf-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="2afcf-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="2afcf-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2afcf-122">-NetworkWatcherName</span></span>
<span data-ttu-id="2afcf-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="2afcf-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="2afcf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2afcf-124">-ResourceGroupName</span></span>
<span data-ttu-id="2afcf-125">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2afcf-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2afcf-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2afcf-126">-TargetResourceId</span></span>
<span data-ttu-id="2afcf-127">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2afcf-127">The target resource ID.</span></span>

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

### <span data-ttu-id="2afcf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2afcf-128">CommonParameters</span></span>
<span data-ttu-id="2afcf-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2afcf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2afcf-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2afcf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2afcf-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2afcf-131">INPUTS</span></span>

### <span data-ttu-id="2afcf-132">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2afcf-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2afcf-133">System.object</span><span class="sxs-lookup"><span data-stu-id="2afcf-133">System.String</span></span>

## <span data-ttu-id="2afcf-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2afcf-134">OUTPUTS</span></span>

### <span data-ttu-id="2afcf-135">PSFlowLog 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2afcf-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="2afcf-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2afcf-136">NOTES</span></span>
<span data-ttu-id="2afcf-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，流程，記錄，flowlog，記錄</span><span class="sxs-lookup"><span data-stu-id="2afcf-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="2afcf-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2afcf-138">RELATED LINKS</span></span>

[<span data-ttu-id="2afcf-139">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2afcf-139">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2afcf-140">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2afcf-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2afcf-141">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2afcf-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2afcf-142">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2afcf-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2afcf-143">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2afcf-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2afcf-144">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2afcf-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2afcf-145">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2afcf-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2afcf-146">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2afcf-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2afcf-147">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2afcf-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2afcf-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2afcf-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2afcf-149">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2afcf-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="2afcf-150">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2afcf-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2afcf-151">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2afcf-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2afcf-152">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2afcf-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2afcf-153">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2afcf-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
