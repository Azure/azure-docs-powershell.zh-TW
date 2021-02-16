---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 3828318840d10e5d88ebda6327ad17b9126bf03d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414232"
---
# <span data-ttu-id="7f3c2-101">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="7f3c2-101">New-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="7f3c2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7f3c2-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3c2-103">建立或更新指定網路安全性群組的流量記錄資源。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-103">Create or update a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="7f3c2-104">語法</span><span class="sxs-lookup"><span data-stu-id="7f3c2-104">SYNTAX</span></span>

### <span data-ttu-id="7f3c2-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="7f3c2-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f3c2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7f3c2-106">SetByResource</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f3c2-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="7f3c2-107">SetByResourceWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f3c2-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="7f3c2-108">SetByNameWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f3c2-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7f3c2-109">SetByLocation</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f3c2-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="7f3c2-110">SetByLocationWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f3c2-111">描述</span><span class="sxs-lookup"><span data-stu-id="7f3c2-111">DESCRIPTION</span></span>
<span data-ttu-id="7f3c2-112">New-AzNetworkWatcherFlowLog命令會建立或更新指定網路安全性群組的流量記錄資源。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-112">New-AzNetworkWatcherFlowLog command creates or updates a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="7f3c2-113">例子</span><span class="sxs-lookup"><span data-stu-id="7f3c2-113">EXAMPLES</span></span>

### <span data-ttu-id="7f3c2-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="7f3c2-114">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $true -EnableRetention $true -RetentionPolicyDays 5 -FormatVersion 2 -EnableTrafficAnalytics -TrafficAnalyticsWorkspaceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace
```

<span data-ttu-id="7f3c2-115">Name : pstest Id : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled : True RetentionPolicy : { "Days": 5, "Enabled": true } Format : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span><span class="sxs-lookup"><span data-stu-id="7f3c2-115">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span></span>

### <span data-ttu-id="7f3c2-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="7f3c2-116">Example 2</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $false -EnableTrafficAnalytics:$false
```

<span data-ttu-id="7f3c2-117">如果您想要停用已針對 TrafficAnalytics 所配置的 flowLog 資源，也有必要停用 TrafficAnalytics。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-117">If you want to disable flowLog resource for which TrafficAnalytics is configured, it is necessary to disable TrafficAnalytics as well.</span></span> <span data-ttu-id="7f3c2-118">它可以像範例 2 一樣完成。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-118">It can be done like in the example 2.</span></span>

<span data-ttu-id="7f3c2-119">名稱 ： pstest Id ： /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag ： W /"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState ： 成功的位置 ： eastus TargetResourceId ： /subscriptions/56abfbd6-ec72-4ce9 -831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId ： /subscriptions/56abfbd6-ec72-4ce9-831f-bc 2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.storage/storageAccounts/MySTorage enabled： False RetentionPolicy ： { "Days"： 0， "Enabled"： false } Format ： { "Type"： "JSON"， "Version"： 1 } FlowAnalyticsConfiguration ： { "networkWatcherFlowAnalyticsConfiguration"： { "enabled"： false， "trafficAnalyticsInterval"： 60 } }</span><span class="sxs-lookup"><span data-stu-id="7f3c2-119">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : False RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span></span>

## <span data-ttu-id="7f3c2-120">參數</span><span class="sxs-lookup"><span data-stu-id="7f3c2-120">PARAMETERS</span></span>

### <span data-ttu-id="7f3c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3c2-121">-DefaultProfile</span></span>
<span data-ttu-id="7f3c2-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f3c2-123">-已啟用</span><span class="sxs-lookup"><span data-stu-id="7f3c2-123">-Enabled</span></span>
<span data-ttu-id="7f3c2-124">標出以啟用/停用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-124">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="7f3c2-125">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="7f3c2-125">-EnableRetention</span></span>
<span data-ttu-id="7f3c2-126">標出以啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-126">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="7f3c2-127">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="7f3c2-127">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="7f3c2-128">啟用/停用 TrafficAnalytics 的標標</span><span class="sxs-lookup"><span data-stu-id="7f3c2-128">Flag to enable/disable TrafficAnalytics</span></span>

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

### <span data-ttu-id="7f3c2-129">-強制</span><span class="sxs-lookup"><span data-stu-id="7f3c2-129">-Force</span></span>
<span data-ttu-id="7f3c2-130">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="7f3c2-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7f3c2-131">-FormatType</span><span class="sxs-lookup"><span data-stu-id="7f3c2-131">-FormatType</span></span>
<span data-ttu-id="7f3c2-132">流程記錄類型的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-132">The file type of flow log.</span></span>
<span data-ttu-id="7f3c2-133">現在唯一支援的值是 'JSON'。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-133">The only supported value now is 'JSON'.</span></span>

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

