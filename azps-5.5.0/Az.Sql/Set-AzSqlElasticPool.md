---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: a420a7edf1d5fb7133087c5ecb9fcf605cbdddf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127394"
---
# <span data-ttu-id="95e6c-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="95e6c-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="95e6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="95e6c-103">修改 Azure SQL 資料庫中彈性資料庫池的屬性。</span><span class="sxs-lookup"><span data-stu-id="95e6c-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="95e6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="95e6c-104">SYNTAX</span></span>

### <span data-ttu-id="95e6c-105">DtuBasedPool (預設) </span><span class="sxs-lookup"><span data-stu-id="95e6c-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95e6c-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="95e6c-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95e6c-107">說明</span><span class="sxs-lookup"><span data-stu-id="95e6c-107">DESCRIPTION</span></span>
<span data-ttu-id="95e6c-108">**AzSqlElasticPool** Cmdlet 會在 Azure SQL Database 中設定彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="95e6c-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="95e6c-109">這個 Cmdlet 可以針對每個池 (*Dtu*) 、每個池 (*StorageMB*) 、每個資料庫最大 eDTUs (*DatabaseDtuMax*) ，以及每個資料庫 () *eDTUs* 的每個 DatabaseDtuMin 的儲存空間大小。</span><span class="sxs-lookup"><span data-stu-id="95e6c-109">This cmdlet can modify the eDTUs per pool (*Dtu*), storage max size per pool (*StorageMB*), maximum eDTUs per database (*DatabaseDtuMax*), and minimum eDTUs per database (*DatabaseDtuMin*).</span></span>
<span data-ttu-id="95e6c-110">多個參數 (*Dtu、-DatabaseDtuMin 及-DatabaseDtuMax*) 需要設定的值來自該參數的有效值清單。</span><span class="sxs-lookup"><span data-stu-id="95e6c-110">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="95e6c-111">例如，標準 100 eDTU 池的-DatabaseDtuMax 只能設定為10、20、50或100。</span><span class="sxs-lookup"><span data-stu-id="95e6c-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="95e6c-112">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="95e6c-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="95e6c-113">示例</span><span class="sxs-lookup"><span data-stu-id="95e6c-113">EXAMPLES</span></span>

### <span data-ttu-id="95e6c-114">範例1：修改彈性池的屬性</span><span class="sxs-lookup"><span data-stu-id="95e6c-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="95e6c-115">這個命令會修改名為 elasticpool01 的彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="95e6c-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="95e6c-116">此命令會將彈性池的 Dtu 數設定為1000，並設定最小和最大 Dtu。</span><span class="sxs-lookup"><span data-stu-id="95e6c-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="95e6c-117">範例2：修改彈性池的儲存空間大小上限</span><span class="sxs-lookup"><span data-stu-id="95e6c-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="95e6c-118">這個命令會修改名為 elasticpool01 的彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="95e6c-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="95e6c-119">此命令會將彈性池的最大儲存空間設定為 2 TB。</span><span class="sxs-lookup"><span data-stu-id="95e6c-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="95e6c-120">範例3</span><span class="sxs-lookup"><span data-stu-id="95e6c-120">Example 3</span></span>

<span data-ttu-id="95e6c-121">修改 Azure SQL 資料庫中彈性資料庫池的屬性。</span><span class="sxs-lookup"><span data-stu-id="95e6c-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="95e6c-122"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="95e6c-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="95e6c-123">參數</span><span class="sxs-lookup"><span data-stu-id="95e6c-123">PARAMETERS</span></span>

