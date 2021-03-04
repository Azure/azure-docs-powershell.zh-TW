---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 17e6c492828f877ebf53c634a7670e8d60c9ccba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913061"
---
# <span data-ttu-id="59bfb-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="59bfb-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="59bfb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="59bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="59bfb-103">設定資料庫的屬性，或將現有的資料庫移至集區。</span><span class="sxs-lookup"><span data-stu-id="59bfb-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="59bfb-104">語法</span><span class="sxs-lookup"><span data-stu-id="59bfb-104">SYNTAX</span></span>

### <span data-ttu-id="59bfb-105">更新 (預設) </span><span class="sxs-lookup"><span data-stu-id="59bfb-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59bfb-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="59bfb-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59bfb-107">重 命名</span><span class="sxs-lookup"><span data-stu-id="59bfb-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59bfb-108">描述</span><span class="sxs-lookup"><span data-stu-id="59bfb-108">DESCRIPTION</span></span>
<span data-ttu-id="59bfb-109">**Set-AzSqlDatabase** Cmdlet 會為 Azure SQL Database 中的資料庫設定屬性。</span><span class="sxs-lookup"><span data-stu-id="59bfb-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="59bfb-110">此 Cmdlet 可以修改適用于資料庫的服務層級 (*Edition*) 、 (*RequestedServiceObjectiveName*) ，以及儲存空間大小 (*MaxSizeBytes*) 。</span><span class="sxs-lookup"><span data-stu-id="59bfb-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="59bfb-111">此外，您可以指定 *一個PoolPoolName* 參數，將資料庫移到一個壓縮資料庫。</span><span class="sxs-lookup"><span data-stu-id="59bfb-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="59bfb-112">如果資料庫已經在資料庫資料庫的資料庫中，您可以使用 *RequestedServiceObjectiveName* 參數，將資料庫從集中式資料庫移出，並移至單一資料庫的績效等級。</span><span class="sxs-lookup"><span data-stu-id="59bfb-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="59bfb-113">例子</span><span class="sxs-lookup"><span data-stu-id="59bfb-113">EXAMPLES</span></span>

### <span data-ttu-id="59bfb-114">範例 1：將資料庫更新為 Standard S0 資料庫</span><span class="sxs-lookup"><span data-stu-id="59bfb-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="59bfb-115">此命令會更新名為 Database01 的資料庫至伺服器名為 Server01 的標準 S0 資料庫。</span><span class="sxs-lookup"><span data-stu-id="59bfb-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="59bfb-116">範例 2：新增資料庫至資料庫資料庫</span><span class="sxs-lookup"><span data-stu-id="59bfb-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="59bfb-117">此命令會將名為 Database01 的資料庫新加到位於伺服器名為 Server01 的一個名為Pool01 的集中資料庫。</span><span class="sxs-lookup"><span data-stu-id="59bfb-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="59bfb-118">範例 3：修改資料庫的儲存空間最大值</span><span class="sxs-lookup"><span data-stu-id="59bfb-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="59bfb-119">此命令會更新名為 Database01 的資料庫，以將資料庫的最大大小設為 1 TB。</span><span class="sxs-lookup"><span data-stu-id="59bfb-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

