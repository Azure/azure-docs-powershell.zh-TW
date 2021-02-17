---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: afa73cab1f0e66ecc9388b9fb2c536ca50bc609d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401601"
---
# <span data-ttu-id="0c9f0-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0c9f0-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="0c9f0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0c9f0-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9f0-103">設定目標資源的流量記錄。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="0c9f0-104">語法</span><span class="sxs-lookup"><span data-stu-id="0c9f0-104">SYNTAX</span></span>

### <span data-ttu-id="0c9f0-105">SetFlowlogByResourceWithoutTA (預設) </span><span class="sxs-lookup"><span data-stu-id="0c9f0-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c9f0-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="0c9f0-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c9f0-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="0c9f0-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c9f0-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="0c9f0-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c9f0-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="0c9f0-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c9f0-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="0c9f0-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c9f0-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="0c9f0-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c9f0-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="0c9f0-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c9f0-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="0c9f0-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c9f0-114">描述</span><span class="sxs-lookup"><span data-stu-id="0c9f0-114">DESCRIPTION</span></span>
<span data-ttu-id="0c9f0-115">此Set-AzNetworkWatcherConfigFlowLog設定目標資源的流量記錄。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="0c9f0-116">要設定的屬性包括：是否針對提供的資源啟用流程記錄、設定儲存帳戶以傳送記錄、流程記錄格式，以及記錄保留原則。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="0c9f0-117">目前網路安全性群組支援流程記錄。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="0c9f0-118">例子</span><span class="sxs-lookup"><span data-stu-id="0c9f0-118">EXAMPLES</span></span>

### <span data-ttu-id="0c9f0-119">範例 1：為指定的 NSG 設定流程記錄</span><span class="sxs-lookup"><span data-stu-id="0c9f0-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="0c9f0-120">在此範例中，我們設定網路安全性群組的流量記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="0c9f0-121">在回應中，我們會看到指定的 NSG 已啟用流程記錄、預設格式，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="0c9f0-122">範例 2：為指定的 NSG 設定流程記錄，並設定流程記錄的版本為 2。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
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

<span data-ttu-id="0c9f0-123">在此範例中，我們在已指定版本 2 記錄 (NSG) 組設定流程記錄。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="0c9f0-124">在回應中，我們會看到指定的 NSG 已啟用流程記錄、已設定格式，而且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="0c9f0-125">如果地區不支援您指定的版本，Network Watcher 會撰寫該區域中預設支援的版本。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="0c9f0-126">範例 3：為指定的 NSG 設定流程記錄與流量分析</span><span class="sxs-lookup"><span data-stu-id="0c9f0-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
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

<span data-ttu-id="0c9f0-127">在此範例中，我們針對網路安全性群組設定流程記錄狀態和流量分析。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="0c9f0-128">在回應中，我們會看到指定的 NSG 已啟用流程記錄與流量分析、預設格式，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="0c9f0-129">範例 4：停用指定 NSG 的流量分析，並已進行流程記錄與流量分析</span><span class="sxs-lookup"><span data-stu-id="0c9f0-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
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

<span data-ttu-id="0c9f0-130">在此範例中，我們針對先前已進行流程記錄與流量分析的網路安全性群組停用流量分析。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="0c9f0-131">在回應中，我們會看到指定的 NSG 已啟用流程記錄，但流量分析已停用。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="0c9f0-132">參數</span><span class="sxs-lookup"><span data-stu-id="0c9f0-132">PARAMETERS</span></span>

### <span data-ttu-id="0c9f0-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c9f0-133">-AsJob</span></span>
<span data-ttu-id="0c9f0-134">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0c9f0-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c9f0-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c9f0-135">-DefaultProfile</span></span>
<span data-ttu-id="0c9f0-136">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c9f0-137">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="0c9f0-137">-EnableFlowLog</span></span>
<span data-ttu-id="0c9f0-138">標出以啟用/停用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-138">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="0c9f0-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="0c9f0-139">-EnableRetention</span></span>
<span data-ttu-id="0c9f0-140">標出以啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-140">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="0c9f0-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="0c9f0-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="0c9f0-142">標出以啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-142">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="0c9f0-143">-FormatType</span><span class="sxs-lookup"><span data-stu-id="0c9f0-143">-FormatType</span></span>
<span data-ttu-id="0c9f0-144">流程記錄格式類型。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-144">Type of flow log format.</span></span>

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

### <span data-ttu-id="0c9f0-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="0c9f0-145">-FormatVersion</span></span>
<span data-ttu-id="0c9f0-146">流程記錄格式的版本。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-146">Version of flow log format.</span></span>

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

### <span data-ttu-id="0c9f0-147">-位置</span><span class="sxs-lookup"><span data-stu-id="0c9f0-147">-Location</span></span>
<span data-ttu-id="0c9f0-148">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-148">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0c9f0-149">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0c9f0-149">-NetworkWatcher</span></span>
<span data-ttu-id="0c9f0-150">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-150">The network watcher resource.</span></span>

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

