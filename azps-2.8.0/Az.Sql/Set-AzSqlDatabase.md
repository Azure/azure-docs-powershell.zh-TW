---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: dd69e345e5e2bac5ebab0ec4e45c03501ccc8139
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792666"
---
# <span data-ttu-id="b6686-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b6686-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="b6686-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6686-102">SYNOPSIS</span></span>
<span data-ttu-id="b6686-103">為資料庫設定屬性，或將現有資料庫移至彈性池中。</span><span class="sxs-lookup"><span data-stu-id="b6686-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="b6686-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6686-104">SYNTAX</span></span>

### <span data-ttu-id="b6686-105">更新 (預設) </span><span class="sxs-lookup"><span data-stu-id="b6686-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6686-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="b6686-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6686-107">重新命名</span><span class="sxs-lookup"><span data-stu-id="b6686-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6686-108">說明</span><span class="sxs-lookup"><span data-stu-id="b6686-108">DESCRIPTION</span></span>
<span data-ttu-id="b6686-109">**AzSqlDatabase** Cmdlet 會在 Azure SQL database 中設定資料庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="b6686-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="b6686-110">這個 Cmdlet 可以修改服務層級 ( *Edition* ) 、效能層 ( *RequestedServiceObjectiveName* ) ，以及資料庫的 ( *MaxSizeBytes* ) 的儲存空間大小上限。</span><span class="sxs-lookup"><span data-stu-id="b6686-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="b6686-111">此外，您也可以指定 *ElasticPoolName* 參數，將資料庫移至彈性池。</span><span class="sxs-lookup"><span data-stu-id="b6686-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="b6686-112">如果資料庫已在彈性池中，您可以使用 *RequestedServiceObjectiveName* 參數，將資料庫從彈性池移出，然後轉化為單一資料庫的效能等級。</span><span class="sxs-lookup"><span data-stu-id="b6686-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="b6686-113">示例</span><span class="sxs-lookup"><span data-stu-id="b6686-113">EXAMPLES</span></span>

### <span data-ttu-id="b6686-114">範例1：將資料庫更新為標準 S0 資料庫</span><span class="sxs-lookup"><span data-stu-id="b6686-114">Example 1: Update a database to a Standard S0 database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S0"
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
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="b6686-115">這個命令會將一個名為 Database01 的資料庫，更新為伺服器上名為 Server01 的標準 S0 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b6686-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="b6686-116">範例2：將資料庫新增至彈性池</span><span class="sxs-lookup"><span data-stu-id="b6686-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="b6686-117">這個命令會將一個名為 Database01 的資料庫，新增到名為 Server01 的伺服器上名為 ElasticPool01 的彈性池。</span><span class="sxs-lookup"><span data-stu-id="b6686-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="b6686-118">範例3：修改資料庫的儲存空間大小上限</span><span class="sxs-lookup"><span data-stu-id="b6686-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
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

<span data-ttu-id="b6686-119">這個命令會更新一個名為 Database01 的資料庫，將其最大大小設成 1 TB。</span><span class="sxs-lookup"><span data-stu-id="b6686-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="b6686-120">參數</span><span class="sxs-lookup"><span data-stu-id="b6686-120">PARAMETERS</span></span>

