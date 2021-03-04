---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: 564bd475b8574f30f8d00cc1a374bc11b4a93ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904822"
---
# <span data-ttu-id="f6134-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f6134-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="f6134-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f6134-102">SYNOPSIS</span></span>
<span data-ttu-id="f6134-103">修改 Azure SQL Database 中彈性資料庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f6134-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="f6134-104">語法</span><span class="sxs-lookup"><span data-stu-id="f6134-104">SYNTAX</span></span>

### <span data-ttu-id="f6134-105">DtuBasedPool (預設) </span><span class="sxs-lookup"><span data-stu-id="f6134-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6134-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="f6134-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6134-107">描述</span><span class="sxs-lookup"><span data-stu-id="f6134-107">DESCRIPTION</span></span>
<span data-ttu-id="f6134-108">**Set-AzSqlElasticPool** Cmdlet 會設定 Azure SQL Database 中集區集區的屬性。</span><span class="sxs-lookup"><span data-stu-id="f6134-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="f6134-109">此 Cmdlet 可以修改每個資料庫的 eDTU (*Dtu*) 、每個資料庫的儲存空間上限 (*StorageMB*) 、每個資料庫的最大 *eDTU (DatabaseDtuMax*) ，以及每個資料庫的最小 eDTU (*DatabaseDtuMin*) 。</span><span class="sxs-lookup"><span data-stu-id="f6134-109">This cmdlet can modify the eDTUs per pool (*Dtu*), storage max size per pool (*StorageMB*), maximum eDTUs per database (*DatabaseDtuMax*), and minimum eDTUs per database (*DatabaseDtuMin*).</span></span>
<span data-ttu-id="f6134-110">需要設定 (*-Dtu、-DatabaseDtuMin 和 -DatabaseDtuMax*) 的數個參數，都是來自該參數的有效值清單。</span><span class="sxs-lookup"><span data-stu-id="f6134-110">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="f6134-111">例如，標準 100 eDTU 集區 -DatabaseDtuMax 只能設定為 10、20、50 或 100。</span><span class="sxs-lookup"><span data-stu-id="f6134-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="f6134-112">有關哪些值有效的詳細資訊，請參閱泳層資料庫內特定大小資料庫 [的表格](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)。</span><span class="sxs-lookup"><span data-stu-id="f6134-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="f6134-113">例子</span><span class="sxs-lookup"><span data-stu-id="f6134-113">EXAMPLES</span></span>

### <span data-ttu-id="f6134-114">範例 1：修改泳層資料庫的屬性</span><span class="sxs-lookup"><span data-stu-id="f6134-114">Example 1: Modify properties for an elastic pool</span></span>
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

<span data-ttu-id="f6134-115">此命令會修改名為poolpool01 的彈性資料庫屬性。</span><span class="sxs-lookup"><span data-stu-id="f6134-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="f6134-116">該命令將集區集區 DTUs 的數量設定為 1000 個，並設定最小和最大 DTUs。</span><span class="sxs-lookup"><span data-stu-id="f6134-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="f6134-117">範例 2：修改彈性資料庫的儲存空間最大大小</span><span class="sxs-lookup"><span data-stu-id="f6134-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

<span data-ttu-id="f6134-118">此命令會修改名為poolpool01 的彈性資料庫屬性。</span><span class="sxs-lookup"><span data-stu-id="f6134-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="f6134-119">此命令將集區集區的最大儲存空間設定為 2 TB。</span><span class="sxs-lookup"><span data-stu-id="f6134-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="f6134-120">範例 3</span><span class="sxs-lookup"><span data-stu-id="f6134-120">Example 3</span></span>

<span data-ttu-id="f6134-121">修改 Azure SQL Database 中彈性資料庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f6134-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="f6134-122"> (自動) </span><span class="sxs-lookup"><span data-stu-id="f6134-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="f6134-123">參數</span><span class="sxs-lookup"><span data-stu-id="f6134-123">PARAMETERS</span></span>

