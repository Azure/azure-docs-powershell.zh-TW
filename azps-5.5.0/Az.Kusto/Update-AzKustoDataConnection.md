---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: ed697798694063c516621d25fb43e153b7a23dbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135183"
---
# <span data-ttu-id="64ec5-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="64ec5-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="64ec5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="64ec5-103">更新資料連線。</span><span class="sxs-lookup"><span data-stu-id="64ec5-103">Updates a data connection.</span></span>

## <span data-ttu-id="64ec5-104">句法</span><span class="sxs-lookup"><span data-stu-id="64ec5-104">SYNTAX</span></span>

### <span data-ttu-id="64ec5-105">UpdateExpandedEventHub (預設) </span><span class="sxs-lookup"><span data-stu-id="64ec5-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="64ec5-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="64ec5-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64ec5-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="64ec5-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="64ec5-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="64ec5-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64ec5-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="64ec5-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="64ec5-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="64ec5-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64ec5-111">說明</span><span class="sxs-lookup"><span data-stu-id="64ec5-111">DESCRIPTION</span></span>
<span data-ttu-id="64ec5-112">更新資料連線。</span><span class="sxs-lookup"><span data-stu-id="64ec5-112">Updates a data connection.</span></span>

## <span data-ttu-id="64ec5-113">示例</span><span class="sxs-lookup"><span data-stu-id="64ec5-113">EXAMPLES</span></span>

### <span data-ttu-id="64ec5-114">範例1：更新現有的 EventHub 資料連線</span><span class="sxs-lookup"><span data-stu-id="64ec5-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="64ec5-115">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase" 更新名為 "myeventhubdc" 的現有 EventHub 資料連線。</span><span class="sxs-lookup"><span data-stu-id="64ec5-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="64ec5-116">範例2：更新現有的 EventGrid 資料連線</span><span class="sxs-lookup"><span data-stu-id="64ec5-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="64ec5-117">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase"，更新名為 "myeventgriddc" 的現有 EventGrid 資料連線。</span><span class="sxs-lookup"><span data-stu-id="64ec5-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="64ec5-118">範例3：更新現有的 IotHub 資料連線</span><span class="sxs-lookup"><span data-stu-id="64ec5-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="64ec5-119">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase"，更新名為 "myiothubdc" 的現有 IotHub 資料連線。</span><span class="sxs-lookup"><span data-stu-id="64ec5-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="64ec5-120">範例4：透過身分識別來更新現有的 EventHub 資料連線</span><span class="sxs-lookup"><span data-stu-id="64ec5-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="64ec5-121">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase" 更新名為 "myeventhubdc" 的現有 EventHub 資料連線。</span><span class="sxs-lookup"><span data-stu-id="64ec5-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="64ec5-122">範例5：透過身分識別更新現有的 EventGrid 資料連線</span><span class="sxs-lookup"><span data-stu-id="64ec5-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="64ec5-123">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase"，更新名為 "myeventgriddc" 的現有 EventGrid 資料連線。</span><span class="sxs-lookup"><span data-stu-id="64ec5-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="64ec5-124">範例6：透過身分識別更新現有的 IotHub 資料連線</span><span class="sxs-lookup"><span data-stu-id="64ec5-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="64ec5-125">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase"，更新名為 "myiothubdc" 的現有 IotHub 資料連線。</span><span class="sxs-lookup"><span data-stu-id="64ec5-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="64ec5-126">參數</span><span class="sxs-lookup"><span data-stu-id="64ec5-126">PARAMETERS</span></span>

### <span data-ttu-id="64ec5-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64ec5-127">-AsJob</span></span>
<span data-ttu-id="64ec5-128">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="64ec5-128">Run the command as a job</span></span>

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

