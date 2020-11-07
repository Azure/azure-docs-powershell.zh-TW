---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967311"
---
# <span data-ttu-id="c1ad0-101">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c1ad0-101">Set-AzureSqlDatabase</span></span>

## <span data-ttu-id="c1ad0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ad0-103">設定 Azure SQL 資料庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-103">Sets properties for an Azure SQL Database.</span></span>

## <span data-ttu-id="c1ad0-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1ad0-104">SYNTAX</span></span>

### <span data-ttu-id="c1ad0-105">ByNameWithConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="c1ad0-105">ByNameWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1ad0-106">ByObjectWithConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="c1ad0-106">ByObjectWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1ad0-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="c1ad0-107">ByNameWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1ad0-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="c1ad0-108">ByObjectWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1ad0-109">說明</span><span class="sxs-lookup"><span data-stu-id="c1ad0-109">DESCRIPTION</span></span>
<span data-ttu-id="c1ad0-110">**AzureSqlDatabase** Cmdlet 會設定 Azure SQL 資料庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-110">The **Set-AzureSqlDatabase** cmdlet sets properties for an Azure SQL Database.</span></span>
<span data-ttu-id="c1ad0-111">您可以依名稱指定資料庫，或透過管線傳送 Azure SQL Database 物件。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-111">You can specify the database by name, or pass an Azure SQL Database object through the pipeline.</span></span>
<span data-ttu-id="c1ad0-112">您可以依名稱指定伺服器，或傳遞 Azure SQL Database server 連接內容。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-112">You can specify the server by name, or pass an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="c1ad0-113">執行 **AzureSqlDatabaseServerCoNtext** Cmdlet 來建立連接內容。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-113">Create a connection context by running the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="c1ad0-114">如果您依名稱指定伺服器，此 Cmdlet 會使用目前的 Azure 訂閱資訊來驗證要求。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-114">If you specify the server by name, the cmdlet uses the current Azure subscription information to authenticate the request.</span></span>

## <span data-ttu-id="c1ad0-115">示例</span><span class="sxs-lookup"><span data-stu-id="c1ad0-115">EXAMPLES</span></span>

### <span data-ttu-id="c1ad0-116">範例1：使用連接內容變更資料庫的大小</span><span class="sxs-lookup"><span data-stu-id="c1ad0-116">Example 1: Change the size of a database by using a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="c1ad0-117">這個範例會在 Azure SQL Database server 連接內容 $CoNtext 中，將名為 Database01 的資料庫大小變更為 20 GB。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-117">This example changes the size of the database named Database01 to 20 GB, in the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="c1ad0-118">範例2：使用伺服器名稱變更資料庫的大小</span><span class="sxs-lookup"><span data-stu-id="c1ad0-118">Example 2: Change the size of a database by using a server name</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="c1ad0-119">這個範例會將名為 Database01 的資料庫大小從伺服器中的 [lpqd0zbr8y] 變更為 20 GB。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-119">This example changes the size of the database named Database01 to 20 GB in the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="c1ad0-120">參數</span><span class="sxs-lookup"><span data-stu-id="c1ad0-120">PARAMETERS</span></span>

### <span data-ttu-id="c1ad0-121">-ConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="c1ad0-121">-ConnectionContext</span></span>
<span data-ttu-id="c1ad0-122">指定伺服器的連接內容。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-122">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ad0-123">-資料庫</span><span class="sxs-lookup"><span data-stu-id="c1ad0-123">-Database</span></span>
<span data-ttu-id="c1ad0-124">指定代表此 Cmdlet 所修改之 Azure SQL 資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-124">Specifies an object that represents the Azure SQL Database that this cmdlet modifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ad0-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c1ad0-125">-DatabaseName</span></span>
<span data-ttu-id="c1ad0-126">指定此 Cmdlet 所修改之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-126">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ad0-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="c1ad0-127">-Edition</span></span>
<span data-ttu-id="c1ad0-128">指定 Azure SQL 資料庫的新版本。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-128">Specifies the new edition for the Azure SQL Database.</span></span>
<span data-ttu-id="c1ad0-129">有效值為：</span><span class="sxs-lookup"><span data-stu-id="c1ad0-129">Valid values are:</span></span> 