### <span data-ttu-id="f6134-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6134-124">-AsJob</span></span>
<span data-ttu-id="f6134-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f6134-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6134-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="f6134-126">-ComputeGeneration</span></span>
<span data-ttu-id="f6134-127">這是要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="f6134-127">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6134-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="f6134-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="f6134-129">指定資料庫中任何單一資料庫可耗用的最大 DTUs 數量。</span><span class="sxs-lookup"><span data-stu-id="f6134-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="f6134-130">有關哪些值有效的詳細資訊，請參閱泳層資料庫內特定大小資料庫 [的表格](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)。</span><span class="sxs-lookup"><span data-stu-id="f6134-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="f6134-131">不同版本的預設值如下：</span><span class="sxs-lookup"><span data-stu-id="f6134-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="f6134-132">基本。</span><span class="sxs-lookup"><span data-stu-id="f6134-132">Basic.</span></span>  <span data-ttu-id="f6134-133">5 個 DTUs</span><span class="sxs-lookup"><span data-stu-id="f6134-133">5 DTUs</span></span>
- <span data-ttu-id="f6134-134">標準。</span><span class="sxs-lookup"><span data-stu-id="f6134-134">Standard.</span></span> <span data-ttu-id="f6134-135">100 個 DTUs</span><span class="sxs-lookup"><span data-stu-id="f6134-135">100 DTUs</span></span>
- <span data-ttu-id="f6134-136">溢價。</span><span class="sxs-lookup"><span data-stu-id="f6134-136">Premium.</span></span> <span data-ttu-id="f6134-137">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="f6134-137">125 DTUs</span></span>

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

### <span data-ttu-id="f6134-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="f6134-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="f6134-139">指定資料庫集中所有資料庫所保證的最小 DTUS 數量。</span><span class="sxs-lookup"><span data-stu-id="f6134-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="f6134-140">有關哪些值有效的詳細資訊，請參閱泳層資料庫內特定大小資料庫 [的表格](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)。</span><span class="sxs-lookup"><span data-stu-id="f6134-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="f6134-141">預設值為 0 (0) 。</span><span class="sxs-lookup"><span data-stu-id="f6134-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="f6134-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="f6134-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="f6134-143">任何 SqlAzure 資料庫都可以在資料庫中使用的最大 VCore 數位。</span><span class="sxs-lookup"><span data-stu-id="f6134-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="f6134-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="f6134-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="f6134-145">任何 SqlAzure 資料庫都可以在資料庫中使用的最小 VCore 數位。</span><span class="sxs-lookup"><span data-stu-id="f6134-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="f6134-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6134-146">-DefaultProfile</span></span>
<span data-ttu-id="f6134-147">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f6134-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6134-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="f6134-148">-Dtu</span></span>
<span data-ttu-id="f6134-149">指定共用資料庫的共用 DTUs 總數。</span><span class="sxs-lookup"><span data-stu-id="f6134-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="f6134-150">有關哪些值有效的詳細資訊，請參閱泳層資料庫內特定大小資料庫 [的表格](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)。</span><span class="sxs-lookup"><span data-stu-id="f6134-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="f6134-151">不同版本的預設值如下：</span><span class="sxs-lookup"><span data-stu-id="f6134-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="f6134-152">基本。</span><span class="sxs-lookup"><span data-stu-id="f6134-152">Basic.</span></span> <span data-ttu-id="f6134-153">100 個 DTUs</span><span class="sxs-lookup"><span data-stu-id="f6134-153">100 DTUs</span></span>
- <span data-ttu-id="f6134-154">標準。</span><span class="sxs-lookup"><span data-stu-id="f6134-154">Standard.</span></span> <span data-ttu-id="f6134-155">100 個 DTUs</span><span class="sxs-lookup"><span data-stu-id="f6134-155">100 DTUs</span></span>
- <span data-ttu-id="f6134-156">溢價。</span><span class="sxs-lookup"><span data-stu-id="f6134-156">Premium.</span></span> <span data-ttu-id="f6134-157">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="f6134-157">125 DTUs</span></span>

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

