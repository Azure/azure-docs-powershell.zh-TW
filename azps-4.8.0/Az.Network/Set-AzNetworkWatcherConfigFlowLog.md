---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 2b6ad73e3a054ee01c2200ea47098fe3c3f206fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136217"
---
# <span data-ttu-id="bd1c0-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="bd1c0-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="bd1c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="bd1c0-103">配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="bd1c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd1c0-104">SYNTAX</span></span>

### <span data-ttu-id="bd1c0-105">SetFlowlogByResourceWithoutTA (預設) </span><span class="sxs-lookup"><span data-stu-id="bd1c0-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd1c0-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="bd1c0-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd1c0-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="bd1c0-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd1c0-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="bd1c0-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd1c0-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="bd1c0-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd1c0-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="bd1c0-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd1c0-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="bd1c0-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd1c0-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="bd1c0-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd1c0-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="bd1c0-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd1c0-114">說明</span><span class="sxs-lookup"><span data-stu-id="bd1c0-114">DESCRIPTION</span></span>
<span data-ttu-id="bd1c0-115">Set-AzNetworkWatcherConfigFlowLog 會配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="bd1c0-116">要設定的屬性包括：是否針對提供的資源啟用流程記錄、已設定的儲存空間帳戶來傳送記錄、流程記錄格式，以及記錄的保留原則。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="bd1c0-117">目前支援資料流程記錄的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="bd1c0-118">示例</span><span class="sxs-lookup"><span data-stu-id="bd1c0-118">EXAMPLES</span></span>

### <span data-ttu-id="bd1c0-119">範例1：針對指定的 NSG 設定流程記錄</span><span class="sxs-lookup"><span data-stu-id="bd1c0-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="bd1c0-120">在這個範例中，我們會設定網路安全性群組的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="bd1c0-121">在回應中，我們會看到指定的 NSG 已啟用流程記錄、預設格式，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="bd1c0-122">範例2：針對指定的 NSG 設定流程記錄，並將 [流程] 記錄的版本設定為2。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
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

<span data-ttu-id="bd1c0-123">在這個範例中，我們會使用指定的版本2記錄，在網路安全性群組 (NSG) 上設定流程記錄。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="bd1c0-124">在回應中，我們會看到指定的 NSG 已啟用流程記錄、設定格式，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="bd1c0-125">如果區域不支援您指定的版本，網路觀察程式將會在區域中寫入預設支援的版本。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="bd1c0-126">範例3：針對指定的 NSG 設定流程記錄和流量分析</span><span class="sxs-lookup"><span data-stu-id="bd1c0-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
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

<span data-ttu-id="bd1c0-127">在這個範例中，我們會為網路安全群組設定流程記錄狀態和流量分析。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="bd1c0-128">在回應中，我們會看到指定的 NSG 已啟用流程記錄和流量分析、預設格式以及沒有設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="bd1c0-129">範例4：針對特定的 NSG 停用流量分析，並設定流量分析</span><span class="sxs-lookup"><span data-stu-id="bd1c0-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
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

<span data-ttu-id="bd1c0-130">在這個範例中，我們會停用 [網路安全性群組] 的流量分析，此群組已設定了較舊的流量記錄和流量分析。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="bd1c0-131">在回應中，我們會看到指定的 NSG 已啟用流程記錄，但流量分析卻停用了。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="bd1c0-132">參數</span><span class="sxs-lookup"><span data-stu-id="bd1c0-132">PARAMETERS</span></span>

### <span data-ttu-id="bd1c0-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd1c0-133">-AsJob</span></span>
<span data-ttu-id="bd1c0-134">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bd1c0-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd1c0-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd1c0-135">-DefaultProfile</span></span>
<span data-ttu-id="bd1c0-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd1c0-137">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="bd1c0-137">-EnableFlowLog</span></span>
<span data-ttu-id="bd1c0-138">[標記] 可啟用/停用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-138">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="bd1c0-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="bd1c0-139">-EnableRetention</span></span>
<span data-ttu-id="bd1c0-140">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-140">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="bd1c0-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="bd1c0-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="bd1c0-142">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-142">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="bd1c0-143">-FormatType</span><span class="sxs-lookup"><span data-stu-id="bd1c0-143">-FormatType</span></span>
<span data-ttu-id="bd1c0-144">資料流程記錄格式的類型。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-144">Type of flow log format.</span></span>

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

### <span data-ttu-id="bd1c0-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="bd1c0-145">-FormatVersion</span></span>
<span data-ttu-id="bd1c0-146">資料流程記錄格式的版本。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-146">Version of flow log format.</span></span>

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

### <span data-ttu-id="bd1c0-147">-位置</span><span class="sxs-lookup"><span data-stu-id="bd1c0-147">-Location</span></span>
<span data-ttu-id="bd1c0-148">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-148">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bd1c0-149">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bd1c0-149">-NetworkWatcher</span></span>
<span data-ttu-id="bd1c0-150">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-150">The network watcher resource.</span></span>

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