### <span data-ttu-id="b6686-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6686-121">-AsJob</span></span>
<span data-ttu-id="b6686-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b6686-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6686-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="b6686-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="b6686-124">僅限資料庫 (無伺服器的自動暫停延遲時間) ，-1 以退出宣告</span><span class="sxs-lookup"><span data-stu-id="b6686-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-125">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="b6686-125">-ComputeGeneration</span></span>
<span data-ttu-id="b6686-126">要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="b6686-126">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-127">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="b6686-127">-ComputeModel</span></span>
<span data-ttu-id="b6686-128">Azure Sql 資料庫的計算模型。</span><span class="sxs-lookup"><span data-stu-id="b6686-128">Computed model of Azure Sql database.</span></span> <span data-ttu-id="b6686-129">無伺服器或已預配</span><span class="sxs-lookup"><span data-stu-id="b6686-129">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b6686-130">-DatabaseName</span></span>
<span data-ttu-id="b6686-131">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6686-131">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6686-132">-DefaultProfile</span></span>
<span data-ttu-id="b6686-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b6686-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6686-134">-Edition</span><span class="sxs-lookup"><span data-stu-id="b6686-134">-Edition</span></span>
<span data-ttu-id="b6686-135">指定資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="b6686-135">Specifies the edition for the database.</span></span>
<span data-ttu-id="b6686-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b6686-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6686-137">所有</span><span class="sxs-lookup"><span data-stu-id="b6686-137">None</span></span>
- <span data-ttu-id="b6686-138">空白</span><span class="sxs-lookup"><span data-stu-id="b6686-138">Basic</span></span>
- <span data-ttu-id="b6686-139">標準</span><span class="sxs-lookup"><span data-stu-id="b6686-139">Standard</span></span>
- <span data-ttu-id="b6686-140">佳</span><span class="sxs-lookup"><span data-stu-id="b6686-140">Premium</span></span>
- <span data-ttu-id="b6686-141">倉庫</span><span class="sxs-lookup"><span data-stu-id="b6686-141">DataWarehouse</span></span>
- <span data-ttu-id="b6686-142">空閒</span><span class="sxs-lookup"><span data-stu-id="b6686-142">Free</span></span>
- <span data-ttu-id="b6686-143">伸縮</span><span class="sxs-lookup"><span data-stu-id="b6686-143">Stretch</span></span>
- <span data-ttu-id="b6686-144">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="b6686-144">GeneralPurpose</span></span>
- <span data-ttu-id="b6686-145">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="b6686-145">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-146">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b6686-146">-ElasticPoolName</span></span>
<span data-ttu-id="b6686-147">指定要在其中移動資料庫的彈性池名稱。</span><span class="sxs-lookup"><span data-stu-id="b6686-147">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b6686-148">-LicenseType</span></span>
<span data-ttu-id="b6686-149">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="b6686-149">The license type for the Azure Sql database.</span></span> <span data-ttu-id="b6686-150">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="b6686-150">Possible values are:</span></span>
- <span data-ttu-id="b6686-151">BasePrice-Azure 混合式福利 () AHB 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="b6686-151">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="b6686-152">現有 SQL Server 授權擁有者的資料庫價格將會打折。</span><span class="sxs-lookup"><span data-stu-id="b6686-152">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="b6686-153">LicenseIncluded-Azure 混合式福利 () AHB 不會套用現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="b6686-153">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="b6686-154">資料庫價格將包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="b6686-154">Database price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-155">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="b6686-155">-MaxSizeBytes</span></span>
<span data-ttu-id="b6686-156">Azure SQL 資料庫的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b6686-156">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-157">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="b6686-157">-MinimumCapacity</span></span>
<span data-ttu-id="b6686-158">資料庫始終已配置的最小產能（如果沒有暫停的話）。</span><span class="sxs-lookup"><span data-stu-id="b6686-158">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="b6686-159">僅限無伺服器的 Azure Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b6686-159">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-160">-NewName</span><span class="sxs-lookup"><span data-stu-id="b6686-160">-NewName</span></span>
<span data-ttu-id="b6686-161">重新命名資料庫的新名稱。</span><span class="sxs-lookup"><span data-stu-id="b6686-161">The new name to rename the database to.</span></span>

```yaml
Type: System.String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-162">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="b6686-162">-ReadScale</span></span>
<span data-ttu-id="b6686-163">要指派給 Azure SQL 資料庫的 [讀取比例] 選項。 (啟用/停用) </span><span class="sxs-lookup"><span data-stu-id="b6686-163">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: Update, VcoreBasedDatabase
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-164">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b6686-164">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="b6686-165">指定要指派給資料庫之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6686-165">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="b6686-166">如需服務目標的相關資訊，請參閱 Microsoft 開發人員網路文件庫中的 [AZURE SQL 資料庫服務層級和效能層級](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) 。</span><span class="sxs-lookup"><span data-stu-id="b6686-166">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6686-167">-ResourceGroupName</span></span>
<span data-ttu-id="b6686-168">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6686-168">Specifies the name of resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-169">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b6686-169">-ServerName</span></span>
<span data-ttu-id="b6686-170">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b6686-170">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-171">-標記</span><span class="sxs-lookup"><span data-stu-id="b6686-171">-Tags</span></span>
<span data-ttu-id="b6686-172">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="b6686-172">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b6686-173">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b6686-173">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update, VcoreBasedDatabase
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-174">-VCore</span><span class="sxs-lookup"><span data-stu-id="b6686-174">-VCore</span></span>
<span data-ttu-id="b6686-175">Azure Sql 資料庫的 Vcore 號碼</span><span class="sxs-lookup"><span data-stu-id="b6686-175">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-176">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="b6686-176">-ZoneRedundant</span></span>
<span data-ttu-id="b6686-177">要與 Azure Sql 資料庫建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="b6686-177">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-178">-確認</span><span class="sxs-lookup"><span data-stu-id="b6686-178">-Confirm</span></span>
<span data-ttu-id="b6686-179">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b6686-179">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6686-180">-WhatIf</span></span>
<span data-ttu-id="b6686-181">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6686-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6686-182">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6686-182">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6686-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6686-183">CommonParameters</span></span>
<span data-ttu-id="b6686-184">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6686-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6686-185">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b6686-185">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6686-186">輸入</span><span class="sxs-lookup"><span data-stu-id="b6686-186">INPUTS</span></span>

### <span data-ttu-id="b6686-187">System.object</span><span class="sxs-lookup"><span data-stu-id="b6686-187">System.String</span></span>

## <span data-ttu-id="b6686-188">輸出</span><span class="sxs-lookup"><span data-stu-id="b6686-188">OUTPUTS</span></span>

### <span data-ttu-id="b6686-189">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="b6686-189">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b6686-190">筆記</span><span class="sxs-lookup"><span data-stu-id="b6686-190">NOTES</span></span>

## <span data-ttu-id="b6686-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6686-191">RELATED LINKS</span></span>

[<span data-ttu-id="b6686-192">AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b6686-192">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="b6686-193">新-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b6686-193">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="b6686-194">移除-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b6686-194">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="b6686-195">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b6686-195">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="b6686-196">暫停-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b6686-196">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="b6686-197">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b6686-197">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
