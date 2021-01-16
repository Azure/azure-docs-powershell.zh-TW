---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 15f9aee8e278a1b33330508a10487e3847820891
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278784"
---
# <span data-ttu-id="98055-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="98055-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="98055-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98055-102">SYNOPSIS</span></span>
<span data-ttu-id="98055-103">為資料庫設定屬性，或將現有資料庫移至彈性池中。</span><span class="sxs-lookup"><span data-stu-id="98055-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="98055-104">句法</span><span class="sxs-lookup"><span data-stu-id="98055-104">SYNTAX</span></span>

### <span data-ttu-id="98055-105">更新 (預設) </span><span class="sxs-lookup"><span data-stu-id="98055-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98055-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="98055-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98055-107">重新命名</span><span class="sxs-lookup"><span data-stu-id="98055-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98055-108">說明</span><span class="sxs-lookup"><span data-stu-id="98055-108">DESCRIPTION</span></span>
<span data-ttu-id="98055-109">**AzSqlDatabase** Cmdlet 會在 Azure SQL database 中設定資料庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="98055-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="98055-110">這個 Cmdlet 可以修改服務層級 (*Edition*) 、效能層 (*RequestedServiceObjectiveName*) ，以及資料庫的 (*MaxSizeBytes*) 的儲存空間大小上限。</span><span class="sxs-lookup"><span data-stu-id="98055-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="98055-111">此外，您也可以指定 *ElasticPoolName* 參數，將資料庫移至彈性池。</span><span class="sxs-lookup"><span data-stu-id="98055-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="98055-112">如果資料庫已在彈性池中，您可以使用 *RequestedServiceObjectiveName* 參數，將資料庫從彈性池移出，然後轉化為單一資料庫的效能等級。</span><span class="sxs-lookup"><span data-stu-id="98055-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="98055-113">示例</span><span class="sxs-lookup"><span data-stu-id="98055-113">EXAMPLES</span></span>

### <span data-ttu-id="98055-114">範例1：將資料庫更新為標準 S0 資料庫</span><span class="sxs-lookup"><span data-stu-id="98055-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="98055-115">這個命令會將一個名為 Database01 的資料庫，更新為伺服器上名為 Server01 的標準 S0 資料庫。</span><span class="sxs-lookup"><span data-stu-id="98055-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="98055-116">範例2：將資料庫新增至彈性池</span><span class="sxs-lookup"><span data-stu-id="98055-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="98055-117">這個命令會將一個名為 Database01 的資料庫，新增到名為 Server01 的伺服器上名為 ElasticPool01 的彈性池。</span><span class="sxs-lookup"><span data-stu-id="98055-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="98055-118">範例3：修改資料庫的儲存空間大小上限</span><span class="sxs-lookup"><span data-stu-id="98055-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="98055-119">這個命令會更新一個名為 Database01 的資料庫，將其最大大小設成 1 TB。</span><span class="sxs-lookup"><span data-stu-id="98055-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="98055-120">參數</span><span class="sxs-lookup"><span data-stu-id="98055-120">PARAMETERS</span></span>

### <span data-ttu-id="98055-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98055-121">-AsJob</span></span>
<span data-ttu-id="98055-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="98055-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98055-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="98055-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="98055-124">僅限資料庫 (無伺服器的自動暫停延遲時間) ，-1 以退出宣告</span><span class="sxs-lookup"><span data-stu-id="98055-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="98055-125">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="98055-125">-BackupStorageRedundancy</span></span>
<span data-ttu-id="98055-126">儲存 SQL 資料庫備份所用的備份儲存空間冗余。</span><span class="sxs-lookup"><span data-stu-id="98055-126">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="98055-127">選項包括： Local、Zone 和 Geo。</span><span class="sxs-lookup"><span data-stu-id="98055-127">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98055-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="98055-128">-ComputeGeneration</span></span>
<span data-ttu-id="98055-129">要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="98055-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="98055-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="98055-130">-ComputeModel</span></span>
<span data-ttu-id="98055-131">Azure Sql 資料庫的計算模型。</span><span class="sxs-lookup"><span data-stu-id="98055-131">Computed model of Azure Sql database.</span></span> <span data-ttu-id="98055-132">無伺服器或已預配</span><span class="sxs-lookup"><span data-stu-id="98055-132">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="98055-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="98055-133">-DatabaseName</span></span>
<span data-ttu-id="98055-134">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="98055-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="98055-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98055-135">-DefaultProfile</span></span>
<span data-ttu-id="98055-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="98055-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98055-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="98055-137">-Edition</span></span>
<span data-ttu-id="98055-138">指定資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="98055-138">Specifies the edition for the database.</span></span>
<span data-ttu-id="98055-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="98055-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="98055-140">所有</span><span class="sxs-lookup"><span data-stu-id="98055-140">None</span></span>
- <span data-ttu-id="98055-141">空白</span><span class="sxs-lookup"><span data-stu-id="98055-141">Basic</span></span>
- <span data-ttu-id="98055-142">標準</span><span class="sxs-lookup"><span data-stu-id="98055-142">Standard</span></span>
- <span data-ttu-id="98055-143">佳</span><span class="sxs-lookup"><span data-stu-id="98055-143">Premium</span></span>
- <span data-ttu-id="98055-144">倉庫</span><span class="sxs-lookup"><span data-stu-id="98055-144">DataWarehouse</span></span>
- <span data-ttu-id="98055-145">空閒</span><span class="sxs-lookup"><span data-stu-id="98055-145">Free</span></span>
- <span data-ttu-id="98055-146">伸縮</span><span class="sxs-lookup"><span data-stu-id="98055-146">Stretch</span></span>
- <span data-ttu-id="98055-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="98055-147">GeneralPurpose</span></span>
- <span data-ttu-id="98055-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="98055-148">BusinessCritical</span></span>

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