### <span data-ttu-id="95e6c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95e6c-124">-AsJob</span></span>
<span data-ttu-id="95e6c-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="95e6c-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95e6c-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="95e6c-126">-ComputeGeneration</span></span>
<span data-ttu-id="95e6c-127">要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="95e6c-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="95e6c-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="95e6c-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="95e6c-129">指定池中任何單一資料庫都能佔用的 Dtu 數目上限。</span><span class="sxs-lookup"><span data-stu-id="95e6c-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="95e6c-130">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="95e6c-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="95e6c-131">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="95e6c-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="95e6c-132">空白.</span><span class="sxs-lookup"><span data-stu-id="95e6c-132">Basic.</span></span>  <span data-ttu-id="95e6c-133">5個 Dtu</span><span class="sxs-lookup"><span data-stu-id="95e6c-133">5 DTUs</span></span>
- <span data-ttu-id="95e6c-134">標準.</span><span class="sxs-lookup"><span data-stu-id="95e6c-134">Standard.</span></span> <span data-ttu-id="95e6c-135">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="95e6c-135">100 DTUs</span></span>
- <span data-ttu-id="95e6c-136">佳.</span><span class="sxs-lookup"><span data-stu-id="95e6c-136">Premium.</span></span> <span data-ttu-id="95e6c-137">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="95e6c-137">125 DTUs</span></span>

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

### <span data-ttu-id="95e6c-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="95e6c-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="95e6c-139">指定彈性池保證對池中所有資料庫的最小 Dtu 數。</span><span class="sxs-lookup"><span data-stu-id="95e6c-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="95e6c-140">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="95e6c-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="95e6c-141">預設值為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="95e6c-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="95e6c-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="95e6c-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="95e6c-143">任何 SqlAzure 資料庫可在池中使用的最大 VCore 數。</span><span class="sxs-lookup"><span data-stu-id="95e6c-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="95e6c-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="95e6c-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="95e6c-145">任何 SqlAzure 資料庫可在池中使用的最小 VCore 數。</span><span class="sxs-lookup"><span data-stu-id="95e6c-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="95e6c-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e6c-146">-DefaultProfile</span></span>
<span data-ttu-id="95e6c-147">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="95e6c-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95e6c-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="95e6c-148">-Dtu</span></span>
<span data-ttu-id="95e6c-149">指定彈性池的共用 Dtu 總數。</span><span class="sxs-lookup"><span data-stu-id="95e6c-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="95e6c-150">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="95e6c-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="95e6c-151">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="95e6c-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="95e6c-152">空白.</span><span class="sxs-lookup"><span data-stu-id="95e6c-152">Basic.</span></span> <span data-ttu-id="95e6c-153">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="95e6c-153">100 DTUs</span></span>
- <span data-ttu-id="95e6c-154">標準.</span><span class="sxs-lookup"><span data-stu-id="95e6c-154">Standard.</span></span> <span data-ttu-id="95e6c-155">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="95e6c-155">100 DTUs</span></span>
- <span data-ttu-id="95e6c-156">佳.</span><span class="sxs-lookup"><span data-stu-id="95e6c-156">Premium.</span></span> <span data-ttu-id="95e6c-157">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="95e6c-157">125 DTUs</span></span>

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

### <span data-ttu-id="95e6c-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="95e6c-158">-Edition</span></span>
<span data-ttu-id="95e6c-159">指定彈性池的 Azure SQL Database 版本。</span><span class="sxs-lookup"><span data-stu-id="95e6c-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="95e6c-160">您無法變更版本。</span><span class="sxs-lookup"><span data-stu-id="95e6c-160">You cannot change the edition.</span></span> <span data-ttu-id="95e6c-161">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="95e6c-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95e6c-162">所有</span><span class="sxs-lookup"><span data-stu-id="95e6c-162">None</span></span>
- <span data-ttu-id="95e6c-163">空白</span><span class="sxs-lookup"><span data-stu-id="95e6c-163">Basic</span></span>
- <span data-ttu-id="95e6c-164">標準</span><span class="sxs-lookup"><span data-stu-id="95e6c-164">Standard</span></span>
- <span data-ttu-id="95e6c-165">佳</span><span class="sxs-lookup"><span data-stu-id="95e6c-165">Premium</span></span>
- <span data-ttu-id="95e6c-166">倉庫</span><span class="sxs-lookup"><span data-stu-id="95e6c-166">DataWarehouse</span></span>
- <span data-ttu-id="95e6c-167">空閒</span><span class="sxs-lookup"><span data-stu-id="95e6c-167">Free</span></span>
- <span data-ttu-id="95e6c-168">伸縮</span><span class="sxs-lookup"><span data-stu-id="95e6c-168">Stretch</span></span>
- <span data-ttu-id="95e6c-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="95e6c-169">GeneralPurpose</span></span>
- <span data-ttu-id="95e6c-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="95e6c-170">BusinessCritical</span></span>

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

