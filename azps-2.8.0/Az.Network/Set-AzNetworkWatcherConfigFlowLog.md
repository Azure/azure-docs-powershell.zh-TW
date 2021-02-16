---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 55e98b23f4da1adf641bcf2a3ce7ced95cf5befd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402672"
---
# <span data-ttu-id="a5c6b-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a5c6b-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="a5c6b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a5c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c6b-103">設定目標資源的流量記錄。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="a5c6b-104">語法</span><span class="sxs-lookup"><span data-stu-id="a5c6b-104">SYNTAX</span></span>

### <span data-ttu-id="a5c6b-105">SetFlowlogByResourceWithoutTA (預設) </span><span class="sxs-lookup"><span data-stu-id="a5c6b-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c6b-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="a5c6b-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c6b-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="a5c6b-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c6b-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="a5c6b-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c6b-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="a5c6b-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c6b-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="a5c6b-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c6b-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="a5c6b-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c6b-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="a5c6b-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c6b-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="a5c6b-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5c6b-114">描述</span><span class="sxs-lookup"><span data-stu-id="a5c6b-114">DESCRIPTION</span></span>
<span data-ttu-id="a5c6b-115">此Set-AzNetworkWatcherConfigFlowLog設定目標資源的流量記錄。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="a5c6b-116">要設定的屬性包括：是否針對提供的資源啟用流程記錄、設定儲存帳戶以傳送記錄、流程記錄格式，以及記錄保留原則。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="a5c6b-117">目前網路安全性群組支援流程記錄。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="a5c6b-118">例子</span><span class="sxs-lookup"><span data-stu-id="a5c6b-118">EXAMPLES</span></span>

### <span data-ttu-id="a5c6b-119">範例 1：為指定的 NSG 設定流程記錄</span><span class="sxs-lookup"><span data-stu-id="a5c6b-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="a5c6b-120">在此範例中，我們設定網路安全性群組的流量記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="a5c6b-121">在回應中，我們會看到指定的 NSG 已啟用流程記錄、預設格式，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="a5c6b-122">範例 2：為指定的 NSG 設定流程記錄，並設定流程記錄的版本為 2。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
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

<span data-ttu-id="a5c6b-123">在此範例中，我們在已指定版本 2 記錄 (NSG) 組設定流程記錄。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="a5c6b-124">在回應中，我們會看到指定的 NSG 已啟用流程記錄、已設定格式，而且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="a5c6b-125">如果地區不支援您指定的版本，Network Watcher 會撰寫該區域中預設支援的版本。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="a5c6b-126">範例 3：為指定的 NSG 設定流程記錄與流量分析</span><span class="sxs-lookup"><span data-stu-id="a5c6b-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
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

<span data-ttu-id="a5c6b-127">在此範例中，我們針對網路安全性群組設定流程記錄狀態和流量分析。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="a5c6b-128">在回應中，我們會看到指定的 NSG 已啟用流程記錄與流量分析、預設格式，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

## <span data-ttu-id="a5c6b-129">參數</span><span class="sxs-lookup"><span data-stu-id="a5c6b-129">PARAMETERS</span></span>

### <span data-ttu-id="a5c6b-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5c6b-130">-AsJob</span></span>
<span data-ttu-id="a5c6b-131">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a5c6b-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5c6b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c6b-132">-DefaultProfile</span></span>
<span data-ttu-id="a5c6b-133">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5c6b-134">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="a5c6b-134">-EnableFlowLog</span></span>
<span data-ttu-id="a5c6b-135">標出以啟用/停用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-135">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="a5c6b-136">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="a5c6b-136">-EnableRetention</span></span>
<span data-ttu-id="a5c6b-137">標出以啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-137">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="a5c6b-138">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="a5c6b-138">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="a5c6b-139">標出以啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-139">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="a5c6b-140">-FormatType</span><span class="sxs-lookup"><span data-stu-id="a5c6b-140">-FormatType</span></span>
<span data-ttu-id="a5c6b-141">流程記錄格式類型。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-141">Type of flow log format.</span></span>

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

### <span data-ttu-id="a5c6b-142">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="a5c6b-142">-FormatVersion</span></span>
<span data-ttu-id="a5c6b-143">流程記錄格式的版本。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-143">Version of flow log format.</span></span>

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

### <span data-ttu-id="a5c6b-144">-位置</span><span class="sxs-lookup"><span data-stu-id="a5c6b-144">-Location</span></span>
<span data-ttu-id="a5c6b-145">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-145">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a5c6b-146">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a5c6b-146">-NetworkWatcher</span></span>
<span data-ttu-id="a5c6b-147">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-147">The network watcher resource.</span></span>

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

### <span data-ttu-id="a5c6b-148">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a5c6b-148">-NetworkWatcherName</span></span>
<span data-ttu-id="a5c6b-149">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-149">The name of network watcher.</span></span>

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

