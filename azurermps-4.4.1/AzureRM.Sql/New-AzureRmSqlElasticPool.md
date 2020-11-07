---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 454aac300aa3b34cbc435df455100d64c5d0abdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626586"
---
# <span data-ttu-id="c008d-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c008d-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="c008d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c008d-102">SYNOPSIS</span></span>
<span data-ttu-id="c008d-103">針對 SQL 資料庫建立彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="c008d-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c008d-104">句法</span><span class="sxs-lookup"><span data-stu-id="c008d-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c008d-105">說明</span><span class="sxs-lookup"><span data-stu-id="c008d-105">DESCRIPTION</span></span>
<span data-ttu-id="c008d-106">**新的-AzureRmSqlElasticPool** Cmdlet 會為 Azure SQL 資料庫建立彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="c008d-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="c008d-107">多個參數 ( *Dtu、-DatabaseDtuMin 及-DatabaseDtuMax* ) 需要設定的值來自該參數的有效值清單。</span><span class="sxs-lookup"><span data-stu-id="c008d-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="c008d-108">例如，標準 100 eDTU 池的-DatabaseDtuMax 只能設定為10、20、50或100。</span><span class="sxs-lookup"><span data-stu-id="c008d-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="c008d-109">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="c008d-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="c008d-110">示例</span><span class="sxs-lookup"><span data-stu-id="c008d-110">EXAMPLES</span></span>

### <span data-ttu-id="c008d-111">範例1：建立彈性池</span><span class="sxs-lookup"><span data-stu-id="c008d-111">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="c008d-112">這個命令會在名為 ElasticPool01 的標準服務層級中建立彈性池。</span><span class="sxs-lookup"><span data-stu-id="c008d-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="c008d-113">名為 server01 的伺服器，指派給名為 ResourceGroup01 的 Azure 資源群組，會將彈性池託管在其中。</span><span class="sxs-lookup"><span data-stu-id="c008d-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="c008d-114">此命令會為 pool 和 pool 中的資料庫指定 DTU 屬性值。</span><span class="sxs-lookup"><span data-stu-id="c008d-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="c008d-115">參數</span><span class="sxs-lookup"><span data-stu-id="c008d-115">PARAMETERS</span></span>

### <span data-ttu-id="c008d-116">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="c008d-116">-DatabaseDtuMax</span></span>
<span data-ttu-id="c008d-117">指定池中任何單一資料庫都可以使用的最大資料庫輸送量單位數量 (Dtu) 。</span><span class="sxs-lookup"><span data-stu-id="c008d-117">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="c008d-118">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="c008d-118">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="c008d-119">空白.</span><span class="sxs-lookup"><span data-stu-id="c008d-119">Basic.</span></span> <span data-ttu-id="c008d-120">5個 Dtu</span><span class="sxs-lookup"><span data-stu-id="c008d-120">5 DTUs</span></span>
- <span data-ttu-id="c008d-121">標準.</span><span class="sxs-lookup"><span data-stu-id="c008d-121">Standard.</span></span> <span data-ttu-id="c008d-122">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="c008d-122">100 DTUs</span></span>
- <span data-ttu-id="c008d-123">佳.</span><span class="sxs-lookup"><span data-stu-id="c008d-123">Premium.</span></span> <span data-ttu-id="c008d-124">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="c008d-124">125 DTUs</span></span>