- <span data-ttu-id="c1ad0-130">所有</span><span class="sxs-lookup"><span data-stu-id="c1ad0-130">None</span></span>
- <span data-ttu-id="c1ad0-131">網站</span><span class="sxs-lookup"><span data-stu-id="c1ad0-131">Web</span></span>
- <span data-ttu-id="c1ad0-132">部門</span><span class="sxs-lookup"><span data-stu-id="c1ad0-132">Business</span></span>
- <span data-ttu-id="c1ad0-133">空白</span><span class="sxs-lookup"><span data-stu-id="c1ad0-133">Basic</span></span>
- <span data-ttu-id="c1ad0-134">標準</span><span class="sxs-lookup"><span data-stu-id="c1ad0-134">Standard</span></span>
-  <span data-ttu-id="c1ad0-135">佳</span><span class="sxs-lookup"><span data-stu-id="c1ad0-135">Premium</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ad0-136">-Force</span><span class="sxs-lookup"><span data-stu-id="c1ad0-136">-Force</span></span>
<span data-ttu-id="c1ad0-137">允許動作完成，不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-137">Allows the action to complete without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c1ad0-138">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="c1ad0-138">-MaxSizeBytes</span></span>
<span data-ttu-id="c1ad0-139">指定資料庫的新的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-139">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="c1ad0-140">您可以指定此參數或 *MaxSizeGB* 參數。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-140">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="c1ad0-141">根據版本，請參閱 *MaxSizeGB* 參數以取得可接受的值。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-141">See the *MaxSizeGB* parameter for acceptable values based on edition.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ad0-142">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="c1ad0-142">-MaxSizeGB</span></span>
<span data-ttu-id="c1ad0-143">指定資料庫的新最大大小（以 gb 為限制）。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-143">Specifies the new maximum size for the database in gigabytes.</span></span>
<span data-ttu-id="c1ad0-144">您可以指定此參數或 *MaxSizeBytes* 參數。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-144">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="c1ad0-145">根據版本，可接受的值會有所不同。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-145">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="c1ad0-146">基本版本值：1或2</span><span class="sxs-lookup"><span data-stu-id="c1ad0-146">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="c1ad0-147">標準版值：1、2、5、10、20、30、40、50、100、150、200或250</span><span class="sxs-lookup"><span data-stu-id="c1ad0-147">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="c1ad0-148">津貼版本值：1、2、5、10、20、30、40、50、100、150、200、250、300、400或500</span><span class="sxs-lookup"><span data-stu-id="c1ad0-148">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="c1ad0-149">網頁版值：1或5</span><span class="sxs-lookup"><span data-stu-id="c1ad0-149">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="c1ad0-150">商務版值：10、20、30、40、50、100或150</span><span class="sxs-lookup"><span data-stu-id="c1ad0-150">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

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

### <span data-ttu-id="c1ad0-151">-NewDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c1ad0-151">-NewDatabaseName</span></span>
<span data-ttu-id="c1ad0-152">指定資料庫的新名稱。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-152">Specifies the new name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ad0-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1ad0-153">-PassThru</span></span>
<span data-ttu-id="c1ad0-154">傳回已更新的 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-154">Returns the updated Azure SQL Database.</span></span>

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

### <span data-ttu-id="c1ad0-155">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c1ad0-155">-Profile</span></span>
<span data-ttu-id="c1ad0-156">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c1ad0-157">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ad0-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c1ad0-158">-ServerName</span></span>
<span data-ttu-id="c1ad0-159">指定包含此 Cmdlet 所修改之資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-159">Specifies the name of the server that contains the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ad0-160">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="c1ad0-160">-ServiceObjective</span></span>
<span data-ttu-id="c1ad0-161">指定代表新服務目標的物件 (此資料庫的效能層級) 。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-161">Specifies an object representing the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="c1ad0-162">有效值為：</span><span class="sxs-lookup"><span data-stu-id="c1ad0-162">Valid values are:</span></span> 

- <span data-ttu-id="c1ad0-163">基本： dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="c1ad0-163">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="c1ad0-164">標準 (S0) ： f1173c43-91bd-4aaa-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="c1ad0-164">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="c1ad0-165">標準 (S1) ：1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="c1ad0-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="c1ad0-166">標準 (S2) ：455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="c1ad0-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="c1ad0-167">\* 標準 (S3) ：789681b8-ca10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="c1ad0-167">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="c1ad0-168">Premium (P1) ：7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="c1ad0-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="c1ad0-169">Premium (P2) ： a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="c1ad0-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="c1ad0-170">Premium (P3) ： a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="c1ad0-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="c1ad0-171">\* 標準 (S3) 是最新的 SQL 資料庫更新 V12 (preview) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-171">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="c1ad0-172">如需詳細資訊，請參閱 Azure SQL 資料庫 V12 Preview 的新增功能 https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ 。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-172">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ad0-173">-同步處理</span><span class="sxs-lookup"><span data-stu-id="c1ad0-173">-Sync</span></span>
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

### <span data-ttu-id="c1ad0-174">-確認</span><span class="sxs-lookup"><span data-stu-id="c1ad0-174">-Confirm</span></span>
<span data-ttu-id="c1ad0-175">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ad0-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1ad0-176">-WhatIf</span></span>
<span data-ttu-id="c1ad0-177">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1ad0-178">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-178">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ad0-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ad0-179">CommonParameters</span></span>
<span data-ttu-id="c1ad0-180">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ad0-181">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1ad0-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ad0-182">輸入</span><span class="sxs-lookup"><span data-stu-id="c1ad0-182">INPUTS</span></span>

### <span data-ttu-id="c1ad0-183">SqlDatabase.. Database （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="c1ad0-183">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="c1ad0-184">輸出</span><span class="sxs-lookup"><span data-stu-id="c1ad0-184">OUTPUTS</span></span>

### <span data-ttu-id="c1ad0-185">SqlDatabase.. Database （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="c1ad0-185">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="c1ad0-186">筆記</span><span class="sxs-lookup"><span data-stu-id="c1ad0-186">NOTES</span></span>

## <span data-ttu-id="c1ad0-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1ad0-187">RELATED LINKS</span></span>

[<span data-ttu-id="c1ad0-188">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="c1ad0-188">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c1ad0-189">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="c1ad0-189">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c1ad0-190">更新資料庫</span><span class="sxs-lookup"><span data-stu-id="c1ad0-190">Update Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[<span data-ttu-id="c1ad0-191">AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c1ad0-191">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="c1ad0-192">新-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c1ad0-192">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="c1ad0-193">移除-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c1ad0-193">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="c1ad0-194">新-AzureSqlDatabaseServerCoNtext</span><span class="sxs-lookup"><span data-stu-id="c1ad0-194">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


