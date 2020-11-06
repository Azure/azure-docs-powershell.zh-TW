---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 20d59fb2a112b32c95b380c114ebc1b365569235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447332"
---
# <span data-ttu-id="1968e-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1968e-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="1968e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1968e-102">SYNOPSIS</span></span>
<span data-ttu-id="1968e-103">配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="1968e-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1968e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1968e-104">SYNTAX</span></span>

### <span data-ttu-id="1968e-105">SetFlowlogByResourceWithoutTA (預設) </span><span class="sxs-lookup"><span data-stu-id="1968e-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1968e-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="1968e-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1968e-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="1968e-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String> -WorkspaceGUID <String>
 -WorkspaceLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1968e-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="1968e-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1968e-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="1968e-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1968e-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="1968e-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1968e-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="1968e-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1968e-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="1968e-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-EnableTrafficAnalytics] -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1968e-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="1968e-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1968e-114">說明</span><span class="sxs-lookup"><span data-stu-id="1968e-114">DESCRIPTION</span></span>
<span data-ttu-id="1968e-115">Set-AzureRmNetworkWatcherConfigFlowLog 會配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="1968e-115">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="1968e-116">要設定的屬性包括：是否針對提供的資源啟用流程記錄、已設定的儲存空間帳戶來傳送記錄，以及記錄的保留原則。</span><span class="sxs-lookup"><span data-stu-id="1968e-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="1968e-117">目前支援資料流程記錄的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="1968e-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="1968e-118">示例</span><span class="sxs-lookup"><span data-stu-id="1968e-118">EXAMPLES</span></span>

### <span data-ttu-id="1968e-119">範例1：針對指定的 NSG 設定流程記錄</span><span class="sxs-lookup"><span data-stu-id="1968e-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="1968e-120">在這個範例中，我們會設定網路安全性群組的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="1968e-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="1968e-121">在回應中，我們會看到指定的 NSG 已啟用流程記錄，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="1968e-121">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

### <span data-ttu-id="1968e-122">範例2：針對指定的 NSG 設定流程記錄和流量分析</span><span class="sxs-lookup"><span data-stu-id="1968e-122">Example 2: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzureRmOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName"
            }
          }