### <span data-ttu-id="0c9f0-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0c9f0-151">-NetworkWatcherName</span></span>
<span data-ttu-id="0c9f0-152">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-152">The name of network watcher.</span></span>

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

### <span data-ttu-id="0c9f0-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c9f0-153">-ResourceGroupName</span></span>
<span data-ttu-id="0c9f0-154">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-154">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0c9f0-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0c9f0-155">-RetentionInDays</span></span>
<span data-ttu-id="0c9f0-156">保留流程記錄記錄的天數。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-156">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="0c9f0-157">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0c9f0-157">-StorageAccountId</span></span>
<span data-ttu-id="0c9f0-158">用來儲存流程記錄表的儲存帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-158">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="0c9f0-159">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0c9f0-159">-TargetResourceId</span></span>
<span data-ttu-id="0c9f0-160">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-160">The target resource ID.</span></span>

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

### <span data-ttu-id="0c9f0-161">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="0c9f0-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="0c9f0-162">以分鐘為單位 (或設定時間間隔) 決定 TA 服務應該執行流程分析的頻率。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="0c9f0-163">-工作區</span><span class="sxs-lookup"><span data-stu-id="0c9f0-163">-Workspace</span></span>
<span data-ttu-id="0c9f0-164">用來儲存流量分析資料的 WS 物件。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-164">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="0c9f0-165">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="0c9f0-165">-WorkspaceGUID</span></span>
<span data-ttu-id="0c9f0-166">用來儲存流量分析資料的 WS GUID。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-166">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="0c9f0-167">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="0c9f0-167">-WorkspaceLocation</span></span>
<span data-ttu-id="0c9f0-168">用來儲存流量分析資料的 WS Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-168">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="0c9f0-169">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="0c9f0-169">-WorkspaceResourceId</span></span>
<span data-ttu-id="0c9f0-170">用來儲存流量分析資料的 WS 訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-170">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="0c9f0-171">-確認</span><span class="sxs-lookup"><span data-stu-id="0c9f0-171">-Confirm</span></span>
<span data-ttu-id="0c9f0-172">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c9f0-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c9f0-173">-WhatIf</span></span>
<span data-ttu-id="0c9f0-174">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c9f0-175">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c9f0-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9f0-176">CommonParameters</span></span>
<span data-ttu-id="0c9f0-177">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9f0-178">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0c9f0-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9f0-179">輸入</span><span class="sxs-lookup"><span data-stu-id="0c9f0-179">INPUTS</span></span>

### <span data-ttu-id="0c9f0-180">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0c9f0-180">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0c9f0-181">System.String</span><span class="sxs-lookup"><span data-stu-id="0c9f0-181">System.String</span></span>

### <span data-ttu-id="0c9f0-182">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c9f0-182">System.Boolean</span></span>

### <span data-ttu-id="0c9f0-183">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0c9f0-183">System.Int32</span></span>

### <span data-ttu-id="0c9f0-184">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0c9f0-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0c9f0-185">Microsoft.Azure.management.Internal.Network.Common.IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="0c9f0-185">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="0c9f0-186">輸出</span><span class="sxs-lookup"><span data-stu-id="0c9f0-186">OUTPUTS</span></span>

### <span data-ttu-id="0c9f0-187">Microsoft.Azure.Commands.network.models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="0c9f0-187">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="0c9f0-188">筆記</span><span class="sxs-lookup"><span data-stu-id="0c9f0-188">NOTES</span></span>
<span data-ttu-id="0c9f0-189">關鍵字：azure、azurerm、arm、resource、management、manager、network、network、watcher、flow、logs、flowlog、logging</span><span class="sxs-lookup"><span data-stu-id="0c9f0-189">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="0c9f0-190">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c9f0-190">RELATED LINKS</span></span>

[<span data-ttu-id="0c9f0-191">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0c9f0-191">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0c9f0-192">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0c9f0-192">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0c9f0-193">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0c9f0-193">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0c9f0-194">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0c9f0-194">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0c9f0-195">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0c9f0-195">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0c9f0-196">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="0c9f0-196">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0c9f0-197">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0c9f0-197">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0c9f0-198">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0c9f0-198">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0c9f0-199">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0c9f0-199">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0c9f0-200">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0c9f0-200">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0c9f0-201">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0c9f0-201">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0c9f0-202">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0c9f0-202">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0c9f0-203">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c9f0-203">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0c9f0-204">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0c9f0-204">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0c9f0-205">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0c9f0-205">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0c9f0-206">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c9f0-206">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0c9f0-207">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c9f0-207">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0c9f0-208">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c9f0-208">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0c9f0-209">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0c9f0-209">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0c9f0-210">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c9f0-210">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0c9f0-211">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c9f0-211">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0c9f0-212">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0c9f0-212">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0c9f0-213">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0c9f0-213">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0c9f0-214">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0c9f0-214">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0c9f0-215">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0c9f0-215">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0c9f0-216">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0c9f0-216">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0c9f0-217">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0c9f0-217">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
