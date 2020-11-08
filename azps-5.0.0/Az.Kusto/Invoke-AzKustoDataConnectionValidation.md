---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: 9eb3ff31873b23fc97f53fffecdbbb38367ac2b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140451"
---
# <span data-ttu-id="2c480-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="2c480-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="2c480-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c480-102">SYNOPSIS</span></span>
<span data-ttu-id="2c480-103">檢查資料連線參數是否有效。</span><span class="sxs-lookup"><span data-stu-id="2c480-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="2c480-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c480-104">SYNTAX</span></span>

### <span data-ttu-id="2c480-105">DataExpandedEventHub (預設) </span><span class="sxs-lookup"><span data-stu-id="2c480-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2c480-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="2c480-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2c480-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="2c480-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2c480-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="2c480-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2c480-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="2c480-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2c480-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="2c480-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2c480-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="2c480-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2c480-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="2c480-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2c480-113">說明</span><span class="sxs-lookup"><span data-stu-id="2c480-113">DESCRIPTION</span></span>
<span data-ttu-id="2c480-114">檢查資料連線參數是否有效。</span><span class="sxs-lookup"><span data-stu-id="2c480-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="2c480-115">示例</span><span class="sxs-lookup"><span data-stu-id="2c480-115">EXAMPLES</span></span>

### <span data-ttu-id="2c480-116">範例1：驗證 EventHub 資料連線參數</span><span class="sxs-lookup"><span data-stu-id="2c480-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="2c480-117">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase" 驗證名為 "myeventhubdc" 的 EventHub 資料連線。</span><span class="sxs-lookup"><span data-stu-id="2c480-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2c480-118">範例2：驗證 EventGrid 資料連線參數</span><span class="sxs-lookup"><span data-stu-id="2c480-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="2c480-119">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase" 驗證名為 "myeventgriddc" 的 EventGrid 資料連線。</span><span class="sxs-lookup"><span data-stu-id="2c480-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2c480-120">範例3：驗證 IotHub 資料連線參數</span><span class="sxs-lookup"><span data-stu-id="2c480-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="2c480-121">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase" 驗證名為 "myiothubdc" 的 IotHub 資料連線。</span><span class="sxs-lookup"><span data-stu-id="2c480-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2c480-122">範例4：透過識別驗證 EventHub 資料連線參數</span><span class="sxs-lookup"><span data-stu-id="2c480-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="2c480-123">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase" 驗證名為 "myeventhubdc" 的 EventHub 資料連線。</span><span class="sxs-lookup"><span data-stu-id="2c480-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2c480-124">範例5：透過身分識別驗證 EventGrid 資料連線參數</span><span class="sxs-lookup"><span data-stu-id="2c480-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="2c480-125">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase" 驗證名為 "myeventgriddc" 的 EventGrid 資料連線。</span><span class="sxs-lookup"><span data-stu-id="2c480-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2c480-126">範例6：透過身分識別驗證 IotHub 資料連線參數</span><span class="sxs-lookup"><span data-stu-id="2c480-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="2c480-127">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase" 驗證名為 "myiothubdc" 的 IotHub 資料連線。</span><span class="sxs-lookup"><span data-stu-id="2c480-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="2c480-128">參數</span><span class="sxs-lookup"><span data-stu-id="2c480-128">PARAMETERS</span></span>