```

<span data-ttu-id="1968e-123">在這個範例中，我們會為網路安全群組設定流程記錄狀態和流量分析。</span><span class="sxs-lookup"><span data-stu-id="1968e-123">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="1968e-124">在回應中，我們會看到指定的 NSG 已啟用流程記錄和流量分析，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="1968e-124">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, and no retention policy set.</span></span>

## <span data-ttu-id="1968e-125">參數</span><span class="sxs-lookup"><span data-stu-id="1968e-125">PARAMETERS</span></span>

### <span data-ttu-id="1968e-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1968e-126">-AsJob</span></span>
<span data-ttu-id="1968e-127">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1968e-127">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1968e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1968e-128">-DefaultProfile</span></span>
<span data-ttu-id="1968e-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1968e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1968e-130">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="1968e-130">-EnableFlowLog</span></span>
<span data-ttu-id="1968e-131">[標記] 可啟用/停用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="1968e-131">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="1968e-132">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="1968e-132">-EnableRetention</span></span>
<span data-ttu-id="1968e-133">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="1968e-133">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="1968e-134">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="1968e-134">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="1968e-135">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="1968e-135">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases: EnableTA

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1968e-136">-位置</span><span class="sxs-lookup"><span data-stu-id="1968e-136">-Location</span></span>
<span data-ttu-id="1968e-137">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="1968e-137">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails, SetFlowlogByLocationWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1968e-138">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1968e-138">-NetworkWatcher</span></span>
<span data-ttu-id="1968e-139">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="1968e-139">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetFlowlogByResourceWithoutTA, SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1968e-140">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1968e-140">-NetworkWatcherName</span></span>
<span data-ttu-id="1968e-141">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1968e-141">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1968e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1968e-142">-ResourceGroupName</span></span>
<span data-ttu-id="1968e-143">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1968e-143">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1968e-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1968e-144">-RetentionInDays</span></span>
<span data-ttu-id="1968e-145">要保留資料流程記錄記錄的天數。</span><span class="sxs-lookup"><span data-stu-id="1968e-145">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="1968e-146">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1968e-146">-StorageAccountId</span></span>
<span data-ttu-id="1968e-147">用來儲存流程記錄的儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="1968e-147">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="1968e-148">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="1968e-148">-TargetResourceId</span></span>
<span data-ttu-id="1968e-149">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1968e-149">The target resource ID.</span></span>

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

### <span data-ttu-id="1968e-150">-工作區</span><span class="sxs-lookup"><span data-stu-id="1968e-150">-Workspace</span></span>
<span data-ttu-id="1968e-151">用來儲存流量分析資料的 WS 物件。</span><span class="sxs-lookup"><span data-stu-id="1968e-151">The WS object which is used to store the traffic analytics data.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByResourceWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByLocationWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1968e-152">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="1968e-152">-WorkspaceGUID</span></span>
<span data-ttu-id="1968e-153">用來儲存流量分析資料之 WS 的 GUID。</span><span class="sxs-lookup"><span data-stu-id="1968e-153">GUID of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1968e-154">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="1968e-154">-WorkspaceLocation</span></span>
<span data-ttu-id="1968e-155">WS 的 Azure 地區，用來儲存流量分析資料。</span><span class="sxs-lookup"><span data-stu-id="1968e-155">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1968e-156">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="1968e-156">-WorkspaceResourceId</span></span>
<span data-ttu-id="1968e-157">用來儲存流量分析資料的 WS 訂閱。</span><span class="sxs-lookup"><span data-stu-id="1968e-157">Subscription of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1968e-158">-確認</span><span class="sxs-lookup"><span data-stu-id="1968e-158">-Confirm</span></span>
<span data-ttu-id="1968e-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1968e-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1968e-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1968e-160">-WhatIf</span></span>
<span data-ttu-id="1968e-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1968e-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1968e-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1968e-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1968e-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1968e-163">CommonParameters</span></span>
<span data-ttu-id="1968e-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1968e-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1968e-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1968e-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1968e-166">輸入</span><span class="sxs-lookup"><span data-stu-id="1968e-166">INPUTS</span></span>

### <span data-ttu-id="1968e-167">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1968e-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1968e-168">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1968e-168">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="1968e-169">System.object</span><span class="sxs-lookup"><span data-stu-id="1968e-169">System.String</span></span>
<span data-ttu-id="1968e-170">參數： NetworkWatcherName (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1968e-170">Parameters: NetworkWatcherName (ByValue)</span></span>

### <span data-ttu-id="1968e-171">System.object</span><span class="sxs-lookup"><span data-stu-id="1968e-171">System.Boolean</span></span>

### <span data-ttu-id="1968e-172">System.object</span><span class="sxs-lookup"><span data-stu-id="1968e-172">System.Int32</span></span>

### <span data-ttu-id="1968e-173">IOperationalInsightWorkspace 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="1968e-173">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="1968e-174">輸出</span><span class="sxs-lookup"><span data-stu-id="1968e-174">OUTPUTS</span></span>

### <span data-ttu-id="1968e-175">PSFlowLog 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1968e-175">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="1968e-176">筆記</span><span class="sxs-lookup"><span data-stu-id="1968e-176">NOTES</span></span>
<span data-ttu-id="1968e-177">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，流程，記錄，flowlog，記錄</span><span class="sxs-lookup"><span data-stu-id="1968e-177">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="1968e-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="1968e-178">RELATED LINKS</span></span>

[<span data-ttu-id="1968e-179">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1968e-179">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1968e-180">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1968e-180">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1968e-181">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1968e-181">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1968e-182">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1968e-182">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="1968e-183">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1968e-183">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1968e-184">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1968e-184">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="1968e-185">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1968e-185">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1968e-186">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1968e-186">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1968e-187">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1968e-187">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="1968e-188">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1968e-188">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1968e-189">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1968e-189">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1968e-190">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1968e-190">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1968e-191">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1968e-191">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1968e-192">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1968e-192">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="1968e-193">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1968e-193">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="1968e-194">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1968e-194">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1968e-195">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1968e-195">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1968e-196">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1968e-196">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1968e-197">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1968e-197">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1968e-198">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1968e-198">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1968e-199">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1968e-199">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1968e-200">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1968e-200">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1968e-201">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1968e-201">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1968e-202">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1968e-202">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1968e-203">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1968e-203">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1968e-204">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1968e-204">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="1968e-205">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1968e-205">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