### <span data-ttu-id="64ec5-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="64ec5-129">-BlobStorageEventType</span></span>
<span data-ttu-id="64ec5-130">要處理之 blob 儲存事件種類的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-130">The name of blob storage event type to process.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.BlobStorageEventType
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="64ec5-131">-ClusterName</span></span>
<span data-ttu-id="64ec5-132">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-133">壓縮</span><span class="sxs-lookup"><span data-stu-id="64ec5-133">-Compression</span></span>
<span data-ttu-id="64ec5-134">事件中心訊息壓縮類型。</span><span class="sxs-lookup"><span data-stu-id="64ec5-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: UpdateExpandedEventHub, UpdateViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="64ec5-135">-ConsumerGroup</span></span>
<span data-ttu-id="64ec5-136">[事件/iot 中心消費者] 群組。</span><span class="sxs-lookup"><span data-stu-id="64ec5-136">The event/iot hub consumer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="64ec5-137">-DatabaseName</span></span>
<span data-ttu-id="64ec5-138">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="64ec5-139">-DataFormat</span></span>
<span data-ttu-id="64ec5-140">郵件的資料格式。</span><span class="sxs-lookup"><span data-stu-id="64ec5-140">The data format of the message.</span></span>
<span data-ttu-id="64ec5-141">或者，您也可以在每封郵件中新增資料格式。</span><span class="sxs-lookup"><span data-stu-id="64ec5-141">Optionally the data format can be added to each message.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EventGridDataFormat
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ec5-142">-DefaultProfile</span></span>
<span data-ttu-id="64ec5-143">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="64ec5-144">-EventHubResourceId</span></span>
<span data-ttu-id="64ec5-145">要用來建立資料連線/事件格線之事件中心的資源識別碼已設定為傳送事件。</span><span class="sxs-lookup"><span data-stu-id="64ec5-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="64ec5-146">-EventSystemProperty</span></span>
<span data-ttu-id="64ec5-147">事件/iot 中心的系統屬性。</span><span class="sxs-lookup"><span data-stu-id="64ec5-147">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpandedEventHub, UpdateExpandedIotHub, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="64ec5-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="64ec5-149">如果設為 true，則表示攝取應該忽略每個檔案的第一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="64ec5-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64ec5-150">-InputObject</span></span>
<span data-ttu-id="64ec5-151">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="64ec5-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="64ec5-152">-IotHubResourceId</span></span>
<span data-ttu-id="64ec5-153">要用來建立資料連線之 Iot 中樞的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="64ec5-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-154">類型</span><span class="sxs-lookup"><span data-stu-id="64ec5-154">-Kind</span></span>
<span data-ttu-id="64ec5-155">資料連線的端點類型</span><span class="sxs-lookup"><span data-stu-id="64ec5-155">Kind of the endpoint for the data connection</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-156">-位置</span><span class="sxs-lookup"><span data-stu-id="64ec5-156">-Location</span></span>
<span data-ttu-id="64ec5-157">資源位置。</span><span class="sxs-lookup"><span data-stu-id="64ec5-157">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="64ec5-158">-MappingRuleName</span></span>
<span data-ttu-id="64ec5-159">要用來攝取資料的對應規則。</span><span class="sxs-lookup"><span data-stu-id="64ec5-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="64ec5-160">或者，您也可以將對應資訊新增到每一封郵件。</span><span class="sxs-lookup"><span data-stu-id="64ec5-160">Optionally the mapping information can be added to each message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-161">-名稱</span><span class="sxs-lookup"><span data-stu-id="64ec5-161">-Name</span></span>
<span data-ttu-id="64ec5-162">資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-162">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-163">-NoWait</span><span class="sxs-lookup"><span data-stu-id="64ec5-163">-NoWait</span></span>
<span data-ttu-id="64ec5-164">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="64ec5-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64ec5-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64ec5-165">-ResourceGroupName</span></span>
<span data-ttu-id="64ec5-166">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-166">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="64ec5-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="64ec5-168">共用訪問原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-168">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="64ec5-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="64ec5-170">資料所在之儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="64ec5-170">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64ec5-171">-SubscriptionId</span></span>
<span data-ttu-id="64ec5-172">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="64ec5-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="64ec5-173">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="64ec5-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="64ec5-174">-TableName</span></span>
<span data-ttu-id="64ec5-175">要 ingested 資料的資料表。</span><span class="sxs-lookup"><span data-stu-id="64ec5-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="64ec5-176">或者，您也可以在每封郵件中新增表格資訊。</span><span class="sxs-lookup"><span data-stu-id="64ec5-176">Optionally the table information can be added to each message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ec5-177">-確認</span><span class="sxs-lookup"><span data-stu-id="64ec5-177">-Confirm</span></span>
<span data-ttu-id="64ec5-178">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64ec5-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64ec5-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64ec5-179">-WhatIf</span></span>
<span data-ttu-id="64ec5-180">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64ec5-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64ec5-181">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64ec5-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64ec5-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ec5-182">CommonParameters</span></span>
<span data-ttu-id="64ec5-183">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64ec5-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ec5-184">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="64ec5-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ec5-185">輸入</span><span class="sxs-lookup"><span data-stu-id="64ec5-185">INPUTS</span></span>

### <span data-ttu-id="64ec5-186">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="64ec5-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="64ec5-187">輸出</span><span class="sxs-lookup"><span data-stu-id="64ec5-187">OUTPUTS</span></span>

### <span data-ttu-id="64ec5-188">IDataConnection （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="64ec5-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="64ec5-189">筆記</span><span class="sxs-lookup"><span data-stu-id="64ec5-189">NOTES</span></span>

<span data-ttu-id="64ec5-190">別名</span><span class="sxs-lookup"><span data-stu-id="64ec5-190">ALIASES</span></span>

<span data-ttu-id="64ec5-191">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="64ec5-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64ec5-192">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="64ec5-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64ec5-193">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="64ec5-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64ec5-194">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="64ec5-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64ec5-195">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="64ec5-196">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="64ec5-197">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="64ec5-198">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="64ec5-199">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="64ec5-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64ec5-200">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="64ec5-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="64ec5-201">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="64ec5-202">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="64ec5-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="64ec5-203">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="64ec5-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="64ec5-204">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="64ec5-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="64ec5-205">相關連結</span><span class="sxs-lookup"><span data-stu-id="64ec5-205">RELATED LINKS</span></span>