### <span data-ttu-id="2c480-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="2c480-129">-BlobStorageEventType</span></span>
<span data-ttu-id="2c480-130">要處理之 blob 儲存事件種類的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c480-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="2c480-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2c480-131">-ClusterName</span></span>
<span data-ttu-id="2c480-132">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c480-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c480-133">壓縮</span><span class="sxs-lookup"><span data-stu-id="2c480-133">-Compression</span></span>
<span data-ttu-id="2c480-134">事件中心訊息壓縮類型。</span><span class="sxs-lookup"><span data-stu-id="2c480-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: DataExpandedEventHub, DataViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c480-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2c480-135">-ConsumerGroup</span></span>
<span data-ttu-id="2c480-136">[事件/iot 中心消費者] 群組。</span><span class="sxs-lookup"><span data-stu-id="2c480-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="2c480-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c480-137">-DatabaseName</span></span>
<span data-ttu-id="2c480-138">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c480-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c480-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="2c480-139">-DataConnectionName</span></span>
<span data-ttu-id="2c480-140">資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c480-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="2c480-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="2c480-141">-DataFormat</span></span>
<span data-ttu-id="2c480-142">郵件的資料格式。</span><span class="sxs-lookup"><span data-stu-id="2c480-142">The data format of the message.</span></span>
<span data-ttu-id="2c480-143">或者，您也可以在每封郵件中新增資料格式。</span><span class="sxs-lookup"><span data-stu-id="2c480-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="2c480-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c480-144">-DefaultProfile</span></span>
<span data-ttu-id="2c480-145">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c480-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c480-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="2c480-146">-EventHubResourceId</span></span>
<span data-ttu-id="2c480-147">要用來建立資料連線/事件格線之事件中心的資源識別碼已設定為傳送事件。</span><span class="sxs-lookup"><span data-stu-id="2c480-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c480-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="2c480-148">-EventSystemProperty</span></span>
<span data-ttu-id="2c480-149">事件/iot 中心的系統屬性。</span><span class="sxs-lookup"><span data-stu-id="2c480-149">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DataExpandedEventHub, DataExpandedIotHub, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c480-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="2c480-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="2c480-151">如果設為 true，則表示攝取應該忽略每個檔案的第一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="2c480-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="2c480-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c480-152">-InputObject</span></span>
<span data-ttu-id="2c480-153">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2c480-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c480-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="2c480-154">-IotHubResourceId</span></span>
<span data-ttu-id="2c480-155">要用來建立資料連線之 Iot 中樞的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c480-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c480-156">類型</span><span class="sxs-lookup"><span data-stu-id="2c480-156">-Kind</span></span>
<span data-ttu-id="2c480-157">資料連線的端點類型</span><span class="sxs-lookup"><span data-stu-id="2c480-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="2c480-158">-位置</span><span class="sxs-lookup"><span data-stu-id="2c480-158">-Location</span></span>
<span data-ttu-id="2c480-159">資源位置。</span><span class="sxs-lookup"><span data-stu-id="2c480-159">Resource location.</span></span>

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

### <span data-ttu-id="2c480-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="2c480-160">-MappingRuleName</span></span>
<span data-ttu-id="2c480-161">要用來攝取資料的對應規則。</span><span class="sxs-lookup"><span data-stu-id="2c480-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="2c480-162">或者，您也可以將對應資訊新增到每一封郵件。</span><span class="sxs-lookup"><span data-stu-id="2c480-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="2c480-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c480-163">-ResourceGroupName</span></span>
<span data-ttu-id="2c480-164">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c480-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c480-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="2c480-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="2c480-166">共用訪問原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c480-166">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c480-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2c480-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="2c480-168">資料所在之儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c480-168">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c480-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c480-169">-SubscriptionId</span></span>
<span data-ttu-id="2c480-170">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="2c480-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2c480-171">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="2c480-171">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c480-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="2c480-172">-TableName</span></span>
<span data-ttu-id="2c480-173">要 ingested 資料的資料表。</span><span class="sxs-lookup"><span data-stu-id="2c480-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="2c480-174">或者，您也可以在每封郵件中新增表格資訊。</span><span class="sxs-lookup"><span data-stu-id="2c480-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="2c480-175">-確認</span><span class="sxs-lookup"><span data-stu-id="2c480-175">-Confirm</span></span>
<span data-ttu-id="2c480-176">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c480-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c480-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c480-177">-WhatIf</span></span>
<span data-ttu-id="2c480-178">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c480-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c480-179">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c480-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c480-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c480-180">CommonParameters</span></span>
<span data-ttu-id="2c480-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c480-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c480-182">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2c480-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c480-183">輸入</span><span class="sxs-lookup"><span data-stu-id="2c480-183">INPUTS</span></span>

### <span data-ttu-id="2c480-184">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="2c480-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2c480-185">輸出</span><span class="sxs-lookup"><span data-stu-id="2c480-185">OUTPUTS</span></span>

### <span data-ttu-id="2c480-186">IDataConnectionValidationResult （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="2c480-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="2c480-187">筆記</span><span class="sxs-lookup"><span data-stu-id="2c480-187">NOTES</span></span>

<span data-ttu-id="2c480-188">別名</span><span class="sxs-lookup"><span data-stu-id="2c480-188">ALIASES</span></span>

<span data-ttu-id="2c480-189">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2c480-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2c480-190">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2c480-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2c480-191">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2c480-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2c480-192">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2c480-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2c480-193">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c480-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2c480-194">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c480-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2c480-195">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c480-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2c480-196">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c480-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2c480-197">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="2c480-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2c480-198">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="2c480-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2c480-199">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c480-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2c480-200">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c480-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2c480-201">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="2c480-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2c480-202">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="2c480-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2c480-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c480-203">RELATED LINKS</span></span>

