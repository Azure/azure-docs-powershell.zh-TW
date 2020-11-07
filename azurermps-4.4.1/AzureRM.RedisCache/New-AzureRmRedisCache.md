---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 493a8e7a4e356284b2ae14241715a7631d99839c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623866"
---
# <span data-ttu-id="4a262-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4a262-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="4a262-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a262-102">SYNOPSIS</span></span>
<span data-ttu-id="4a262-103">建立 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4a262-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a262-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a262-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a262-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a262-105">DESCRIPTION</span></span>
<span data-ttu-id="4a262-106">**新的-AzureRmRedisCache** Cmdlet 會建立 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="4a262-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="4a262-107">示例</span><span class="sxs-lookup"><span data-stu-id="4a262-107">EXAMPLES</span></span>

### <span data-ttu-id="4a262-108">範例1：建立 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="4a262-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
```

<span data-ttu-id="4a262-109">這個命令會建立 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4a262-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="4a262-110">範例2：建立標準 SKU Redis 快取</span><span class="sxs-lookup"><span data-stu-id="4a262-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]} 
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
```

<span data-ttu-id="4a262-111">這個命令會建立 Redis 快取，或在已存在的情況下更新 Redis 的快取。</span><span class="sxs-lookup"><span data-stu-id="4a262-111">This command creates a Redis Cache or updates the Redis Cache if it already exists.</span></span>

## <span data-ttu-id="4a262-112">參數</span><span class="sxs-lookup"><span data-stu-id="4a262-112">PARAMETERS</span></span>

### <span data-ttu-id="4a262-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="4a262-113">-EnableNonSslPort</span></span>
<span data-ttu-id="4a262-114">指出是否已啟用非 SSL 埠。</span><span class="sxs-lookup"><span data-stu-id="4a262-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="4a262-115">預設值為 $False (停用非 SSL 埠) 。</span><span class="sxs-lookup"><span data-stu-id="4a262-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-116">-位置</span><span class="sxs-lookup"><span data-stu-id="4a262-116">-Location</span></span>
<span data-ttu-id="4a262-117">指定要建立 Redis 快取的位置。</span><span class="sxs-lookup"><span data-stu-id="4a262-117">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="4a262-118">有效值為：</span><span class="sxs-lookup"><span data-stu-id="4a262-118">Valid values are:</span></span> 