### <span data-ttu-id="95e6c-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="95e6c-171">-ElasticPoolName</span></span>
<span data-ttu-id="95e6c-172">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="95e6c-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="95e6c-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="95e6c-173">-LicenseType</span></span>
<span data-ttu-id="95e6c-174">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="95e6c-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="95e6c-175">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="95e6c-175">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="95e6c-176">SQL 彈性池的維護配置識別碼。</span><span class="sxs-lookup"><span data-stu-id="95e6c-176">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="95e6c-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95e6c-177">-ResourceGroupName</span></span>
<span data-ttu-id="95e6c-178">指定將彈性池指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="95e6c-178">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="95e6c-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="95e6c-179">-ServerName</span></span>
<span data-ttu-id="95e6c-180">指定主持彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="95e6c-180">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="95e6c-181">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="95e6c-181">-StorageMB</span></span>
<span data-ttu-id="95e6c-182">指定彈性池的儲存空間限制（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="95e6c-182">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="95e6c-183">如需詳細資訊，請參閱 New-AzSqlElasticPool Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95e6c-183">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="95e6c-184">-標記</span><span class="sxs-lookup"><span data-stu-id="95e6c-184">-Tags</span></span>
<span data-ttu-id="95e6c-185">指定一個鍵值對的字典，此 Cmdlet 會以雜湊資料表的形式與彈性池相關聯。</span><span class="sxs-lookup"><span data-stu-id="95e6c-185">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="95e6c-186">例如： `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="95e6c-186">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="95e6c-187">-VCore</span><span class="sxs-lookup"><span data-stu-id="95e6c-187">-VCore</span></span>
<span data-ttu-id="95e6c-188">Sql Azure 彈性池的共用總 Vcore 數。</span><span class="sxs-lookup"><span data-stu-id="95e6c-188">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="95e6c-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="95e6c-189">-ZoneRedundant</span></span>
<span data-ttu-id="95e6c-190">要與 Azure Sql 彈性池建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="95e6c-190">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="95e6c-191">-確認</span><span class="sxs-lookup"><span data-stu-id="95e6c-191">-Confirm</span></span>
<span data-ttu-id="95e6c-192">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="95e6c-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95e6c-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95e6c-193">-WhatIf</span></span>
<span data-ttu-id="95e6c-194">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95e6c-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95e6c-195">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95e6c-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95e6c-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e6c-196">CommonParameters</span></span>
<span data-ttu-id="95e6c-197">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95e6c-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e6c-198">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="95e6c-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e6c-199">輸入</span><span class="sxs-lookup"><span data-stu-id="95e6c-199">INPUTS</span></span>

### <span data-ttu-id="95e6c-200">System.object</span><span class="sxs-lookup"><span data-stu-id="95e6c-200">System.String</span></span>

## <span data-ttu-id="95e6c-201">輸出</span><span class="sxs-lookup"><span data-stu-id="95e6c-201">OUTPUTS</span></span>

### <span data-ttu-id="95e6c-202">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="95e6c-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="95e6c-203">筆記</span><span class="sxs-lookup"><span data-stu-id="95e6c-203">NOTES</span></span>

## <span data-ttu-id="95e6c-204">相關連結</span><span class="sxs-lookup"><span data-stu-id="95e6c-204">RELATED LINKS</span></span>

[<span data-ttu-id="95e6c-205">AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="95e6c-205">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="95e6c-206">AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="95e6c-206">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="95e6c-207">AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="95e6c-207">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="95e6c-208">新-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="95e6c-208">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="95e6c-209">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="95e6c-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
