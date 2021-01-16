---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 04a9b4c0ca8b613ce4d4c590572d80a729a65147
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279223"
---
# <span data-ttu-id="2e16e-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="2e16e-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="2e16e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e16e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e16e-103">更新資料流程記錄記錄資源。</span><span class="sxs-lookup"><span data-stu-id="2e16e-103">Updates flow log resource.</span></span>

## <span data-ttu-id="2e16e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e16e-104">SYNTAX</span></span>

### <span data-ttu-id="2e16e-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="2e16e-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e16e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2e16e-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e16e-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="2e16e-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e16e-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="2e16e-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e16e-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2e16e-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e16e-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="2e16e-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e16e-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e16e-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e16e-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="2e16e-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e16e-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e16e-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e16e-114">說明</span><span class="sxs-lookup"><span data-stu-id="2e16e-114">DESCRIPTION</span></span>
<span data-ttu-id="2e16e-115">更新資料流程記錄記錄資源。</span><span class="sxs-lookup"><span data-stu-id="2e16e-115">Updates flow log resource.</span></span>

## <span data-ttu-id="2e16e-116">示例</span><span class="sxs-lookup"><span data-stu-id="2e16e-116">EXAMPLES</span></span>

### <span data-ttu-id="2e16e-117">範例1</span><span class="sxs-lookup"><span data-stu-id="2e16e-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="2e16e-118">Name （名稱）： pstest Id：/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag： W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState： Succeeded 位置： eastus TargetResourceId：/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs//networkSecurityGroups/MyNSG StorageId：/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/MyStorage 已啟用： True RetentionPolicy： {"Days"：0，"Enabled"： false} 格式： {"類型"： "JSON"，"Version"： 2} FlowAnalyticsConfiguration： {}</span><span class="sxs-lookup"><span data-stu-id="2e16e-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="2e16e-119">參數</span><span class="sxs-lookup"><span data-stu-id="2e16e-119">PARAMETERS</span></span>

