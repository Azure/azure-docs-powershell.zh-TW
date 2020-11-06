---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 5b1901ef5d06d24e6561861dca3c8e1d89185d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448874"
---
# <span data-ttu-id="11af3-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="11af3-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="11af3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11af3-102">SYNOPSIS</span></span>
<span data-ttu-id="11af3-103">針對 SQL 資料庫建立彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="11af3-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11af3-104">句法</span><span class="sxs-lookup"><span data-stu-id="11af3-104">SYNTAX</span></span>

### <span data-ttu-id="11af3-105">DtuBasedPool (預設) </span><span class="sxs-lookup"><span data-stu-id="11af3-105">DtuBasedPool (Default)</span></span>
```
New-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11af3-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="11af3-106">VcoreBasedPool</span></span>
```
New-AzureRmSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11af3-107">說明</span><span class="sxs-lookup"><span data-stu-id="11af3-107">DESCRIPTION</span></span>
<span data-ttu-id="11af3-108">**新的-AzureRmSqlElasticPool** Cmdlet 會為 Azure SQL 資料庫建立彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="11af3-108">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="11af3-109">多個參數 ( *Dtu、-DatabaseDtuMin 及-DatabaseDtuMax* ) 需要設定的值來自該參數的有效值清單。</span><span class="sxs-lookup"><span data-stu-id="11af3-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="11af3-110">例如，標準 100 eDTU 池的-DatabaseDtuMax 只能設定為10、20、50或100。</span><span class="sxs-lookup"><span data-stu-id="11af3-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="11af3-111">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="11af3-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="11af3-112">示例</span><span class="sxs-lookup"><span data-stu-id="11af3-112">EXAMPLES</span></span>

### <span data-ttu-id="11af3-113">範例1：建立彈性池</span><span class="sxs-lookup"><span data-stu-id="11af3-113">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
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

<span data-ttu-id="11af3-114">這個命令會在名為 ElasticPool01 的標準服務層級中建立彈性池。</span><span class="sxs-lookup"><span data-stu-id="11af3-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="11af3-115">名為 server01 的伺服器，指派給名為 ResourceGroup01 的 Azure 資源群組，會將彈性池託管在其中。</span><span class="sxs-lookup"><span data-stu-id="11af3-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="11af3-116">此命令會為 pool 和 pool 中的資料庫指定 DTU 屬性值。</span><span class="sxs-lookup"><span data-stu-id="11af3-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="11af3-117">參數</span><span class="sxs-lookup"><span data-stu-id="11af3-117">PARAMETERS</span></span>

### <span data-ttu-id="11af3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11af3-118">-AsJob</span></span>
<span data-ttu-id="11af3-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11af3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11af3-120">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="11af3-120">-ComputeGeneration</span></span>
<span data-ttu-id="11af3-121">要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="11af3-121">The compute generation to assign.</span></span>

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