- <span data-ttu-id="4a262-119">美國中北部</span><span class="sxs-lookup"><span data-stu-id="4a262-119">North Central US</span></span>
- <span data-ttu-id="4a262-120">美國中南部</span><span class="sxs-lookup"><span data-stu-id="4a262-120">South Central US</span></span>
- <span data-ttu-id="4a262-121">美國中部</span><span class="sxs-lookup"><span data-stu-id="4a262-121">Central US</span></span>
- <span data-ttu-id="4a262-122">西歐</span><span class="sxs-lookup"><span data-stu-id="4a262-122">West Europe</span></span>
- <span data-ttu-id="4a262-123">北歐</span><span class="sxs-lookup"><span data-stu-id="4a262-123">North Europe</span></span>
- <span data-ttu-id="4a262-124">美國西部</span><span class="sxs-lookup"><span data-stu-id="4a262-124">West US</span></span>
- <span data-ttu-id="4a262-125">東美國</span><span class="sxs-lookup"><span data-stu-id="4a262-125">East US</span></span>
- <span data-ttu-id="4a262-126">東美國2</span><span class="sxs-lookup"><span data-stu-id="4a262-126">East US 2</span></span>
- <span data-ttu-id="4a262-127">日本東</span><span class="sxs-lookup"><span data-stu-id="4a262-127">Japan East</span></span>
- <span data-ttu-id="4a262-128">日本西部</span><span class="sxs-lookup"><span data-stu-id="4a262-128">Japan West</span></span>
- <span data-ttu-id="4a262-129">巴西南部</span><span class="sxs-lookup"><span data-stu-id="4a262-129">Brazil South</span></span>
- <span data-ttu-id="4a262-130">東南亞</span><span class="sxs-lookup"><span data-stu-id="4a262-130">Southeast Asia</span></span>
- <span data-ttu-id="4a262-131">東亞</span><span class="sxs-lookup"><span data-stu-id="4a262-131">East Asia</span></span>
- <span data-ttu-id="4a262-132">澳大利亞東</span><span class="sxs-lookup"><span data-stu-id="4a262-132">Australia East</span></span>
- <span data-ttu-id="4a262-133">澳大利亞東南部</span><span class="sxs-lookup"><span data-stu-id="4a262-133">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-134">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="4a262-134">-MaxMemoryPolicy</span></span>
<span data-ttu-id="4a262-135">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="4a262-135">This parameter has been deprecated.</span></span>
<span data-ttu-id="4a262-136">使用 *RedisConfiguration* 參數來設定 maxmemory 原則。</span><span class="sxs-lookup"><span data-stu-id="4a262-136">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="4a262-137">例如：</span><span class="sxs-lookup"><span data-stu-id="4a262-137">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a262-138">-Name</span></span>
<span data-ttu-id="4a262-139">指定要建立之 Redis 緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a262-139">Specifies the name of the Redis Cache to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a262-140">-RedisConfiguration</span></span>
<span data-ttu-id="4a262-141">指定 Redis 設定。</span><span class="sxs-lookup"><span data-stu-id="4a262-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="4a262-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4a262-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4a262-143">rdb-備份-啟用。</span><span class="sxs-lookup"><span data-stu-id="4a262-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="4a262-144">指定已啟用 Redis 資料暫留。</span><span class="sxs-lookup"><span data-stu-id="4a262-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="4a262-145">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4a262-145">Premium tier only.</span></span>
- <span data-ttu-id="4a262-146">rdb-儲存體-連接字串。</span><span class="sxs-lookup"><span data-stu-id="4a262-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="4a262-147">指定 Redis 資料暫留的儲存空間帳戶連接字串。</span><span class="sxs-lookup"><span data-stu-id="4a262-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="4a262-148">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4a262-148">Premium tier only.</span></span>
- <span data-ttu-id="4a262-149">rdb-備份頻率。</span><span class="sxs-lookup"><span data-stu-id="4a262-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="4a262-150">指定 Redis 資料暫留的備份頻率。</span><span class="sxs-lookup"><span data-stu-id="4a262-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="4a262-151">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4a262-151">Premium tier only.</span></span> 
- <span data-ttu-id="4a262-152">maxmemory-保留。</span><span class="sxs-lookup"><span data-stu-id="4a262-152">maxmemory-reserved.</span></span>
<span data-ttu-id="4a262-153">針對非快取程式配置保留的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4a262-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="4a262-154">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4a262-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4a262-155">maxmemory-原則。</span><span class="sxs-lookup"><span data-stu-id="4a262-155">maxmemory-policy.</span></span>
<span data-ttu-id="4a262-156">設定快取的快取原則。</span><span class="sxs-lookup"><span data-stu-id="4a262-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="4a262-157">所有定價層。</span><span class="sxs-lookup"><span data-stu-id="4a262-157">All pricing tiers.</span></span> 
- <span data-ttu-id="4a262-158">notify-keyspace-事件。</span><span class="sxs-lookup"><span data-stu-id="4a262-158">notify-keyspace-events.</span></span>
<span data-ttu-id="4a262-159">配置 keyspace 通知。</span><span class="sxs-lookup"><span data-stu-id="4a262-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="4a262-160">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4a262-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="4a262-161">散列-最大值-ziplist-專案。</span><span class="sxs-lookup"><span data-stu-id="4a262-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="4a262-162">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="4a262-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4a262-163">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4a262-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4a262-164">散列-最大值-ziplist。</span><span class="sxs-lookup"><span data-stu-id="4a262-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="4a262-165">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="4a262-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4a262-166">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4a262-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4a262-167">intset-專案（最大值）。</span><span class="sxs-lookup"><span data-stu-id="4a262-167">set-max-intset-entries.</span></span>
<span data-ttu-id="4a262-168">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="4a262-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4a262-169">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4a262-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4a262-170">zset-最大 ziplist 專案。</span><span class="sxs-lookup"><span data-stu-id="4a262-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="4a262-171">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="4a262-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4a262-172">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4a262-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4a262-173">zset-最大 ziplist 值。</span><span class="sxs-lookup"><span data-stu-id="4a262-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="4a262-174">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="4a262-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4a262-175">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4a262-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4a262-176">資料庫.</span><span class="sxs-lookup"><span data-stu-id="4a262-176">databases.</span></span>
<span data-ttu-id="4a262-177">設定資料庫的數目。</span><span class="sxs-lookup"><span data-stu-id="4a262-177">Configures the number of databases.</span></span>
<span data-ttu-id="4a262-178">這個屬性只能在建立快取記憶體時設定。</span><span class="sxs-lookup"><span data-stu-id="4a262-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="4a262-179">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4a262-179">Standard and Premium tiers.</span></span>