### <span data-ttu-id="a5c6b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c6b-150">-ResourceGroupName</span></span>
<span data-ttu-id="a5c6b-151">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-151">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a5c6b-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a5c6b-152">-RetentionInDays</span></span>
<span data-ttu-id="a5c6b-153">保留流程記錄記錄的天數。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-153">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="a5c6b-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a5c6b-154">-StorageAccountId</span></span>
<span data-ttu-id="a5c6b-155">儲存流程記錄所使用之儲存帳戶的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-155">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="a5c6b-156">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a5c6b-156">-TargetResourceId</span></span>
<span data-ttu-id="a5c6b-157">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-157">The target resource ID.</span></span>

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

### <span data-ttu-id="a5c6b-158">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="a5c6b-158">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="a5c6b-159">以分鐘為單位 (或設定時間間隔) 決定 TA 服務應該執行流程分析的頻率。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-159">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="a5c6b-160">-工作區</span><span class="sxs-lookup"><span data-stu-id="a5c6b-160">-Workspace</span></span>
<span data-ttu-id="a5c6b-161">用來儲存流量分析資料的 WS 物件。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-161">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="a5c6b-162">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="a5c6b-162">-WorkspaceGUID</span></span>
<span data-ttu-id="a5c6b-163">用來儲存流量分析資料的 WS GUID。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-163">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="a5c6b-164">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="a5c6b-164">-WorkspaceLocation</span></span>
<span data-ttu-id="a5c6b-165">用來儲存流量分析資料的 WS Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-165">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="a5c6b-166">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="a5c6b-166">-WorkspaceResourceId</span></span>
<span data-ttu-id="a5c6b-167">用來儲存流量分析資料的 WS 訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-167">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="a5c6b-168">-確認</span><span class="sxs-lookup"><span data-stu-id="a5c6b-168">-Confirm</span></span>
<span data-ttu-id="a5c6b-169">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c6b-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c6b-170">-WhatIf</span></span>
<span data-ttu-id="a5c6b-171">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5c6b-172">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c6b-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c6b-173">CommonParameters</span></span>
<span data-ttu-id="a5c6b-174">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c6b-175">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a5c6b-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c6b-176">輸入</span><span class="sxs-lookup"><span data-stu-id="a5c6b-176">INPUTS</span></span>

### <span data-ttu-id="a5c6b-177">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a5c6b-177">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a5c6b-178">System.String</span><span class="sxs-lookup"><span data-stu-id="a5c6b-178">System.String</span></span>

### <span data-ttu-id="a5c6b-179">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5c6b-179">System.Boolean</span></span>

### <span data-ttu-id="a5c6b-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a5c6b-180">System.Int32</span></span>

### <span data-ttu-id="a5c6b-181">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a5c6b-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a5c6b-182">Microsoft.Azure.management.Internal.Network.Common.IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5c6b-182">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="a5c6b-183">輸出</span><span class="sxs-lookup"><span data-stu-id="a5c6b-183">OUTPUTS</span></span>

### <span data-ttu-id="a5c6b-184">Microsoft.Azure.Commands.network.models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="a5c6b-184">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="a5c6b-185">筆記</span><span class="sxs-lookup"><span data-stu-id="a5c6b-185">NOTES</span></span>
<span data-ttu-id="a5c6b-186">關鍵字：azure、azurerm、arm、resource、management、manager、network、network、watcher、flow、logs、flowlog、logging</span><span class="sxs-lookup"><span data-stu-id="a5c6b-186">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="a5c6b-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5c6b-187">RELATED LINKS</span></span>

[<span data-ttu-id="a5c6b-188">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a5c6b-188">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a5c6b-189">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a5c6b-189">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a5c6b-190">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a5c6b-190">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a5c6b-191">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a5c6b-191">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a5c6b-192">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a5c6b-192">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a5c6b-193">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="a5c6b-193">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a5c6b-194">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a5c6b-194">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a5c6b-195">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a5c6b-195">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a5c6b-196">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a5c6b-196">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a5c6b-197">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a5c6b-197">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a5c6b-198">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a5c6b-198">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a5c6b-199">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a5c6b-199">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a5c6b-200">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5c6b-200">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a5c6b-201">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a5c6b-201">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a5c6b-202">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a5c6b-202">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a5c6b-203">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5c6b-203">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a5c6b-204">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5c6b-204">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a5c6b-205">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5c6b-205">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a5c6b-206">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a5c6b-206">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a5c6b-207">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5c6b-207">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a5c6b-208">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5c6b-208">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a5c6b-209">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a5c6b-209">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a5c6b-210">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a5c6b-210">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a5c6b-211">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a5c6b-211">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a5c6b-212">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a5c6b-212">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a5c6b-213">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a5c6b-213">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a5c6b-214">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5c6b-214">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
