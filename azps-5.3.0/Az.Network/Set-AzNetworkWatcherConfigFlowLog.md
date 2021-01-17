---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 6d4dca8cdaa9e80fd1417fd65a9200eb5e3ecf7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450119"
---
# <span data-ttu-id="70a75-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="70a75-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="70a75-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70a75-102">SYNOPSIS</span></span>
<span data-ttu-id="70a75-103">配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="70a75-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="70a75-104">句法</span><span class="sxs-lookup"><span data-stu-id="70a75-104">SYNTAX</span></span>

### <span data-ttu-id="70a75-105">SetFlowlogByResourceWithoutTA (預設) </span><span class="sxs-lookup"><span data-stu-id="70a75-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70a75-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="70a75-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70a75-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="70a75-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70a75-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="70a75-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70a75-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="70a75-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70a75-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="70a75-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70a75-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="70a75-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70a75-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="70a75-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70a75-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="70a75-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70a75-114">說明</span><span class="sxs-lookup"><span data-stu-id="70a75-114">DESCRIPTION</span></span>
<span data-ttu-id="70a75-115">Set-AzNetworkWatcherConfigFlowLog 會配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="70a75-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="70a75-116">要設定的屬性包括：是否針對提供的資源啟用流程記錄、已設定的儲存空間帳戶來傳送記錄、流程記錄格式，以及記錄的保留原則。</span><span class="sxs-lookup"><span data-stu-id="70a75-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="70a75-117">目前支援資料流程記錄的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="70a75-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="70a75-118">示例</span><span class="sxs-lookup"><span data-stu-id="70a75-118">EXAMPLES</span></span>

### <span data-ttu-id="70a75-119">範例1：針對指定的 NSG 設定流程記錄</span><span class="sxs-lookup"><span data-stu-id="70a75-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
```

<span data-ttu-id="70a75-120">在這個範例中，我們會設定網路安全性群組的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="70a75-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="70a75-121">在回應中，我們會看到指定的 NSG 已啟用流程記錄、預設格式，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="70a75-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="70a75-122">範例2：針對指定的 NSG 設定流程記錄，並將 [流程] 記錄的版本設定為2。</span><span class="sxs-lookup"><span data-stu-id="70a75-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -FormatVersion 2

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 2
                   }
```

<span data-ttu-id="70a75-123">在這個範例中，我們會使用指定的版本2記錄，在網路安全性群組 (NSG) 上設定流程記錄。</span><span class="sxs-lookup"><span data-stu-id="70a75-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="70a75-124">在回應中，我們會看到指定的 NSG 已啟用流程記錄、設定格式，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="70a75-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="70a75-125">如果區域不支援您指定的版本，網路觀察程式將會在區域中寫入預設支援的版本。</span><span class="sxs-lookup"><span data-stu-id="70a75-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="70a75-126">範例3：針對指定的 NSG 設定流程記錄和流量分析</span><span class="sxs-lookup"><span data-stu-id="70a75-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="70a75-127">在這個範例中，我們會為網路安全群組設定流程記錄狀態和流量分析。</span><span class="sxs-lookup"><span data-stu-id="70a75-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="70a75-128">在回應中，我們會看到指定的 NSG 已啟用流程記錄和流量分析、預設格式以及沒有設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="70a75-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="70a75-129">範例4：針對特定的 NSG 停用流量分析，並設定流量分析</span><span class="sxs-lookup"><span data-stu-id="70a75-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg
PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics:$false -Workspace $workspace

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": false,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
          "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="70a75-130">在這個範例中，我們會停用 [網路安全性群組] 的流量分析，此群組已設定了較舊的流量記錄和流量分析。</span><span class="sxs-lookup"><span data-stu-id="70a75-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="70a75-131">在回應中，我們會看到指定的 NSG 已啟用流程記錄，但流量分析卻停用了。</span><span class="sxs-lookup"><span data-stu-id="70a75-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="70a75-132">參數</span><span class="sxs-lookup"><span data-stu-id="70a75-132">PARAMETERS</span></span>

### <span data-ttu-id="70a75-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70a75-133">-AsJob</span></span>
<span data-ttu-id="70a75-134">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="70a75-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70a75-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a75-135">-DefaultProfile</span></span>
<span data-ttu-id="70a75-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70a75-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a75-137">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="70a75-137">-EnableFlowLog</span></span>
<span data-ttu-id="70a75-138">[標記] 可啟用/停用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="70a75-138">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="70a75-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="70a75-139">-EnableRetention</span></span>
<span data-ttu-id="70a75-140">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="70a75-140">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="70a75-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="70a75-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="70a75-142">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="70a75-142">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="70a75-143">-FormatType</span><span class="sxs-lookup"><span data-stu-id="70a75-143">-FormatType</span></span>
<span data-ttu-id="70a75-144">資料流程記錄格式的類型。</span><span class="sxs-lookup"><span data-stu-id="70a75-144">Type of flow log format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a75-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="70a75-145">-FormatVersion</span></span>
<span data-ttu-id="70a75-146">資料流程記錄格式的版本。</span><span class="sxs-lookup"><span data-stu-id="70a75-146">Version of flow log format.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a75-147">-位置</span><span class="sxs-lookup"><span data-stu-id="70a75-147">-Location</span></span>
<span data-ttu-id="70a75-148">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="70a75-148">Location of the network watcher.</span></span>

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

