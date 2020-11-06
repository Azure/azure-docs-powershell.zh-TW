---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: b0493433f7419039acacd696748b3c5f9518aef5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447595"
---
# <span data-ttu-id="ed031-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed031-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="ed031-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed031-102">SYNOPSIS</span></span>
<span data-ttu-id="ed031-103">為資料庫設定屬性，或將現有資料庫移至彈性池中。</span><span class="sxs-lookup"><span data-stu-id="ed031-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed031-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed031-104">SYNTAX</span></span>

### <span data-ttu-id="ed031-105">時更新</span><span class="sxs-lookup"><span data-stu-id="ed031-105">Update</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed031-106">重新命名</span><span class="sxs-lookup"><span data-stu-id="ed031-106">Rename</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed031-107">說明</span><span class="sxs-lookup"><span data-stu-id="ed031-107">DESCRIPTION</span></span>
<span data-ttu-id="ed031-108">**AzureRmSqlDatabase** Cmdlet 會在 Azure SQL database 中設定資料庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ed031-108">The **Set-AzureRmSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="ed031-109">這個 Cmdlet 可以修改服務層級 ( *Edition* ) 、效能層 ( *RequestedServiceObjectiveName* ) ，以及資料庫的 ( *MaxSizeBytes* ) 的儲存空間大小上限。</span><span class="sxs-lookup"><span data-stu-id="ed031-109">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="ed031-110">此外，您也可以指定 *ElasticPoolName* 參數，將資料庫移至彈性池。</span><span class="sxs-lookup"><span data-stu-id="ed031-110">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="ed031-111">如果資料庫已在彈性池中，您可以使用 *RequestedServiceObjectiveName* 參數，將資料庫從彈性池移出，然後轉化為單一資料庫的效能等級。</span><span class="sxs-lookup"><span data-stu-id="ed031-111">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="ed031-112">示例</span><span class="sxs-lookup"><span data-stu-id="ed031-112">EXAMPLES</span></span>

### <span data-ttu-id="ed031-113">範例1：將資料庫更新為標準的 S2 資料庫</span><span class="sxs-lookup"><span data-stu-id="ed031-113">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="ed031-114">這個命令會將一個名為 Database01 的資料庫，更新為伺服器上名為 Server01 的標準 S2 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ed031-114">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="ed031-115">範例2：將資料庫新增至彈性池</span><span class="sxs-lookup"><span data-stu-id="ed031-115">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="ed031-116">這個命令會將一個名為 Database01 的資料庫，新增到名為 Server01 的伺服器上名為 ElasticPool01 的彈性池。</span><span class="sxs-lookup"><span data-stu-id="ed031-116">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="ed031-117">範例3：修改資料庫的儲存空間大小上限</span><span class="sxs-lookup"><span data-stu-id="ed031-117">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="ed031-118">這個命令會更新一個名為 Database01 的資料庫，將其最大大小設成 1 TB。</span><span class="sxs-lookup"><span data-stu-id="ed031-118">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="ed031-119">參數</span><span class="sxs-lookup"><span data-stu-id="ed031-119">PARAMETERS</span></span>

