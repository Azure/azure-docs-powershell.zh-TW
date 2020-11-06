---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 512c77862c44af68b26eb300eb9a692c115b0750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447906"
---
# <span data-ttu-id="5afe4-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5afe4-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="5afe4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5afe4-102">SYNOPSIS</span></span>
<span data-ttu-id="5afe4-103">修改 Azure SQL 資料庫中彈性資料庫池的屬性。</span><span class="sxs-lookup"><span data-stu-id="5afe4-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5afe4-104">句法</span><span class="sxs-lookup"><span data-stu-id="5afe4-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5afe4-105">說明</span><span class="sxs-lookup"><span data-stu-id="5afe4-105">DESCRIPTION</span></span>
<span data-ttu-id="5afe4-106">**AzureRmSqlElasticPool** Cmdlet 會修改 Azure SQL 資料庫中彈性資料庫池的屬性。</span><span class="sxs-lookup"><span data-stu-id="5afe4-106">The **Set-AzureRmSqlElasticPool** cmdlet modifies properties for an elastic database pool in an Azure SQL Database.</span></span> <span data-ttu-id="5afe4-107">這個 Cmdlet 可以針對每個資料庫修改最小的資料庫輸送量單位 (Dtu) ，除了每個資料庫的最大 Dtu、池子的 Dtu 數，以及池的儲存空間限制。</span><span class="sxs-lookup"><span data-stu-id="5afe4-107">This cmdlet can modify the minimum Database Throughput Units (DTUs) per database in addition to the maximum DTUs per database, the number of DTUs for the pool, and the storage limit for the pool.</span></span>

<span data-ttu-id="5afe4-108">多個參數 ( *Dtu、-DatabaseDtuMin 及-DatabaseDtuMax* ) 需要設定的值來自該參數的有效值清單。</span><span class="sxs-lookup"><span data-stu-id="5afe4-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="5afe4-109">例如，標準 100 eDTU 池的-DatabaseDtuMax 只能設定為10、20、50或100。</span><span class="sxs-lookup"><span data-stu-id="5afe4-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="5afe4-110">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="5afe4-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="5afe4-111">示例</span><span class="sxs-lookup"><span data-stu-id="5afe4-111">EXAMPLES</span></span>

### <span data-ttu-id="5afe4-112">範例1：修改彈性池的屬性</span><span class="sxs-lookup"><span data-stu-id="5afe4-112">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="5afe4-113">這個命令會修改名為 elasticpool01 的彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="5afe4-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="5afe4-114">此命令會將彈性池的 Dtu 數設定為1000，並設定最小和最大 Dtu。</span><span class="sxs-lookup"><span data-stu-id="5afe4-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="5afe4-115">範例2：修改彈性池的最大儲存空間</span><span class="sxs-lookup"><span data-stu-id="5afe4-115">Example 2: Modify the max storage of an elastic pool</span></span>
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

<span data-ttu-id="5afe4-116">這個命令會修改名為 elasticpool01 的彈性池的屬性。</span><span class="sxs-lookup"><span data-stu-id="5afe4-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="5afe4-117">此命令會將彈性池的最大儲存空間設定為 2 TB。</span><span class="sxs-lookup"><span data-stu-id="5afe4-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="5afe4-118">參數</span><span class="sxs-lookup"><span data-stu-id="5afe4-118">PARAMETERS</span></span>

### <span data-ttu-id="5afe4-119">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="5afe4-119">-DatabaseDtuMax</span></span>
<span data-ttu-id="5afe4-120">指定池中任何單一資料庫都能佔用的 Dtu 數目上限。</span><span class="sxs-lookup"><span data-stu-id="5afe4-120">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="5afe4-121">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="5afe4-121">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="5afe4-122">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="5afe4-122">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="5afe4-123">空白.</span><span class="sxs-lookup"><span data-stu-id="5afe4-123">Basic.</span></span>  <span data-ttu-id="5afe4-124">5個 Dtu</span><span class="sxs-lookup"><span data-stu-id="5afe4-124">5 DTUs</span></span>
- <span data-ttu-id="5afe4-125">標準.</span><span class="sxs-lookup"><span data-stu-id="5afe4-125">Standard.</span></span> <span data-ttu-id="5afe4-126">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="5afe4-126">100 DTUs</span></span>
- <span data-ttu-id="5afe4-127">佳.</span><span class="sxs-lookup"><span data-stu-id="5afe4-127">Premium.</span></span> <span data-ttu-id="5afe4-128">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="5afe4-128">125 DTUs</span></span>


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

### <span data-ttu-id="5afe4-129">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="5afe4-129">-DatabaseDtuMin</span></span>
<span data-ttu-id="5afe4-130">指定彈性池保證對池中所有資料庫的最小 Dtu 數。</span><span class="sxs-lookup"><span data-stu-id="5afe4-130">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="5afe4-131">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="5afe4-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="5afe4-132">預設值為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="5afe4-132">The default value is zero (0).</span></span>

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

