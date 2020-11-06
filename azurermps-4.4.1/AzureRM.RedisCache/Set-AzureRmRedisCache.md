---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448023"
---
# <span data-ttu-id="96f03-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="96f03-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="96f03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96f03-102">SYNOPSIS</span></span>
<span data-ttu-id="96f03-103">修改 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="96f03-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96f03-104">句法</span><span class="sxs-lookup"><span data-stu-id="96f03-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96f03-105">說明</span><span class="sxs-lookup"><span data-stu-id="96f03-105">DESCRIPTION</span></span>
<span data-ttu-id="96f03-106">**AzureRmRedisCache** Cmdlet 會修改 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="96f03-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="96f03-107">示例</span><span class="sxs-lookup"><span data-stu-id="96f03-107">EXAMPLES</span></span>

### <span data-ttu-id="96f03-108">範例1：修改 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="96f03-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
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

<span data-ttu-id="96f03-109">這個命令會更新名為 MyCache 的 Redis 快取 maxmemory 原則。</span><span class="sxs-lookup"><span data-stu-id="96f03-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="96f03-110">參數</span><span class="sxs-lookup"><span data-stu-id="96f03-110">PARAMETERS</span></span>

### <span data-ttu-id="96f03-111">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="96f03-111">-EnableNonSslPort</span></span>
<span data-ttu-id="96f03-112">指出是否已啟用非 SSL 埠。</span><span class="sxs-lookup"><span data-stu-id="96f03-112">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="96f03-113">預設值為 $False (停用非 SSL 埠) 。</span><span class="sxs-lookup"><span data-stu-id="96f03-113">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="96f03-114">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="96f03-114">-MaxMemoryPolicy</span></span>
<span data-ttu-id="96f03-115">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="96f03-115">This parameter has been deprecated.</span></span>
<span data-ttu-id="96f03-116">使用 *RedisConfiguration* 參數來設定 maxmemory 原則。</span><span class="sxs-lookup"><span data-stu-id="96f03-116">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="96f03-117">例如：</span><span class="sxs-lookup"><span data-stu-id="96f03-117">For example:</span></span> 

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