<span data-ttu-id="4a262-180">如需詳細資訊，請參閱使用 Azure PowerShell (管理 Azure Redis Cache https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) 。</span><span class="sxs-lookup"><span data-stu-id="4a262-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-181">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="4a262-181">-RedisVersion</span></span>
<span data-ttu-id="4a262-182">此參數已棄用，將會從未來版本中移除。</span><span class="sxs-lookup"><span data-stu-id="4a262-182">This parameter is deprecated and will be removed from future releases.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a262-183">-ResourceGroupName</span></span>
<span data-ttu-id="4a262-184">指定要在其中建立 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a262-184">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-185">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="4a262-185">-ShardCount</span></span>
<span data-ttu-id="4a262-186">指定要在 Premium 群集快取上建立的 shards 數目。</span><span class="sxs-lookup"><span data-stu-id="4a262-186">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="4a262-187">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4a262-187">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4a262-188">sr-1</span><span class="sxs-lookup"><span data-stu-id="4a262-188">1</span></span>
- <span data-ttu-id="4a262-189">pplx-2</span><span class="sxs-lookup"><span data-stu-id="4a262-189">2</span></span>
- <span data-ttu-id="4a262-190">3</span><span class="sxs-lookup"><span data-stu-id="4a262-190">3</span></span>
- <span data-ttu-id="4a262-191">4</span><span class="sxs-lookup"><span data-stu-id="4a262-191">4</span></span>
- <span data-ttu-id="4a262-192">500</span><span class="sxs-lookup"><span data-stu-id="4a262-192">5</span></span>
- <span data-ttu-id="4a262-193">6</span><span class="sxs-lookup"><span data-stu-id="4a262-193">6</span></span>
- <span data-ttu-id="4a262-194">utf-7</span><span class="sxs-lookup"><span data-stu-id="4a262-194">7</span></span>
- <span data-ttu-id="4a262-195">型</span><span class="sxs-lookup"><span data-stu-id="4a262-195">8</span></span>
- <span data-ttu-id="4a262-196">9</span><span class="sxs-lookup"><span data-stu-id="4a262-196">9</span></span> 
- <span data-ttu-id="4a262-197">第</span><span class="sxs-lookup"><span data-stu-id="4a262-197">10</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-198">-大小</span><span class="sxs-lookup"><span data-stu-id="4a262-198">-Size</span></span>
<span data-ttu-id="4a262-199">指定 Redis 快取的大小。</span><span class="sxs-lookup"><span data-stu-id="4a262-199">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="4a262-200">有效值為：</span><span class="sxs-lookup"><span data-stu-id="4a262-200">Valid values are:</span></span> 

- <span data-ttu-id="4a262-201">P1</span><span class="sxs-lookup"><span data-stu-id="4a262-201">P1</span></span>
- <span data-ttu-id="4a262-202">又</span><span class="sxs-lookup"><span data-stu-id="4a262-202">P2</span></span>
- <span data-ttu-id="4a262-203">P3</span><span class="sxs-lookup"><span data-stu-id="4a262-203">P3</span></span>
- <span data-ttu-id="4a262-204">P4</span><span class="sxs-lookup"><span data-stu-id="4a262-204">P4</span></span>
- <span data-ttu-id="4a262-205">C0</span><span class="sxs-lookup"><span data-stu-id="4a262-205">C0</span></span>
- <span data-ttu-id="4a262-206">C1</span><span class="sxs-lookup"><span data-stu-id="4a262-206">C1</span></span>
- <span data-ttu-id="4a262-207">C3</span><span class="sxs-lookup"><span data-stu-id="4a262-207">C2</span></span>
- <span data-ttu-id="4a262-208">C3</span><span class="sxs-lookup"><span data-stu-id="4a262-208">C3</span></span>
- <span data-ttu-id="4a262-209">C4</span><span class="sxs-lookup"><span data-stu-id="4a262-209">C4</span></span>
- <span data-ttu-id="4a262-210">C5</span><span class="sxs-lookup"><span data-stu-id="4a262-210">C5</span></span>
- <span data-ttu-id="4a262-211">C6</span><span class="sxs-lookup"><span data-stu-id="4a262-211">C6</span></span>
- <span data-ttu-id="4a262-212">250MB</span><span class="sxs-lookup"><span data-stu-id="4a262-212">250MB</span></span>
- <span data-ttu-id="4a262-213">1GB</span><span class="sxs-lookup"><span data-stu-id="4a262-213">1GB</span></span>
- <span data-ttu-id="4a262-214">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="4a262-214">2.5GB</span></span>
- <span data-ttu-id="4a262-215">6GB</span><span class="sxs-lookup"><span data-stu-id="4a262-215">6GB</span></span>
- <span data-ttu-id="4a262-216">13GB</span><span class="sxs-lookup"><span data-stu-id="4a262-216">13GB</span></span>
- <span data-ttu-id="4a262-217">26GB</span><span class="sxs-lookup"><span data-stu-id="4a262-217">26GB</span></span>
- <span data-ttu-id="4a262-218">53GB</span><span class="sxs-lookup"><span data-stu-id="4a262-218">53GB</span></span>

