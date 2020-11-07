---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: d78ca6ef2e342982dc6f5e53e8fff4de606dd5ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792587"
---
# <span data-ttu-id="0374f-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0374f-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="0374f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0374f-102">SYNOPSIS</span></span>
<span data-ttu-id="0374f-103">修改 Azure SQL 資料庫中彈性資料庫池的屬性。</span><span class="sxs-lookup"><span data-stu-id="0374f-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="0374f-104">句法</span><span class="sxs-lookup"><span data-stu-id="0374f-104">SYNTAX</span></span>

### <span data-ttu-id="0374f-105">DtuBasedPool (預設) </span><span class="sxs-lookup"><span data-stu-id="0374f-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0374f-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="0374f-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0374f-107">說明</span><span class="sxs-lookup"><span data-stu-id="0374f-107">DESCRIPTION</span></span>
<span data-ttu-id="0374f-108">**AzSqlElasticPool** Cmdlet 會在 Azure SQL Database 中設定彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="0374f-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="0374f-109">這個 Cmdlet 可以針對每個池 ( *Dtu* ) 、每個池 ( *StorageMB* ) 、每個資料庫最大 eDTUs ( *DatabaseDtuMax* ) ，以及每個資料庫 () *eDTUs* 的每個 DatabaseDtuMin 的儲存空間大小。</span><span class="sxs-lookup"><span data-stu-id="0374f-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="0374f-110">多個參數 ( *Dtu、-DatabaseDtuMin 及-DatabaseDtuMax* ) 需要設定的值來自該參數的有效值清單。</span><span class="sxs-lookup"><span data-stu-id="0374f-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="0374f-111">例如，標準 100 eDTU 池的-DatabaseDtuMax 只能設定為10、20、50或100。</span><span class="sxs-lookup"><span data-stu-id="0374f-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="0374f-112">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="0374f-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="0374f-113">示例</span><span class="sxs-lookup"><span data-stu-id="0374f-113">EXAMPLES</span></span>

### <span data-ttu-id="0374f-114">範例1：修改彈性池的屬性</span><span class="sxs-lookup"><span data-stu-id="0374f-114">Example 1: Modify properties for an elastic pool</span></span>
```
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

<span data-ttu-id="0374f-115">這個命令會修改名為 elasticpool01 的彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="0374f-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="0374f-116">此命令會將彈性池的 Dtu 數設定為1000，並設定最小和最大 Dtu。</span><span class="sxs-lookup"><span data-stu-id="0374f-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="0374f-117">範例2：修改彈性池的儲存空間大小上限</span><span class="sxs-lookup"><span data-stu-id="0374f-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```
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

<span data-ttu-id="0374f-118">這個命令會修改名為 elasticpool01 的彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="0374f-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="0374f-119">此命令會將彈性池的最大儲存空間設定為 2 TB。</span><span class="sxs-lookup"><span data-stu-id="0374f-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="0374f-120">參數</span><span class="sxs-lookup"><span data-stu-id="0374f-120">PARAMETERS</span></span>

### <span data-ttu-id="0374f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0374f-121">-AsJob</span></span>
<span data-ttu-id="0374f-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0374f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0374f-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0374f-123">-ComputeGeneration</span></span>
<span data-ttu-id="0374f-124">要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="0374f-124">The compute generation to assign.</span></span>

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

### <span data-ttu-id="0374f-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="0374f-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="0374f-126">指定池中任何單一資料庫都能佔用的 Dtu 數目上限。</span><span class="sxs-lookup"><span data-stu-id="0374f-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="0374f-127">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="0374f-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="0374f-128">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="0374f-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="0374f-129">空白.</span><span class="sxs-lookup"><span data-stu-id="0374f-129">Basic.</span></span>  <span data-ttu-id="0374f-130">5個 Dtu</span><span class="sxs-lookup"><span data-stu-id="0374f-130">5 DTUs</span></span>
- <span data-ttu-id="0374f-131">標準.</span><span class="sxs-lookup"><span data-stu-id="0374f-131">Standard.</span></span> <span data-ttu-id="0374f-132">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="0374f-132">100 DTUs</span></span>
- <span data-ttu-id="0374f-133">佳.</span><span class="sxs-lookup"><span data-stu-id="0374f-133">Premium.</span></span> <span data-ttu-id="0374f-134">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="0374f-134">125 DTUs</span></span>

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

### <span data-ttu-id="0374f-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="0374f-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="0374f-136">指定彈性池保證對池中所有資料庫的最小 Dtu 數。</span><span class="sxs-lookup"><span data-stu-id="0374f-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="0374f-137">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="0374f-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="0374f-138">預設值為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="0374f-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="0374f-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="0374f-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="0374f-140">任何 SqlAzure 資料庫可在池中使用的最大 VCore 數。</span><span class="sxs-lookup"><span data-stu-id="0374f-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="0374f-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="0374f-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="0374f-142">任何 SqlAzure 資料庫可在池中使用的最小 VCore 數。</span><span class="sxs-lookup"><span data-stu-id="0374f-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="0374f-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0374f-143">-DefaultProfile</span></span>
<span data-ttu-id="0374f-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0374f-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0374f-145">-Dtu</span><span class="sxs-lookup"><span data-stu-id="0374f-145">-Dtu</span></span>
<span data-ttu-id="0374f-146">指定彈性池的共用 Dtu 總數。</span><span class="sxs-lookup"><span data-stu-id="0374f-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="0374f-147">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="0374f-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="0374f-148">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="0374f-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="0374f-149">空白.</span><span class="sxs-lookup"><span data-stu-id="0374f-149">Basic.</span></span> <span data-ttu-id="0374f-150">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="0374f-150">100 DTUs</span></span>
- <span data-ttu-id="0374f-151">標準.</span><span class="sxs-lookup"><span data-stu-id="0374f-151">Standard.</span></span> <span data-ttu-id="0374f-152">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="0374f-152">100 DTUs</span></span>
- <span data-ttu-id="0374f-153">佳.</span><span class="sxs-lookup"><span data-stu-id="0374f-153">Premium.</span></span> <span data-ttu-id="0374f-154">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="0374f-154">125 DTUs</span></span>

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

