---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: d625e28b0007a9dc99434f0257a910ea804e3644
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906474"
---
# <span data-ttu-id="86d43-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="86d43-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="86d43-102">簡介</span><span class="sxs-lookup"><span data-stu-id="86d43-102">SYNOPSIS</span></span>
<span data-ttu-id="86d43-103">建立 SQL 資料庫的彈性資料庫資料庫。</span><span class="sxs-lookup"><span data-stu-id="86d43-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="86d43-104">語法</span><span class="sxs-lookup"><span data-stu-id="86d43-104">SYNTAX</span></span>

### <span data-ttu-id="86d43-105">DtuBasedPool (預設) </span><span class="sxs-lookup"><span data-stu-id="86d43-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86d43-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="86d43-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86d43-107">描述</span><span class="sxs-lookup"><span data-stu-id="86d43-107">DESCRIPTION</span></span>
<span data-ttu-id="86d43-108">**New-AzSqlElasticPool** Cmdlet 為 Azure SQL Database 建立一個彈性資料庫資料庫。</span><span class="sxs-lookup"><span data-stu-id="86d43-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="86d43-109">需要設定 (*-Dtu、-DatabaseDtuMin 和 -DatabaseDtuMax*) 的數個參數，都是來自該參數的有效值清單。</span><span class="sxs-lookup"><span data-stu-id="86d43-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="86d43-110">例如，標準 100 eDTU 集區 -DatabaseDtuMax 只能設定為 10、20、50 或 100。</span><span class="sxs-lookup"><span data-stu-id="86d43-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="86d43-111">有關哪些值有效的詳細資訊，請參閱泳層資料庫內特定大小資料庫 [的表格](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)。</span><span class="sxs-lookup"><span data-stu-id="86d43-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="86d43-112">例子</span><span class="sxs-lookup"><span data-stu-id="86d43-112">EXAMPLES</span></span>

### <span data-ttu-id="86d43-113">範例 1：建立 DTU 資料庫</span><span class="sxs-lookup"><span data-stu-id="86d43-113">Example 1: Create a DTU elastic pool</span></span>

