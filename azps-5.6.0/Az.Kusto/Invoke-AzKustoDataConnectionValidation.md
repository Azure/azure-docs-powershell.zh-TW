---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: c12c38227c4d0a3d0a6b58685c1b8b5233c161ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903829"
---
# <span data-ttu-id="9acbb-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="9acbb-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="9acbb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9acbb-102">SYNOPSIS</span></span>
<span data-ttu-id="9acbb-103">檢查資料連線參數是否有效。</span><span class="sxs-lookup"><span data-stu-id="9acbb-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="9acbb-104">語法</span><span class="sxs-lookup"><span data-stu-id="9acbb-104">SYNTAX</span></span>

### <span data-ttu-id="9acbb-105">DataExpandedEventHub (預設) </span><span class="sxs-lookup"><span data-stu-id="9acbb-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9acbb-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="9acbb-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9acbb-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="9acbb-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9acbb-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="9acbb-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9acbb-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="9acbb-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9acbb-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="9acbb-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9acbb-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="9acbb-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9acbb-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="9acbb-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9acbb-113">描述</span><span class="sxs-lookup"><span data-stu-id="9acbb-113">DESCRIPTION</span></span>
<span data-ttu-id="9acbb-114">檢查資料連線參數是否有效。</span><span class="sxs-lookup"><span data-stu-id="9acbb-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="9acbb-115">例子</span><span class="sxs-lookup"><span data-stu-id="9acbb-115">EXAMPLES</span></span>

### <span data-ttu-id="9acbb-116">範例 1：驗證 EventHub 資料連線參數</span><span class="sxs-lookup"><span data-stu-id="9acbb-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="9acbb-117">上述命令會驗證名為 "myeventhubdc" 的 EventHub 資料連線，以用於叢集"testnewkustocluster"中的資料庫"mykustodatabase"。</span><span class="sxs-lookup"><span data-stu-id="9acbb-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="9acbb-118">範例 2：驗證 EventGrid 資料連線參數</span><span class="sxs-lookup"><span data-stu-id="9acbb-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="9acbb-119">上述命令會驗證名為 "myeventgriddc" 的 EventGrid 資料連線，以用於叢集"testnewkustocluster"中的資料庫"mykustodatabase"。</span><span class="sxs-lookup"><span data-stu-id="9acbb-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="9acbb-120">範例 3：驗證 IotHub 資料連線參數</span><span class="sxs-lookup"><span data-stu-id="9acbb-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="9acbb-121">上述命令會驗證名為 "myiothubdc" 的 IotHub 資料連線，以用於叢集"testnewkustocluster"中的資料庫"mykustodatabase"。</span><span class="sxs-lookup"><span data-stu-id="9acbb-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="9acbb-122">範例 4：透過身分識別驗證 EventHub 資料連線參數</span><span class="sxs-lookup"><span data-stu-id="9acbb-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="9acbb-123">上述命令會驗證名為 "myeventhubdc" 的 EventHub 資料連線，以用於叢集"testnewkustocluster"中的資料庫"mykustodatabase"。</span><span class="sxs-lookup"><span data-stu-id="9acbb-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="9acbb-124">範例 5：透過身分識別驗證 EventGrid 資料連線參數</span><span class="sxs-lookup"><span data-stu-id="9acbb-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="9acbb-125">上述命令會驗證名為 "myeventgriddc" 的 EventGrid 資料連線，以用於叢集"testnewkustocluster"中的資料庫"mykustodatabase"。</span><span class="sxs-lookup"><span data-stu-id="9acbb-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="9acbb-126">範例 6：透過身分識別驗證 IotHub 資料連線參數</span><span class="sxs-lookup"><span data-stu-id="9acbb-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="9acbb-127">上述命令會驗證名為 "myiothubdc" 的 IotHub 資料連線，以用於叢集"testnewkustocluster"中的資料庫"mykustodatabase"。</span><span class="sxs-lookup"><span data-stu-id="9acbb-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="9acbb-128">參數</span><span class="sxs-lookup"><span data-stu-id="9acbb-128">PARAMETERS</span></span>

