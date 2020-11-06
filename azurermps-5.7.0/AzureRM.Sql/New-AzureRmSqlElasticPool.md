---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3d93b0d82a2769acce620ce97141be68c003c281
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450451"
---
# <span data-ttu-id="30f52-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="30f52-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="30f52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30f52-102">SYNOPSIS</span></span>
<span data-ttu-id="30f52-103">針對 SQL 資料庫建立彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="30f52-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30f52-104">句法</span><span class="sxs-lookup"><span data-stu-id="30f52-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30f52-105">說明</span><span class="sxs-lookup"><span data-stu-id="30f52-105">DESCRIPTION</span></span>
<span data-ttu-id="30f52-106">**新的-AzureRmSqlElasticPool** Cmdlet 會為 Azure SQL 資料庫建立彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="30f52-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="30f52-107">多個參數 ( *Dtu、-DatabaseDtuMin 及-DatabaseDtuMax* ) 需要設定的值來自該參數的有效值清單。</span><span class="sxs-lookup"><span data-stu-id="30f52-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="30f52-108">例如，標準 100 eDTU 池的-DatabaseDtuMax 只能設定為10、20、50或100。</span><span class="sxs-lookup"><span data-stu-id="30f52-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="30f52-109">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="30f52-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="30f52-110">示例</span><span class="sxs-lookup"><span data-stu-id="30f52-110">EXAMPLES</span></span>

### <span data-ttu-id="30f52-111">範例1：建立彈性池</span><span class="sxs-lookup"><span data-stu-id="30f52-111">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="30f52-112">這個命令會在名為 ElasticPool01 的標準服務層級中建立彈性池。</span><span class="sxs-lookup"><span data-stu-id="30f52-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="30f52-113">名為 server01 的伺服器，指派給名為 ResourceGroup01 的 Azure 資源群組，會將彈性池託管在其中。</span><span class="sxs-lookup"><span data-stu-id="30f52-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="30f52-114">此命令會為 pool 和 pool 中的資料庫指定 DTU 屬性值。</span><span class="sxs-lookup"><span data-stu-id="30f52-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="30f52-115">參數</span><span class="sxs-lookup"><span data-stu-id="30f52-115">PARAMETERS</span></span>

### <span data-ttu-id="30f52-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30f52-116">-AsJob</span></span>
<span data-ttu-id="30f52-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="30f52-117">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-118">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="30f52-118">-DatabaseDtuMax</span></span>
<span data-ttu-id="30f52-119">指定池中任何單一資料庫都可以使用的最大資料庫輸送量單位數量 (Dtu) 。</span><span class="sxs-lookup"><span data-stu-id="30f52-119">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="30f52-120">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="30f52-120">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="30f52-121">空白.</span><span class="sxs-lookup"><span data-stu-id="30f52-121">Basic.</span></span> <span data-ttu-id="30f52-122">5個 Dtu</span><span class="sxs-lookup"><span data-stu-id="30f52-122">5 DTUs</span></span>
- <span data-ttu-id="30f52-123">標準.</span><span class="sxs-lookup"><span data-stu-id="30f52-123">Standard.</span></span> <span data-ttu-id="30f52-124">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="30f52-124">100 DTUs</span></span>
- <span data-ttu-id="30f52-125">佳.</span><span class="sxs-lookup"><span data-stu-id="30f52-125">Premium.</span></span> <span data-ttu-id="30f52-126">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="30f52-126">125 DTUs</span></span>

