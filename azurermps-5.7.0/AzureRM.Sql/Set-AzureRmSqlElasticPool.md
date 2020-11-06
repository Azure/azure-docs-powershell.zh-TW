---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 563cddc1723f0706eb5cdde691e9ab960e871989
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450431"
---
# <span data-ttu-id="4df15-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4df15-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="4df15-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4df15-102">SYNOPSIS</span></span>
<span data-ttu-id="4df15-103">修改 Azure SQL 資料庫中彈性資料庫池的屬性。</span><span class="sxs-lookup"><span data-stu-id="4df15-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4df15-104">句法</span><span class="sxs-lookup"><span data-stu-id="4df15-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4df15-105">說明</span><span class="sxs-lookup"><span data-stu-id="4df15-105">DESCRIPTION</span></span>
<span data-ttu-id="4df15-106">**AzureRmSqlElasticPool** Cmdlet 會在 Azure SQL Database 中設定彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="4df15-106">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="4df15-107">這個 Cmdlet 可以針對每個池 ( *Dtu* ) 、每個池 ( *StorageMB* ) 、每個資料庫最大 eDTUs ( *DatabaseDtuMax* ) ，以及每個資料庫 () *eDTUs* 的每個 DatqabaseDtuMin 的儲存空間大小。</span><span class="sxs-lookup"><span data-stu-id="4df15-107">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>

<span data-ttu-id="4df15-108">多個參數 ( *Dtu、-DatabaseDtuMin 及-DatabaseDtuMax* ) 需要設定的值來自該參數的有效值清單。</span><span class="sxs-lookup"><span data-stu-id="4df15-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="4df15-109">例如，標準 100 eDTU 池的-DatabaseDtuMax 只能設定為10、20、50或100。</span><span class="sxs-lookup"><span data-stu-id="4df15-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="4df15-110">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="4df15-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="4df15-111">示例</span><span class="sxs-lookup"><span data-stu-id="4df15-111">EXAMPLES</span></span>

### <span data-ttu-id="4df15-112">範例1：修改彈性池的屬性</span><span class="sxs-lookup"><span data-stu-id="4df15-112">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
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

<span data-ttu-id="4df15-113">這個命令會修改名為 elasticpool01 的彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="4df15-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="4df15-114">此命令會將彈性池的 Dtu 數設定為1000，並設定最小和最大 Dtu。</span><span class="sxs-lookup"><span data-stu-id="4df15-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="4df15-115">範例2：修改彈性池的儲存空間大小上限</span><span class="sxs-lookup"><span data-stu-id="4df15-115">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
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

<span data-ttu-id="4df15-116">這個命令會修改名為 elasticpool01 的彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="4df15-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="4df15-117">此命令會將彈性池的最大儲存空間設定為 2 TB。</span><span class="sxs-lookup"><span data-stu-id="4df15-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="4df15-118">參數</span><span class="sxs-lookup"><span data-stu-id="4df15-118">PARAMETERS</span></span>

### <span data-ttu-id="4df15-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4df15-119">-AsJob</span></span>
<span data-ttu-id="4df15-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4df15-120">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="4df15-121">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="4df15-121">-DatabaseDtuMax</span></span>
<span data-ttu-id="4df15-122">指定池中任何單一資料庫都能佔用的 Dtu 數目上限。</span><span class="sxs-lookup"><span data-stu-id="4df15-122">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="4df15-123">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="4df15-123">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="4df15-124">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="4df15-124">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="4df15-125">空白.</span><span class="sxs-lookup"><span data-stu-id="4df15-125">Basic.</span></span>  <span data-ttu-id="4df15-126">5個 Dtu</span><span class="sxs-lookup"><span data-stu-id="4df15-126">5 DTUs</span></span>
- <span data-ttu-id="4df15-127">標準.</span><span class="sxs-lookup"><span data-stu-id="4df15-127">Standard.</span></span> <span data-ttu-id="4df15-128">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="4df15-128">100 DTUs</span></span>
- <span data-ttu-id="4df15-129">佳.</span><span class="sxs-lookup"><span data-stu-id="4df15-129">Premium.</span></span> <span data-ttu-id="4df15-130">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="4df15-130">125 DTUs</span></span>


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

### <span data-ttu-id="4df15-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="4df15-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="4df15-132">指定彈性池保證對池中所有資料庫的最小 Dtu 數。</span><span class="sxs-lookup"><span data-stu-id="4df15-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="4df15-133">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="4df15-133">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="4df15-134">預設值為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="4df15-134">The default value is zero (0).</span></span>

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

