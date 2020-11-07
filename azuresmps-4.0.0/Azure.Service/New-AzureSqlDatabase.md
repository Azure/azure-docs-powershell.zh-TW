---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967419"
---
# <span data-ttu-id="5ccc2-101">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ccc2-101">New-AzureSqlDatabase</span></span>

## <span data-ttu-id="5ccc2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ccc2-102">SYNOPSIS</span></span>
<span data-ttu-id="5ccc2-103">建立 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-103">Creates an Azure SQL Database.</span></span>

## <span data-ttu-id="5ccc2-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ccc2-104">SYNTAX</span></span>

### <span data-ttu-id="5ccc2-105">ByConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="5ccc2-105">ByConnectionContext</span></span>
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ccc2-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="5ccc2-106">ByServerName</span></span>
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ccc2-107">說明</span><span class="sxs-lookup"><span data-stu-id="5ccc2-107">DESCRIPTION</span></span>
<span data-ttu-id="5ccc2-108">**新的-AzureSqlDatabase** Cmdlet 會建立 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-108">The **New-AzureSqlDatabase** cmdlet creates an Azure SQL Database.</span></span>
<span data-ttu-id="5ccc2-109">您可以使用您使用 **AzureSqlDatabaseServerCoNtext** Cmdlet 建立的 Azure SQL Database server 連接內容來指定伺服器。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-109">You can specify the server by using an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="5ccc2-110">或者，如果您指定伺服器名稱，此 Cmdlet 會使用目前的 Azure 訂閱資訊來驗證存取伺服器的要求。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-110">Or, if you specify the server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="5ccc2-111">當您透過指定 Azure SQL 資料庫伺服器建立新資料庫時， **新的 AzureSqlDatabase** Cmdlet 會使用指定的伺服器名稱和目前的 Azure 訂閱資訊來建立暫時的線上內容，以執行操作。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-111">When you create a new database by specifying an Azure SQL Database server, the **New-AzureSqlDatabase** cmdlet creates a temporary connection context using the specified server name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="5ccc2-112">示例</span><span class="sxs-lookup"><span data-stu-id="5ccc2-112">EXAMPLES</span></span>

### <span data-ttu-id="5ccc2-113">範例1：建立資料庫</span><span class="sxs-lookup"><span data-stu-id="5ccc2-113">Example 1: Create a database</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="5ccc2-114">這個命令會建立一個名為 Database1 的 Azure SQL 資料庫，以供 Azure SQL Database server 連接內容 $CoNtext 使用。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-114">This command creates an Azure SQL Database named Database1, for the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="5ccc2-115">範例2：在目前的訂閱中建立資料庫</span><span class="sxs-lookup"><span data-stu-id="5ccc2-115">Example 2: Create a database in the current subscription</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="5ccc2-116">這個範例會在指定的 Azure SQL 資料庫伺服器（名為 lpqd0zbr8y）中建立名為 Database1 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-116">This example creates a database named Database1, in the specified Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="5ccc2-117">此 Cmdlet 會使用目前的 Azure 訂閱資訊來驗證存取伺服器的要求。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-117">The cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

## <span data-ttu-id="5ccc2-118">參數</span><span class="sxs-lookup"><span data-stu-id="5ccc2-118">PARAMETERS</span></span>

### <span data-ttu-id="5ccc2-119">-排序規則</span><span class="sxs-lookup"><span data-stu-id="5ccc2-119">-Collation</span></span>
<span data-ttu-id="5ccc2-120">指定新資料庫的排序規則。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-120">Specifies a collation for the new database.</span></span>

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

### <span data-ttu-id="5ccc2-121">-ConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="5ccc2-121">-ConnectionContext</span></span>
<span data-ttu-id="5ccc2-122">指定此 Cmdlet 建立資料庫的伺服器連接內容。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-122">Specifies the connection context of a server where this cmdlet creates a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ccc2-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ccc2-123">-DatabaseName</span></span>
<span data-ttu-id="5ccc2-124">指定新資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-124">Specifies the name of the new database.</span></span>

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

### <span data-ttu-id="5ccc2-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="5ccc2-125">-Edition</span></span>
<span data-ttu-id="5ccc2-126">指定新 Azure SQL 資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-126">Specifies the edition for the new Azure SQL Database.</span></span>
<span data-ttu-id="5ccc2-127">有效值為：</span><span class="sxs-lookup"><span data-stu-id="5ccc2-127">Valid values are:</span></span> 

- <span data-ttu-id="5ccc2-128">所有</span><span class="sxs-lookup"><span data-stu-id="5ccc2-128">None</span></span>
- <span data-ttu-id="5ccc2-129">網站</span><span class="sxs-lookup"><span data-stu-id="5ccc2-129">Web</span></span>
- <span data-ttu-id="5ccc2-130">部門</span><span class="sxs-lookup"><span data-stu-id="5ccc2-130">Business</span></span>
- <span data-ttu-id="5ccc2-131">空白</span><span class="sxs-lookup"><span data-stu-id="5ccc2-131">Basic</span></span>
- <span data-ttu-id="5ccc2-132">標準</span><span class="sxs-lookup"><span data-stu-id="5ccc2-132">Standard</span></span>
-  <span data-ttu-id="5ccc2-133">佳</span><span class="sxs-lookup"><span data-stu-id="5ccc2-133">Premium</span></span>

<span data-ttu-id="5ccc2-134">預設值為 [Web]。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-134">The default value is Web.</span></span>

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