<span data-ttu-id="30f52-127">如需哪些值有效的詳細資料，請參閱[彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表</span><span class="sxs-lookup"><span data-stu-id="30f52-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-128">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="30f52-128">-DatabaseDtuMin</span></span>
<span data-ttu-id="30f52-129">指定彈性池保證對池中所有資料庫的最小 Dtu 數。</span><span class="sxs-lookup"><span data-stu-id="30f52-129">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="30f52-130">預設值為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="30f52-130">The default value is zero (0).</span></span>

<span data-ttu-id="30f52-131">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="30f52-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f52-132">-DefaultProfile</span></span>
<span data-ttu-id="30f52-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="30f52-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-134">-Dtu</span><span class="sxs-lookup"><span data-stu-id="30f52-134">-Dtu</span></span>
<span data-ttu-id="30f52-135">指定彈性池的共用 Dtu 總數。</span><span class="sxs-lookup"><span data-stu-id="30f52-135">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="30f52-136">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="30f52-136">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="30f52-137">空白.</span><span class="sxs-lookup"><span data-stu-id="30f52-137">Basic.</span></span>
<span data-ttu-id="30f52-138">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="30f52-138">100 DTUs</span></span>
- <span data-ttu-id="30f52-139">標準.</span><span class="sxs-lookup"><span data-stu-id="30f52-139">Standard.</span></span>
<span data-ttu-id="30f52-140">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="30f52-140">100 DTUs</span></span>
- <span data-ttu-id="30f52-141">佳.</span><span class="sxs-lookup"><span data-stu-id="30f52-141">Premium.</span></span>
<span data-ttu-id="30f52-142">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="30f52-142">125 DTUs</span></span>

<span data-ttu-id="30f52-143">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="30f52-143">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-144">-Edition</span><span class="sxs-lookup"><span data-stu-id="30f52-144">-Edition</span></span>
<span data-ttu-id="30f52-145">指定用於彈性池的 Azure SQL 資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="30f52-145">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="30f52-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="30f52-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30f52-147">佳</span><span class="sxs-lookup"><span data-stu-id="30f52-147">Premium</span></span>
- <span data-ttu-id="30f52-148">空白</span><span class="sxs-lookup"><span data-stu-id="30f52-148">Basic</span></span>
- <span data-ttu-id="30f52-149">標準</span><span class="sxs-lookup"><span data-stu-id="30f52-149">Standard</span></span>
- <span data-ttu-id="30f52-150">倉庫</span><span class="sxs-lookup"><span data-stu-id="30f52-150">DataWarehouse</span></span>
- <span data-ttu-id="30f52-151">伸縮</span><span class="sxs-lookup"><span data-stu-id="30f52-151">Stretch</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="30f52-152">-ElasticPoolName</span></span>
<span data-ttu-id="30f52-153">指定此 Cmdlet 所建立之彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="30f52-153">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f52-154">-ResourceGroupName</span></span>
<span data-ttu-id="30f52-155">指定此 Cmdlet 指派彈性池之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="30f52-155">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="30f52-156">-ServerName</span></span>
<span data-ttu-id="30f52-157">指定主持彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="30f52-157">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-158">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="30f52-158">-StorageMB</span></span>
<span data-ttu-id="30f52-159">指定彈性池的儲存空間限制（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="30f52-159">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="30f52-160">如果您沒有指定此參數，這個 Cmdlet 會根據 *Dtu* 參數的值來計算值。</span><span class="sxs-lookup"><span data-stu-id="30f52-160">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="30f52-161">請參閱可能值的 [eDTU 與儲存空間限制](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) 。</span><span class="sxs-lookup"><span data-stu-id="30f52-161">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-162">-標記</span><span class="sxs-lookup"><span data-stu-id="30f52-162">-Tags</span></span>
<span data-ttu-id="30f52-163">指定以雜湊資料表形式表示的鍵值對字典，此 Cmdlet 會與彈性池相關聯。</span><span class="sxs-lookup"><span data-stu-id="30f52-163">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="30f52-164">例如：</span><span class="sxs-lookup"><span data-stu-id="30f52-164">For example:</span></span>

<span data-ttu-id="30f52-165">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="30f52-165">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-166">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="30f52-166">-ZoneRedundant</span></span>
<span data-ttu-id="30f52-167">要與 Azure Sql 彈性池建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="30f52-167">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-168">-確認</span><span class="sxs-lookup"><span data-stu-id="30f52-168">-Confirm</span></span>
<span data-ttu-id="30f52-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30f52-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f52-170">-WhatIf</span></span>
<span data-ttu-id="30f52-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30f52-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30f52-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30f52-172">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f52-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f52-173">CommonParameters</span></span>
<span data-ttu-id="30f52-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30f52-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f52-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30f52-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f52-176">輸入</span><span class="sxs-lookup"><span data-stu-id="30f52-176">INPUTS</span></span>

### <span data-ttu-id="30f52-177">所有</span><span class="sxs-lookup"><span data-stu-id="30f52-177">None</span></span>
<span data-ttu-id="30f52-178">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="30f52-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30f52-179">輸出</span><span class="sxs-lookup"><span data-stu-id="30f52-179">OUTPUTS</span></span>

### <span data-ttu-id="30f52-180">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="30f52-180">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="30f52-181">筆記</span><span class="sxs-lookup"><span data-stu-id="30f52-181">NOTES</span></span>

## <span data-ttu-id="30f52-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="30f52-182">RELATED LINKS</span></span>

[<span data-ttu-id="30f52-183">AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="30f52-183">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="30f52-184">AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="30f52-184">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="30f52-185">AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="30f52-185">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="30f52-186">移除-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="30f52-186">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="30f52-187">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="30f52-187">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="30f52-188">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="30f52-188">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
