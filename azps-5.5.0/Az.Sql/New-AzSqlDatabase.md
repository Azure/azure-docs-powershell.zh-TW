---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 57af759caa940686d69118157973eb01c9a6928e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137071"
---
# <span data-ttu-id="46a60-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46a60-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="46a60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46a60-102">SYNOPSIS</span></span>
<span data-ttu-id="46a60-103">建立資料庫或彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="46a60-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="46a60-104">句法</span><span class="sxs-lookup"><span data-stu-id="46a60-104">SYNTAX</span></span>

### <span data-ttu-id="46a60-105">DtuBasedDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="46a60-105">DtuBasedDatabase (Default)</span></span>
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

### <span data-ttu-id="46a60-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="46a60-106">VcoreBasedDatabase</span></span>
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

## <span data-ttu-id="46a60-107">說明</span><span class="sxs-lookup"><span data-stu-id="46a60-107">DESCRIPTION</span></span>
<span data-ttu-id="46a60-108">**新的-AzSqlDatabase** Cmdlet 會建立 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="46a60-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="46a60-109">您也可以將 *ElasticPoolName* 參數設定為現有彈性池，以建立彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="46a60-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="46a60-110">示例</span><span class="sxs-lookup"><span data-stu-id="46a60-110">EXAMPLES</span></span>

### <span data-ttu-id="46a60-111">範例1：在指定的伺服器上建立資料庫</span><span class="sxs-lookup"><span data-stu-id="46a60-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="46a60-112">這個命令會在伺服器 Server01 上建立名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="46a60-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="46a60-113">範例2：在指定的伺服器上建立彈性資料庫</span><span class="sxs-lookup"><span data-stu-id="46a60-113">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="46a60-114">這個命令會在伺服器 Server01 上名為 ElasticPool01 的彈性池中建立名為 Database02 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="46a60-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="46a60-115">範例3：在指定的伺服器上建立 Vcore 資料庫</span><span class="sxs-lookup"><span data-stu-id="46a60-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="46a60-116">這個命令會在伺服器 Server01 上建立名為 Database03 的 Vcore 資料庫。</span><span class="sxs-lookup"><span data-stu-id="46a60-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="46a60-117">範例4：在指定的伺服器上建立無伺服器資料庫</span><span class="sxs-lookup"><span data-stu-id="46a60-117">Example 4: Create an Serverless database on the specified server</span></span>
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

<span data-ttu-id="46a60-118">這個命令會在伺服器 Server01 上建立一個名為 Database04 的無伺服器資料庫。</span><span class="sxs-lookup"><span data-stu-id="46a60-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="46a60-119">參數</span><span class="sxs-lookup"><span data-stu-id="46a60-119">PARAMETERS</span></span>

### <span data-ttu-id="46a60-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46a60-120">-AsJob</span></span>
<span data-ttu-id="46a60-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46a60-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46a60-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="46a60-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="46a60-123">僅限資料庫 (無伺服器的自動暫停延遲時間) ，-1 以退出宣告</span><span class="sxs-lookup"><span data-stu-id="46a60-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="46a60-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="46a60-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="46a60-125">儲存 SQL 資料庫備份所用的備份儲存空間冗余。</span><span class="sxs-lookup"><span data-stu-id="46a60-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="46a60-126">選項包括： Local、Zone 和 Geo。</span><span class="sxs-lookup"><span data-stu-id="46a60-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="46a60-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="46a60-127">-CatalogCollation</span></span>
<span data-ttu-id="46a60-128">指定 SQL 資料庫編目排序規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="46a60-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="46a60-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="46a60-129">-CollationName</span></span>
<span data-ttu-id="46a60-130">指定 SQL 資料庫排序規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="46a60-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="46a60-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="46a60-131">-ComputeGeneration</span></span>
<span data-ttu-id="46a60-132">要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="46a60-132">The compute generation to assign.</span></span>

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

