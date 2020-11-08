---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fed3f32f5ff0a9920b87438b75cb25cee7c9217
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127291"
---
# <span data-ttu-id="0cc59-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0cc59-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="0cc59-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0cc59-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc59-103">針對 SQL 資料庫建立彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="0cc59-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="0cc59-104">句法</span><span class="sxs-lookup"><span data-stu-id="0cc59-104">SYNTAX</span></span>

### <span data-ttu-id="0cc59-105">DtuBasedPool (預設) </span><span class="sxs-lookup"><span data-stu-id="0cc59-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cc59-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="0cc59-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cc59-107">說明</span><span class="sxs-lookup"><span data-stu-id="0cc59-107">DESCRIPTION</span></span>
<span data-ttu-id="0cc59-108">**新的-AzSqlElasticPool** Cmdlet 會為 Azure SQL 資料庫建立彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="0cc59-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="0cc59-109">多個參數 ( *Dtu、-DatabaseDtuMin 及-DatabaseDtuMax* ) 需要設定的值來自該參數的有效值清單。</span><span class="sxs-lookup"><span data-stu-id="0cc59-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="0cc59-110">例如，標準 100 eDTU 池的-DatabaseDtuMax 只能設定為10、20、50或100。</span><span class="sxs-lookup"><span data-stu-id="0cc59-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="0cc59-111">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="0cc59-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="0cc59-112">示例</span><span class="sxs-lookup"><span data-stu-id="0cc59-112">EXAMPLES</span></span>

### <span data-ttu-id="0cc59-113">範例1：建立 DTU 彈性池</span><span class="sxs-lookup"><span data-stu-id="0cc59-113">Example 1: Create a DTU elastic pool</span></span>

```powershell
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

<span data-ttu-id="0cc59-114">這個命令會在名為 ElasticPool01 的標準服務層級中建立彈性池。</span><span class="sxs-lookup"><span data-stu-id="0cc59-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="0cc59-115">名為 server01 的伺服器，指派給名為 ResourceGroup01 的 Azure 資源群組，會將彈性池託管在其中。</span><span class="sxs-lookup"><span data-stu-id="0cc59-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="0cc59-116">此命令會為 pool 和 pool 中的資料庫指定 DTU 屬性值。</span><span class="sxs-lookup"><span data-stu-id="0cc59-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="0cc59-117">範例2：建立 vCore 彈性池</span><span class="sxs-lookup"><span data-stu-id="0cc59-117">Example 2: Create a vCore elastic pool</span></span>

```powershell
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

<span data-ttu-id="0cc59-118">這個命令會在 GengeralPurpose 服務層級（名為 ElasticPool01）中建立彈性池。</span><span class="sxs-lookup"><span data-stu-id="0cc59-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="0cc59-119">名為 server01 的伺服器，指派給名為 ResourceGroup01 的 Azure 資源群組，會將彈性池託管在其中。</span><span class="sxs-lookup"><span data-stu-id="0cc59-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="0cc59-120">此命令會指定池的 vCore 屬性值，以及池中的資料庫。</span><span class="sxs-lookup"><span data-stu-id="0cc59-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="0cc59-121">範例3</span><span class="sxs-lookup"><span data-stu-id="0cc59-121">Example 3</span></span>

<span data-ttu-id="0cc59-122">針對 SQL 資料庫建立彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="0cc59-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="0cc59-123"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="0cc59-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="0cc59-124">參數</span><span class="sxs-lookup"><span data-stu-id="0cc59-124">PARAMETERS</span></span>

