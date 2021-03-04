---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: c4ccb57292fd4abc2c9b6fd14c5e4492047a2e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903070"
---
# <span data-ttu-id="edde1-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="edde1-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="edde1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="edde1-102">SYNOPSIS</span></span>
<span data-ttu-id="edde1-103">建立資料庫或彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="edde1-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="edde1-104">語法</span><span class="sxs-lookup"><span data-stu-id="edde1-104">SYNTAX</span></span>

### <span data-ttu-id="edde1-105">DtuBasedDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="edde1-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edde1-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="edde1-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edde1-107">描述</span><span class="sxs-lookup"><span data-stu-id="edde1-107">DESCRIPTION</span></span>
<span data-ttu-id="edde1-108">**New-AzSqlDatabase** Cmdlet 會建立 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="edde1-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="edde1-109">您也可以將 *PoolPoolName* 參數設定為現有的彈性資料庫，以建立彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="edde1-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="edde1-110">例子</span><span class="sxs-lookup"><span data-stu-id="edde1-110">EXAMPLES</span></span>

### <span data-ttu-id="edde1-111">範例 1：在指定的伺服器上建立資料庫</span><span class="sxs-lookup"><span data-stu-id="edde1-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="edde1-112">此命令會在伺服器上建立名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="edde1-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="edde1-113">範例 2：在指定的伺服器上建立彈性資料庫</span><span class="sxs-lookup"><span data-stu-id="edde1-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="edde1-114">此命令在 Server Server01 上名為Pool01 的壓縮資料庫資料庫中，建立名為 Database02 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="edde1-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="edde1-115">範例 3：在指定的伺服器上建立 Vcore 資料庫</span><span class="sxs-lookup"><span data-stu-id="edde1-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="edde1-116">此命令會在伺服器上建立名為 Database03 的 Vcore 資料庫。</span><span class="sxs-lookup"><span data-stu-id="edde1-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="edde1-117">範例 4：在指定的伺服器上建立無伺服器資料庫</span><span class="sxs-lookup"><span data-stu-id="edde1-117">Example 4: Create an Serverless database on the specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database04" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen5" -ComputeModel Serverless
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database04
Location                      : Central US
DatabaseId                    : ef5a9698-012c-4def-8d94-7f6bfb7b4f04
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 34359738368
Status                        : Online
CreationDate                  : 4/12/2019 11:20:29 PM
CurrentServiceObjectiveName   : GP_S_Gen5_2
RequestedServiceObjectiveName : GP_S_Gen5_2
ElasticPoolName               :
EarliestRestoreDate           : 4/12/2019 11:50:29 PM
Tags                          :
CreateMode                    :
ReadScale                     : Disabled
ZoneRedundant                 : False
Capacity                      : 2
Family                        : Gen5
SkuName                       : GP_S_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       : 360
MinimumCapacity          : 0.5
```

<span data-ttu-id="edde1-118">此命令會在伺服器上建立名為 Database04 的無伺服器資料庫。</span><span class="sxs-lookup"><span data-stu-id="edde1-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="edde1-119">參數</span><span class="sxs-lookup"><span data-stu-id="edde1-119">PARAMETERS</span></span>

### <span data-ttu-id="edde1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edde1-120">-AsJob</span></span>
<span data-ttu-id="edde1-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="edde1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edde1-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="edde1-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="edde1-123">資料庫的自動暫停延遲以分鐘 (伺服器，) ，-1 才能退出宣告</span><span class="sxs-lookup"><span data-stu-id="edde1-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="edde1-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="edde1-125">用來儲存 SQL Database 備份的備份儲存空間。</span><span class="sxs-lookup"><span data-stu-id="edde1-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="edde1-126">選項為：本地、區域及地理位置。</span><span class="sxs-lookup"><span data-stu-id="edde1-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="edde1-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="edde1-127">-CatalogCollation</span></span>
<span data-ttu-id="edde1-128">指定 SQL 資料庫目錄排序規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="edde1-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="edde1-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="edde1-129">-CollationName</span></span>
<span data-ttu-id="edde1-130">指定 SQL 資料庫排序規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="edde1-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="edde1-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="edde1-131">-ComputeGeneration</span></span>
<span data-ttu-id="edde1-132">這是要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="edde1-132">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="edde1-133">-ComputeModel</span></span>
<span data-ttu-id="edde1-134">Azure Sql 資料庫的計算模型。</span><span class="sxs-lookup"><span data-stu-id="edde1-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="edde1-135">無伺服器或已置備</span><span class="sxs-lookup"><span data-stu-id="edde1-135">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="edde1-136">-DatabaseName</span></span>
<span data-ttu-id="edde1-137">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="edde1-137">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edde1-138">-DefaultProfile</span></span>
<span data-ttu-id="edde1-139">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="edde1-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edde1-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="edde1-140">-Edition</span></span>
<span data-ttu-id="edde1-141">指定要指派給資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="edde1-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="edde1-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="edde1-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="edde1-143">沒有</span><span class="sxs-lookup"><span data-stu-id="edde1-143">None</span></span>
- <span data-ttu-id="edde1-144">基本</span><span class="sxs-lookup"><span data-stu-id="edde1-144">Basic</span></span>
- <span data-ttu-id="edde1-145">標準</span><span class="sxs-lookup"><span data-stu-id="edde1-145">Standard</span></span>
- <span data-ttu-id="edde1-146">溢價</span><span class="sxs-lookup"><span data-stu-id="edde1-146">Premium</span></span>
- <span data-ttu-id="edde1-147">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="edde1-147">DataWarehouse</span></span>
- <span data-ttu-id="edde1-148">自由</span><span class="sxs-lookup"><span data-stu-id="edde1-148">Free</span></span>
- <span data-ttu-id="edde1-149">伸展</span><span class="sxs-lookup"><span data-stu-id="edde1-149">Stretch</span></span>
- <span data-ttu-id="edde1-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="edde1-150">GeneralPurpose</span></span>
- <span data-ttu-id="edde1-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="edde1-151">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-152">-PoolPoolName</span><span class="sxs-lookup"><span data-stu-id="edde1-152">-ElasticPoolName</span></span>
<span data-ttu-id="edde1-153">指定要放入資料庫的集中資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="edde1-153">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-154">-強制</span><span class="sxs-lookup"><span data-stu-id="edde1-154">-Force</span></span>
<span data-ttu-id="edde1-155">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="edde1-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="edde1-156">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="edde1-156">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="edde1-157">與資料庫相關聯的唯讀次要複本數，可路由至唯讀應用程式意圖連結。</span><span class="sxs-lookup"><span data-stu-id="edde1-157">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="edde1-158">此屬性僅適用于 Hyperscale 版本資料庫的設定表。</span><span class="sxs-lookup"><span data-stu-id="edde1-158">This property is only settable for Hyperscale edition databases.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="edde1-159">-LicenseType</span></span>
<span data-ttu-id="edde1-160">Azure Sql 資料庫授權類型。</span><span class="sxs-lookup"><span data-stu-id="edde1-160">The license type for the Azure Sql database.</span></span> <span data-ttu-id="edde1-161">可能的值有：</span><span class="sxs-lookup"><span data-stu-id="edde1-161">Possible values are:</span></span>
- <span data-ttu-id="edde1-162">BasePrice - Azure 混合式權益 (AHB) 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="edde1-162">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="edde1-163">現有 SQL Server 授權擁有者將折扣資料庫價格。</span><span class="sxs-lookup"><span data-stu-id="edde1-163">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="edde1-164">LicenseIncluded - Azure 混合式權益 (AHB) 現有 SQL Server 授權擁有者的折扣價格不會適用。</span><span class="sxs-lookup"><span data-stu-id="edde1-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="edde1-165">資料庫價格會包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="edde1-165">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="edde1-166">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="edde1-166">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="edde1-167">SQL 資料庫的維護組組識別碼。</span><span class="sxs-lookup"><span data-stu-id="edde1-167">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="edde1-168">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="edde1-168">-MaxSizeBytes</span></span>
<span data-ttu-id="edde1-169">指定資料庫的大小上限 ，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="edde1-169">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-170">-Minimum一級</span><span class="sxs-lookup"><span data-stu-id="edde1-170">-MinimumCapacity</span></span>
<span data-ttu-id="edde1-171">資料庫一定會配置最小容量 ，如果未暫停。</span><span class="sxs-lookup"><span data-stu-id="edde1-171">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="edde1-172">僅適用于無伺服器 Azure Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="edde1-172">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="edde1-173">-ReadScale</span></span>
<span data-ttu-id="edde1-174">如果啟用，將應用程式意圖設定為在連接字串中以唯讀方式執行的連接，可能會路由至唯讀次要複本。</span><span class="sxs-lookup"><span data-stu-id="edde1-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="edde1-175">此屬性僅適用于 Premium 和 Business Critical 資料庫的設定表。</span><span class="sxs-lookup"><span data-stu-id="edde1-175">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="edde1-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="edde1-177">指定要指派給資料庫的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="edde1-177">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edde1-178">-ResourceGroupName</span></span>
<span data-ttu-id="edde1-179">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="edde1-179">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="edde1-180">-SampleName</span><span class="sxs-lookup"><span data-stu-id="edde1-180">-SampleName</span></span>
<span data-ttu-id="edde1-181">建立此資料庫時要申請的範例架構名稱。</span><span class="sxs-lookup"><span data-stu-id="edde1-181">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-182">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="edde1-182">-SecondaryType</span></span>
<span data-ttu-id="edde1-183">資料庫的次要類型如果為次要類型。</span><span class="sxs-lookup"><span data-stu-id="edde1-183">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="edde1-184">有效的值為地理位置和命名。</span><span class="sxs-lookup"><span data-stu-id="edde1-184">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="edde1-185">-ServerName</span><span class="sxs-lookup"><span data-stu-id="edde1-185">-ServerName</span></span>
<span data-ttu-id="edde1-186">指定主資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="edde1-186">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="edde1-187">-標記</span><span class="sxs-lookup"><span data-stu-id="edde1-187">-Tags</span></span>
<span data-ttu-id="edde1-188">指定此 Cmdlet 與新資料庫關聯之雜湊資料表形式的索引鍵值組字典。</span><span class="sxs-lookup"><span data-stu-id="edde1-188">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="edde1-189">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="edde1-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-190">-VCore</span><span class="sxs-lookup"><span data-stu-id="edde1-190">-VCore</span></span>
<span data-ttu-id="edde1-191">Azure Sql 資料庫的 Vcore 數位</span><span class="sxs-lookup"><span data-stu-id="edde1-191">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde1-192">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="edde1-192">-ZoneRedundant</span></span>
<span data-ttu-id="edde1-193">與 Azure Sql Database 建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="edde1-193">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="edde1-194">-確認</span><span class="sxs-lookup"><span data-stu-id="edde1-194">-Confirm</span></span>
<span data-ttu-id="edde1-195">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="edde1-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edde1-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edde1-196">-WhatIf</span></span>
<span data-ttu-id="edde1-197">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="edde1-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edde1-198">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="edde1-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edde1-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edde1-199">CommonParameters</span></span>
<span data-ttu-id="edde1-200">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="edde1-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edde1-201">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edde1-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edde1-202">輸入</span><span class="sxs-lookup"><span data-stu-id="edde1-202">INPUTS</span></span>

### <span data-ttu-id="edde1-203">System.String</span><span class="sxs-lookup"><span data-stu-id="edde1-203">System.String</span></span>

## <span data-ttu-id="edde1-204">輸出</span><span class="sxs-lookup"><span data-stu-id="edde1-204">OUTPUTS</span></span>

### <span data-ttu-id="edde1-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="edde1-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="edde1-206">筆記</span><span class="sxs-lookup"><span data-stu-id="edde1-206">NOTES</span></span>

## <span data-ttu-id="edde1-207">相關連結</span><span class="sxs-lookup"><span data-stu-id="edde1-207">RELATED LINKS</span></span>

[<span data-ttu-id="edde1-208">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="edde1-208">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="edde1-209">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="edde1-209">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="edde1-210">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="edde1-210">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="edde1-211">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="edde1-211">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="edde1-212">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="edde1-212">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="edde1-213">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="edde1-213">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="edde1-214">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="edde1-214">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="edde1-215">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="edde1-215">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

