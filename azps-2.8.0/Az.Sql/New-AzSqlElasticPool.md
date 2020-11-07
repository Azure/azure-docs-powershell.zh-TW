---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: f16313710e0ab007f23df0cfa3a2214f78a8963a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792448"
---
# <span data-ttu-id="1eb52-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1eb52-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="1eb52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1eb52-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb52-103">針對 SQL 資料庫建立彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="1eb52-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="1eb52-104">句法</span><span class="sxs-lookup"><span data-stu-id="1eb52-104">SYNTAX</span></span>

### <span data-ttu-id="1eb52-105">DtuBasedPool (預設) </span><span class="sxs-lookup"><span data-stu-id="1eb52-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eb52-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="1eb52-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eb52-107">說明</span><span class="sxs-lookup"><span data-stu-id="1eb52-107">DESCRIPTION</span></span>
<span data-ttu-id="1eb52-108">**新的-AzSqlElasticPool** Cmdlet 會為 Azure SQL 資料庫建立彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="1eb52-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="1eb52-109">多個參數 ( *Dtu、-DatabaseDtuMin 及-DatabaseDtuMax* ) 需要設定的值來自該參數的有效值清單。</span><span class="sxs-lookup"><span data-stu-id="1eb52-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="1eb52-110">例如，標準 100 eDTU 池的-DatabaseDtuMax 只能設定為10、20、50或100。</span><span class="sxs-lookup"><span data-stu-id="1eb52-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="1eb52-111">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="1eb52-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="1eb52-112">示例</span><span class="sxs-lookup"><span data-stu-id="1eb52-112">EXAMPLES</span></span>

### <span data-ttu-id="1eb52-113">範例1：建立 DTU 彈性池</span><span class="sxs-lookup"><span data-stu-id="1eb52-113">Example 1: Create a DTU elastic pool</span></span>

```
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

<span data-ttu-id="1eb52-114">這個命令會在名為 ElasticPool01 的標準服務層級中建立彈性池。</span><span class="sxs-lookup"><span data-stu-id="1eb52-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="1eb52-115">名為 server01 的伺服器，指派給名為 ResourceGroup01 的 Azure 資源群組，會將彈性池託管在其中。</span><span class="sxs-lookup"><span data-stu-id="1eb52-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="1eb52-116">此命令會為 pool 和 pool 中的資料庫指定 DTU 屬性值。</span><span class="sxs-lookup"><span data-stu-id="1eb52-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="1eb52-117">範例2：建立 vCore 彈性池</span><span class="sxs-lookup"><span data-stu-id="1eb52-117">Example 2: Create a vCore elastic pool</span></span>

```
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


<span data-ttu-id="1eb52-118">這個命令會在 GengeralPurpose 服務層級（名為 ElasticPool01）中建立彈性池。</span><span class="sxs-lookup"><span data-stu-id="1eb52-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="1eb52-119">名為 server01 的伺服器，指派給名為 ResourceGroup01 的 Azure 資源群組，會將彈性池託管在其中。</span><span class="sxs-lookup"><span data-stu-id="1eb52-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="1eb52-120">此命令會指定池的 vCore 屬性值，以及池中的資料庫。</span><span class="sxs-lookup"><span data-stu-id="1eb52-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="1eb52-121">參數</span><span class="sxs-lookup"><span data-stu-id="1eb52-121">PARAMETERS</span></span>