### <span data-ttu-id="98055-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="98055-149">-ElasticPoolName</span></span>
<span data-ttu-id="98055-150">指定要在其中移動資料庫的彈性池名稱。</span><span class="sxs-lookup"><span data-stu-id="98055-150">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="98055-151">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="98055-151">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="98055-152">與資料庫相關聯的唯讀次要副本數目。</span><span class="sxs-lookup"><span data-stu-id="98055-152">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="98055-153">僅適用于 Hyperscale 版本。</span><span class="sxs-lookup"><span data-stu-id="98055-153">For Hyperscale edition only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98055-154">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="98055-154">-LicenseType</span></span>
<span data-ttu-id="98055-155">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="98055-155">The license type for the Azure Sql database.</span></span> <span data-ttu-id="98055-156">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="98055-156">Possible values are:</span></span>
- <span data-ttu-id="98055-157">BasePrice-Azure 混合式福利 () AHB 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="98055-157">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="98055-158">現有 SQL Server 授權擁有者的資料庫價格將會打折。</span><span class="sxs-lookup"><span data-stu-id="98055-158">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="98055-159">LicenseIncluded-Azure 混合式福利 () AHB 不會套用現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="98055-159">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="98055-160">資料庫價格將包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="98055-160">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="98055-161">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="98055-161">-MaxSizeBytes</span></span>
<span data-ttu-id="98055-162">Azure SQL 資料庫的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="98055-162">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="98055-163">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="98055-163">-MinimumCapacity</span></span>
<span data-ttu-id="98055-164">資料庫始終已配置的最小產能（如果沒有暫停的話）。</span><span class="sxs-lookup"><span data-stu-id="98055-164">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="98055-165">僅限無伺服器的 Azure Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="98055-165">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98055-166">-NewName</span><span class="sxs-lookup"><span data-stu-id="98055-166">-NewName</span></span>
<span data-ttu-id="98055-167">重新命名資料庫的新名稱。</span><span class="sxs-lookup"><span data-stu-id="98055-167">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="98055-168">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="98055-168">-ReadScale</span></span>
<span data-ttu-id="98055-169">如果已啟用，則在其連線字串中將應用程式意向設定為 readonly 的連線，可能會路由到 readonly 次要複本。</span><span class="sxs-lookup"><span data-stu-id="98055-169">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="98055-170">這個屬性僅適用于 Premium 和商務重要的資料庫。</span><span class="sxs-lookup"><span data-stu-id="98055-170">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="98055-171">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="98055-171">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="98055-172">指定要指派給資料庫之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="98055-172">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="98055-173">如需服務目標的相關資訊，請參閱 Microsoft 開發人員網路文件庫中的 [AZURE SQL 資料庫服務層級和效能層級](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) 。</span><span class="sxs-lookup"><span data-stu-id="98055-173">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="98055-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98055-174">-ResourceGroupName</span></span>
<span data-ttu-id="98055-175">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="98055-175">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="98055-176">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="98055-176">-SecondaryType</span></span>
<span data-ttu-id="98055-177">如果資料庫是副，則為資料庫的次要類型。</span><span class="sxs-lookup"><span data-stu-id="98055-177">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="98055-178">有效值為 Geo 且命名。</span><span class="sxs-lookup"><span data-stu-id="98055-178">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98055-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="98055-179">-ServerName</span></span>
<span data-ttu-id="98055-180">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="98055-180">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="98055-181">-標記</span><span class="sxs-lookup"><span data-stu-id="98055-181">-Tags</span></span>
<span data-ttu-id="98055-182">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="98055-182">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="98055-183">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="98055-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="98055-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="98055-184">-VCore</span></span>
<span data-ttu-id="98055-185">Azure Sql 資料庫的 Vcore 號碼</span><span class="sxs-lookup"><span data-stu-id="98055-185">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="98055-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="98055-186">-ZoneRedundant</span></span>
<span data-ttu-id="98055-187">要與 Azure Sql 資料庫建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="98055-187">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="98055-188">-確認</span><span class="sxs-lookup"><span data-stu-id="98055-188">-Confirm</span></span>
<span data-ttu-id="98055-189">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98055-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98055-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98055-190">-WhatIf</span></span>
<span data-ttu-id="98055-191">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98055-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98055-192">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98055-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98055-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98055-193">CommonParameters</span></span>
<span data-ttu-id="98055-194">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98055-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98055-195">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="98055-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98055-196">輸入</span><span class="sxs-lookup"><span data-stu-id="98055-196">INPUTS</span></span>

### <span data-ttu-id="98055-197">System.object</span><span class="sxs-lookup"><span data-stu-id="98055-197">System.String</span></span>

## <span data-ttu-id="98055-198">輸出</span><span class="sxs-lookup"><span data-stu-id="98055-198">OUTPUTS</span></span>

### <span data-ttu-id="98055-199">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="98055-199">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="98055-200">筆記</span><span class="sxs-lookup"><span data-stu-id="98055-200">NOTES</span></span>

## <span data-ttu-id="98055-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="98055-201">RELATED LINKS</span></span>

[<span data-ttu-id="98055-202">AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="98055-202">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="98055-203">新-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="98055-203">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="98055-204">移除-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="98055-204">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="98055-205">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="98055-205">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="98055-206">暫停-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="98055-206">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="98055-207">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="98055-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