<span data-ttu-id="4a262-219">預設值為1GB 或 C1。</span><span class="sxs-lookup"><span data-stu-id="4a262-219">The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-220">-Sku</span><span class="sxs-lookup"><span data-stu-id="4a262-220">-Sku</span></span>
<span data-ttu-id="4a262-221">指定要建立之 Redis 快取的 SKU。</span><span class="sxs-lookup"><span data-stu-id="4a262-221">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="4a262-222">有效值為：</span><span class="sxs-lookup"><span data-stu-id="4a262-222">Valid values are:</span></span> 

- <span data-ttu-id="4a262-223">空白</span><span class="sxs-lookup"><span data-stu-id="4a262-223">Basic</span></span>
- <span data-ttu-id="4a262-224">標準</span><span class="sxs-lookup"><span data-stu-id="4a262-224">Standard</span></span>
- <span data-ttu-id="4a262-225">佳</span><span class="sxs-lookup"><span data-stu-id="4a262-225">Premium</span></span>

<span data-ttu-id="4a262-226">預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="4a262-226">The default value is Standard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-227">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="4a262-227">-StaticIP</span></span>
<span data-ttu-id="4a262-228">在 Redis 快取的子網上指定唯一的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4a262-228">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="4a262-229">如果您沒有指定此參數的值，這個 Cmdlet 會從子網上選擇 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4a262-229">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-230">-子網</span><span class="sxs-lookup"><span data-stu-id="4a262-230">-Subnet</span></span>
<span data-ttu-id="4a262-231">指定要在其中部署 Redis 快取的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="4a262-231">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-232">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4a262-232">-SubnetId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-233">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="4a262-233">-TenantSettings</span></span>
<span data-ttu-id="4a262-234">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="4a262-234">This parameter has been deprecated.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-235">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4a262-235">-VirtualNetwork</span></span>
<span data-ttu-id="4a262-236">指定要部署 Redis 快取的虛擬網路資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a262-236">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a262-237">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a262-237">-DefaultProfile</span></span>
<span data-ttu-id="4a262-238">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a262-238">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a262-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a262-239">CommonParameters</span></span>
<span data-ttu-id="4a262-240">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a262-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a262-241">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a262-241">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a262-242">輸入</span><span class="sxs-lookup"><span data-stu-id="4a262-242">INPUTS</span></span>

### <span data-ttu-id="4a262-243">所有</span><span class="sxs-lookup"><span data-stu-id="4a262-243">None</span></span>
<span data-ttu-id="4a262-244">您可以依名稱將輸入管到這個 Cmdlet，但不能依值進行。</span><span class="sxs-lookup"><span data-stu-id="4a262-244">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="4a262-245">輸出</span><span class="sxs-lookup"><span data-stu-id="4a262-245">OUTPUTS</span></span>

### <span data-ttu-id="4a262-246">RedisCacheAttributesWithAccessKeys 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="4a262-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="4a262-247">這個 Cmdlet 會傳回 Redis 快取的所有屬性，包括主要和次要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="4a262-247">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="4a262-248">筆記</span><span class="sxs-lookup"><span data-stu-id="4a262-248">NOTES</span></span>

## <span data-ttu-id="4a262-249">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a262-249">RELATED LINKS</span></span>

[<span data-ttu-id="4a262-250">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4a262-250">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="4a262-251">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4a262-251">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="4a262-252">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4a262-252">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


