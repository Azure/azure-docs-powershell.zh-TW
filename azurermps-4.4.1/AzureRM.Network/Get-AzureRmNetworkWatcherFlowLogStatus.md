---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 1c7e67eacc52e995632a526514c84bf7a9f45425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453392"
---
# <span data-ttu-id="a556f-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a556f-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="a556f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a556f-102">SYNOPSIS</span></span>
<span data-ttu-id="a556f-103">取得資源的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="a556f-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a556f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a556f-104">SYNTAX</span></span>

### <span data-ttu-id="a556f-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a556f-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a556f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a556f-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a556f-107">說明</span><span class="sxs-lookup"><span data-stu-id="a556f-107">DESCRIPTION</span></span>
<span data-ttu-id="a556f-108">Get-AzureRmNetworkWatcherFlowLogStatus Cmdlet 會取得資源的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="a556f-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="a556f-109">狀態包括是否針對提供的資源、已設定的儲存空間帳戶來傳送記錄，以及記錄的保留原則，都已啟用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="a556f-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="a556f-110">目前支援資料流程記錄的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a556f-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="a556f-111">示例</span><span class="sxs-lookup"><span data-stu-id="a556f-111">EXAMPLES</span></span>

### <span data-ttu-id="a556f-112">---範例1：取得指定 NSG 的流程記錄狀態---</span><span class="sxs-lookup"><span data-stu-id="a556f-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
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

<span data-ttu-id="a556f-113">在這個範例中，我們會取得網路安全性群組的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="a556f-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="a556f-114">指定的 NSG 已啟用流程記錄，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="a556f-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="a556f-115">參數</span><span class="sxs-lookup"><span data-stu-id="a556f-115">PARAMETERS</span></span>

### <span data-ttu-id="a556f-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a556f-116">-NetworkWatcher</span></span>
<span data-ttu-id="a556f-117">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="a556f-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="a556f-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a556f-118">-NetworkWatcherName</span></span>
<span data-ttu-id="a556f-119">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a556f-119">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a556f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a556f-120">-ResourceGroupName</span></span>
<span data-ttu-id="a556f-121">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a556f-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a556f-122">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a556f-122">-TargetResourceId</span></span>
<span data-ttu-id="a556f-123">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a556f-123">The target resource ID.</span></span>

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

### <span data-ttu-id="a556f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a556f-124">-DefaultProfile</span></span>
<span data-ttu-id="a556f-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a556f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a556f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a556f-126">CommonParameters</span></span>
<span data-ttu-id="a556f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a556f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a556f-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a556f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a556f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a556f-129">INPUTS</span></span>

### <span data-ttu-id="a556f-130">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a556f-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a556f-131">System.object</span><span class="sxs-lookup"><span data-stu-id="a556f-131">System.String</span></span>

## <span data-ttu-id="a556f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="a556f-132">OUTPUTS</span></span>

### <span data-ttu-id="a556f-133">PSFlowLog 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a556f-133">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="a556f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="a556f-134">NOTES</span></span>
<span data-ttu-id="a556f-135">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，流程，記錄，flowlog，記錄</span><span class="sxs-lookup"><span data-stu-id="a556f-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="a556f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a556f-136">RELATED LINKS</span></span>

[<span data-ttu-id="a556f-137">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a556f-137">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a556f-138">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a556f-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a556f-139">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a556f-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a556f-140">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a556f-140">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a556f-141">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a556f-141">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a556f-142">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a556f-142">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="a556f-143">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a556f-143">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a556f-144">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a556f-144">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a556f-145">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a556f-145">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a556f-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a556f-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="a556f-147">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a556f-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="a556f-148">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a556f-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a556f-149">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a556f-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="a556f-150">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a556f-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a556f-151">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a556f-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
