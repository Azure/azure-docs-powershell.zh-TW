---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 33441112856ebdbcb12da237542ed3ce62a3944c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957721"
---
# <span data-ttu-id="b5e56-101">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="b5e56-101">New-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="b5e56-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5e56-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e56-103">建立或更新指定網路安全性群組的流量記錄資源。</span><span class="sxs-lookup"><span data-stu-id="b5e56-103">Create or update a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="b5e56-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5e56-104">SYNTAX</span></span>

### <span data-ttu-id="b5e56-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="b5e56-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5e56-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b5e56-106">SetByResource</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5e56-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="b5e56-107">SetByResourceWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5e56-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="b5e56-108">SetByNameWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5e56-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b5e56-109">SetByLocation</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5e56-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="b5e56-110">SetByLocationWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5e56-111">說明</span><span class="sxs-lookup"><span data-stu-id="b5e56-111">DESCRIPTION</span></span>
<span data-ttu-id="b5e56-112">New-AzNetworkWatcherFlowLog 命令會建立或更新指定網路安全性群組的流量記錄資源。</span><span class="sxs-lookup"><span data-stu-id="b5e56-112">New-AzNetworkWatcherFlowLog command creates or updates a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="b5e56-113">示例</span><span class="sxs-lookup"><span data-stu-id="b5e56-113">EXAMPLES</span></span>

### <span data-ttu-id="b5e56-114">範例1</span><span class="sxs-lookup"><span data-stu-id="b5e56-114">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $true -EnableRetention $true -RetentionPolicyDays 5 -FormatVersion 2 -EnableTrafficAnalytics -TrafficAnalyticsWorkspaceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace
```

<span data-ttu-id="b5e56-115">Name （名稱）： pstest Id：/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/networkWatchers/NetworkWatcher_eastus//FlowLogs/pstest Etag： W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState：成功的位置： eastus TargetResourceId：/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/microsoft. Network/networkSecurityGroups/MyNSG StorageId：/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/： [Enabled "（天數）：5，" 已啟用]： True} 格式： {"Type"： "JSON"，"版本"： 2} FlowAnalyticsConfiguration： {"networkWatcherFlowAnalyticsConfiguration"： {"Enabled"： True，"workspaceId"： "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb"，"workspaceRegion"： "eastus"，"workspaceResourceId"： "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr"，"oups"： "FlowLogsV2Demo OperationalInsights/MyWorkspace"，"trafficAnalyticsInterval"： 60}}</span><span class="sxs-lookup"><span data-stu-id="b5e56-115">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span></span>

### <span data-ttu-id="b5e56-116">範例2</span><span class="sxs-lookup"><span data-stu-id="b5e56-116">Example 2</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $false -EnableTrafficAnalytics:$false
```

<span data-ttu-id="b5e56-117">如果您想要停用 TrafficAnalytics 設定的 flowLog 資源，也必須停用 TrafficAnalytics。</span><span class="sxs-lookup"><span data-stu-id="b5e56-117">If you want to disable flowLog resource for which TrafficAnalytics is configured, it is necessary to disable TrafficAnalytics as well.</span></span> <span data-ttu-id="b5e56-118">它可以在範例2中完成。</span><span class="sxs-lookup"><span data-stu-id="b5e56-118">It can be done like in the example 2.</span></span>

<span data-ttu-id="b5e56-119">Name （名稱）： pstest Id：/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag： W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState：成功位置： eastus TargetResourceId：/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft。 Network/networkSecurityGroups/MyNSG StorageId：/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. 儲存/storageAccounts/MySTorage 已啟用： False RetentionPolicy： {[Days]：0，"Enabled"： false} 格式： {"Type"： "JSON"，"版本"： 1} FlowAnalyticsConfiguration： {"networkWatcherFlowAnalyticsConfiguration"： {"Enabled"： False，"trafficAnalyticsInterval"： 60}}</span><span class="sxs-lookup"><span data-stu-id="b5e56-119">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : False RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span></span>

## <span data-ttu-id="b5e56-120">參數</span><span class="sxs-lookup"><span data-stu-id="b5e56-120">PARAMETERS</span></span>