### <span data-ttu-id="11af3-122">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="11af3-122">-DatabaseDtuMax</span></span>
<span data-ttu-id="11af3-123">指定池中任何單一資料庫都可以使用的最大資料庫輸送量單位數量 (Dtu) 。</span><span class="sxs-lookup"><span data-stu-id="11af3-123">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="11af3-124">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="11af3-124">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="11af3-125">空白.</span><span class="sxs-lookup"><span data-stu-id="11af3-125">Basic.</span></span> <span data-ttu-id="11af3-126">5個 Dtu</span><span class="sxs-lookup"><span data-stu-id="11af3-126">5 DTUs</span></span>
- <span data-ttu-id="11af3-127">標準.</span><span class="sxs-lookup"><span data-stu-id="11af3-127">Standard.</span></span> <span data-ttu-id="11af3-128">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="11af3-128">100 DTUs</span></span>
- <span data-ttu-id="11af3-129">佳.</span><span class="sxs-lookup"><span data-stu-id="11af3-129">Premium.</span></span> <span data-ttu-id="11af3-130">125 Dtu 如需哪些值有效的詳細資料，請參閱[彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的表格</span><span class="sxs-lookup"><span data-stu-id="11af3-130">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="11af3-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="11af3-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="11af3-132">指定彈性池保證對池中所有資料庫的最小 Dtu 數。</span><span class="sxs-lookup"><span data-stu-id="11af3-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="11af3-133">預設值為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="11af3-133">The default value is zero (0).</span></span>
<span data-ttu-id="11af3-134">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="11af3-134">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="11af3-135">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="11af3-135">-DatabaseVCoreMax</span></span>
<span data-ttu-id="11af3-136">任何 SqlAzure 資料庫可在池中使用的 maxmium VCore 號碼。</span><span class="sxs-lookup"><span data-stu-id="11af3-136">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="11af3-137">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="11af3-137">-DatabaseVCoreMin</span></span>
<span data-ttu-id="11af3-138">任何 SqlAzure 資料庫可在池中使用的最小 VCore 數。</span><span class="sxs-lookup"><span data-stu-id="11af3-138">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="11af3-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11af3-139">-DefaultProfile</span></span>
<span data-ttu-id="11af3-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="11af3-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11af3-141">-Dtu</span><span class="sxs-lookup"><span data-stu-id="11af3-141">-Dtu</span></span>
<span data-ttu-id="11af3-142">指定彈性池的共用 Dtu 總數。</span><span class="sxs-lookup"><span data-stu-id="11af3-142">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="11af3-143">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="11af3-143">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="11af3-144">空白.</span><span class="sxs-lookup"><span data-stu-id="11af3-144">Basic.</span></span>
<span data-ttu-id="11af3-145">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="11af3-145">100 DTUs</span></span>
- <span data-ttu-id="11af3-146">標準.</span><span class="sxs-lookup"><span data-stu-id="11af3-146">Standard.</span></span>
<span data-ttu-id="11af3-147">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="11af3-147">100 DTUs</span></span>
- <span data-ttu-id="11af3-148">佳.</span><span class="sxs-lookup"><span data-stu-id="11af3-148">Premium.</span></span>
<span data-ttu-id="11af3-149">125 Dtu 如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的表格。</span><span class="sxs-lookup"><span data-stu-id="11af3-149">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="11af3-150">-Edition</span><span class="sxs-lookup"><span data-stu-id="11af3-150">-Edition</span></span>
<span data-ttu-id="11af3-151">指定用於彈性池的 Azure SQL 資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="11af3-151">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="11af3-152">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="11af3-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11af3-153">所有</span><span class="sxs-lookup"><span data-stu-id="11af3-153">None</span></span>
- <span data-ttu-id="11af3-154">空白</span><span class="sxs-lookup"><span data-stu-id="11af3-154">Basic</span></span>
- <span data-ttu-id="11af3-155">標準</span><span class="sxs-lookup"><span data-stu-id="11af3-155">Standard</span></span>
- <span data-ttu-id="11af3-156">佳</span><span class="sxs-lookup"><span data-stu-id="11af3-156">Premium</span></span>
- <span data-ttu-id="11af3-157">倉庫</span><span class="sxs-lookup"><span data-stu-id="11af3-157">DataWarehouse</span></span>
- <span data-ttu-id="11af3-158">空閒</span><span class="sxs-lookup"><span data-stu-id="11af3-158">Free</span></span>
- <span data-ttu-id="11af3-159">伸縮</span><span class="sxs-lookup"><span data-stu-id="11af3-159">Stretch</span></span>
- <span data-ttu-id="11af3-160">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="11af3-160">GeneralPurpose</span></span>
- <span data-ttu-id="11af3-161">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="11af3-161">BusinessCritical</span></span>

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

### <span data-ttu-id="11af3-162">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="11af3-162">-ElasticPoolName</span></span>
<span data-ttu-id="11af3-163">指定此 Cmdlet 所建立之彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="11af3-163">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="11af3-164">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="11af3-164">-LicenseType</span></span>
<span data-ttu-id="11af3-165">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="11af3-165">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="11af3-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11af3-166">-ResourceGroupName</span></span>
<span data-ttu-id="11af3-167">指定此 Cmdlet 指派彈性池之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11af3-167">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="11af3-168">-ServerName</span><span class="sxs-lookup"><span data-stu-id="11af3-168">-ServerName</span></span>
<span data-ttu-id="11af3-169">指定主持彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="11af3-169">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="11af3-170">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="11af3-170">-StorageMB</span></span>
<span data-ttu-id="11af3-171">指定彈性池的儲存空間限制（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="11af3-171">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="11af3-172">如果您沒有指定此參數，這個 Cmdlet 會根據 *Dtu* 參數的值來計算值。</span><span class="sxs-lookup"><span data-stu-id="11af3-172">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="11af3-173">請參閱可能值的 [eDTU 與儲存空間限制](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) 。</span><span class="sxs-lookup"><span data-stu-id="11af3-173">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="11af3-174">-標記</span><span class="sxs-lookup"><span data-stu-id="11af3-174">-Tags</span></span>
<span data-ttu-id="11af3-175">指定以雜湊資料表形式表示的鍵值對字典，此 Cmdlet 會與彈性池相關聯。</span><span class="sxs-lookup"><span data-stu-id="11af3-175">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="11af3-176">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="11af3-176">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="11af3-177">-VCore</span><span class="sxs-lookup"><span data-stu-id="11af3-177">-VCore</span></span>
<span data-ttu-id="11af3-178">Sql Azure 彈性池的共用總 Vcores 數。</span><span class="sxs-lookup"><span data-stu-id="11af3-178">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="11af3-179">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="11af3-179">-ZoneRedundant</span></span>
<span data-ttu-id="11af3-180">要與 Azure Sql 彈性池建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="11af3-180">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="11af3-181">-確認</span><span class="sxs-lookup"><span data-stu-id="11af3-181">-Confirm</span></span>
<span data-ttu-id="11af3-182">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11af3-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11af3-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11af3-183">-WhatIf</span></span>
<span data-ttu-id="11af3-184">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11af3-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11af3-185">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11af3-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11af3-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11af3-186">CommonParameters</span></span>
<span data-ttu-id="11af3-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11af3-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11af3-188">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11af3-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11af3-189">輸入</span><span class="sxs-lookup"><span data-stu-id="11af3-189">INPUTS</span></span>

### <span data-ttu-id="11af3-190">System.object</span><span class="sxs-lookup"><span data-stu-id="11af3-190">System.String</span></span>

## <span data-ttu-id="11af3-191">輸出</span><span class="sxs-lookup"><span data-stu-id="11af3-191">OUTPUTS</span></span>

### <span data-ttu-id="11af3-192">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="11af3-192">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="11af3-193">筆記</span><span class="sxs-lookup"><span data-stu-id="11af3-193">NOTES</span></span>

## <span data-ttu-id="11af3-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="11af3-194">RELATED LINKS</span></span>

[<span data-ttu-id="11af3-195">AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="11af3-195">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="11af3-196">AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="11af3-196">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="11af3-197">AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="11af3-197">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="11af3-198">移除-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="11af3-198">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="11af3-199">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="11af3-199">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="11af3-200">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="11af3-200">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)