### <span data-ttu-id="0374f-155">-Edition</span><span class="sxs-lookup"><span data-stu-id="0374f-155">-Edition</span></span>
<span data-ttu-id="0374f-156">指定彈性池的 Azure SQL Database 版本。</span><span class="sxs-lookup"><span data-stu-id="0374f-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="0374f-157">您無法變更版本。</span><span class="sxs-lookup"><span data-stu-id="0374f-157">You cannot change the edition.</span></span> <span data-ttu-id="0374f-158">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0374f-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0374f-159">所有</span><span class="sxs-lookup"><span data-stu-id="0374f-159">None</span></span>
- <span data-ttu-id="0374f-160">空白</span><span class="sxs-lookup"><span data-stu-id="0374f-160">Basic</span></span>
- <span data-ttu-id="0374f-161">標準</span><span class="sxs-lookup"><span data-stu-id="0374f-161">Standard</span></span>
- <span data-ttu-id="0374f-162">佳</span><span class="sxs-lookup"><span data-stu-id="0374f-162">Premium</span></span>
- <span data-ttu-id="0374f-163">倉庫</span><span class="sxs-lookup"><span data-stu-id="0374f-163">DataWarehouse</span></span>
- <span data-ttu-id="0374f-164">空閒</span><span class="sxs-lookup"><span data-stu-id="0374f-164">Free</span></span>
- <span data-ttu-id="0374f-165">伸縮</span><span class="sxs-lookup"><span data-stu-id="0374f-165">Stretch</span></span>
- <span data-ttu-id="0374f-166">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="0374f-166">GeneralPurpose</span></span>
- <span data-ttu-id="0374f-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="0374f-167">BusinessCritical</span></span>

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

### <span data-ttu-id="0374f-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0374f-168">-ElasticPoolName</span></span>
<span data-ttu-id="0374f-169">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="0374f-169">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="0374f-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0374f-170">-LicenseType</span></span>
<span data-ttu-id="0374f-171">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="0374f-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="0374f-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0374f-172">-ResourceGroupName</span></span>
<span data-ttu-id="0374f-173">指定將彈性池指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0374f-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="0374f-174">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0374f-174">-ServerName</span></span>
<span data-ttu-id="0374f-175">指定主持彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0374f-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="0374f-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="0374f-176">-StorageMB</span></span>
<span data-ttu-id="0374f-177">指定彈性池的儲存空間限制（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="0374f-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="0374f-178">如需詳細資訊，請參閱 New-AzSqlElasticPool Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0374f-178">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="0374f-179">-標記</span><span class="sxs-lookup"><span data-stu-id="0374f-179">-Tags</span></span>
<span data-ttu-id="0374f-180">指定一個鍵值對的字典，此 Cmdlet 會以雜湊資料表的形式與彈性池相關聯。</span><span class="sxs-lookup"><span data-stu-id="0374f-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="0374f-181">例如： `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="0374f-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="0374f-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="0374f-182">-VCore</span></span>
<span data-ttu-id="0374f-183">Sql Azure 彈性池的共用總 Vcore 數。</span><span class="sxs-lookup"><span data-stu-id="0374f-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="0374f-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="0374f-184">-ZoneRedundant</span></span>
<span data-ttu-id="0374f-185">要與 Azure Sql 彈性池建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="0374f-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="0374f-186">-確認</span><span class="sxs-lookup"><span data-stu-id="0374f-186">-Confirm</span></span>
<span data-ttu-id="0374f-187">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0374f-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0374f-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0374f-188">-WhatIf</span></span>
<span data-ttu-id="0374f-189">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0374f-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0374f-190">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0374f-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0374f-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0374f-191">CommonParameters</span></span>
<span data-ttu-id="0374f-192">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0374f-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0374f-193">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0374f-193">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0374f-194">輸入</span><span class="sxs-lookup"><span data-stu-id="0374f-194">INPUTS</span></span>

### <span data-ttu-id="0374f-195">System.object</span><span class="sxs-lookup"><span data-stu-id="0374f-195">System.String</span></span>

## <span data-ttu-id="0374f-196">輸出</span><span class="sxs-lookup"><span data-stu-id="0374f-196">OUTPUTS</span></span>

### <span data-ttu-id="0374f-197">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="0374f-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="0374f-198">筆記</span><span class="sxs-lookup"><span data-stu-id="0374f-198">NOTES</span></span>

## <span data-ttu-id="0374f-199">相關連結</span><span class="sxs-lookup"><span data-stu-id="0374f-199">RELATED LINKS</span></span>

[<span data-ttu-id="0374f-200">AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0374f-200">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="0374f-201">AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="0374f-201">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="0374f-202">AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="0374f-202">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="0374f-203">新-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0374f-203">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="0374f-204">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="0374f-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