### <span data-ttu-id="b5e56-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e56-121">-DefaultProfile</span></span>
<span data-ttu-id="b5e56-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5e56-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-123">-啟用</span><span class="sxs-lookup"><span data-stu-id="b5e56-123">-Enabled</span></span>
<span data-ttu-id="b5e56-124">[標記] 可啟用/停用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="b5e56-124">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-125">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="b5e56-125">-EnableRetention</span></span>
<span data-ttu-id="b5e56-126">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="b5e56-126">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-127">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="b5e56-127">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="b5e56-128">啟用/停用 TrafficAnalytics 標誌</span><span class="sxs-lookup"><span data-stu-id="b5e56-128">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-129">-Force</span><span class="sxs-lookup"><span data-stu-id="b5e56-129">-Force</span></span>
<span data-ttu-id="b5e56-130">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="b5e56-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b5e56-131">-FormatType</span><span class="sxs-lookup"><span data-stu-id="b5e56-131">-FormatType</span></span>
<span data-ttu-id="b5e56-132">資料流程記錄的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="b5e56-132">The file type of flow log.</span></span>
<span data-ttu-id="b5e56-133">目前唯一支援的值為 "JSON"。</span><span class="sxs-lookup"><span data-stu-id="b5e56-133">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-134">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="b5e56-134">-FormatVersion</span></span>
<span data-ttu-id="b5e56-135">資料流程記錄的版本 (修訂) 。</span><span class="sxs-lookup"><span data-stu-id="b5e56-135">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-136">-位置</span><span class="sxs-lookup"><span data-stu-id="b5e56-136">-Location</span></span>
<span data-ttu-id="b5e56-137">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="b5e56-137">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5e56-138">-Name</span></span>
<span data-ttu-id="b5e56-139">流程記錄名稱。</span><span class="sxs-lookup"><span data-stu-id="b5e56-139">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b5e56-140">-NetworkWatcher</span></span>
<span data-ttu-id="b5e56-141">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="b5e56-141">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b5e56-142">-NetworkWatcherName</span></span>
<span data-ttu-id="b5e56-143">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5e56-143">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5e56-144">-ResourceGroupName</span></span>
<span data-ttu-id="b5e56-145">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5e56-145">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-146">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="b5e56-146">-RetentionPolicyDays</span></span>
<span data-ttu-id="b5e56-147">要保留資料流程記錄記錄的天數。</span><span class="sxs-lookup"><span data-stu-id="b5e56-147">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-148">-StorageId</span><span class="sxs-lookup"><span data-stu-id="b5e56-148">-StorageId</span></span>
<span data-ttu-id="b5e56-149">用來儲存流程記錄的儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="b5e56-149">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="b5e56-150">-Tag</span></span>
<span data-ttu-id="b5e56-151">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="b5e56-151">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b5e56-152">-TargetResourceId</span></span>
<span data-ttu-id="b5e56-153">要套用資料流程記錄的網路安全性群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5e56-153">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-154">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="b5e56-154">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="b5e56-155">間隔時間（以分鐘為單位），決定 TA 服務執行流程分析的頻率。</span><span class="sxs-lookup"><span data-stu-id="b5e56-155">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-156">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="b5e56-156">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="b5e56-157">已附加工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5e56-157">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e56-158">-確認</span><span class="sxs-lookup"><span data-stu-id="b5e56-158">-Confirm</span></span>
<span data-ttu-id="b5e56-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b5e56-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5e56-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5e56-160">-WhatIf</span></span>
<span data-ttu-id="b5e56-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5e56-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5e56-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5e56-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5e56-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e56-163">CommonParameters</span></span>
<span data-ttu-id="b5e56-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5e56-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e56-165">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b5e56-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e56-166">輸入</span><span class="sxs-lookup"><span data-stu-id="b5e56-166">INPUTS</span></span>

### <span data-ttu-id="b5e56-167">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b5e56-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="b5e56-168">輸出</span><span class="sxs-lookup"><span data-stu-id="b5e56-168">OUTPUTS</span></span>

### <span data-ttu-id="b5e56-169">PSFlowLogResource 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b5e56-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="b5e56-170">筆記</span><span class="sxs-lookup"><span data-stu-id="b5e56-170">NOTES</span></span>

## <span data-ttu-id="b5e56-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5e56-171">RELATED LINKS</span></span>

[<span data-ttu-id="b5e56-172">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b5e56-172">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b5e56-173">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b5e56-173">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b5e56-174">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b5e56-174">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b5e56-175">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b5e56-175">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b5e56-176">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b5e56-176">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b5e56-177">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b5e56-177">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b5e56-178">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b5e56-178">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b5e56-179">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5e56-179">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b5e56-180">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b5e56-180">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b5e56-181">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5e56-181">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b5e56-182">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5e56-182">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b5e56-183">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5e56-183">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b5e56-184">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5e56-184">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b5e56-185">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b5e56-185">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b5e56-186">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b5e56-186">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b5e56-187">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b5e56-187">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b5e56-188">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b5e56-188">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b5e56-189">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b5e56-189">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b5e56-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b5e56-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b5e56-191">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b5e56-191">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b5e56-192">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b5e56-192">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b5e56-193">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b5e56-193">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b5e56-194">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b5e56-194">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b5e56-195">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b5e56-195">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b5e56-196">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b5e56-196">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b5e56-197">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b5e56-197">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="b5e56-198">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b5e56-198">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="b5e56-199">AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="b5e56-199">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="b5e56-200">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="b5e56-200">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog)

[<span data-ttu-id="b5e56-201">移除-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="b5e56-201">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog)