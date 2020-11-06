---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: 3f90358bcf7109690940b8627a02b6b602353fb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614720"
---
# <span data-ttu-id="c454c-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c454c-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="c454c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c454c-102">SYNOPSIS</span></span>
<span data-ttu-id="c454c-103">修改 Azure SQL 資料庫中彈性資料庫池的屬性。</span><span class="sxs-lookup"><span data-stu-id="c454c-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="c454c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c454c-104">SYNTAX</span></span>

### <span data-ttu-id="c454c-105">DtuBasedPool (預設) </span><span class="sxs-lookup"><span data-stu-id="c454c-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c454c-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="c454c-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c454c-107">說明</span><span class="sxs-lookup"><span data-stu-id="c454c-107">DESCRIPTION</span></span>
<span data-ttu-id="c454c-108">**AzSqlElasticPool** Cmdlet 會在 Azure SQL Database 中設定彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="c454c-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="c454c-109">這個 Cmdlet 可以針對每個池 ( *Dtu* ) 、每個池 ( *StorageMB* ) 、每個資料庫最大 eDTUs ( *DatabaseDtuMax* ) ，以及每個資料庫 () *eDTUs* 的每個 DatqabaseDtuMin 的儲存空間大小。</span><span class="sxs-lookup"><span data-stu-id="c454c-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>
<span data-ttu-id="c454c-110">多個參數 ( *Dtu、-DatabaseDtuMin 及-DatabaseDtuMax* ) 需要設定的值來自該參數的有效值清單。</span><span class="sxs-lookup"><span data-stu-id="c454c-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="c454c-111">例如，標準 100 eDTU 池的-DatabaseDtuMax 只能設定為10、20、50或100。</span><span class="sxs-lookup"><span data-stu-id="c454c-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="c454c-112">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="c454c-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="c454c-113">示例</span><span class="sxs-lookup"><span data-stu-id="c454c-113">EXAMPLES</span></span>

### <span data-ttu-id="c454c-114">範例1：修改彈性池的屬性</span><span class="sxs-lookup"><span data-stu-id="c454c-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="c454c-115">這個命令會修改名為 elasticpool01 的彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="c454c-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="c454c-116">此命令會將彈性池的 Dtu 數設定為1000，並設定最小和最大 Dtu。</span><span class="sxs-lookup"><span data-stu-id="c454c-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="c454c-117">範例2：修改彈性池的儲存空間大小上限</span><span class="sxs-lookup"><span data-stu-id="c454c-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="c454c-118">這個命令會修改名為 elasticpool01 的彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="c454c-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="c454c-119">此命令會將彈性池的最大儲存空間設定為 2 TB。</span><span class="sxs-lookup"><span data-stu-id="c454c-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="c454c-120">參數</span><span class="sxs-lookup"><span data-stu-id="c454c-120">PARAMETERS</span></span>

### <span data-ttu-id="c454c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c454c-121">-AsJob</span></span>
<span data-ttu-id="c454c-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c454c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c454c-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="c454c-123">-ComputeGeneration</span></span>
<span data-ttu-id="c454c-124">要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="c454c-124">The compute generation to assign.</span></span>

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

### <span data-ttu-id="c454c-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="c454c-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="c454c-126">指定池中任何單一資料庫都能佔用的 Dtu 數目上限。</span><span class="sxs-lookup"><span data-stu-id="c454c-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="c454c-127">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="c454c-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="c454c-128">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="c454c-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="c454c-129">空白.</span><span class="sxs-lookup"><span data-stu-id="c454c-129">Basic.</span></span>  <span data-ttu-id="c454c-130">5個 Dtu</span><span class="sxs-lookup"><span data-stu-id="c454c-130">5 DTUs</span></span>
- <span data-ttu-id="c454c-131">標準.</span><span class="sxs-lookup"><span data-stu-id="c454c-131">Standard.</span></span> <span data-ttu-id="c454c-132">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="c454c-132">100 DTUs</span></span>
- <span data-ttu-id="c454c-133">佳.</span><span class="sxs-lookup"><span data-stu-id="c454c-133">Premium.</span></span> <span data-ttu-id="c454c-134">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="c454c-134">125 DTUs</span></span>

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

### <span data-ttu-id="c454c-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="c454c-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="c454c-136">指定彈性池保證對池中所有資料庫的最小 Dtu 數。</span><span class="sxs-lookup"><span data-stu-id="c454c-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="c454c-137">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="c454c-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="c454c-138">預設值為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="c454c-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="c454c-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="c454c-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="c454c-140">任何 SqlAzure 資料庫可在池中使用的 maxmium VCore 號碼。</span><span class="sxs-lookup"><span data-stu-id="c454c-140">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="c454c-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="c454c-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="c454c-142">任何 SqlAzure 資料庫可在池中使用的最小 VCore 數。</span><span class="sxs-lookup"><span data-stu-id="c454c-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="c454c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c454c-143">-DefaultProfile</span></span>
<span data-ttu-id="c454c-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c454c-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c454c-145">-Dtu</span><span class="sxs-lookup"><span data-stu-id="c454c-145">-Dtu</span></span>
<span data-ttu-id="c454c-146">指定彈性池的共用 Dtu 總數。</span><span class="sxs-lookup"><span data-stu-id="c454c-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="c454c-147">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="c454c-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="c454c-148">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="c454c-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="c454c-149">空白.</span><span class="sxs-lookup"><span data-stu-id="c454c-149">Basic.</span></span> <span data-ttu-id="c454c-150">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="c454c-150">100 DTUs</span></span>
- <span data-ttu-id="c454c-151">標準.</span><span class="sxs-lookup"><span data-stu-id="c454c-151">Standard.</span></span> <span data-ttu-id="c454c-152">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="c454c-152">100 DTUs</span></span>
- <span data-ttu-id="c454c-153">佳.</span><span class="sxs-lookup"><span data-stu-id="c454c-153">Premium.</span></span> <span data-ttu-id="c454c-154">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="c454c-154">125 DTUs</span></span>

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