### <span data-ttu-id="2e16e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e16e-120">-DefaultProfile</span></span>
<span data-ttu-id="2e16e-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e16e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e16e-122">-啟用</span><span class="sxs-lookup"><span data-stu-id="2e16e-122">-Enabled</span></span>
<span data-ttu-id="2e16e-123">[標記] 可啟用/停用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="2e16e-123">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="2e16e-124">-EnableRetention</span></span>
<span data-ttu-id="2e16e-125">[標記] 可啟用/停用保留。</span><span class="sxs-lookup"><span data-stu-id="2e16e-125">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="2e16e-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="2e16e-127">啟用/停用 TrafficAnalytics 標誌</span><span class="sxs-lookup"><span data-stu-id="2e16e-127">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-128">-Force</span><span class="sxs-lookup"><span data-stu-id="2e16e-128">-Force</span></span>
<span data-ttu-id="2e16e-129">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="2e16e-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2e16e-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="2e16e-130">-FormatType</span></span>
<span data-ttu-id="2e16e-131">資料流程記錄的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="2e16e-131">The file type of flow log.</span></span>
<span data-ttu-id="2e16e-132">目前唯一支援的值為 "JSON"。</span><span class="sxs-lookup"><span data-stu-id="2e16e-132">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="2e16e-133">-FormatVersion</span></span>
<span data-ttu-id="2e16e-134">資料流程記錄的版本 (修訂) 。</span><span class="sxs-lookup"><span data-stu-id="2e16e-134">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e16e-135">-InputObject</span></span>
<span data-ttu-id="2e16e-136">Flow lof 物件。</span><span class="sxs-lookup"><span data-stu-id="2e16e-136">Flow lof object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-137">-位置</span><span class="sxs-lookup"><span data-stu-id="2e16e-137">-Location</span></span>
<span data-ttu-id="2e16e-138">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="2e16e-138">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2e16e-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e16e-139">-Name</span></span>
<span data-ttu-id="2e16e-140">流程記錄名稱。</span><span class="sxs-lookup"><span data-stu-id="2e16e-140">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e16e-141">-NetworkWatcher</span></span>
<span data-ttu-id="2e16e-142">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="2e16e-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="2e16e-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2e16e-143">-NetworkWatcherName</span></span>
<span data-ttu-id="2e16e-144">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e16e-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="2e16e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e16e-145">-ResourceGroupName</span></span>
<span data-ttu-id="2e16e-146">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e16e-146">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2e16e-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e16e-147">-ResourceId</span></span>
<span data-ttu-id="2e16e-148">FlowLog 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e16e-148">FlowLog resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="2e16e-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="2e16e-150">要保留資料流程記錄記錄的天數。</span><span class="sxs-lookup"><span data-stu-id="2e16e-150">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-151">-StorageId</span><span class="sxs-lookup"><span data-stu-id="2e16e-151">-StorageId</span></span>
<span data-ttu-id="2e16e-152">用來儲存流程記錄的儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="2e16e-152">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e16e-153">-Tag</span></span>
<span data-ttu-id="2e16e-154">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="2e16e-154">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2e16e-155">-TargetResourceId</span></span>
<span data-ttu-id="2e16e-156">要套用資料流程記錄的網路安全性群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e16e-156">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="2e16e-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="2e16e-158">間隔時間（以分鐘為單位），決定 TA 服務執行流程分析的頻率。</span><span class="sxs-lookup"><span data-stu-id="2e16e-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="2e16e-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="2e16e-160">已附加工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e16e-160">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16e-161">-確認</span><span class="sxs-lookup"><span data-stu-id="2e16e-161">-Confirm</span></span>
<span data-ttu-id="2e16e-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2e16e-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e16e-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e16e-163">-WhatIf</span></span>
<span data-ttu-id="2e16e-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e16e-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e16e-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e16e-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e16e-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e16e-166">CommonParameters</span></span>
<span data-ttu-id="2e16e-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e16e-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e16e-168">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2e16e-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e16e-169">輸入</span><span class="sxs-lookup"><span data-stu-id="2e16e-169">INPUTS</span></span>

### <span data-ttu-id="2e16e-170">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2e16e-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2e16e-171">System.object</span><span class="sxs-lookup"><span data-stu-id="2e16e-171">System.String</span></span>

### <span data-ttu-id="2e16e-172">PSFlowLogResource 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2e16e-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="2e16e-173">輸出</span><span class="sxs-lookup"><span data-stu-id="2e16e-173">OUTPUTS</span></span>

### <span data-ttu-id="2e16e-174">PSFlowLogResource 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2e16e-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="2e16e-175">筆記</span><span class="sxs-lookup"><span data-stu-id="2e16e-175">NOTES</span></span>

## <span data-ttu-id="2e16e-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e16e-176">RELATED LINKS</span></span>

[<span data-ttu-id="2e16e-177">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e16e-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2e16e-178">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e16e-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2e16e-179">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e16e-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2e16e-180">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2e16e-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2e16e-181">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2e16e-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2e16e-182">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2e16e-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2e16e-183">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2e16e-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2e16e-184">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e16e-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e16e-185">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2e16e-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2e16e-186">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e16e-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e16e-187">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e16e-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e16e-188">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e16e-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e16e-189">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e16e-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2e16e-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2e16e-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2e16e-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2e16e-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2e16e-192">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e16e-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e16e-193">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e16e-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e16e-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e16e-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e16e-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2e16e-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2e16e-196">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e16e-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e16e-197">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e16e-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e16e-198">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2e16e-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2e16e-199">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2e16e-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2e16e-200">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2e16e-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2e16e-201">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2e16e-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2e16e-202">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2e16e-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2e16e-203">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e16e-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="2e16e-204">新-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="2e16e-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="2e16e-205">AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="2e16e-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="2e16e-206">移除-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="2e16e-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