### <span data-ttu-id="5afe4-133">-Dtu</span><span class="sxs-lookup"><span data-stu-id="5afe4-133">-Dtu</span></span>
<span data-ttu-id="5afe4-134">指定彈性池的共用 Dtu 總數。</span><span class="sxs-lookup"><span data-stu-id="5afe4-134">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="5afe4-135">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="5afe4-135">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="5afe4-136">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="5afe4-136">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="5afe4-137">空白.</span><span class="sxs-lookup"><span data-stu-id="5afe4-137">Basic.</span></span> <span data-ttu-id="5afe4-138">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="5afe4-138">100 DTUs</span></span>
- <span data-ttu-id="5afe4-139">標準.</span><span class="sxs-lookup"><span data-stu-id="5afe4-139">Standard.</span></span> <span data-ttu-id="5afe4-140">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="5afe4-140">100 DTUs</span></span>
- <span data-ttu-id="5afe4-141">佳.</span><span class="sxs-lookup"><span data-stu-id="5afe4-141">Premium.</span></span> <span data-ttu-id="5afe4-142">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="5afe4-142">125 DTUs</span></span>

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

### <span data-ttu-id="5afe4-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="5afe4-143">-Edition</span></span>
<span data-ttu-id="5afe4-144">指定彈性池的 Azure SQL Database 版本。</span><span class="sxs-lookup"><span data-stu-id="5afe4-144">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="5afe4-145">您無法變更版本。</span><span class="sxs-lookup"><span data-stu-id="5afe4-145">You cannot change the edition.</span></span> <span data-ttu-id="5afe4-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5afe4-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5afe4-147">所有</span><span class="sxs-lookup"><span data-stu-id="5afe4-147">None</span></span>
- <span data-ttu-id="5afe4-148">空白</span><span class="sxs-lookup"><span data-stu-id="5afe4-148">Basic</span></span>
- <span data-ttu-id="5afe4-149">標準</span><span class="sxs-lookup"><span data-stu-id="5afe4-149">Standard</span></span>
- <span data-ttu-id="5afe4-150">佳</span><span class="sxs-lookup"><span data-stu-id="5afe4-150">Premium</span></span>
- <span data-ttu-id="5afe4-151">PremiumRS</span><span class="sxs-lookup"><span data-stu-id="5afe4-151">PremiumRS</span></span>
- <span data-ttu-id="5afe4-152">倉庫</span><span class="sxs-lookup"><span data-stu-id="5afe4-152">DataWarehouse</span></span>
- <span data-ttu-id="5afe4-153">空閒</span><span class="sxs-lookup"><span data-stu-id="5afe4-153">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5afe4-154">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5afe4-154">-ElasticPoolName</span></span>
<span data-ttu-id="5afe4-155">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="5afe4-155">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="5afe4-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5afe4-156">-ResourceGroupName</span></span>
<span data-ttu-id="5afe4-157">指定將彈性池指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5afe4-157">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="5afe4-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5afe4-158">-ServerName</span></span>
<span data-ttu-id="5afe4-159">指定主持彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="5afe4-159">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="5afe4-160">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="5afe4-160">-StorageMB</span></span>
<span data-ttu-id="5afe4-161">指定彈性池的儲存空間限制（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="5afe4-161">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="5afe4-162">如需詳細資訊，請參閱 New-AzureRmSqlElasticPool Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5afe4-162">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="5afe4-163">-標記</span><span class="sxs-lookup"><span data-stu-id="5afe4-163">-Tags</span></span>
<span data-ttu-id="5afe4-164">指定一個鍵值對的字典，此 Cmdlet 會以雜湊資料表的形式與彈性池相關聯。</span><span class="sxs-lookup"><span data-stu-id="5afe4-164">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="5afe4-165">例如：</span><span class="sxs-lookup"><span data-stu-id="5afe4-165">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="5afe4-166">-確認</span><span class="sxs-lookup"><span data-stu-id="5afe4-166">-Confirm</span></span>
<span data-ttu-id="5afe4-167">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5afe4-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5afe4-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5afe4-168">-WhatIf</span></span>
<span data-ttu-id="5afe4-169">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5afe4-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5afe4-170">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5afe4-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5afe4-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5afe4-171">-DefaultProfile</span></span>
<span data-ttu-id="5afe4-172">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5afe4-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5afe4-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5afe4-173">CommonParameters</span></span>
<span data-ttu-id="5afe4-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5afe4-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5afe4-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5afe4-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5afe4-176">輸入</span><span class="sxs-lookup"><span data-stu-id="5afe4-176">INPUTS</span></span>

## <span data-ttu-id="5afe4-177">輸出</span><span class="sxs-lookup"><span data-stu-id="5afe4-177">OUTPUTS</span></span>

### <span data-ttu-id="5afe4-178">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="5afe4-178">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="5afe4-179">筆記</span><span class="sxs-lookup"><span data-stu-id="5afe4-179">NOTES</span></span>

## <span data-ttu-id="5afe4-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="5afe4-180">RELATED LINKS</span></span>

[<span data-ttu-id="5afe4-181">AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5afe4-181">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="5afe4-182">AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="5afe4-182">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="5afe4-183">AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="5afe4-183">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="5afe4-184">新-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5afe4-184">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="5afe4-185">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="5afe4-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