### <span data-ttu-id="46a60-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="46a60-133">-ComputeModel</span></span>
<span data-ttu-id="46a60-134">Azure Sql 資料庫的計算模型。</span><span class="sxs-lookup"><span data-stu-id="46a60-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="46a60-135">無伺服器或已預配</span><span class="sxs-lookup"><span data-stu-id="46a60-135">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="46a60-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="46a60-136">-DatabaseName</span></span>
<span data-ttu-id="46a60-137">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="46a60-137">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="46a60-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a60-138">-DefaultProfile</span></span>
<span data-ttu-id="46a60-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="46a60-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46a60-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="46a60-140">-Edition</span></span>
<span data-ttu-id="46a60-141">指定要指派給資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="46a60-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="46a60-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="46a60-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46a60-143">所有</span><span class="sxs-lookup"><span data-stu-id="46a60-143">None</span></span>
- <span data-ttu-id="46a60-144">空白</span><span class="sxs-lookup"><span data-stu-id="46a60-144">Basic</span></span>
- <span data-ttu-id="46a60-145">標準</span><span class="sxs-lookup"><span data-stu-id="46a60-145">Standard</span></span>
- <span data-ttu-id="46a60-146">佳</span><span class="sxs-lookup"><span data-stu-id="46a60-146">Premium</span></span>
- <span data-ttu-id="46a60-147">倉庫</span><span class="sxs-lookup"><span data-stu-id="46a60-147">DataWarehouse</span></span>
- <span data-ttu-id="46a60-148">空閒</span><span class="sxs-lookup"><span data-stu-id="46a60-148">Free</span></span>
- <span data-ttu-id="46a60-149">伸縮</span><span class="sxs-lookup"><span data-stu-id="46a60-149">Stretch</span></span>
- <span data-ttu-id="46a60-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="46a60-150">GeneralPurpose</span></span>
- <span data-ttu-id="46a60-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="46a60-151">BusinessCritical</span></span>

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

### <span data-ttu-id="46a60-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="46a60-152">-ElasticPoolName</span></span>
<span data-ttu-id="46a60-153">指定要放入資料庫之彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="46a60-153">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="46a60-154">-Force</span><span class="sxs-lookup"><span data-stu-id="46a60-154">-Force</span></span>
<span data-ttu-id="46a60-155">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="46a60-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="46a60-156">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="46a60-156">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="46a60-157">與資料庫相關聯的唯讀次要副本數目，可路由至唯讀應用程式意圖連接。</span><span class="sxs-lookup"><span data-stu-id="46a60-157">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="46a60-158">這個屬性只能在 Hyperscale edition 資料庫中設定。</span><span class="sxs-lookup"><span data-stu-id="46a60-158">This property is only settable for Hyperscale edition databases.</span></span>

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

