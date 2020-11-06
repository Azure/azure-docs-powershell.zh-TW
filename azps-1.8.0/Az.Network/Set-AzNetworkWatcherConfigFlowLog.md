---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 4a64226f5445c77c262f1c0521a58d4f3f00ac99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621430"
---
# <span data-ttu-id="a70e1-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a70e1-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="a70e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a70e1-102">SYNOPSIS</span></span>
<span data-ttu-id="a70e1-103">配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="a70e1-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="a70e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="a70e1-104">SYNTAX</span></span>

### <span data-ttu-id="a70e1-105">SetFlowlogByResourceWithoutTA (預設) </span><span class="sxs-lookup"><span data-stu-id="a70e1-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a70e1-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="a70e1-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a70e1-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="a70e1-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a70e1-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="a70e1-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a70e1-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="a70e1-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a70e1-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="a70e1-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a70e1-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="a70e1-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a70e1-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="a70e1-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a70e1-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="a70e1-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a70e1-114">說明</span><span class="sxs-lookup"><span data-stu-id="a70e1-114">DESCRIPTION</span></span>
<span data-ttu-id="a70e1-115">Set-AzNetworkWatcherConfigFlowLog 會配置目標資源的流程記錄。</span><span class="sxs-lookup"><span data-stu-id="a70e1-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="a70e1-116">要設定的屬性包括：是否針對提供的資源啟用流程記錄、已設定的儲存空間帳戶來傳送記錄、流程記錄格式，以及記錄的保留原則。</span><span class="sxs-lookup"><span data-stu-id="a70e1-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="a70e1-117">目前支援資料流程記錄的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a70e1-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="a70e1-118">示例</span><span class="sxs-lookup"><span data-stu-id="a70e1-118">EXAMPLES</span></span>

### <span data-ttu-id="a70e1-119">範例1：針對指定的 NSG 設定流程記錄</span><span class="sxs-lookup"><span data-stu-id="a70e1-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="a70e1-120">在這個範例中，我們會設定網路安全性群組的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="a70e1-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="a70e1-121">在回應中，我們會看到指定的 NSG 已啟用流程記錄、預設格式，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="a70e1-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="a70e1-122">範例2：針對指定的 NSG 設定流程記錄，並將 [流程] 記錄的版本設定為2。</span><span class="sxs-lookup"><span data-stu-id="a70e1-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
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

<span data-ttu-id="a70e1-123">在這個範例中，我們會使用指定的版本2記錄，在網路安全性群組 (NSG) 上設定流程記錄。</span><span class="sxs-lookup"><span data-stu-id="a70e1-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="a70e1-124">在回應中，我們會看到指定的 NSG 已啟用流程記錄、設定格式，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="a70e1-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="a70e1-125">如果區域不支援您以的版本，網路觀察程式將會在區域中寫入預設支援的版本。</span><span class="sxs-lookup"><span data-stu-id="a70e1-125">If the region does not support version you specificed, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="a70e1-126">範例3：針對指定的 NSG 設定流程記錄和流量分析</span><span class="sxs-lookup"><span data-stu-id="a70e1-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
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

<span data-ttu-id="a70e1-127">在這個範例中，我們會為網路安全群組設定流程記錄狀態和流量分析。</span><span class="sxs-lookup"><span data-stu-id="a70e1-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="a70e1-128">在回應中，我們會看到指定的 NSG 已啟用流程記錄和流量分析、預設格式以及沒有設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="a70e1-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

## <span data-ttu-id="a70e1-129">參數</span><span class="sxs-lookup"><span data-stu-id="a70e1-129">PARAMETERS</span></span>

### <span data-ttu-id="a70e1-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a70e1-130">-AsJob</span></span>
<span data-ttu-id="a70e1-131">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a70e1-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a70e1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70e1-132">-DefaultProfile</span></span>
<span data-ttu-id="a70e1-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a70e1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a70e1-134">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="a70e1-134">-EnableFlowLog</span></span>
<span data-ttu-id="a70e1-135">[標記] 可啟用/停用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="a70e1-135">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="a70e1-136">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="a70e1-136">-EnableRetention</span></span>
<span data-ttu-id="a70e1-137">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="a70e1-137">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="a70e1-138">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="a70e1-138">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="a70e1-139">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="a70e1-139">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="a70e1-140">-FormatType</span><span class="sxs-lookup"><span data-stu-id="a70e1-140">-FormatType</span></span>
<span data-ttu-id="a70e1-141">資料流程記錄格式的類型。</span><span class="sxs-lookup"><span data-stu-id="a70e1-141">Type of flow log format.</span></span>

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

### <span data-ttu-id="a70e1-142">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="a70e1-142">-FormatVersion</span></span>
<span data-ttu-id="a70e1-143">資料流程記錄格式的版本。</span><span class="sxs-lookup"><span data-stu-id="a70e1-143">Version of flow log format.</span></span>

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

### <span data-ttu-id="a70e1-144">-位置</span><span class="sxs-lookup"><span data-stu-id="a70e1-144">-Location</span></span>
<span data-ttu-id="a70e1-145">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="a70e1-145">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a70e1-146">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a70e1-146">-NetworkWatcher</span></span>
<span data-ttu-id="a70e1-147">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="a70e1-147">The network watcher resource.</span></span>

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