### <span data-ttu-id="1eb52-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1eb52-122">-AsJob</span></span>
<span data-ttu-id="1eb52-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1eb52-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1eb52-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="1eb52-124">-ComputeGeneration</span></span>
<span data-ttu-id="1eb52-125">要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="1eb52-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="1eb52-126">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="1eb52-126">-DatabaseDtuMax</span></span>
<span data-ttu-id="1eb52-127">指定池中任何單一資料庫都可以使用的最大資料庫輸送量單位數量 (Dtu) 。</span><span class="sxs-lookup"><span data-stu-id="1eb52-127">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="1eb52-128">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="1eb52-128">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="1eb52-129">空白.</span><span class="sxs-lookup"><span data-stu-id="1eb52-129">Basic.</span></span> <span data-ttu-id="1eb52-130">5個 Dtu</span><span class="sxs-lookup"><span data-stu-id="1eb52-130">5 DTUs</span></span>
- <span data-ttu-id="1eb52-131">標準.</span><span class="sxs-lookup"><span data-stu-id="1eb52-131">Standard.</span></span> <span data-ttu-id="1eb52-132">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="1eb52-132">100 DTUs</span></span>
- <span data-ttu-id="1eb52-133">佳.</span><span class="sxs-lookup"><span data-stu-id="1eb52-133">Premium.</span></span> <span data-ttu-id="1eb52-134">125 Dtu 如需哪些值有效的詳細資料，請參閱[彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的表格</span><span class="sxs-lookup"><span data-stu-id="1eb52-134">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="1eb52-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="1eb52-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="1eb52-136">指定彈性池保證對池中所有資料庫的最小 Dtu 數。</span><span class="sxs-lookup"><span data-stu-id="1eb52-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="1eb52-137">預設值為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="1eb52-137">The default value is zero (0).</span></span>
<span data-ttu-id="1eb52-138">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="1eb52-138">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="1eb52-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="1eb52-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="1eb52-140">任何 SqlAzure 資料庫可在池中使用的最大 VCore 數。</span><span class="sxs-lookup"><span data-stu-id="1eb52-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="1eb52-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="1eb52-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="1eb52-142">任何 SqlAzure 資料庫可在池中使用的最小 VCore 數。</span><span class="sxs-lookup"><span data-stu-id="1eb52-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="1eb52-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb52-143">-DefaultProfile</span></span>
<span data-ttu-id="1eb52-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1eb52-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1eb52-145">-Dtu</span><span class="sxs-lookup"><span data-stu-id="1eb52-145">-Dtu</span></span>
<span data-ttu-id="1eb52-146">指定彈性池的共用 Dtu 總數。</span><span class="sxs-lookup"><span data-stu-id="1eb52-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="1eb52-147">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="1eb52-147">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="1eb52-148">空白.</span><span class="sxs-lookup"><span data-stu-id="1eb52-148">Basic.</span></span>
<span data-ttu-id="1eb52-149">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="1eb52-149">100 DTUs</span></span>
- <span data-ttu-id="1eb52-150">標準.</span><span class="sxs-lookup"><span data-stu-id="1eb52-150">Standard.</span></span>
<span data-ttu-id="1eb52-151">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="1eb52-151">100 DTUs</span></span>
- <span data-ttu-id="1eb52-152">佳.</span><span class="sxs-lookup"><span data-stu-id="1eb52-152">Premium.</span></span>
<span data-ttu-id="1eb52-153">125 Dtu 如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的表格。</span><span class="sxs-lookup"><span data-stu-id="1eb52-153">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="1eb52-154">-Edition</span><span class="sxs-lookup"><span data-stu-id="1eb52-154">-Edition</span></span>
<span data-ttu-id="1eb52-155">指定用於彈性池的 Azure SQL 資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="1eb52-155">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="1eb52-156">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1eb52-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1eb52-157">所有</span><span class="sxs-lookup"><span data-stu-id="1eb52-157">None</span></span>
- <span data-ttu-id="1eb52-158">空白</span><span class="sxs-lookup"><span data-stu-id="1eb52-158">Basic</span></span>
- <span data-ttu-id="1eb52-159">標準</span><span class="sxs-lookup"><span data-stu-id="1eb52-159">Standard</span></span>
- <span data-ttu-id="1eb52-160">佳</span><span class="sxs-lookup"><span data-stu-id="1eb52-160">Premium</span></span>
- <span data-ttu-id="1eb52-161">倉庫</span><span class="sxs-lookup"><span data-stu-id="1eb52-161">DataWarehouse</span></span>
- <span data-ttu-id="1eb52-162">空閒</span><span class="sxs-lookup"><span data-stu-id="1eb52-162">Free</span></span>
- <span data-ttu-id="1eb52-163">伸縮</span><span class="sxs-lookup"><span data-stu-id="1eb52-163">Stretch</span></span>
- <span data-ttu-id="1eb52-164">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="1eb52-164">GeneralPurpose</span></span>
- <span data-ttu-id="1eb52-165">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="1eb52-165">BusinessCritical</span></span>

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

### <span data-ttu-id="1eb52-166">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1eb52-166">-ElasticPoolName</span></span>
<span data-ttu-id="1eb52-167">指定此 Cmdlet 所建立之彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb52-167">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1eb52-168">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1eb52-168">-LicenseType</span></span>
<span data-ttu-id="1eb52-169">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="1eb52-169">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="1eb52-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb52-170">-ResourceGroupName</span></span>
<span data-ttu-id="1eb52-171">指定此 Cmdlet 指派彈性池之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb52-171">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="1eb52-172">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1eb52-172">-ServerName</span></span>
<span data-ttu-id="1eb52-173">指定主持彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1eb52-173">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="1eb52-174">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="1eb52-174">-StorageMB</span></span>
<span data-ttu-id="1eb52-175">指定彈性池的儲存空間限制（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="1eb52-175">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="1eb52-176">如果您沒有指定此參數，這個 Cmdlet 會根據 *Dtu* 參數的值來計算值。</span><span class="sxs-lookup"><span data-stu-id="1eb52-176">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="1eb52-177">請參閱可能值的 [eDTU 與儲存空間限制](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) 。</span><span class="sxs-lookup"><span data-stu-id="1eb52-177">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="1eb52-178">-標記</span><span class="sxs-lookup"><span data-stu-id="1eb52-178">-Tags</span></span>
<span data-ttu-id="1eb52-179">指定以雜湊資料表形式表示的鍵值對字典，此 Cmdlet 會與彈性池相關聯。</span><span class="sxs-lookup"><span data-stu-id="1eb52-179">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="1eb52-180">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1eb52-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1eb52-181">-VCore</span><span class="sxs-lookup"><span data-stu-id="1eb52-181">-VCore</span></span>
<span data-ttu-id="1eb52-182">Sql Azure 彈性池的共用總 Vcores 數。</span><span class="sxs-lookup"><span data-stu-id="1eb52-182">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="1eb52-183">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="1eb52-183">-ZoneRedundant</span></span>
<span data-ttu-id="1eb52-184">要與 Azure Sql 彈性池建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="1eb52-184">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="1eb52-185">-確認</span><span class="sxs-lookup"><span data-stu-id="1eb52-185">-Confirm</span></span>
<span data-ttu-id="1eb52-186">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1eb52-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eb52-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb52-187">-WhatIf</span></span>
<span data-ttu-id="1eb52-188">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1eb52-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eb52-189">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1eb52-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eb52-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb52-190">CommonParameters</span></span>
<span data-ttu-id="1eb52-191">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1eb52-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb52-192">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1eb52-192">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb52-193">輸入</span><span class="sxs-lookup"><span data-stu-id="1eb52-193">INPUTS</span></span>

### <span data-ttu-id="1eb52-194">System.object</span><span class="sxs-lookup"><span data-stu-id="1eb52-194">System.String</span></span>

## <span data-ttu-id="1eb52-195">輸出</span><span class="sxs-lookup"><span data-stu-id="1eb52-195">OUTPUTS</span></span>

### <span data-ttu-id="1eb52-196">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="1eb52-196">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="1eb52-197">筆記</span><span class="sxs-lookup"><span data-stu-id="1eb52-197">NOTES</span></span>

## <span data-ttu-id="1eb52-198">相關連結</span><span class="sxs-lookup"><span data-stu-id="1eb52-198">RELATED LINKS</span></span>

[<span data-ttu-id="1eb52-199">AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1eb52-199">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="1eb52-200">AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="1eb52-200">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="1eb52-201">AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="1eb52-201">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="1eb52-202">移除-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1eb52-202">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="1eb52-203">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1eb52-203">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="1eb52-204">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1eb52-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