### <span data-ttu-id="bd1c0-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bd1c0-151">-NetworkWatcherName</span></span>
<span data-ttu-id="bd1c0-152">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-152">The name of network watcher.</span></span>

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

### <span data-ttu-id="bd1c0-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd1c0-153">-ResourceGroupName</span></span>
<span data-ttu-id="bd1c0-154">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-154">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bd1c0-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="bd1c0-155">-RetentionInDays</span></span>
<span data-ttu-id="bd1c0-156">要保留資料流程記錄記錄的天數。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-156">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="bd1c0-157">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bd1c0-157">-StorageAccountId</span></span>
<span data-ttu-id="bd1c0-158">用來儲存流程記錄的儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-158">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="bd1c0-159">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="bd1c0-159">-TargetResourceId</span></span>
<span data-ttu-id="bd1c0-160">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-160">The target resource ID.</span></span>

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

### <span data-ttu-id="bd1c0-161">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="bd1c0-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="bd1c0-162">取得或設定間隔 (（分鐘）) 這會決定 TA 服務執行流程分析的頻率。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="bd1c0-163">-工作區</span><span class="sxs-lookup"><span data-stu-id="bd1c0-163">-Workspace</span></span>
<span data-ttu-id="bd1c0-164">用來儲存流量分析資料的 WS 物件。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-164">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="bd1c0-165">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="bd1c0-165">-WorkspaceGUID</span></span>
<span data-ttu-id="bd1c0-166">用來儲存流量分析資料之 WS 的 GUID。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-166">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="bd1c0-167">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="bd1c0-167">-WorkspaceLocation</span></span>
<span data-ttu-id="bd1c0-168">WS 的 Azure 地區，用來儲存流量分析資料。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-168">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="bd1c0-169">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="bd1c0-169">-WorkspaceResourceId</span></span>
<span data-ttu-id="bd1c0-170">用來儲存流量分析資料的 WS 訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-170">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="bd1c0-171">-確認</span><span class="sxs-lookup"><span data-stu-id="bd1c0-171">-Confirm</span></span>
<span data-ttu-id="bd1c0-172">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd1c0-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd1c0-173">-WhatIf</span></span>
<span data-ttu-id="bd1c0-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd1c0-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd1c0-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd1c0-176">CommonParameters</span></span>
<span data-ttu-id="bd1c0-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd1c0-178">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd1c0-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd1c0-179">輸入</span><span class="sxs-lookup"><span data-stu-id="bd1c0-179">INPUTS</span></span>

### <span data-ttu-id="bd1c0-180">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bd1c0-180">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="bd1c0-181">System.object</span><span class="sxs-lookup"><span data-stu-id="bd1c0-181">System.String</span></span>

### <span data-ttu-id="bd1c0-182">System.object</span><span class="sxs-lookup"><span data-stu-id="bd1c0-182">System.Boolean</span></span>

### <span data-ttu-id="bd1c0-183">System.object</span><span class="sxs-lookup"><span data-stu-id="bd1c0-183">System.Int32</span></span>

### <span data-ttu-id="bd1c0-184">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bd1c0-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bd1c0-185">IOperationalInsightWorkspace 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="bd1c0-185">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="bd1c0-186">輸出</span><span class="sxs-lookup"><span data-stu-id="bd1c0-186">OUTPUTS</span></span>

### <span data-ttu-id="bd1c0-187">PSFlowLog 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bd1c0-187">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="bd1c0-188">筆記</span><span class="sxs-lookup"><span data-stu-id="bd1c0-188">NOTES</span></span>
<span data-ttu-id="bd1c0-189">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，流程，記錄，flowlog，記錄</span><span class="sxs-lookup"><span data-stu-id="bd1c0-189">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="bd1c0-190">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd1c0-190">RELATED LINKS</span></span>

[<span data-ttu-id="bd1c0-191">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bd1c0-191">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="bd1c0-192">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bd1c0-192">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="bd1c0-193">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bd1c0-193">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="bd1c0-194">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bd1c0-194">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="bd1c0-195">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bd1c0-195">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bd1c0-196">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bd1c0-196">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="bd1c0-197">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bd1c0-197">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="bd1c0-198">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bd1c0-198">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bd1c0-199">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bd1c0-199">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="bd1c0-200">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bd1c0-200">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bd1c0-201">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bd1c0-201">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bd1c0-202">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bd1c0-202">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bd1c0-203">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd1c0-203">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="bd1c0-204">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bd1c0-204">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="bd1c0-205">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="bd1c0-205">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="bd1c0-206">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bd1c0-206">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bd1c0-207">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bd1c0-207">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bd1c0-208">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bd1c0-208">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bd1c0-209">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="bd1c0-209">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="bd1c0-210">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bd1c0-210">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bd1c0-211">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bd1c0-211">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bd1c0-212">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="bd1c0-212">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="bd1c0-213">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="bd1c0-213">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="bd1c0-214">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="bd1c0-214">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="bd1c0-215">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="bd1c0-215">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="bd1c0-216">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="bd1c0-216">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="bd1c0-217">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bd1c0-217">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