### <span data-ttu-id="5ccc2-135">-Force</span><span class="sxs-lookup"><span data-stu-id="5ccc2-135">-Force</span></span>
<span data-ttu-id="5ccc2-136">允許動作完成，不會提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-136">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="5ccc2-137">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="5ccc2-137">-MaxSizeBytes</span></span>
<span data-ttu-id="5ccc2-138">指定資料庫的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-138">Specifies the maximum size of the database in bytes.</span></span>
<span data-ttu-id="5ccc2-139">您可以指定此參數或 *MaxSizeGB* 參數。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-139">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="5ccc2-140">根據版本，請參閱 *MaxSizeGB* 參數描述，以取得可接受的值。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-140">See the *MaxSizeGB* parameter description for acceptable values based on edition.</span></span>

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

### <span data-ttu-id="5ccc2-141">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="5ccc2-141">-MaxSizeGB</span></span>
<span data-ttu-id="5ccc2-142">以千百萬位元組指定資料庫的大小上限。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-142">Specifies the maximum size of the database in gigabytes.</span></span>
<span data-ttu-id="5ccc2-143">您可以指定此參數或 *MaxSizeBytes* 參數。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-143">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="5ccc2-144">根據版本，可接受的值會有所不同。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-144">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="5ccc2-145">基本版本值：1或2</span><span class="sxs-lookup"><span data-stu-id="5ccc2-145">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="5ccc2-146">標準版值：1、2、5、10、20、30、40、50、100、150、200或250</span><span class="sxs-lookup"><span data-stu-id="5ccc2-146">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="5ccc2-147">津貼版本值：1、2、5、10、20、30、40、50、100、150、200、250、300、400或500</span><span class="sxs-lookup"><span data-stu-id="5ccc2-147">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="5ccc2-148">網頁版值：1或5</span><span class="sxs-lookup"><span data-stu-id="5ccc2-148">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="5ccc2-149">商務版值：10、20、30、40、50、100或150</span><span class="sxs-lookup"><span data-stu-id="5ccc2-149">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

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

### <span data-ttu-id="5ccc2-150">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5ccc2-150">-Profile</span></span>
<span data-ttu-id="5ccc2-151">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ccc2-152">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ccc2-153">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5ccc2-153">-ServerName</span></span>
<span data-ttu-id="5ccc2-154">指定要包含新資料庫之 Azure SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-154">Specifies the name of the Azure SQL Database server to contain the new database.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ccc2-155">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="5ccc2-155">-ServiceObjective</span></span>
<span data-ttu-id="5ccc2-156">指定代表新服務目標的物件 (此資料庫的效能層級) 。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-156">Specifies an object that represent the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="5ccc2-157">這個值代表指派給此資料庫的資源層級。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-157">This value represents the level of resources assigned to this database.</span></span>
<span data-ttu-id="5ccc2-158">有效值為：</span><span class="sxs-lookup"><span data-stu-id="5ccc2-158">Valid values are:</span></span> 

<span data-ttu-id="5ccc2-159">基本： dd6d99bb-f193-4ec1-86f2-43d3bccbc49c 標準 (S0) ： f1173c43-91bd-4aaa-973c-54e79e15235b 標準 (S1) ：1b1ebd4d-d903-4baa-97f9-4ea675f5e928 標準 (S2) ： 455330e1-00cd-488b-b5fa-177c226f28b7 \* 標準 (S3) ： 789681b8-ca10-4eb0-bdf2-e0b050601b40 premium (P1) ： 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium () ： 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2) ： a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3) ： a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="5ccc2-159">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="5ccc2-160">\* 標準 (S3) 是最新的 SQL 資料庫更新 V12 (preview) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-160">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="5ccc2-161">如需詳細資訊，請參閱 Azure SQL 資料庫 V12 Preview 的新增功能 https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ 。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-161">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

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

### <span data-ttu-id="5ccc2-162">-確認</span><span class="sxs-lookup"><span data-stu-id="5ccc2-162">-Confirm</span></span>
<span data-ttu-id="5ccc2-163">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ccc2-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ccc2-164">-WhatIf</span></span>
<span data-ttu-id="5ccc2-165">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ccc2-166">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ccc2-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ccc2-167">CommonParameters</span></span>
<span data-ttu-id="5ccc2-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ccc2-169">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ccc2-170">輸入</span><span class="sxs-lookup"><span data-stu-id="5ccc2-170">INPUTS</span></span>

## <span data-ttu-id="5ccc2-171">輸出</span><span class="sxs-lookup"><span data-stu-id="5ccc2-171">OUTPUTS</span></span>

### <span data-ttu-id="5ccc2-172">SqlDatabase.. Database （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="5ccc2-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="5ccc2-173">筆記</span><span class="sxs-lookup"><span data-stu-id="5ccc2-173">NOTES</span></span>
* <span data-ttu-id="5ccc2-174">若要刪除由 **新的 AzureSqlDatabase** 所建立的資料庫，請使用 Remove-AzureSqlDatabase Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ccc2-174">To delete a database that was created by **New-AzureSqlDatabase** , use the Remove-AzureSqlDatabase cmdlet.</span></span>

## <span data-ttu-id="5ccc2-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ccc2-175">RELATED LINKS</span></span>

[<span data-ttu-id="5ccc2-176">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="5ccc2-176">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="5ccc2-177">建立資料庫</span><span class="sxs-lookup"><span data-stu-id="5ccc2-177">Create Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[<span data-ttu-id="5ccc2-178">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="5ccc2-178">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="5ccc2-179">AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ccc2-179">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="5ccc2-180">新-AzureSqlDatabaseServerCoNtext</span><span class="sxs-lookup"><span data-stu-id="5ccc2-180">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="5ccc2-181">移除-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ccc2-181">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="5ccc2-182">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5ccc2-182">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