### <span data-ttu-id="9acbb-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="9acbb-129">-BlobStorageEventType</span></span>
<span data-ttu-id="9acbb-130">要處理之 Blob 儲存事件種類的名稱。</span><span class="sxs-lookup"><span data-stu-id="9acbb-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="9acbb-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9acbb-131">-ClusterName</span></span>
<span data-ttu-id="9acbb-132">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="9acbb-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9acbb-133">-壓縮</span><span class="sxs-lookup"><span data-stu-id="9acbb-133">-Compression</span></span>
<span data-ttu-id="9acbb-134">事件中樞訊息壓縮類型。</span><span class="sxs-lookup"><span data-stu-id="9acbb-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="9acbb-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="9acbb-135">-ConsumerGroup</span></span>
<span data-ttu-id="9acbb-136">事件/iot 中樞消費者群組。</span><span class="sxs-lookup"><span data-stu-id="9acbb-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="9acbb-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9acbb-137">-DatabaseName</span></span>
<span data-ttu-id="9acbb-138">Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="9acbb-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="9acbb-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="9acbb-139">-DataConnectionName</span></span>
<span data-ttu-id="9acbb-140">資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="9acbb-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="9acbb-141">-資料格式</span><span class="sxs-lookup"><span data-stu-id="9acbb-141">-DataFormat</span></span>
<span data-ttu-id="9acbb-142">郵件的資料格式。</span><span class="sxs-lookup"><span data-stu-id="9acbb-142">The data format of the message.</span></span>
<span data-ttu-id="9acbb-143">或者，資料格式也可以新增到每封郵件中。</span><span class="sxs-lookup"><span data-stu-id="9acbb-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="9acbb-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9acbb-144">-DefaultProfile</span></span>
<span data-ttu-id="9acbb-145">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9acbb-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9acbb-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="9acbb-146">-EventHubResourceId</span></span>
<span data-ttu-id="9acbb-147">事件中樞的資源識別碼，可用來建立資料連線/事件格線，其為傳送事件。</span><span class="sxs-lookup"><span data-stu-id="9acbb-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="9acbb-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="9acbb-148">-EventSystemProperty</span></span>
<span data-ttu-id="9acbb-149">事件/iot 中樞的系統屬性。</span><span class="sxs-lookup"><span data-stu-id="9acbb-149">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="9acbb-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="9acbb-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="9acbb-151">如果設為 True，表示要忽略每個檔案的第一個記錄。</span><span class="sxs-lookup"><span data-stu-id="9acbb-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="9acbb-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9acbb-152">-InputObject</span></span>
<span data-ttu-id="9acbb-153">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9acbb-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9acbb-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="9acbb-154">-IotHubResourceId</span></span>
<span data-ttu-id="9acbb-155">用來建立資料連線的 Iot 中樞資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9acbb-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="9acbb-156">-Kind</span><span class="sxs-lookup"><span data-stu-id="9acbb-156">-Kind</span></span>
<span data-ttu-id="9acbb-157">資料連線的端點類型</span><span class="sxs-lookup"><span data-stu-id="9acbb-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="9acbb-158">-位置</span><span class="sxs-lookup"><span data-stu-id="9acbb-158">-Location</span></span>
<span data-ttu-id="9acbb-159">資源位置。</span><span class="sxs-lookup"><span data-stu-id="9acbb-159">Resource location.</span></span>

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

### <span data-ttu-id="9acbb-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="9acbb-160">-MappingRuleName</span></span>
<span data-ttu-id="9acbb-161">要用於輸入資料的地圖規則。</span><span class="sxs-lookup"><span data-stu-id="9acbb-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="9acbb-162">您也可以選擇在每封郵件中新增地圖資訊。</span><span class="sxs-lookup"><span data-stu-id="9acbb-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="9acbb-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9acbb-163">-ResourceGroupName</span></span>
<span data-ttu-id="9acbb-164">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9acbb-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9acbb-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="9acbb-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="9acbb-166">共用存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="9acbb-166">The name of the share access policy.</span></span>

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

### <span data-ttu-id="9acbb-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9acbb-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="9acbb-168">資料所在之儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9acbb-168">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="9acbb-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9acbb-169">-SubscriptionId</span></span>
<span data-ttu-id="9acbb-170">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9acbb-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9acbb-171">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9acbb-171">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9acbb-172">-TableName</span><span class="sxs-lookup"><span data-stu-id="9acbb-172">-TableName</span></span>
<span data-ttu-id="9acbb-173">應輸入資料的資料表。</span><span class="sxs-lookup"><span data-stu-id="9acbb-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="9acbb-174">您也可以選擇在每封郵件中新增表格資訊。</span><span class="sxs-lookup"><span data-stu-id="9acbb-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="9acbb-175">-確認</span><span class="sxs-lookup"><span data-stu-id="9acbb-175">-Confirm</span></span>
<span data-ttu-id="9acbb-176">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9acbb-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9acbb-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9acbb-177">-WhatIf</span></span>
<span data-ttu-id="9acbb-178">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9acbb-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9acbb-179">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9acbb-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9acbb-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9acbb-180">CommonParameters</span></span>
<span data-ttu-id="9acbb-181">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9acbb-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9acbb-182">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9acbb-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9acbb-183">輸入</span><span class="sxs-lookup"><span data-stu-id="9acbb-183">INPUTS</span></span>

### <span data-ttu-id="9acbb-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9acbb-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9acbb-185">輸出</span><span class="sxs-lookup"><span data-stu-id="9acbb-185">OUTPUTS</span></span>

### <span data-ttu-id="9acbb-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="9acbb-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="9acbb-187">筆記</span><span class="sxs-lookup"><span data-stu-id="9acbb-187">NOTES</span></span>

<span data-ttu-id="9acbb-188">別名</span><span class="sxs-lookup"><span data-stu-id="9acbb-188">ALIASES</span></span>

<span data-ttu-id="9acbb-189">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9acbb-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9acbb-190">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9acbb-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9acbb-191">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9acbb-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9acbb-192">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9acbb-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9acbb-193">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="9acbb-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9acbb-194">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="9acbb-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9acbb-195">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="9acbb-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9acbb-196">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="9acbb-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9acbb-197">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="9acbb-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9acbb-198">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="9acbb-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9acbb-199">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9acbb-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9acbb-200">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9acbb-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9acbb-201">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9acbb-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9acbb-202">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9acbb-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9acbb-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="9acbb-203">RELATED LINKS</span></span>

