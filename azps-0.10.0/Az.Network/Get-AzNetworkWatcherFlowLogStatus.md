---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 2f855175065f743bdfec5fb8dc9c917af262b05b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794387"
---
# <span data-ttu-id="2aadd-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2aadd-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="2aadd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2aadd-102">SYNOPSIS</span></span>
<span data-ttu-id="2aadd-103">取得資源的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="2aadd-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="2aadd-104">句法</span><span class="sxs-lookup"><span data-stu-id="2aadd-104">SYNTAX</span></span>

### <span data-ttu-id="2aadd-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="2aadd-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2aadd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2aadd-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aadd-107">說明</span><span class="sxs-lookup"><span data-stu-id="2aadd-107">DESCRIPTION</span></span>
<span data-ttu-id="2aadd-108">Get-AzNetworkWatcherFlowLogStatus Cmdlet 會取得資源的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="2aadd-108">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="2aadd-109">狀態包括是否針對提供的資源、已設定的儲存空間帳戶來傳送記錄，以及記錄的保留原則，都已啟用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="2aadd-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="2aadd-110">目前支援資料流程記錄的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="2aadd-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="2aadd-111">示例</span><span class="sxs-lookup"><span data-stu-id="2aadd-111">EXAMPLES</span></span>

### <span data-ttu-id="2aadd-112">---範例1：取得指定 NSG 的流程記錄狀態---</span><span class="sxs-lookup"><span data-stu-id="2aadd-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

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

<span data-ttu-id="2aadd-113">在這個範例中，我們會取得網路安全性群組的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="2aadd-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="2aadd-114">指定的 NSG 已啟用流程記錄，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="2aadd-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="2aadd-115">參數</span><span class="sxs-lookup"><span data-stu-id="2aadd-115">PARAMETERS</span></span>

### <span data-ttu-id="2aadd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2aadd-116">-AsJob</span></span>
<span data-ttu-id="2aadd-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2aadd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2aadd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aadd-118">-DefaultProfile</span></span>
<span data-ttu-id="2aadd-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2aadd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aadd-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2aadd-120">-NetworkWatcher</span></span>
<span data-ttu-id="2aadd-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="2aadd-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="2aadd-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2aadd-122">-NetworkWatcherName</span></span>
<span data-ttu-id="2aadd-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="2aadd-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="2aadd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aadd-124">-ResourceGroupName</span></span>
<span data-ttu-id="2aadd-125">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2aadd-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2aadd-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2aadd-126">-TargetResourceId</span></span>
<span data-ttu-id="2aadd-127">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2aadd-127">The target resource ID.</span></span>

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

### <span data-ttu-id="2aadd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aadd-128">CommonParameters</span></span>
<span data-ttu-id="2aadd-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2aadd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aadd-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2aadd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aadd-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2aadd-131">INPUTS</span></span>

### <span data-ttu-id="2aadd-132">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2aadd-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2aadd-133">System.object</span><span class="sxs-lookup"><span data-stu-id="2aadd-133">System.String</span></span>

## <span data-ttu-id="2aadd-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2aadd-134">OUTPUTS</span></span>

### <span data-ttu-id="2aadd-135">PSFlowLog 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2aadd-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="2aadd-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2aadd-136">NOTES</span></span>
<span data-ttu-id="2aadd-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，流程，記錄，flowlog，記錄</span><span class="sxs-lookup"><span data-stu-id="2aadd-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="2aadd-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2aadd-138">RELATED LINKS</span></span>

[<span data-ttu-id="2aadd-139">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2aadd-139">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2aadd-140">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2aadd-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2aadd-141">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2aadd-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2aadd-142">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2aadd-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2aadd-143">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2aadd-143">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2aadd-144">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2aadd-144">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2aadd-145">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2aadd-145">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2aadd-146">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2aadd-146">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2aadd-147">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2aadd-147">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2aadd-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2aadd-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2aadd-149">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2aadd-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2aadd-150">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2aadd-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2aadd-151">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2aadd-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2aadd-152">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2aadd-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2aadd-153">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2aadd-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