### <span data-ttu-id="f6134-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="f6134-158">-Edition</span></span>
<span data-ttu-id="f6134-159">指定 Azure SQL 資料庫的版本，以用於建立資料庫。</span><span class="sxs-lookup"><span data-stu-id="f6134-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="f6134-160">您無法變更版本。</span><span class="sxs-lookup"><span data-stu-id="f6134-160">You cannot change the edition.</span></span> <span data-ttu-id="f6134-161">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f6134-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6134-162">沒有</span><span class="sxs-lookup"><span data-stu-id="f6134-162">None</span></span>
- <span data-ttu-id="f6134-163">基本</span><span class="sxs-lookup"><span data-stu-id="f6134-163">Basic</span></span>
- <span data-ttu-id="f6134-164">標準</span><span class="sxs-lookup"><span data-stu-id="f6134-164">Standard</span></span>
- <span data-ttu-id="f6134-165">溢價</span><span class="sxs-lookup"><span data-stu-id="f6134-165">Premium</span></span>
- <span data-ttu-id="f6134-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="f6134-166">DataWarehouse</span></span>
- <span data-ttu-id="f6134-167">自由</span><span class="sxs-lookup"><span data-stu-id="f6134-167">Free</span></span>
- <span data-ttu-id="f6134-168">伸展</span><span class="sxs-lookup"><span data-stu-id="f6134-168">Stretch</span></span>
- <span data-ttu-id="f6134-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="f6134-169">GeneralPurpose</span></span>
- <span data-ttu-id="f6134-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="f6134-170">BusinessCritical</span></span>

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

### <span data-ttu-id="f6134-171">-PoolPoolName</span><span class="sxs-lookup"><span data-stu-id="f6134-171">-ElasticPoolName</span></span>
<span data-ttu-id="f6134-172">指定泳層資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6134-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="f6134-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f6134-173">-LicenseType</span></span>
<span data-ttu-id="f6134-174">Azure Sql 資料庫授權類型。</span><span class="sxs-lookup"><span data-stu-id="f6134-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="f6134-175">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f6134-175">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="f6134-176">SQL 集中區維護組組識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6134-176">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="f6134-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6134-177">-ResourceGroupName</span></span>
<span data-ttu-id="f6134-178">指定指派了壓縮資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f6134-178">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="f6134-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f6134-179">-ServerName</span></span>
<span data-ttu-id="f6134-180">指定主設備資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f6134-180">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="f6134-181">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="f6134-181">-StorageMB</span></span>
<span data-ttu-id="f6134-182">指定儲存空間資料庫的儲存空間限制 ，以 MB 為單位。</span><span class="sxs-lookup"><span data-stu-id="f6134-182">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="f6134-183">有關詳細資訊，請參閱 New-AzSqlElasticPool Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6134-183">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="f6134-184">-標記</span><span class="sxs-lookup"><span data-stu-id="f6134-184">-Tags</span></span>
<span data-ttu-id="f6134-185">指定此 Cmdlet 與雜湊表格形式之資料庫關聯之索引鍵值組字典。</span><span class="sxs-lookup"><span data-stu-id="f6134-185">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="f6134-186">例如： `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="f6134-186">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="f6134-187">-VCore</span><span class="sxs-lookup"><span data-stu-id="f6134-187">-VCore</span></span>
<span data-ttu-id="f6134-188">Sql Azure Azure 管理資料庫的 Vcore 共用總數。</span><span class="sxs-lookup"><span data-stu-id="f6134-188">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6134-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="f6134-189">-ZoneRedundant</span></span>
<span data-ttu-id="f6134-190">與 Azure Sql 優化資料庫建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="f6134-190">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="f6134-191">-確認</span><span class="sxs-lookup"><span data-stu-id="f6134-191">-Confirm</span></span>
<span data-ttu-id="f6134-192">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f6134-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6134-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6134-193">-WhatIf</span></span>
<span data-ttu-id="f6134-194">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6134-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6134-195">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6134-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6134-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6134-196">CommonParameters</span></span>
<span data-ttu-id="f6134-197">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f6134-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6134-198">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6134-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6134-199">輸入</span><span class="sxs-lookup"><span data-stu-id="f6134-199">INPUTS</span></span>

### <span data-ttu-id="f6134-200">System.String</span><span class="sxs-lookup"><span data-stu-id="f6134-200">System.String</span></span>

## <span data-ttu-id="f6134-201">輸出</span><span class="sxs-lookup"><span data-stu-id="f6134-201">OUTPUTS</span></span>

### <span data-ttu-id="f6134-202">Microsoft.Azure.Commands.Sql.Pool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="f6134-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="f6134-203">筆記</span><span class="sxs-lookup"><span data-stu-id="f6134-203">NOTES</span></span>

## <span data-ttu-id="f6134-204">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6134-204">RELATED LINKS</span></span>

[<span data-ttu-id="f6134-205">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f6134-205">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="f6134-206">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f6134-206">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="f6134-207">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="f6134-207">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="f6134-208">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f6134-208">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="f6134-209">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="f6134-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