### <span data-ttu-id="a70e1-148">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a70e1-148">-NetworkWatcherName</span></span>
<span data-ttu-id="a70e1-149">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a70e1-149">The name of network watcher.</span></span>

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

### <span data-ttu-id="a70e1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70e1-150">-ResourceGroupName</span></span>
<span data-ttu-id="a70e1-151">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a70e1-151">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a70e1-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a70e1-152">-RetentionInDays</span></span>
<span data-ttu-id="a70e1-153">要保留資料流程記錄記錄的天數。</span><span class="sxs-lookup"><span data-stu-id="a70e1-153">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="a70e1-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a70e1-154">-StorageAccountId</span></span>
<span data-ttu-id="a70e1-155">用來儲存流程記錄的儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="a70e1-155">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="a70e1-156">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a70e1-156">-TargetResourceId</span></span>
<span data-ttu-id="a70e1-157">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a70e1-157">The target resource ID.</span></span>

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

### <span data-ttu-id="a70e1-158">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="a70e1-158">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="a70e1-159">取得或設定間隔 (（分鐘）) 這會決定 TA 服務執行流程分析的頻率。</span><span class="sxs-lookup"><span data-stu-id="a70e1-159">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="a70e1-160">-工作區</span><span class="sxs-lookup"><span data-stu-id="a70e1-160">-Workspace</span></span>
<span data-ttu-id="a70e1-161">用來儲存流量分析資料的 WS 物件。</span><span class="sxs-lookup"><span data-stu-id="a70e1-161">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="a70e1-162">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="a70e1-162">-WorkspaceGUID</span></span>
<span data-ttu-id="a70e1-163">用來儲存流量分析資料之 WS 的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a70e1-163">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="a70e1-164">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="a70e1-164">-WorkspaceLocation</span></span>
<span data-ttu-id="a70e1-165">WS 的 Azure 地區，用來儲存流量分析資料。</span><span class="sxs-lookup"><span data-stu-id="a70e1-165">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="a70e1-166">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="a70e1-166">-WorkspaceResourceId</span></span>
<span data-ttu-id="a70e1-167">用來儲存流量分析資料的 WS 訂閱。</span><span class="sxs-lookup"><span data-stu-id="a70e1-167">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="a70e1-168">-確認</span><span class="sxs-lookup"><span data-stu-id="a70e1-168">-Confirm</span></span>
<span data-ttu-id="a70e1-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a70e1-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a70e1-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a70e1-170">-WhatIf</span></span>
<span data-ttu-id="a70e1-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a70e1-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a70e1-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a70e1-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a70e1-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70e1-173">CommonParameters</span></span>
<span data-ttu-id="a70e1-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a70e1-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70e1-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a70e1-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70e1-176">輸入</span><span class="sxs-lookup"><span data-stu-id="a70e1-176">INPUTS</span></span>

### <span data-ttu-id="a70e1-177">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a70e1-177">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a70e1-178">System.object</span><span class="sxs-lookup"><span data-stu-id="a70e1-178">System.String</span></span>

### <span data-ttu-id="a70e1-179">System.object</span><span class="sxs-lookup"><span data-stu-id="a70e1-179">System.Boolean</span></span>

### <span data-ttu-id="a70e1-180">System.object</span><span class="sxs-lookup"><span data-stu-id="a70e1-180">System.Int32</span></span>

### <span data-ttu-id="a70e1-181">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a70e1-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a70e1-182">IOperationalInsightWorkspace 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="a70e1-182">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="a70e1-183">輸出</span><span class="sxs-lookup"><span data-stu-id="a70e1-183">OUTPUTS</span></span>

### <span data-ttu-id="a70e1-184">PSFlowLog 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a70e1-184">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="a70e1-185">筆記</span><span class="sxs-lookup"><span data-stu-id="a70e1-185">NOTES</span></span>
<span data-ttu-id="a70e1-186">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，流程，記錄，flowlog，記錄</span><span class="sxs-lookup"><span data-stu-id="a70e1-186">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="a70e1-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="a70e1-187">RELATED LINKS</span></span>

[<span data-ttu-id="a70e1-188">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a70e1-188">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a70e1-189">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a70e1-189">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a70e1-190">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a70e1-190">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a70e1-191">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a70e1-191">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a70e1-192">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a70e1-192">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a70e1-193">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a70e1-193">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a70e1-194">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a70e1-194">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a70e1-195">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a70e1-195">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a70e1-196">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a70e1-196">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a70e1-197">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a70e1-197">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a70e1-198">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a70e1-198">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a70e1-199">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a70e1-199">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a70e1-200">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a70e1-200">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a70e1-201">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a70e1-201">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a70e1-202">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a70e1-202">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a70e1-203">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a70e1-203">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a70e1-204">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a70e1-204">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a70e1-205">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a70e1-205">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a70e1-206">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a70e1-206">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a70e1-207">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a70e1-207">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a70e1-208">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a70e1-208">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a70e1-209">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a70e1-209">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a70e1-210">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a70e1-210">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a70e1-211">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a70e1-211">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a70e1-212">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a70e1-212">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a70e1-213">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a70e1-213">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="a70e1-214">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a70e1-214">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