### <span data-ttu-id="70a75-149">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70a75-149">-NetworkWatcher</span></span>
<span data-ttu-id="70a75-150">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="70a75-150">The network watcher resource.</span></span>

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

### <span data-ttu-id="70a75-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="70a75-151">-NetworkWatcherName</span></span>
<span data-ttu-id="70a75-152">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="70a75-152">The name of network watcher.</span></span>

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

### <span data-ttu-id="70a75-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70a75-153">-ResourceGroupName</span></span>
<span data-ttu-id="70a75-154">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="70a75-154">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="70a75-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="70a75-155">-RetentionInDays</span></span>
<span data-ttu-id="70a75-156">要保留資料流程記錄記錄的天數。</span><span class="sxs-lookup"><span data-stu-id="70a75-156">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="70a75-157">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="70a75-157">-StorageAccountId</span></span>
<span data-ttu-id="70a75-158">用來儲存流程記錄的儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="70a75-158">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="70a75-159">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="70a75-159">-TargetResourceId</span></span>
<span data-ttu-id="70a75-160">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="70a75-160">The target resource ID.</span></span>

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

### <span data-ttu-id="70a75-161">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="70a75-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="70a75-162">取得或設定間隔 (（分鐘）) 這會決定 TA 服務執行流程分析的頻率。</span><span class="sxs-lookup"><span data-stu-id="70a75-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span> <span data-ttu-id="70a75-163">支援的值為10和60分鐘。</span><span class="sxs-lookup"><span data-stu-id="70a75-163">Supported values are 10 and 60 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a75-164">-工作區</span><span class="sxs-lookup"><span data-stu-id="70a75-164">-Workspace</span></span>
<span data-ttu-id="70a75-165">用來儲存流量分析資料的 WS 物件。</span><span class="sxs-lookup"><span data-stu-id="70a75-165">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="70a75-166">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="70a75-166">-WorkspaceGUID</span></span>
<span data-ttu-id="70a75-167">用來儲存流量分析資料之 WS 的 GUID。</span><span class="sxs-lookup"><span data-stu-id="70a75-167">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="70a75-168">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="70a75-168">-WorkspaceLocation</span></span>
<span data-ttu-id="70a75-169">WS 的 Azure 地區，用來儲存流量分析資料。</span><span class="sxs-lookup"><span data-stu-id="70a75-169">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="70a75-170">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="70a75-170">-WorkspaceResourceId</span></span>
<span data-ttu-id="70a75-171">用來儲存流量分析資料的 WS 訂閱。</span><span class="sxs-lookup"><span data-stu-id="70a75-171">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="70a75-172">-確認</span><span class="sxs-lookup"><span data-stu-id="70a75-172">-Confirm</span></span>
<span data-ttu-id="70a75-173">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="70a75-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70a75-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70a75-174">-WhatIf</span></span>
<span data-ttu-id="70a75-175">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="70a75-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70a75-176">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70a75-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70a75-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a75-177">CommonParameters</span></span>
<span data-ttu-id="70a75-178">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70a75-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a75-179">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="70a75-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a75-180">輸入</span><span class="sxs-lookup"><span data-stu-id="70a75-180">INPUTS</span></span>

### <span data-ttu-id="70a75-181">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="70a75-181">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="70a75-182">System.object</span><span class="sxs-lookup"><span data-stu-id="70a75-182">System.String</span></span>

### <span data-ttu-id="70a75-183">System.object</span><span class="sxs-lookup"><span data-stu-id="70a75-183">System.Boolean</span></span>

### <span data-ttu-id="70a75-184">System.object</span><span class="sxs-lookup"><span data-stu-id="70a75-184">System.Int32</span></span>

### <span data-ttu-id="70a75-185">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="70a75-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="70a75-186">IOperationalInsightWorkspace 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="70a75-186">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="70a75-187">輸出</span><span class="sxs-lookup"><span data-stu-id="70a75-187">OUTPUTS</span></span>

### <span data-ttu-id="70a75-188">PSFlowLog 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="70a75-188">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="70a75-189">筆記</span><span class="sxs-lookup"><span data-stu-id="70a75-189">NOTES</span></span>
<span data-ttu-id="70a75-190">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，流程，記錄，flowlog，記錄</span><span class="sxs-lookup"><span data-stu-id="70a75-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="70a75-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="70a75-191">RELATED LINKS</span></span>

[<span data-ttu-id="70a75-192">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70a75-192">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="70a75-193">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70a75-193">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="70a75-194">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70a75-194">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="70a75-195">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="70a75-195">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="70a75-196">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="70a75-196">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="70a75-197">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="70a75-197">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="70a75-198">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="70a75-198">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="70a75-199">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70a75-199">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="70a75-200">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="70a75-200">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="70a75-201">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70a75-201">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="70a75-202">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70a75-202">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="70a75-203">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70a75-203">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="70a75-204">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="70a75-204">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="70a75-205">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="70a75-205">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="70a75-206">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="70a75-206">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="70a75-207">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70a75-207">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70a75-208">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70a75-208">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70a75-209">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70a75-209">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70a75-210">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="70a75-210">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="70a75-211">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70a75-211">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70a75-212">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70a75-212">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70a75-213">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="70a75-213">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="70a75-214">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="70a75-214">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="70a75-215">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="70a75-215">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="70a75-216">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="70a75-216">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="70a75-217">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="70a75-217">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="70a75-218">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70a75-218">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