### <span data-ttu-id="59bfb-120">範例 4：將現有的一般用途資料庫更新為超大規模服務層級</span><span class="sxs-lookup"><span data-stu-id="59bfb-120">Example 4: Update a existing General Purpose database to Hyperscale service tier</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Hyperscale" -RequestedServiceObjectiveName "HS_Gen5_2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : 56246136-839f-4171-80af-4c28142463b1
Edition                       : Hyperscale
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : -1
Status                        : Online
CreationDate                  : 12/6/2020 5:34:16 PM
CurrentServiceObjectiveId     : 00000000-0000-0000-0000-000000000000
CurrentServiceObjectiveName   : HS_Gen5_2
RequestedServiceObjectiveName : HS_Gen5_2
RequestedServiceObjectiveId   :
ElasticPoolName               :
EarliestRestoreDate           : 12/6/2020 5:34:16 PM
Tags                          : {}
ResourceId                    : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/Server01/databases/Database01
CreateMode                    :
ReadScale                     : Enabled
ZoneRedundant                 :
Capacity                      : 2
Family                        : Gen5
SkuName                       : HS_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       :
MinimumCapacity               :
ReadReplicaCount              : 1
BackupStorageRedundancy       : Geo
```

<span data-ttu-id="59bfb-121">此命令會更新名為 Database01 的資料庫，從一般用途更新為超大規模服務層級。</span><span class="sxs-lookup"><span data-stu-id="59bfb-121">This command updates a database named Database01 from General Purpose to Hyperscale service tier.</span></span>

## <span data-ttu-id="59bfb-122">參數</span><span class="sxs-lookup"><span data-stu-id="59bfb-122">PARAMETERS</span></span>

### <span data-ttu-id="59bfb-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59bfb-123">-AsJob</span></span>
<span data-ttu-id="59bfb-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="59bfb-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59bfb-125">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="59bfb-125">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="59bfb-126">資料庫的自動暫停延遲以分鐘 (伺服器，) ，-1 才能退出宣告</span><span class="sxs-lookup"><span data-stu-id="59bfb-126">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="59bfb-127">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="59bfb-127">-BackupStorageRedundancy</span></span>
<span data-ttu-id="59bfb-128">用來儲存 SQL Database 備份的備份儲存空間。</span><span class="sxs-lookup"><span data-stu-id="59bfb-128">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="59bfb-129">選項為：本地、區域及地理位置。</span><span class="sxs-lookup"><span data-stu-id="59bfb-129">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="59bfb-130">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="59bfb-130">-ComputeGeneration</span></span>
<span data-ttu-id="59bfb-131">這是要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="59bfb-131">The compute generation to assign.</span></span>

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

### <span data-ttu-id="59bfb-132">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="59bfb-132">-ComputeModel</span></span>
<span data-ttu-id="59bfb-133">Azure Sql 資料庫的計算模型。</span><span class="sxs-lookup"><span data-stu-id="59bfb-133">Computed model of Azure Sql database.</span></span> <span data-ttu-id="59bfb-134">無伺服器或已置備</span><span class="sxs-lookup"><span data-stu-id="59bfb-134">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="59bfb-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59bfb-135">-DatabaseName</span></span>
<span data-ttu-id="59bfb-136">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="59bfb-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="59bfb-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59bfb-137">-DefaultProfile</span></span>
<span data-ttu-id="59bfb-138">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="59bfb-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59bfb-139">-Edition</span><span class="sxs-lookup"><span data-stu-id="59bfb-139">-Edition</span></span>
<span data-ttu-id="59bfb-140">指定資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="59bfb-140">Specifies the edition for the database.</span></span>
<span data-ttu-id="59bfb-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="59bfb-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59bfb-142">沒有</span><span class="sxs-lookup"><span data-stu-id="59bfb-142">None</span></span>
- <span data-ttu-id="59bfb-143">基本</span><span class="sxs-lookup"><span data-stu-id="59bfb-143">Basic</span></span>
- <span data-ttu-id="59bfb-144">標準</span><span class="sxs-lookup"><span data-stu-id="59bfb-144">Standard</span></span>
- <span data-ttu-id="59bfb-145">溢價</span><span class="sxs-lookup"><span data-stu-id="59bfb-145">Premium</span></span>
- <span data-ttu-id="59bfb-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="59bfb-146">DataWarehouse</span></span>
- <span data-ttu-id="59bfb-147">自由</span><span class="sxs-lookup"><span data-stu-id="59bfb-147">Free</span></span>
- <span data-ttu-id="59bfb-148">伸展</span><span class="sxs-lookup"><span data-stu-id="59bfb-148">Stretch</span></span>
- <span data-ttu-id="59bfb-149">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="59bfb-149">GeneralPurpose</span></span>
- <span data-ttu-id="59bfb-150">超縮放</span><span class="sxs-lookup"><span data-stu-id="59bfb-150">Hyperscale</span></span>
- <span data-ttu-id="59bfb-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="59bfb-151">BusinessCritical</span></span>

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

### <span data-ttu-id="59bfb-152">-PoolPoolName</span><span class="sxs-lookup"><span data-stu-id="59bfb-152">-ElasticPoolName</span></span>
<span data-ttu-id="59bfb-153">指定要移動資料庫的集中資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="59bfb-153">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="59bfb-154">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="59bfb-154">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="59bfb-155">與資料庫相關聯的唯讀次要複本數目。</span><span class="sxs-lookup"><span data-stu-id="59bfb-155">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="59bfb-156">僅適用于超大規模版本。</span><span class="sxs-lookup"><span data-stu-id="59bfb-156">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="59bfb-157">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="59bfb-157">-LicenseType</span></span>
<span data-ttu-id="59bfb-158">Azure Sql 資料庫授權類型。</span><span class="sxs-lookup"><span data-stu-id="59bfb-158">The license type for the Azure Sql database.</span></span> <span data-ttu-id="59bfb-159">可能的值有：</span><span class="sxs-lookup"><span data-stu-id="59bfb-159">Possible values are:</span></span>
- <span data-ttu-id="59bfb-160">BasePrice - Azure 混合式權益 (AHB) 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="59bfb-160">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="59bfb-161">現有 SQL Server 授權擁有者將折扣資料庫價格。</span><span class="sxs-lookup"><span data-stu-id="59bfb-161">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="59bfb-162">LicenseIncluded - Azure 混合式權益 (AHB) 現有 SQL Server 授權擁有者的折扣價格不會適用。</span><span class="sxs-lookup"><span data-stu-id="59bfb-162">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="59bfb-163">資料庫價格會包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="59bfb-163">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="59bfb-164">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="59bfb-164">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="59bfb-165">SQL 資料庫的維護組組識別碼。</span><span class="sxs-lookup"><span data-stu-id="59bfb-165">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="59bfb-166">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="59bfb-166">-MaxSizeBytes</span></span>
<span data-ttu-id="59bfb-167">Azure SQL Database 的大小上限 ，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="59bfb-167">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="59bfb-168">-Minimum一級</span><span class="sxs-lookup"><span data-stu-id="59bfb-168">-MinimumCapacity</span></span>
<span data-ttu-id="59bfb-169">資料庫一定會配置最小容量 ，如果未暫停。</span><span class="sxs-lookup"><span data-stu-id="59bfb-169">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="59bfb-170">僅適用于無伺服器 Azure Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="59bfb-170">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="59bfb-171">-NewName</span><span class="sxs-lookup"><span data-stu-id="59bfb-171">-NewName</span></span>
<span data-ttu-id="59bfb-172">要重新命名資料庫的新名稱。</span><span class="sxs-lookup"><span data-stu-id="59bfb-172">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="59bfb-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="59bfb-173">-ReadScale</span></span>
<span data-ttu-id="59bfb-174">如果啟用，將應用程式意圖設定為在連接字串中以唯讀方式執行的連接，可能會路由至唯讀次要複本。</span><span class="sxs-lookup"><span data-stu-id="59bfb-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="59bfb-175">此屬性僅適用于 Premium 和 Business Critical 資料庫的設定表。</span><span class="sxs-lookup"><span data-stu-id="59bfb-175">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="59bfb-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="59bfb-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="59bfb-177">指定要指派給資料庫的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="59bfb-177">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="59bfb-178">有關服務目標的資訊，請參閱 Microsoft 開發人員網路庫中 [的 Azure SQL 資料庫](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases) 服務層級和績效等級。</span><span class="sxs-lookup"><span data-stu-id="59bfb-178">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="59bfb-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59bfb-179">-ResourceGroupName</span></span>
<span data-ttu-id="59bfb-180">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="59bfb-180">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="59bfb-181">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="59bfb-181">-SecondaryType</span></span>
<span data-ttu-id="59bfb-182">資料庫的次要類型如果為次要類型。</span><span class="sxs-lookup"><span data-stu-id="59bfb-182">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="59bfb-183">有效的值為地理位置和命名。</span><span class="sxs-lookup"><span data-stu-id="59bfb-183">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="59bfb-184">-ServerName</span><span class="sxs-lookup"><span data-stu-id="59bfb-184">-ServerName</span></span>
<span data-ttu-id="59bfb-185">指定主資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="59bfb-185">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="59bfb-186">-標記</span><span class="sxs-lookup"><span data-stu-id="59bfb-186">-Tags</span></span>
<span data-ttu-id="59bfb-187">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="59bfb-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="59bfb-188">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="59bfb-188">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="59bfb-189">-VCore</span><span class="sxs-lookup"><span data-stu-id="59bfb-189">-VCore</span></span>
<span data-ttu-id="59bfb-190">Azure Sql 資料庫的 Vcore 數位</span><span class="sxs-lookup"><span data-stu-id="59bfb-190">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="59bfb-191">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="59bfb-191">-ZoneRedundant</span></span>
<span data-ttu-id="59bfb-192">與 Azure Sql Database 建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="59bfb-192">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="59bfb-193">-確認</span><span class="sxs-lookup"><span data-stu-id="59bfb-193">-Confirm</span></span>
<span data-ttu-id="59bfb-194">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="59bfb-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59bfb-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59bfb-195">-WhatIf</span></span>
<span data-ttu-id="59bfb-196">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59bfb-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59bfb-197">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59bfb-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59bfb-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bfb-198">CommonParameters</span></span>
<span data-ttu-id="59bfb-199">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="59bfb-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bfb-200">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59bfb-200">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bfb-201">輸入</span><span class="sxs-lookup"><span data-stu-id="59bfb-201">INPUTS</span></span>

### <span data-ttu-id="59bfb-202">System.String</span><span class="sxs-lookup"><span data-stu-id="59bfb-202">System.String</span></span>

## <span data-ttu-id="59bfb-203">輸出</span><span class="sxs-lookup"><span data-stu-id="59bfb-203">OUTPUTS</span></span>

### <span data-ttu-id="59bfb-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="59bfb-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="59bfb-205">筆記</span><span class="sxs-lookup"><span data-stu-id="59bfb-205">NOTES</span></span>

## <span data-ttu-id="59bfb-206">相關連結</span><span class="sxs-lookup"><span data-stu-id="59bfb-206">RELATED LINKS</span></span>

[<span data-ttu-id="59bfb-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="59bfb-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="59bfb-208">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="59bfb-208">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="59bfb-209">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="59bfb-209">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="59bfb-210">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="59bfb-210">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="59bfb-211">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="59bfb-211">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="59bfb-212">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="59bfb-212">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