### <span data-ttu-id="96f03-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="96f03-118">-Name</span></span>
<span data-ttu-id="96f03-119">指定要更新之 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="96f03-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="96f03-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="96f03-120">-RedisConfiguration</span></span>
<span data-ttu-id="96f03-121">指定 Redis 設定。</span><span class="sxs-lookup"><span data-stu-id="96f03-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="96f03-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="96f03-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96f03-123">rdb-備份-啟用。</span><span class="sxs-lookup"><span data-stu-id="96f03-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="96f03-124">指定已啟用 Redis 資料暫留。</span><span class="sxs-lookup"><span data-stu-id="96f03-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="96f03-125">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="96f03-125">Premium tier only.</span></span>
- <span data-ttu-id="96f03-126">rdb-儲存體-連接字串。</span><span class="sxs-lookup"><span data-stu-id="96f03-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="96f03-127">指定 Redis 資料暫留的儲存空間帳戶連接字串。</span><span class="sxs-lookup"><span data-stu-id="96f03-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="96f03-128">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="96f03-128">Premium tier only.</span></span>
- <span data-ttu-id="96f03-129">rdb-備份頻率。</span><span class="sxs-lookup"><span data-stu-id="96f03-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="96f03-130">指定 Redis 資料暫留的備份頻率。</span><span class="sxs-lookup"><span data-stu-id="96f03-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="96f03-131">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="96f03-131">Premium tier only.</span></span> 
- <span data-ttu-id="96f03-132">maxmemory-保留。</span><span class="sxs-lookup"><span data-stu-id="96f03-132">maxmemory-reserved.</span></span>
<span data-ttu-id="96f03-133">針對非快取程式配置保留的記憶體。</span><span class="sxs-lookup"><span data-stu-id="96f03-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="96f03-134">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="96f03-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="96f03-135">maxmemory-原則。</span><span class="sxs-lookup"><span data-stu-id="96f03-135">maxmemory-policy.</span></span>
<span data-ttu-id="96f03-136">設定快取的快取原則。</span><span class="sxs-lookup"><span data-stu-id="96f03-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="96f03-137">所有定價層。</span><span class="sxs-lookup"><span data-stu-id="96f03-137">All pricing tiers.</span></span> 
- <span data-ttu-id="96f03-138">notify-keyspace-事件。</span><span class="sxs-lookup"><span data-stu-id="96f03-138">notify-keyspace-events.</span></span>
<span data-ttu-id="96f03-139">配置 keyspace 通知。</span><span class="sxs-lookup"><span data-stu-id="96f03-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="96f03-140">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="96f03-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="96f03-141">散列-最大值-ziplist-專案。</span><span class="sxs-lookup"><span data-stu-id="96f03-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="96f03-142">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="96f03-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="96f03-143">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="96f03-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="96f03-144">散列-最大值-ziplist。</span><span class="sxs-lookup"><span data-stu-id="96f03-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="96f03-145">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="96f03-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="96f03-146">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="96f03-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="96f03-147">intset-專案（最大值）。</span><span class="sxs-lookup"><span data-stu-id="96f03-147">set-max-intset-entries.</span></span>
<span data-ttu-id="96f03-148">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="96f03-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="96f03-149">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="96f03-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="96f03-150">zset-最大 ziplist 專案。</span><span class="sxs-lookup"><span data-stu-id="96f03-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="96f03-151">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="96f03-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="96f03-152">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="96f03-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="96f03-153">zset-最大 ziplist 值。</span><span class="sxs-lookup"><span data-stu-id="96f03-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="96f03-154">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="96f03-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="96f03-155">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="96f03-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="96f03-156">資料庫.</span><span class="sxs-lookup"><span data-stu-id="96f03-156">databases.</span></span>
<span data-ttu-id="96f03-157">設定資料庫的數目。</span><span class="sxs-lookup"><span data-stu-id="96f03-157">Configures the number of databases.</span></span>
<span data-ttu-id="96f03-158">這個屬性只能在建立快取記憶體時設定。</span><span class="sxs-lookup"><span data-stu-id="96f03-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="96f03-159">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="96f03-159">Standard and Premium tiers.</span></span>

<span data-ttu-id="96f03-160">如需詳細資訊，請參閱使用 Azure PowerShell (管理 Azure Redis Cache https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) 。</span><span class="sxs-lookup"><span data-stu-id="96f03-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="96f03-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96f03-161">-ResourceGroupName</span></span>
<span data-ttu-id="96f03-162">指定包含 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96f03-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="96f03-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="96f03-163">-ShardCount</span></span>
<span data-ttu-id="96f03-164">指定要在 Premium 群集快取上建立的 shards 數目。</span><span class="sxs-lookup"><span data-stu-id="96f03-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="96f03-165">-大小</span><span class="sxs-lookup"><span data-stu-id="96f03-165">-Size</span></span>
<span data-ttu-id="96f03-166">指定 Redis 快取的大小。</span><span class="sxs-lookup"><span data-stu-id="96f03-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="96f03-167">有效值為：</span><span class="sxs-lookup"><span data-stu-id="96f03-167">Valid values are:</span></span> 

