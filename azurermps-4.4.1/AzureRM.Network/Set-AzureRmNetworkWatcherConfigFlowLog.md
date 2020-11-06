---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: e8ce107453a447ef2da4cb8528b2f3e1f24a3ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448108"
---
# <span data-ttu-id="482f7-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="482f7-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="482f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="482f7-102">SYNOPSIS</span></span>
<span data-ttu-id="482f7-103">配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="482f7-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="482f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="482f7-104">SYNTAX</span></span>

### <span data-ttu-id="482f7-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="482f7-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="482f7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="482f7-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="482f7-107">說明</span><span class="sxs-lookup"><span data-stu-id="482f7-107">DESCRIPTION</span></span>
<span data-ttu-id="482f7-108">Set-AzureRmNetworkWatcherConfigFlowLog 會配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="482f7-108">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="482f7-109">要設定的屬性包括：是否針對提供的資源啟用流程記錄、已設定的儲存空間帳戶來傳送記錄，以及記錄的保留原則。</span><span class="sxs-lookup"><span data-stu-id="482f7-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="482f7-110">目前支援資料流程記錄的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="482f7-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="482f7-111">示例</span><span class="sxs-lookup"><span data-stu-id="482f7-111">EXAMPLES</span></span>

### <span data-ttu-id="482f7-112">---範例1：針對指定的 NSG 設定流程記錄---</span><span class="sxs-lookup"><span data-stu-id="482f7-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
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

<span data-ttu-id="482f7-113">在這個範例中，我們會設定網路安全性群組的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="482f7-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="482f7-114">在回應中，我們會看到指定的 NSG 已啟用流程記錄，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="482f7-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="482f7-115">參數</span><span class="sxs-lookup"><span data-stu-id="482f7-115">PARAMETERS</span></span>

### <span data-ttu-id="482f7-116">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="482f7-116">-EnableFlowLog</span></span>
<span data-ttu-id="482f7-117">[標記] 可啟用/停用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="482f7-117">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="482f7-118">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="482f7-118">-EnableRetention</span></span>
<span data-ttu-id="482f7-119">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="482f7-119">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="482f7-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="482f7-120">-NetworkWatcher</span></span>
<span data-ttu-id="482f7-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="482f7-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="482f7-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="482f7-122">-NetworkWatcherName</span></span>
<span data-ttu-id="482f7-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="482f7-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="482f7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="482f7-124">-ResourceGroupName</span></span>
<span data-ttu-id="482f7-125">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="482f7-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="482f7-126">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="482f7-126">-RetentionInDays</span></span>
<span data-ttu-id="482f7-127">要保留資料流程記錄記錄的天數。</span><span class="sxs-lookup"><span data-stu-id="482f7-127">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="482f7-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="482f7-128">-StorageAccountId</span></span>
<span data-ttu-id="482f7-129">用來儲存流程記錄的儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="482f7-129">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="482f7-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="482f7-130">-TargetResourceId</span></span>
<span data-ttu-id="482f7-131">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="482f7-131">The target resource ID.</span></span>

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

### <span data-ttu-id="482f7-132">-確認</span><span class="sxs-lookup"><span data-stu-id="482f7-132">-Confirm</span></span>
<span data-ttu-id="482f7-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="482f7-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="482f7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="482f7-134">-WhatIf</span></span>
<span data-ttu-id="482f7-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="482f7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="482f7-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="482f7-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="482f7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="482f7-137">-DefaultProfile</span></span>
<span data-ttu-id="482f7-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="482f7-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="482f7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482f7-139">CommonParameters</span></span>
<span data-ttu-id="482f7-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="482f7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482f7-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="482f7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482f7-142">輸入</span><span class="sxs-lookup"><span data-stu-id="482f7-142">INPUTS</span></span>

### <span data-ttu-id="482f7-143">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="482f7-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="482f7-144">System.object （系統字串） Int32</span><span class="sxs-lookup"><span data-stu-id="482f7-144">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="482f7-145">輸出</span><span class="sxs-lookup"><span data-stu-id="482f7-145">OUTPUTS</span></span>

### <span data-ttu-id="482f7-146">PSFlowLog 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="482f7-146">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="482f7-147">筆記</span><span class="sxs-lookup"><span data-stu-id="482f7-147">NOTES</span></span>
<span data-ttu-id="482f7-148">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，流程，記錄，flowlog，記錄</span><span class="sxs-lookup"><span data-stu-id="482f7-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="482f7-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="482f7-149">RELATED LINKS</span></span>

[<span data-ttu-id="482f7-150">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="482f7-150">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="482f7-151">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="482f7-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="482f7-152">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="482f7-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="482f7-153">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="482f7-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="482f7-154">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="482f7-154">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="482f7-155">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="482f7-155">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="482f7-156">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="482f7-156">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="482f7-157">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="482f7-157">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="482f7-158">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="482f7-158">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="482f7-159">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="482f7-159">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="482f7-160">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="482f7-160">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="482f7-161">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="482f7-161">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="482f7-162">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="482f7-162">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="482f7-163">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="482f7-163">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="482f7-164">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="482f7-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