### <span data-ttu-id="7f3c2-134">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="7f3c2-134">-FormatVersion</span></span>
<span data-ttu-id="7f3c2-135">版本 (流程) 的修訂。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-135">The version (revision) of the flow log.</span></span>

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

### <span data-ttu-id="7f3c2-136">-位置</span><span class="sxs-lookup"><span data-stu-id="7f3c2-136">-Location</span></span>
<span data-ttu-id="7f3c2-137">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7f3c2-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f3c2-138">-Name</span></span>
<span data-ttu-id="7f3c2-139">流程記錄名稱。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-139">The flow log name.</span></span>

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

### <span data-ttu-id="7f3c2-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f3c2-140">-NetworkWatcher</span></span>
<span data-ttu-id="7f3c2-141">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="7f3c2-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7f3c2-142">-NetworkWatcherName</span></span>
<span data-ttu-id="7f3c2-143">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="7f3c2-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f3c2-144">-ResourceGroupName</span></span>
<span data-ttu-id="7f3c2-145">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7f3c2-146">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="7f3c2-146">-RetentionPolicyDays</span></span>
<span data-ttu-id="7f3c2-147">保留流程記錄記錄的天數。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-147">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="7f3c2-148">-StorageId</span><span class="sxs-lookup"><span data-stu-id="7f3c2-148">-StorageId</span></span>
<span data-ttu-id="7f3c2-149">用來儲存流程記錄表的儲存帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-149">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="7f3c2-150">-標記</span><span class="sxs-lookup"><span data-stu-id="7f3c2-150">-Tag</span></span>
<span data-ttu-id="7f3c2-151">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-151">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7f3c2-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7f3c2-152">-TargetResourceId</span></span>
<span data-ttu-id="7f3c2-153">將適用流程記錄之網路安全性群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-153">ID of network security group to which flow log will be applied.</span></span>

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

### <span data-ttu-id="7f3c2-154">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="7f3c2-154">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="7f3c2-155">時間間隔以分鐘為單位，決定 TA 服務應該執行流程分析的頻率。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-155">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="7f3c2-156">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="7f3c2-156">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="7f3c2-157">附加工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-157">Resource Id of the attached workspace.</span></span>

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

### <span data-ttu-id="7f3c2-158">-確認</span><span class="sxs-lookup"><span data-stu-id="7f3c2-158">-Confirm</span></span>
<span data-ttu-id="7f3c2-159">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f3c2-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f3c2-160">-WhatIf</span></span>
<span data-ttu-id="7f3c2-161">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f3c2-162">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f3c2-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3c2-163">CommonParameters</span></span>
<span data-ttu-id="7f3c2-164">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7f3c2-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3c2-165">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f3c2-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3c2-166">輸入</span><span class="sxs-lookup"><span data-stu-id="7f3c2-166">INPUTS</span></span>

### <span data-ttu-id="7f3c2-167">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f3c2-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="7f3c2-168">輸出</span><span class="sxs-lookup"><span data-stu-id="7f3c2-168">OUTPUTS</span></span>

### <span data-ttu-id="7f3c2-169">Microsoft.Azure.Commands.Network.models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="7f3c2-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="7f3c2-170">筆記</span><span class="sxs-lookup"><span data-stu-id="7f3c2-170">NOTES</span></span>

## <span data-ttu-id="7f3c2-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f3c2-171">RELATED LINKS</span></span>

[<span data-ttu-id="7f3c2-172">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f3c2-172">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7f3c2-173">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f3c2-173">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7f3c2-174">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f3c2-174">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7f3c2-175">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7f3c2-175">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7f3c2-176">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7f3c2-176">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7f3c2-177">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="7f3c2-177">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7f3c2-178">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7f3c2-178">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7f3c2-179">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f3c2-179">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f3c2-180">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7f3c2-180">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7f3c2-181">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f3c2-181">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f3c2-182">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f3c2-182">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f3c2-183">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f3c2-183">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f3c2-184">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f3c2-184">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7f3c2-185">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7f3c2-185">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7f3c2-186">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7f3c2-186">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7f3c2-187">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7f3c2-187">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7f3c2-188">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7f3c2-188">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7f3c2-189">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7f3c2-189">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7f3c2-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7f3c2-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7f3c2-191">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7f3c2-191">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7f3c2-192">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7f3c2-192">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7f3c2-193">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7f3c2-193">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7f3c2-194">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7f3c2-194">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7f3c2-195">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7f3c2-195">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7f3c2-196">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7f3c2-196">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7f3c2-197">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7f3c2-197">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7f3c2-198">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7f3c2-198">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7f3c2-199">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="7f3c2-199">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="7f3c2-200">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="7f3c2-200">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="7f3c2-201">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="7f3c2-201">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