### <span data-ttu-id="ed031-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed031-120">-AsJob</span></span>
<span data-ttu-id="ed031-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ed031-121">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="ed031-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed031-122">-DatabaseName</span></span>
<span data-ttu-id="ed031-123">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed031-123">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed031-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed031-124">-DefaultProfile</span></span>
<span data-ttu-id="ed031-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ed031-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed031-126">-Edition</span><span class="sxs-lookup"><span data-stu-id="ed031-126">-Edition</span></span>
<span data-ttu-id="ed031-127">指定資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="ed031-127">Specifies the edition for the database.</span></span>
<span data-ttu-id="ed031-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ed031-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ed031-129">所有</span><span class="sxs-lookup"><span data-stu-id="ed031-129">None</span></span>
- <span data-ttu-id="ed031-130">佳</span><span class="sxs-lookup"><span data-stu-id="ed031-130">Premium</span></span>
- <span data-ttu-id="ed031-131">空白</span><span class="sxs-lookup"><span data-stu-id="ed031-131">Basic</span></span>
- <span data-ttu-id="ed031-132">標準</span><span class="sxs-lookup"><span data-stu-id="ed031-132">Standard</span></span>
- <span data-ttu-id="ed031-133">倉庫</span><span class="sxs-lookup"><span data-stu-id="ed031-133">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: Update
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed031-134">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ed031-134">-ElasticPoolName</span></span>
<span data-ttu-id="ed031-135">指定要在其中移動資料庫的彈性池名稱。</span><span class="sxs-lookup"><span data-stu-id="ed031-135">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed031-136">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="ed031-136">-MaxSizeBytes</span></span>
<span data-ttu-id="ed031-137">Azure SQL 資料庫的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ed031-137">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed031-138">-NewName</span><span class="sxs-lookup"><span data-stu-id="ed031-138">-NewName</span></span>
<span data-ttu-id="ed031-139">重新命名資料庫的新名稱。</span><span class="sxs-lookup"><span data-stu-id="ed031-139">The new name to rename the database to.</span></span>

```yaml
Type: String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed031-140">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="ed031-140">-ReadScale</span></span>
<span data-ttu-id="ed031-141">要指派給 Azure SQL 資料庫的 [讀取比例] 選項。 (啟用/停用) </span><span class="sxs-lookup"><span data-stu-id="ed031-141">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: Update
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed031-142">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ed031-142">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="ed031-143">指定要指派給資料庫之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed031-143">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="ed031-144">如需服務目標的相關資訊，請參閱 Microsoft 開發人員網路文件庫中的 [AZURE SQL 資料庫服務層級和效能層級](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="ed031-144">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed031-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed031-145">-ResourceGroupName</span></span>
<span data-ttu-id="ed031-146">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed031-146">Specifies the name of resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed031-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ed031-147">-ServerName</span></span>
<span data-ttu-id="ed031-148">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ed031-148">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed031-149">-標記</span><span class="sxs-lookup"><span data-stu-id="ed031-149">-Tags</span></span>
<span data-ttu-id="ed031-150">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="ed031-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ed031-151">例如：</span><span class="sxs-lookup"><span data-stu-id="ed031-151">For example:</span></span>

<span data-ttu-id="ed031-152">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ed031-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Update
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed031-153">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="ed031-153">-ZoneRedundant</span></span>
<span data-ttu-id="ed031-154">要與 Azure Sql 資料庫建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="ed031-154">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed031-155">-確認</span><span class="sxs-lookup"><span data-stu-id="ed031-155">-Confirm</span></span>
<span data-ttu-id="ed031-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed031-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed031-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed031-157">-WhatIf</span></span>
<span data-ttu-id="ed031-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed031-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed031-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed031-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed031-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed031-160">CommonParameters</span></span>
<span data-ttu-id="ed031-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed031-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed031-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed031-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed031-163">輸入</span><span class="sxs-lookup"><span data-stu-id="ed031-163">INPUTS</span></span>

### <span data-ttu-id="ed031-164">所有</span><span class="sxs-lookup"><span data-stu-id="ed031-164">None</span></span>
<span data-ttu-id="ed031-165">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ed031-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed031-166">輸出</span><span class="sxs-lookup"><span data-stu-id="ed031-166">OUTPUTS</span></span>

### <span data-ttu-id="ed031-167">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="ed031-167">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ed031-168">筆記</span><span class="sxs-lookup"><span data-stu-id="ed031-168">NOTES</span></span>

## <span data-ttu-id="ed031-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed031-169">RELATED LINKS</span></span>

[<span data-ttu-id="ed031-170">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed031-170">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="ed031-171">新-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed031-171">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="ed031-172">移除-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed031-172">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="ed031-173">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed031-173">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="ed031-174">暫停-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed031-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="ed031-175">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ed031-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
