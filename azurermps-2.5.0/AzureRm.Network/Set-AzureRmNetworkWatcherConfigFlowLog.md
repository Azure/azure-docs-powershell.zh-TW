---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
ms.openlocfilehash: e8e8462ded1f122a050c85877e8e82b2ecc0dd9d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800058"
---
# <span data-ttu-id="94fcf-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="94fcf-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="94fcf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="94fcf-103">配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="94fcf-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94fcf-104">句法</span><span class="sxs-lookup"><span data-stu-id="94fcf-104">SYNTAX</span></span>

### <span data-ttu-id="94fcf-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="94fcf-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94fcf-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="94fcf-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94fcf-107">說明</span><span class="sxs-lookup"><span data-stu-id="94fcf-107">DESCRIPTION</span></span>
<span data-ttu-id="94fcf-108">Set-AzureRmNetworkWatcherConfigFlowLog 會配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="94fcf-108">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="94fcf-109">要設定的屬性包括：是否針對提供的資源啟用流程記錄、已設定的儲存空間帳戶來傳送記錄，以及記錄的保留原則。</span><span class="sxs-lookup"><span data-stu-id="94fcf-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="94fcf-110">目前支援資料流程記錄的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="94fcf-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="94fcf-111">示例</span><span class="sxs-lookup"><span data-stu-id="94fcf-111">EXAMPLES</span></span>

### <span data-ttu-id="94fcf-112">---範例1：針對指定的 NSG 設定流程記錄---</span><span class="sxs-lookup"><span data-stu-id="94fcf-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="94fcf-113">在這個範例中，我們會設定網路安全性群組的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="94fcf-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="94fcf-114">在回應中，我們會看到指定的 NSG 已啟用流程記錄，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="94fcf-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="94fcf-115">參數</span><span class="sxs-lookup"><span data-stu-id="94fcf-115">PARAMETERS</span></span>

### <span data-ttu-id="94fcf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94fcf-116">-AsJob</span></span>
<span data-ttu-id="94fcf-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="94fcf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94fcf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94fcf-118">-DefaultProfile</span></span>
<span data-ttu-id="94fcf-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94fcf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94fcf-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="94fcf-120">-EnableFlowLog</span></span>
<span data-ttu-id="94fcf-121">[標記] 可啟用/停用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="94fcf-121">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94fcf-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="94fcf-122">-EnableRetention</span></span>
<span data-ttu-id="94fcf-123">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="94fcf-123">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94fcf-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="94fcf-124">-NetworkWatcher</span></span>
<span data-ttu-id="94fcf-125">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="94fcf-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="94fcf-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="94fcf-126">-NetworkWatcherName</span></span>
<span data-ttu-id="94fcf-127">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="94fcf-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="94fcf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94fcf-128">-ResourceGroupName</span></span>
<span data-ttu-id="94fcf-129">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94fcf-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="94fcf-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="94fcf-130">-RetentionInDays</span></span>
<span data-ttu-id="94fcf-131">要保留資料流程記錄記錄的天數。</span><span class="sxs-lookup"><span data-stu-id="94fcf-131">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94fcf-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="94fcf-132">-StorageAccountId</span></span>
<span data-ttu-id="94fcf-133">用來儲存流程記錄的儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="94fcf-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="94fcf-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="94fcf-134">-TargetResourceId</span></span>
<span data-ttu-id="94fcf-135">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="94fcf-135">The target resource ID.</span></span>

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

### <span data-ttu-id="94fcf-136">-確認</span><span class="sxs-lookup"><span data-stu-id="94fcf-136">-Confirm</span></span>
<span data-ttu-id="94fcf-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94fcf-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94fcf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94fcf-138">-WhatIf</span></span>
<span data-ttu-id="94fcf-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94fcf-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94fcf-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94fcf-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94fcf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94fcf-141">CommonParameters</span></span>
<span data-ttu-id="94fcf-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94fcf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94fcf-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94fcf-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94fcf-144">輸入</span><span class="sxs-lookup"><span data-stu-id="94fcf-144">INPUTS</span></span>

### <span data-ttu-id="94fcf-145">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="94fcf-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="94fcf-146">System.object （系統字串） Int32</span><span class="sxs-lookup"><span data-stu-id="94fcf-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="94fcf-147">輸出</span><span class="sxs-lookup"><span data-stu-id="94fcf-147">OUTPUTS</span></span>

### <span data-ttu-id="94fcf-148">PSFlowLog 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="94fcf-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="94fcf-149">筆記</span><span class="sxs-lookup"><span data-stu-id="94fcf-149">NOTES</span></span>
<span data-ttu-id="94fcf-150">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，流程，記錄，flowlog，記錄</span><span class="sxs-lookup"><span data-stu-id="94fcf-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="94fcf-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="94fcf-151">RELATED LINKS</span></span>

[<span data-ttu-id="94fcf-152">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="94fcf-152">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="94fcf-153">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="94fcf-153">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="94fcf-154">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="94fcf-154">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="94fcf-155">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="94fcf-155">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="94fcf-156">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="94fcf-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="94fcf-157">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="94fcf-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="94fcf-158">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="94fcf-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="94fcf-159">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="94fcf-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="94fcf-160">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="94fcf-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="94fcf-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="94fcf-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="94fcf-162">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="94fcf-162">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="94fcf-163">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="94fcf-163">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="94fcf-164">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="94fcf-164">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="94fcf-165">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="94fcf-165">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="94fcf-166">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="94fcf-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