### <span data-ttu-id="c454c-155">-Edition</span><span class="sxs-lookup"><span data-stu-id="c454c-155">-Edition</span></span>
<span data-ttu-id="c454c-156">指定彈性池的 Azure SQL Database 版本。</span><span class="sxs-lookup"><span data-stu-id="c454c-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="c454c-157">您無法變更版本。</span><span class="sxs-lookup"><span data-stu-id="c454c-157">You cannot change the edition.</span></span> <span data-ttu-id="c454c-158">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c454c-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c454c-159">所有</span><span class="sxs-lookup"><span data-stu-id="c454c-159">None</span></span>
- <span data-ttu-id="c454c-160">空白</span><span class="sxs-lookup"><span data-stu-id="c454c-160">Basic</span></span>
- <span data-ttu-id="c454c-161">標準</span><span class="sxs-lookup"><span data-stu-id="c454c-161">Standard</span></span>
- <span data-ttu-id="c454c-162">佳</span><span class="sxs-lookup"><span data-stu-id="c454c-162">Premium</span></span>
- <span data-ttu-id="c454c-163">倉庫</span><span class="sxs-lookup"><span data-stu-id="c454c-163">DataWarehouse</span></span>
- <span data-ttu-id="c454c-164">空閒</span><span class="sxs-lookup"><span data-stu-id="c454c-164">Free</span></span>
- <span data-ttu-id="c454c-165">伸縮</span><span class="sxs-lookup"><span data-stu-id="c454c-165">Stretch</span></span>
- <span data-ttu-id="c454c-166">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="c454c-166">GeneralPurpose</span></span>
- <span data-ttu-id="c454c-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="c454c-167">BusinessCritical</span></span>

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

### <span data-ttu-id="c454c-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c454c-168">-ElasticPoolName</span></span>
<span data-ttu-id="c454c-169">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="c454c-169">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="c454c-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c454c-170">-LicenseType</span></span>
<span data-ttu-id="c454c-171">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="c454c-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="c454c-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c454c-172">-ResourceGroupName</span></span>
<span data-ttu-id="c454c-173">指定將彈性池指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c454c-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="c454c-174">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c454c-174">-ServerName</span></span>
<span data-ttu-id="c454c-175">指定主持彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c454c-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="c454c-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="c454c-176">-StorageMB</span></span>
<span data-ttu-id="c454c-177">指定彈性池的儲存空間限制（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="c454c-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="c454c-178">如需詳細資訊，請參閱 New-AzSqlElasticPool Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c454c-178">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="c454c-179">-標記</span><span class="sxs-lookup"><span data-stu-id="c454c-179">-Tags</span></span>
<span data-ttu-id="c454c-180">指定一個鍵值對的字典，此 Cmdlet 會以雜湊資料表的形式與彈性池相關聯。</span><span class="sxs-lookup"><span data-stu-id="c454c-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="c454c-181">例如： `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="c454c-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="c454c-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="c454c-182">-VCore</span></span>
<span data-ttu-id="c454c-183">Sql Azure 彈性池的共用總 Vcore 數。</span><span class="sxs-lookup"><span data-stu-id="c454c-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="c454c-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="c454c-184">-ZoneRedundant</span></span>
<span data-ttu-id="c454c-185">要與 Azure Sql 彈性池建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="c454c-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="c454c-186">-確認</span><span class="sxs-lookup"><span data-stu-id="c454c-186">-Confirm</span></span>
<span data-ttu-id="c454c-187">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c454c-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c454c-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c454c-188">-WhatIf</span></span>
<span data-ttu-id="c454c-189">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c454c-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c454c-190">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c454c-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c454c-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c454c-191">CommonParameters</span></span>
<span data-ttu-id="c454c-192">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c454c-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c454c-193">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c454c-193">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c454c-194">輸入</span><span class="sxs-lookup"><span data-stu-id="c454c-194">INPUTS</span></span>

### <span data-ttu-id="c454c-195">System.object</span><span class="sxs-lookup"><span data-stu-id="c454c-195">System.String</span></span>

## <span data-ttu-id="c454c-196">輸出</span><span class="sxs-lookup"><span data-stu-id="c454c-196">OUTPUTS</span></span>

### <span data-ttu-id="c454c-197">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="c454c-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="c454c-198">筆記</span><span class="sxs-lookup"><span data-stu-id="c454c-198">NOTES</span></span>

## <span data-ttu-id="c454c-199">相關連結</span><span class="sxs-lookup"><span data-stu-id="c454c-199">RELATED LINKS</span></span>

[<span data-ttu-id="c454c-200">AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c454c-200">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="c454c-201">AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="c454c-201">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="c454c-202">AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="c454c-202">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="c454c-203">新-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c454c-203">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="c454c-204">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c454c-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)