### <span data-ttu-id="4df15-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df15-135">-DefaultProfile</span></span>
<span data-ttu-id="4df15-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4df15-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4df15-137">-Dtu</span><span class="sxs-lookup"><span data-stu-id="4df15-137">-Dtu</span></span>
<span data-ttu-id="4df15-138">指定彈性池的共用 Dtu 總數。</span><span class="sxs-lookup"><span data-stu-id="4df15-138">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="4df15-139">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="4df15-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="4df15-140">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="4df15-140">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="4df15-141">空白.</span><span class="sxs-lookup"><span data-stu-id="4df15-141">Basic.</span></span> <span data-ttu-id="4df15-142">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="4df15-142">100 DTUs</span></span>
- <span data-ttu-id="4df15-143">標準.</span><span class="sxs-lookup"><span data-stu-id="4df15-143">Standard.</span></span> <span data-ttu-id="4df15-144">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="4df15-144">100 DTUs</span></span>
- <span data-ttu-id="4df15-145">佳.</span><span class="sxs-lookup"><span data-stu-id="4df15-145">Premium.</span></span> <span data-ttu-id="4df15-146">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="4df15-146">125 DTUs</span></span>

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

### <span data-ttu-id="4df15-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="4df15-147">-Edition</span></span>
<span data-ttu-id="4df15-148">指定彈性池的 Azure SQL Database 版本。</span><span class="sxs-lookup"><span data-stu-id="4df15-148">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="4df15-149">您無法變更版本。</span><span class="sxs-lookup"><span data-stu-id="4df15-149">You cannot change the edition.</span></span> <span data-ttu-id="4df15-150">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4df15-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4df15-151">所有</span><span class="sxs-lookup"><span data-stu-id="4df15-151">None</span></span>
- <span data-ttu-id="4df15-152">空白</span><span class="sxs-lookup"><span data-stu-id="4df15-152">Basic</span></span>
- <span data-ttu-id="4df15-153">標準</span><span class="sxs-lookup"><span data-stu-id="4df15-153">Standard</span></span>
- <span data-ttu-id="4df15-154">佳</span><span class="sxs-lookup"><span data-stu-id="4df15-154">Premium</span></span>
- <span data-ttu-id="4df15-155">倉庫</span><span class="sxs-lookup"><span data-stu-id="4df15-155">DataWarehouse</span></span>

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

### <span data-ttu-id="4df15-156">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4df15-156">-ElasticPoolName</span></span>
<span data-ttu-id="4df15-157">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="4df15-157">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df15-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df15-158">-ResourceGroupName</span></span>
<span data-ttu-id="4df15-159">指定將彈性池指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4df15-159">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="4df15-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4df15-160">-ServerName</span></span>
<span data-ttu-id="4df15-161">指定主持彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="4df15-161">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="4df15-162">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="4df15-162">-StorageMB</span></span>
<span data-ttu-id="4df15-163">指定彈性池的儲存空間限制（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="4df15-163">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="4df15-164">如需詳細資訊，請參閱 New-AzureRmSqlElasticPool Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4df15-164">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="4df15-165">-標記</span><span class="sxs-lookup"><span data-stu-id="4df15-165">-Tags</span></span>
<span data-ttu-id="4df15-166">指定一個鍵值對的字典，此 Cmdlet 會以雜湊資料表的形式與彈性池相關聯。</span><span class="sxs-lookup"><span data-stu-id="4df15-166">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="4df15-167">例如：</span><span class="sxs-lookup"><span data-stu-id="4df15-167">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="4df15-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="4df15-168">-ZoneRedundant</span></span>
<span data-ttu-id="4df15-169">要與 Azure Sql 彈性池建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="4df15-169">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="4df15-170">-確認</span><span class="sxs-lookup"><span data-stu-id="4df15-170">-Confirm</span></span>
<span data-ttu-id="4df15-171">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4df15-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4df15-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4df15-172">-WhatIf</span></span>
<span data-ttu-id="4df15-173">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4df15-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4df15-174">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4df15-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4df15-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df15-175">CommonParameters</span></span>
<span data-ttu-id="4df15-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4df15-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df15-177">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4df15-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df15-178">輸入</span><span class="sxs-lookup"><span data-stu-id="4df15-178">INPUTS</span></span>

### <span data-ttu-id="4df15-179">所有</span><span class="sxs-lookup"><span data-stu-id="4df15-179">None</span></span>
<span data-ttu-id="4df15-180">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4df15-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4df15-181">輸出</span><span class="sxs-lookup"><span data-stu-id="4df15-181">OUTPUTS</span></span>

### <span data-ttu-id="4df15-182">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="4df15-182">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="4df15-183">筆記</span><span class="sxs-lookup"><span data-stu-id="4df15-183">NOTES</span></span>

## <span data-ttu-id="4df15-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="4df15-184">RELATED LINKS</span></span>

[<span data-ttu-id="4df15-185">AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4df15-185">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4df15-186">AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="4df15-186">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="4df15-187">AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="4df15-187">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="4df15-188">新-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4df15-188">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4df15-189">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="4df15-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