### <span data-ttu-id="0cc59-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cc59-125">-AsJob</span></span>
<span data-ttu-id="0cc59-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0cc59-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0cc59-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0cc59-127">-ComputeGeneration</span></span>
<span data-ttu-id="0cc59-128">要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="0cc59-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="0cc59-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="0cc59-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="0cc59-130">指定池中任何單一資料庫都可以使用的最大資料庫輸送量單位數量 (Dtu) 。</span><span class="sxs-lookup"><span data-stu-id="0cc59-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="0cc59-131">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="0cc59-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="0cc59-132">空白.</span><span class="sxs-lookup"><span data-stu-id="0cc59-132">Basic.</span></span> <span data-ttu-id="0cc59-133">5個 Dtu</span><span class="sxs-lookup"><span data-stu-id="0cc59-133">5 DTUs</span></span>
- <span data-ttu-id="0cc59-134">標準.</span><span class="sxs-lookup"><span data-stu-id="0cc59-134">Standard.</span></span> <span data-ttu-id="0cc59-135">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="0cc59-135">100 DTUs</span></span>
- <span data-ttu-id="0cc59-136">佳.</span><span class="sxs-lookup"><span data-stu-id="0cc59-136">Premium.</span></span> <span data-ttu-id="0cc59-137">125 Dtu 如需哪些值有效的詳細資料，請參閱[彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的表格</span><span class="sxs-lookup"><span data-stu-id="0cc59-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="0cc59-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="0cc59-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="0cc59-139">指定彈性池保證對池中所有資料庫的最小 Dtu 數。</span><span class="sxs-lookup"><span data-stu-id="0cc59-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="0cc59-140">預設值為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="0cc59-140">The default value is zero (0).</span></span>
<span data-ttu-id="0cc59-141">如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的資料表。</span><span class="sxs-lookup"><span data-stu-id="0cc59-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="0cc59-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="0cc59-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="0cc59-143">任何 SqlAzure 資料庫可在池中使用的最大 VCore 數。</span><span class="sxs-lookup"><span data-stu-id="0cc59-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="0cc59-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="0cc59-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="0cc59-145">任何 SqlAzure 資料庫可在池中使用的最小 VCore 數。</span><span class="sxs-lookup"><span data-stu-id="0cc59-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="0cc59-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc59-146">-DefaultProfile</span></span>
<span data-ttu-id="0cc59-147">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0cc59-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cc59-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="0cc59-148">-Dtu</span></span>
<span data-ttu-id="0cc59-149">指定彈性池的共用 Dtu 總數。</span><span class="sxs-lookup"><span data-stu-id="0cc59-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="0cc59-150">不同版本的預設值如下所示：</span><span class="sxs-lookup"><span data-stu-id="0cc59-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="0cc59-151">空白.</span><span class="sxs-lookup"><span data-stu-id="0cc59-151">Basic.</span></span>
<span data-ttu-id="0cc59-152">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="0cc59-152">100 DTUs</span></span>
- <span data-ttu-id="0cc59-153">標準.</span><span class="sxs-lookup"><span data-stu-id="0cc59-153">Standard.</span></span>
<span data-ttu-id="0cc59-154">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="0cc59-154">100 DTUs</span></span>
- <span data-ttu-id="0cc59-155">佳.</span><span class="sxs-lookup"><span data-stu-id="0cc59-155">Premium.</span></span>
<span data-ttu-id="0cc59-156">125 Dtu 如需哪些值有效的詳細資料，請參閱 [彈性池中](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)特定大小池的表格。</span><span class="sxs-lookup"><span data-stu-id="0cc59-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="0cc59-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="0cc59-157">-Edition</span></span>
<span data-ttu-id="0cc59-158">指定用於彈性池的 Azure SQL 資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="0cc59-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="0cc59-159">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0cc59-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0cc59-160">所有</span><span class="sxs-lookup"><span data-stu-id="0cc59-160">None</span></span>
- <span data-ttu-id="0cc59-161">空白</span><span class="sxs-lookup"><span data-stu-id="0cc59-161">Basic</span></span>
- <span data-ttu-id="0cc59-162">標準</span><span class="sxs-lookup"><span data-stu-id="0cc59-162">Standard</span></span>
- <span data-ttu-id="0cc59-163">佳</span><span class="sxs-lookup"><span data-stu-id="0cc59-163">Premium</span></span>
- <span data-ttu-id="0cc59-164">倉庫</span><span class="sxs-lookup"><span data-stu-id="0cc59-164">DataWarehouse</span></span>
- <span data-ttu-id="0cc59-165">空閒</span><span class="sxs-lookup"><span data-stu-id="0cc59-165">Free</span></span>
- <span data-ttu-id="0cc59-166">伸縮</span><span class="sxs-lookup"><span data-stu-id="0cc59-166">Stretch</span></span>
- <span data-ttu-id="0cc59-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="0cc59-167">GeneralPurpose</span></span>
- <span data-ttu-id="0cc59-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="0cc59-168">BusinessCritical</span></span>

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

### <span data-ttu-id="0cc59-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0cc59-169">-ElasticPoolName</span></span>
<span data-ttu-id="0cc59-170">指定此 Cmdlet 所建立之彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cc59-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0cc59-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0cc59-171">-LicenseType</span></span>
<span data-ttu-id="0cc59-172">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="0cc59-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="0cc59-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cc59-173">-ResourceGroupName</span></span>
<span data-ttu-id="0cc59-174">指定此 Cmdlet 指派彈性池之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cc59-174">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="0cc59-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0cc59-175">-ServerName</span></span>
<span data-ttu-id="0cc59-176">指定主持彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0cc59-176">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="0cc59-177">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="0cc59-177">-StorageMB</span></span>
<span data-ttu-id="0cc59-178">指定彈性池的儲存空間限制（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="0cc59-178">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="0cc59-179">如果您沒有指定此參數，這個 Cmdlet 會根據 *Dtu* 參數的值來計算值。</span><span class="sxs-lookup"><span data-stu-id="0cc59-179">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="0cc59-180">請參閱可能值的 [eDTU 與儲存空間限制](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) 。</span><span class="sxs-lookup"><span data-stu-id="0cc59-180">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="0cc59-181">-標記</span><span class="sxs-lookup"><span data-stu-id="0cc59-181">-Tags</span></span>
<span data-ttu-id="0cc59-182">指定以雜湊資料表形式表示的鍵值對字典，此 Cmdlet 會與彈性池相關聯。</span><span class="sxs-lookup"><span data-stu-id="0cc59-182">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="0cc59-183">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0cc59-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0cc59-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="0cc59-184">-VCore</span></span>
<span data-ttu-id="0cc59-185">Sql Azure 彈性池的共用總 Vcores 數。</span><span class="sxs-lookup"><span data-stu-id="0cc59-185">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="0cc59-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="0cc59-186">-ZoneRedundant</span></span>
<span data-ttu-id="0cc59-187">要與 Azure Sql 彈性池建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="0cc59-187">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="0cc59-188">-確認</span><span class="sxs-lookup"><span data-stu-id="0cc59-188">-Confirm</span></span>
<span data-ttu-id="0cc59-189">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0cc59-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cc59-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cc59-190">-WhatIf</span></span>
<span data-ttu-id="0cc59-191">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0cc59-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cc59-192">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0cc59-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cc59-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc59-193">CommonParameters</span></span>
<span data-ttu-id="0cc59-194">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0cc59-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc59-195">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0cc59-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc59-196">輸入</span><span class="sxs-lookup"><span data-stu-id="0cc59-196">INPUTS</span></span>

### <span data-ttu-id="0cc59-197">System.object</span><span class="sxs-lookup"><span data-stu-id="0cc59-197">System.String</span></span>

## <span data-ttu-id="0cc59-198">輸出</span><span class="sxs-lookup"><span data-stu-id="0cc59-198">OUTPUTS</span></span>

### <span data-ttu-id="0cc59-199">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="0cc59-199">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="0cc59-200">筆記</span><span class="sxs-lookup"><span data-stu-id="0cc59-200">NOTES</span></span>

## <span data-ttu-id="0cc59-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="0cc59-201">RELATED LINKS</span></span>

[<span data-ttu-id="0cc59-202">AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0cc59-202">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="0cc59-203">AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="0cc59-203">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="0cc59-204">AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="0cc59-204">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="0cc59-205">移除-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0cc59-205">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="0cc59-206">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0cc59-206">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="0cc59-207">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="0cc59-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