<span data-ttu-id="c008d-125">如需哪些值有效的詳細資料，請參閱[彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表</span><span class="sxs-lookup"><span data-stu-id="c008d-125">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


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

### <span data-ttu-id="c008d-126">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="c008d-126">-DatabaseDtuMin</span></span>
<span data-ttu-id="c008d-127">指定彈性池保證對池中所有資料庫的最小 Dtu 數。</span><span class="sxs-lookup"><span data-stu-id="c008d-127">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="c008d-128">預設值為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="c008d-128">The default value is zero (0).</span></span>

<span data-ttu-id="c008d-129">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="c008d-129">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="c008d-130">-Dtu</span><span class="sxs-lookup"><span data-stu-id="c008d-130">-Dtu</span></span>
<span data-ttu-id="c008d-131">指定彈性池的共用 Dtu 總數。</span><span class="sxs-lookup"><span data-stu-id="c008d-131">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="c008d-132">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="c008d-132">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="c008d-133">空白.</span><span class="sxs-lookup"><span data-stu-id="c008d-133">Basic.</span></span>
<span data-ttu-id="c008d-134">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="c008d-134">100 DTUs</span></span>
- <span data-ttu-id="c008d-135">標準.</span><span class="sxs-lookup"><span data-stu-id="c008d-135">Standard.</span></span>
<span data-ttu-id="c008d-136">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="c008d-136">100 DTUs</span></span>
- <span data-ttu-id="c008d-137">佳.</span><span class="sxs-lookup"><span data-stu-id="c008d-137">Premium.</span></span>
<span data-ttu-id="c008d-138">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="c008d-138">125 DTUs</span></span>

<span data-ttu-id="c008d-139">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="c008d-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="c008d-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="c008d-140">-Edition</span></span>
<span data-ttu-id="c008d-141">指定用於彈性池的 Azure SQL 資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="c008d-141">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="c008d-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c008d-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c008d-143">佳</span><span class="sxs-lookup"><span data-stu-id="c008d-143">Premium</span></span>
- <span data-ttu-id="c008d-144">空白</span><span class="sxs-lookup"><span data-stu-id="c008d-144">Basic</span></span>
- <span data-ttu-id="c008d-145">標準</span><span class="sxs-lookup"><span data-stu-id="c008d-145">Standard</span></span>
- <span data-ttu-id="c008d-146">倉庫</span><span class="sxs-lookup"><span data-stu-id="c008d-146">DataWarehouse</span></span>
- <span data-ttu-id="c008d-147">伸縮</span><span class="sxs-lookup"><span data-stu-id="c008d-147">Stretch</span></span>
- <span data-ttu-id="c008d-148">空閒</span><span class="sxs-lookup"><span data-stu-id="c008d-148">Free</span></span>
- <span data-ttu-id="c008d-149">PremiumRS</span><span class="sxs-lookup"><span data-stu-id="c008d-149">PremiumRS</span></span>

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

### <span data-ttu-id="c008d-150">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c008d-150">-ElasticPoolName</span></span>
<span data-ttu-id="c008d-151">指定此 Cmdlet 所建立之彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="c008d-151">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c008d-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c008d-152">-ResourceGroupName</span></span>
<span data-ttu-id="c008d-153">指定此 Cmdlet 指派彈性池之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c008d-153">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="c008d-154">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c008d-154">-ServerName</span></span>
<span data-ttu-id="c008d-155">指定主持彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c008d-155">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="c008d-156">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="c008d-156">-StorageMB</span></span>
<span data-ttu-id="c008d-157">指定彈性池的儲存空間限制（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="c008d-157">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="c008d-158">如果您沒有指定此參數，這個 Cmdlet 會根據 *Dtu* 參數的值來計算值。</span><span class="sxs-lookup"><span data-stu-id="c008d-158">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="c008d-159">請參閱可能值的 [eDTU 與儲存空間限制](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) 。</span><span class="sxs-lookup"><span data-stu-id="c008d-159">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="c008d-160">-標記</span><span class="sxs-lookup"><span data-stu-id="c008d-160">-Tags</span></span>
<span data-ttu-id="c008d-161">指定以雜湊資料表形式表示的鍵值對字典，此 Cmdlet 會與彈性池相關聯。</span><span class="sxs-lookup"><span data-stu-id="c008d-161">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="c008d-162">例如：</span><span class="sxs-lookup"><span data-stu-id="c008d-162">For example:</span></span>

<span data-ttu-id="c008d-163">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c008d-163">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c008d-164">-確認</span><span class="sxs-lookup"><span data-stu-id="c008d-164">-Confirm</span></span>
<span data-ttu-id="c008d-165">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c008d-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c008d-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c008d-166">-WhatIf</span></span>
<span data-ttu-id="c008d-167">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c008d-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c008d-168">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c008d-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c008d-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c008d-169">-DefaultProfile</span></span>
<span data-ttu-id="c008d-170">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c008d-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c008d-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c008d-171">CommonParameters</span></span>
<span data-ttu-id="c008d-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c008d-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c008d-173">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c008d-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c008d-174">輸入</span><span class="sxs-lookup"><span data-stu-id="c008d-174">INPUTS</span></span>

## <span data-ttu-id="c008d-175">輸出</span><span class="sxs-lookup"><span data-stu-id="c008d-175">OUTPUTS</span></span>

### <span data-ttu-id="c008d-176">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="c008d-176">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="c008d-177">筆記</span><span class="sxs-lookup"><span data-stu-id="c008d-177">NOTES</span></span>

## <span data-ttu-id="c008d-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="c008d-178">RELATED LINKS</span></span>

[<span data-ttu-id="c008d-179">AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c008d-179">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c008d-180">AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="c008d-180">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="c008d-181">AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="c008d-181">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="c008d-182">移除-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c008d-182">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c008d-183">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c008d-183">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c008d-184">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c008d-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