### <span data-ttu-id="46a60-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="46a60-159">-LicenseType</span></span>
<span data-ttu-id="46a60-160">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="46a60-160">The license type for the Azure Sql database.</span></span> <span data-ttu-id="46a60-161">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="46a60-161">Possible values are:</span></span>
- <span data-ttu-id="46a60-162">BasePrice-Azure 混合式福利 () AHB 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="46a60-162">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="46a60-163">現有 SQL Server 授權擁有者的資料庫價格將會打折。</span><span class="sxs-lookup"><span data-stu-id="46a60-163">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="46a60-164">LicenseIncluded-Azure 混合式福利 () AHB 不會套用現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="46a60-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="46a60-165">資料庫價格將包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="46a60-165">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="46a60-166">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="46a60-166">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="46a60-167">SQL 資料庫的維護配置識別碼。</span><span class="sxs-lookup"><span data-stu-id="46a60-167">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="46a60-168">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="46a60-168">-MaxSizeBytes</span></span>
<span data-ttu-id="46a60-169">指定資料庫的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="46a60-169">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="46a60-170">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="46a60-170">-MinimumCapacity</span></span>
<span data-ttu-id="46a60-171">資料庫始終已配置的最小產能（如果沒有暫停的話）。</span><span class="sxs-lookup"><span data-stu-id="46a60-171">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="46a60-172">僅限無伺服器的 Azure Sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="46a60-172">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="46a60-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="46a60-173">-ReadScale</span></span>
<span data-ttu-id="46a60-174">如果已啟用，則在其連線字串中將應用程式意向設定為 readonly 的連線，可能會路由到 readonly 次要複本。</span><span class="sxs-lookup"><span data-stu-id="46a60-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="46a60-175">這個屬性僅適用于 Premium 和商務重要的資料庫。</span><span class="sxs-lookup"><span data-stu-id="46a60-175">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="46a60-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="46a60-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="46a60-177">指定要指派給資料庫之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="46a60-177">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="46a60-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a60-178">-ResourceGroupName</span></span>
<span data-ttu-id="46a60-179">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="46a60-179">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="46a60-180">-SampleName</span><span class="sxs-lookup"><span data-stu-id="46a60-180">-SampleName</span></span>
<span data-ttu-id="46a60-181">建立此資料庫時要套用之範例架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="46a60-181">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="46a60-182">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="46a60-182">-SecondaryType</span></span>
<span data-ttu-id="46a60-183">如果資料庫是副，則為資料庫的次要類型。</span><span class="sxs-lookup"><span data-stu-id="46a60-183">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="46a60-184">有效值為 Geo 且命名。</span><span class="sxs-lookup"><span data-stu-id="46a60-184">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="46a60-185">-ServerName</span><span class="sxs-lookup"><span data-stu-id="46a60-185">-ServerName</span></span>
<span data-ttu-id="46a60-186">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="46a60-186">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="46a60-187">-標記</span><span class="sxs-lookup"><span data-stu-id="46a60-187">-Tags</span></span>
<span data-ttu-id="46a60-188">以這個 Cmdlet 所關聯的雜湊資料表形式，指定鍵值對的字典。</span><span class="sxs-lookup"><span data-stu-id="46a60-188">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="46a60-189">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="46a60-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="46a60-190">-VCore</span><span class="sxs-lookup"><span data-stu-id="46a60-190">-VCore</span></span>
<span data-ttu-id="46a60-191">Azure Sql 資料庫的 Vcore 號碼</span><span class="sxs-lookup"><span data-stu-id="46a60-191">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="46a60-192">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="46a60-192">-ZoneRedundant</span></span>
<span data-ttu-id="46a60-193">要與 Azure Sql 資料庫建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="46a60-193">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="46a60-194">-確認</span><span class="sxs-lookup"><span data-stu-id="46a60-194">-Confirm</span></span>
<span data-ttu-id="46a60-195">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46a60-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a60-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a60-196">-WhatIf</span></span>
<span data-ttu-id="46a60-197">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46a60-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46a60-198">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46a60-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a60-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a60-199">CommonParameters</span></span>
<span data-ttu-id="46a60-200">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46a60-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a60-201">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="46a60-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a60-202">輸入</span><span class="sxs-lookup"><span data-stu-id="46a60-202">INPUTS</span></span>

### <span data-ttu-id="46a60-203">System.object</span><span class="sxs-lookup"><span data-stu-id="46a60-203">System.String</span></span>

## <span data-ttu-id="46a60-204">輸出</span><span class="sxs-lookup"><span data-stu-id="46a60-204">OUTPUTS</span></span>

### <span data-ttu-id="46a60-205">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="46a60-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="46a60-206">筆記</span><span class="sxs-lookup"><span data-stu-id="46a60-206">NOTES</span></span>

## <span data-ttu-id="46a60-207">相關連結</span><span class="sxs-lookup"><span data-stu-id="46a60-207">RELATED LINKS</span></span>

[<span data-ttu-id="46a60-208">AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46a60-208">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="46a60-209">新-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46a60-209">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="46a60-210">新-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="46a60-210">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="46a60-211">移除-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46a60-211">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="46a60-212">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46a60-212">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="46a60-213">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46a60-213">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="46a60-214">暫停-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46a60-214">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="46a60-215">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="46a60-215">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