```powershell
PS C:\>New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="86d43-114">此命令在名為Pool01 的標準服務層級中建立一個資料庫化資料庫。</span><span class="sxs-lookup"><span data-stu-id="86d43-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="86d43-115">伺服器名稱為 server01 ，指派給名為 ResourceGroup01 的 Azure 資源群組，主在集中處理資料庫。</span><span class="sxs-lookup"><span data-stu-id="86d43-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="86d43-116">該命令會指定資料庫和資料庫中資料庫的 DTU 屬性值。</span><span class="sxs-lookup"><span data-stu-id="86d43-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="86d43-117">範例 2：建立 vCore 計算資料庫</span><span class="sxs-lookup"><span data-stu-id="86d43-117">Example 2: Create a vCore elastic pool</span></span>

```powershell
PS C:\> New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "GeneralPurpose" -vCore 2 -ComputeGeneration Gen5
ResourceId          : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/server01/elasticPools/ElasticPool01
ResourceGroupName   : ResourceGroup01
ServerName          : Server01
ElasticPoolName     : ElasticPool01
Location            : Central US
CreationDate        : 8/29/2019 2:16:40 AM
State               : Ready
Edition             : GeneralPurpose
SkuName             : GP_Gen5
Dtu                 : 2
DatabaseDtuMax      : 2
DatabaseDtuMin      : 0
Capacity            : 2
DatabaseCapacityMin : 0
DatabaseCapacityMax : 2
Family              : Gen5
MaxSizeBytes        : 34359738368
StorageMB           : 32768
Tags                :
```

<span data-ttu-id="86d43-118">此命令在 GengeralPurpose 服務層級中建立名為Pool01 的彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="86d43-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="86d43-119">伺服器名稱為 server01 ，指派給名為 ResourceGroup01 的 Azure 資源群組，主在集中處理資料庫。</span><span class="sxs-lookup"><span data-stu-id="86d43-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="86d43-120">命令會指定資料庫和資料庫的 vCore 屬性值。</span><span class="sxs-lookup"><span data-stu-id="86d43-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="86d43-121">範例 3</span><span class="sxs-lookup"><span data-stu-id="86d43-121">Example 3</span></span>

<span data-ttu-id="86d43-122">建立 SQL 資料庫的彈性資料庫資料庫。</span><span class="sxs-lookup"><span data-stu-id="86d43-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="86d43-123"> (自動) </span><span class="sxs-lookup"><span data-stu-id="86d43-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="86d43-124">參數</span><span class="sxs-lookup"><span data-stu-id="86d43-124">PARAMETERS</span></span>

### <span data-ttu-id="86d43-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86d43-125">-AsJob</span></span>
<span data-ttu-id="86d43-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="86d43-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86d43-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="86d43-127">-ComputeGeneration</span></span>
<span data-ttu-id="86d43-128">這是要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="86d43-128">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d43-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="86d43-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="86d43-130">指定資料庫中任何單一資料庫 (DTUs) 之資料庫輸送量單位上限。</span><span class="sxs-lookup"><span data-stu-id="86d43-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="86d43-131">不同版本的預設值如下：</span><span class="sxs-lookup"><span data-stu-id="86d43-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="86d43-132">基本。</span><span class="sxs-lookup"><span data-stu-id="86d43-132">Basic.</span></span> <span data-ttu-id="86d43-133">5 個 DTUs</span><span class="sxs-lookup"><span data-stu-id="86d43-133">5 DTUs</span></span>
- <span data-ttu-id="86d43-134">標準。</span><span class="sxs-lookup"><span data-stu-id="86d43-134">Standard.</span></span> <span data-ttu-id="86d43-135">100 個 DTUs</span><span class="sxs-lookup"><span data-stu-id="86d43-135">100 DTUs</span></span>
- <span data-ttu-id="86d43-136">溢價。</span><span class="sxs-lookup"><span data-stu-id="86d43-136">Premium.</span></span> <span data-ttu-id="86d43-137">125 DTUs 有關哪些值有效的詳細資訊，請參閱泳場中特定大小資料庫 [的表格](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="86d43-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d43-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="86d43-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="86d43-139">指定資料庫集中所有資料庫所保證的最小 DTUS 數量。</span><span class="sxs-lookup"><span data-stu-id="86d43-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="86d43-140">預設值為 0 (0) 。</span><span class="sxs-lookup"><span data-stu-id="86d43-140">The default value is zero (0).</span></span>
<span data-ttu-id="86d43-141">有關哪些值有效的詳細資訊，請參閱泳層資料庫內特定大小資料庫 [的表格](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)。</span><span class="sxs-lookup"><span data-stu-id="86d43-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d43-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="86d43-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="86d43-143">任何 SqlAzure 資料庫都可以在資料庫中使用的最大 VCore 數位。</span><span class="sxs-lookup"><span data-stu-id="86d43-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d43-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="86d43-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="86d43-145">任何 SqlAzure 資料庫都可以在資料庫中使用的最小 VCore 數位。</span><span class="sxs-lookup"><span data-stu-id="86d43-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d43-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d43-146">-DefaultProfile</span></span>
<span data-ttu-id="86d43-147">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="86d43-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86d43-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="86d43-148">-Dtu</span></span>
<span data-ttu-id="86d43-149">指定共用資料庫的共用 DTUs 總數。</span><span class="sxs-lookup"><span data-stu-id="86d43-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="86d43-150">不同版本的預設值如下：</span><span class="sxs-lookup"><span data-stu-id="86d43-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="86d43-151">基本。</span><span class="sxs-lookup"><span data-stu-id="86d43-151">Basic.</span></span>
<span data-ttu-id="86d43-152">100 個 DTUs</span><span class="sxs-lookup"><span data-stu-id="86d43-152">100 DTUs</span></span>
- <span data-ttu-id="86d43-153">標準。</span><span class="sxs-lookup"><span data-stu-id="86d43-153">Standard.</span></span>
<span data-ttu-id="86d43-154">100 個 DTUs</span><span class="sxs-lookup"><span data-stu-id="86d43-154">100 DTUs</span></span>
- <span data-ttu-id="86d43-155">溢價。</span><span class="sxs-lookup"><span data-stu-id="86d43-155">Premium.</span></span>
<span data-ttu-id="86d43-156">125 DTUs 有關哪些值有效的詳細資訊，請參閱位於泳層資料庫的特定大小 [資料庫資料表](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)。</span><span class="sxs-lookup"><span data-stu-id="86d43-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d43-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="86d43-157">-Edition</span></span>
<span data-ttu-id="86d43-158">指定用於壓縮資料庫的 Azure SQL 資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="86d43-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="86d43-159">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="86d43-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="86d43-160">沒有</span><span class="sxs-lookup"><span data-stu-id="86d43-160">None</span></span>
- <span data-ttu-id="86d43-161">基本</span><span class="sxs-lookup"><span data-stu-id="86d43-161">Basic</span></span>
- <span data-ttu-id="86d43-162">標準</span><span class="sxs-lookup"><span data-stu-id="86d43-162">Standard</span></span>
- <span data-ttu-id="86d43-163">溢價</span><span class="sxs-lookup"><span data-stu-id="86d43-163">Premium</span></span>
- <span data-ttu-id="86d43-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="86d43-164">DataWarehouse</span></span>
- <span data-ttu-id="86d43-165">自由</span><span class="sxs-lookup"><span data-stu-id="86d43-165">Free</span></span>
- <span data-ttu-id="86d43-166">伸展</span><span class="sxs-lookup"><span data-stu-id="86d43-166">Stretch</span></span>
- <span data-ttu-id="86d43-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="86d43-167">GeneralPurpose</span></span>
- <span data-ttu-id="86d43-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="86d43-168">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d43-169">-PoolPoolName</span><span class="sxs-lookup"><span data-stu-id="86d43-169">-ElasticPoolName</span></span>
<span data-ttu-id="86d43-170">指定此 Cmdlet 所建立之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="86d43-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d43-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="86d43-171">-LicenseType</span></span>
<span data-ttu-id="86d43-172">Azure Sql 資料庫授權類型。</span><span class="sxs-lookup"><span data-stu-id="86d43-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="86d43-173">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="86d43-173">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="86d43-174">SQL 集中區維護組組識別碼。</span><span class="sxs-lookup"><span data-stu-id="86d43-174">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="86d43-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d43-175">-ResourceGroupName</span></span>
<span data-ttu-id="86d43-176">指定此 Cmdlet 會指派資源資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="86d43-176">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="86d43-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="86d43-177">-ServerName</span></span>
<span data-ttu-id="86d43-178">指定主設備資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="86d43-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="86d43-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="86d43-179">-StorageMB</span></span>
<span data-ttu-id="86d43-180">指定儲存空間資料庫的儲存空間限制 ，以 MB 為單位。</span><span class="sxs-lookup"><span data-stu-id="86d43-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="86d43-181">如果您未指定此參數，此 Cmdlet 會計算取決於 *Dtu* 參數值的值。</span><span class="sxs-lookup"><span data-stu-id="86d43-181">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="86d43-182">請參閱 [eDTU 和儲存空間限制](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) 以尋找可能的值。</span><span class="sxs-lookup"><span data-stu-id="86d43-182">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="86d43-183">-標記</span><span class="sxs-lookup"><span data-stu-id="86d43-183">-Tags</span></span>
<span data-ttu-id="86d43-184">以雜湊表格的形式指定索引鍵值組字典，此 Cmdlet 會與壓縮資料庫關聯。</span><span class="sxs-lookup"><span data-stu-id="86d43-184">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="86d43-185">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="86d43-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="86d43-186">-VCore</span><span class="sxs-lookup"><span data-stu-id="86d43-186">-VCore</span></span>
<span data-ttu-id="86d43-187">Sql Azure Azure 管理資料庫的 Vcore 共用總數。</span><span class="sxs-lookup"><span data-stu-id="86d43-187">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d43-188">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="86d43-188">-ZoneRedundant</span></span>
<span data-ttu-id="86d43-189">與 Azure Sql 優化資料庫建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="86d43-189">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="86d43-190">-確認</span><span class="sxs-lookup"><span data-stu-id="86d43-190">-Confirm</span></span>
<span data-ttu-id="86d43-191">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="86d43-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86d43-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d43-192">-WhatIf</span></span>
<span data-ttu-id="86d43-193">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="86d43-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86d43-194">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="86d43-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86d43-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d43-195">CommonParameters</span></span>
<span data-ttu-id="86d43-196">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="86d43-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d43-197">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86d43-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d43-198">輸入</span><span class="sxs-lookup"><span data-stu-id="86d43-198">INPUTS</span></span>

### <span data-ttu-id="86d43-199">System.String</span><span class="sxs-lookup"><span data-stu-id="86d43-199">System.String</span></span>

## <span data-ttu-id="86d43-200">輸出</span><span class="sxs-lookup"><span data-stu-id="86d43-200">OUTPUTS</span></span>

### <span data-ttu-id="86d43-201">Microsoft.Azure.Commands.Sql.Pool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="86d43-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="86d43-202">筆記</span><span class="sxs-lookup"><span data-stu-id="86d43-202">NOTES</span></span>

## <span data-ttu-id="86d43-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="86d43-203">RELATED LINKS</span></span>

[<span data-ttu-id="86d43-204">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="86d43-204">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="86d43-205">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="86d43-205">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="86d43-206">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="86d43-206">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="86d43-207">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="86d43-207">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="86d43-208">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="86d43-208">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="86d43-209">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="86d43-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