- <span data-ttu-id="96f03-168">P1</span><span class="sxs-lookup"><span data-stu-id="96f03-168">P1</span></span>
- <span data-ttu-id="96f03-169">又</span><span class="sxs-lookup"><span data-stu-id="96f03-169">P2</span></span>
- <span data-ttu-id="96f03-170">P3</span><span class="sxs-lookup"><span data-stu-id="96f03-170">P3</span></span>
- <span data-ttu-id="96f03-171">P4</span><span class="sxs-lookup"><span data-stu-id="96f03-171">P4</span></span>
- <span data-ttu-id="96f03-172">C0</span><span class="sxs-lookup"><span data-stu-id="96f03-172">C0</span></span>
- <span data-ttu-id="96f03-173">C1</span><span class="sxs-lookup"><span data-stu-id="96f03-173">C1</span></span>
- <span data-ttu-id="96f03-174">C3</span><span class="sxs-lookup"><span data-stu-id="96f03-174">C2</span></span>
- <span data-ttu-id="96f03-175">C3</span><span class="sxs-lookup"><span data-stu-id="96f03-175">C3</span></span>
- <span data-ttu-id="96f03-176">C4</span><span class="sxs-lookup"><span data-stu-id="96f03-176">C4</span></span>
- <span data-ttu-id="96f03-177">C5</span><span class="sxs-lookup"><span data-stu-id="96f03-177">C5</span></span>
- <span data-ttu-id="96f03-178">C6</span><span class="sxs-lookup"><span data-stu-id="96f03-178">C6</span></span>
- <span data-ttu-id="96f03-179">250MB</span><span class="sxs-lookup"><span data-stu-id="96f03-179">250MB</span></span>
- <span data-ttu-id="96f03-180">1GB</span><span class="sxs-lookup"><span data-stu-id="96f03-180">1GB</span></span>
- <span data-ttu-id="96f03-181">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="96f03-181">2.5GB</span></span>
- <span data-ttu-id="96f03-182">6GB</span><span class="sxs-lookup"><span data-stu-id="96f03-182">6GB</span></span>
- <span data-ttu-id="96f03-183">13GB</span><span class="sxs-lookup"><span data-stu-id="96f03-183">13GB</span></span>
- <span data-ttu-id="96f03-184">26GB</span><span class="sxs-lookup"><span data-stu-id="96f03-184">26GB</span></span>
- <span data-ttu-id="96f03-185">53GB</span><span class="sxs-lookup"><span data-stu-id="96f03-185">53GB</span></span>

<span data-ttu-id="96f03-186">預設值為1GB 或 C1。</span><span class="sxs-lookup"><span data-stu-id="96f03-186">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="96f03-187">-Sku</span><span class="sxs-lookup"><span data-stu-id="96f03-187">-Sku</span></span>
<span data-ttu-id="96f03-188">指定要建立之 Redis 快取的 SKU。</span><span class="sxs-lookup"><span data-stu-id="96f03-188">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="96f03-189">有效值為：</span><span class="sxs-lookup"><span data-stu-id="96f03-189">Valid values are:</span></span> 

- <span data-ttu-id="96f03-190">空白</span><span class="sxs-lookup"><span data-stu-id="96f03-190">Basic</span></span>
- <span data-ttu-id="96f03-191">標準</span><span class="sxs-lookup"><span data-stu-id="96f03-191">Standard</span></span>
- <span data-ttu-id="96f03-192">佳</span><span class="sxs-lookup"><span data-stu-id="96f03-192">Premium</span></span>

<span data-ttu-id="96f03-193">預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="96f03-193">The default value is Standard.</span></span>

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

### <span data-ttu-id="96f03-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="96f03-194">-TenantSettings</span></span>
<span data-ttu-id="96f03-195">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="96f03-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="96f03-196">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f03-196">-DefaultProfile</span></span>
<span data-ttu-id="96f03-197">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96f03-197">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96f03-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f03-198">CommonParameters</span></span>
<span data-ttu-id="96f03-199">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96f03-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f03-200">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96f03-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f03-201">輸入</span><span class="sxs-lookup"><span data-stu-id="96f03-201">INPUTS</span></span>

### <span data-ttu-id="96f03-202">所有</span><span class="sxs-lookup"><span data-stu-id="96f03-202">None</span></span>
<span data-ttu-id="96f03-203">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96f03-203">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="96f03-204">輸出</span><span class="sxs-lookup"><span data-stu-id="96f03-204">OUTPUTS</span></span>

### <span data-ttu-id="96f03-205">RedisCacheAttributesWithAccessKeys 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="96f03-205">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="96f03-206">傳回 Redis 快取的所有屬性，包括主要和次要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="96f03-206">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="96f03-207">筆記</span><span class="sxs-lookup"><span data-stu-id="96f03-207">NOTES</span></span>

## <span data-ttu-id="96f03-208">相關連結</span><span class="sxs-lookup"><span data-stu-id="96f03-208">RELATED LINKS</span></span>

[<span data-ttu-id="96f03-209">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="96f03-209">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="96f03-210">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="96f03-210">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="96f03-211">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="96f03-211">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


