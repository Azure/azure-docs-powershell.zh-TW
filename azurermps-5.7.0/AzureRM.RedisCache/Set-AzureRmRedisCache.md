---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 951198c93918c08f69f28dc6db3c5fe605e6d3bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448585"
---
# <span data-ttu-id="3a665-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a665-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="3a665-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a665-102">SYNOPSIS</span></span>
<span data-ttu-id="3a665-103">修改 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="3a665-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a665-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a665-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a665-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a665-105">DESCRIPTION</span></span>
<span data-ttu-id="3a665-106">**AzureRmRedisCache** Cmdlet 會修改 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="3a665-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="3a665-107">示例</span><span class="sxs-lookup"><span data-stu-id="3a665-107">EXAMPLES</span></span>

### <span data-ttu-id="3a665-108">範例1：修改 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="3a665-108">Example 1: Modify a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="3a665-109">這個命令會更新名為 MyCache 的 Redis 快取 maxmemory 原則。</span><span class="sxs-lookup"><span data-stu-id="3a665-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="3a665-110">參數</span><span class="sxs-lookup"><span data-stu-id="3a665-110">PARAMETERS</span></span>

### <span data-ttu-id="3a665-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a665-111">-DefaultProfile</span></span>
<span data-ttu-id="3a665-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a665-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a665-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="3a665-113">-EnableNonSslPort</span></span>
<span data-ttu-id="3a665-114">指出是否已啟用非 SSL 埠。</span><span class="sxs-lookup"><span data-stu-id="3a665-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="3a665-115">預設值為 $False (停用非 SSL 埠) 。</span><span class="sxs-lookup"><span data-stu-id="3a665-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a665-116">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="3a665-116">-MaxMemoryPolicy</span></span>
<span data-ttu-id="3a665-117">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="3a665-117">This parameter has been deprecated.</span></span>
<span data-ttu-id="3a665-118">使用 *RedisConfiguration* 參數來設定 maxmemory 原則。</span><span class="sxs-lookup"><span data-stu-id="3a665-118">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="3a665-119">例如：</span><span class="sxs-lookup"><span data-stu-id="3a665-119">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a665-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a665-120">-Name</span></span>
<span data-ttu-id="3a665-121">指定要更新之 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a665-121">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a665-122">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a665-122">-RedisConfiguration</span></span>
<span data-ttu-id="3a665-123">指定 Redis 設定。</span><span class="sxs-lookup"><span data-stu-id="3a665-123">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="3a665-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3a665-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a665-125">rdb-備份-啟用。</span><span class="sxs-lookup"><span data-stu-id="3a665-125">rdb-backup-enabled.</span></span>
<span data-ttu-id="3a665-126">指定已啟用 Redis 資料暫留。</span><span class="sxs-lookup"><span data-stu-id="3a665-126">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="3a665-127">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="3a665-127">Premium tier only.</span></span>
- <span data-ttu-id="3a665-128">rdb-儲存體-連接字串。</span><span class="sxs-lookup"><span data-stu-id="3a665-128">rdb-storage-connection-string.</span></span>
<span data-ttu-id="3a665-129">指定 Redis 資料暫留的儲存空間帳戶連接字串。</span><span class="sxs-lookup"><span data-stu-id="3a665-129">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="3a665-130">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="3a665-130">Premium tier only.</span></span>
- <span data-ttu-id="3a665-131">rdb-備份頻率。</span><span class="sxs-lookup"><span data-stu-id="3a665-131">rdb-backup-frequency.</span></span>
<span data-ttu-id="3a665-132">指定 Redis 資料暫留的備份頻率。</span><span class="sxs-lookup"><span data-stu-id="3a665-132">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="3a665-133">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="3a665-133">Premium tier only.</span></span> 
- <span data-ttu-id="3a665-134">maxmemory-保留。</span><span class="sxs-lookup"><span data-stu-id="3a665-134">maxmemory-reserved.</span></span>
<span data-ttu-id="3a665-135">針對非快取程式配置保留的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3a665-135">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="3a665-136">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="3a665-136">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="3a665-137">maxmemory-原則。</span><span class="sxs-lookup"><span data-stu-id="3a665-137">maxmemory-policy.</span></span>
<span data-ttu-id="3a665-138">設定快取的快取原則。</span><span class="sxs-lookup"><span data-stu-id="3a665-138">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="3a665-139">所有定價層。</span><span class="sxs-lookup"><span data-stu-id="3a665-139">All pricing tiers.</span></span> 
- <span data-ttu-id="3a665-140">notify-keyspace-事件。</span><span class="sxs-lookup"><span data-stu-id="3a665-140">notify-keyspace-events.</span></span>
<span data-ttu-id="3a665-141">配置 keyspace 通知。</span><span class="sxs-lookup"><span data-stu-id="3a665-141">Configures keyspace notifications.</span></span>
<span data-ttu-id="3a665-142">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="3a665-142">Standard and premium tiers.</span></span> 
- <span data-ttu-id="3a665-143">散列-最大值-ziplist-專案。</span><span class="sxs-lookup"><span data-stu-id="3a665-143">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="3a665-144">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="3a665-144">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="3a665-145">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="3a665-145">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="3a665-146">散列-最大值-ziplist。</span><span class="sxs-lookup"><span data-stu-id="3a665-146">hash-max-ziplist-value.</span></span>
<span data-ttu-id="3a665-147">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="3a665-147">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="3a665-148">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="3a665-148">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="3a665-149">intset-專案（最大值）。</span><span class="sxs-lookup"><span data-stu-id="3a665-149">set-max-intset-entries.</span></span>
<span data-ttu-id="3a665-150">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="3a665-150">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="3a665-151">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="3a665-151">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="3a665-152">zset-最大 ziplist 專案。</span><span class="sxs-lookup"><span data-stu-id="3a665-152">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="3a665-153">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="3a665-153">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="3a665-154">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="3a665-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="3a665-155">zset-最大 ziplist 值。</span><span class="sxs-lookup"><span data-stu-id="3a665-155">zset-max-ziplist-value.</span></span>
<span data-ttu-id="3a665-156">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="3a665-156">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="3a665-157">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="3a665-157">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="3a665-158">資料庫.</span><span class="sxs-lookup"><span data-stu-id="3a665-158">databases.</span></span>
<span data-ttu-id="3a665-159">設定資料庫的數目。</span><span class="sxs-lookup"><span data-stu-id="3a665-159">Configures the number of databases.</span></span>
<span data-ttu-id="3a665-160">這個屬性只能在建立快取記憶體時設定。</span><span class="sxs-lookup"><span data-stu-id="3a665-160">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="3a665-161">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="3a665-161">Standard and Premium tiers.</span></span>

<span data-ttu-id="3a665-162">如需詳細資訊，請參閱使用 Azure PowerShell (管理 Azure Redis Cache https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) 。</span><span class="sxs-lookup"><span data-stu-id="3a665-162">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a665-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a665-163">-ResourceGroupName</span></span>
<span data-ttu-id="3a665-164">指定包含 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a665-164">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a665-165">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="3a665-165">-ShardCount</span></span>
<span data-ttu-id="3a665-166">指定要在 Premium 群集快取上建立的 shards 數目。</span><span class="sxs-lookup"><span data-stu-id="3a665-166">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a665-167">-大小</span><span class="sxs-lookup"><span data-stu-id="3a665-167">-Size</span></span>
<span data-ttu-id="3a665-168">指定 Redis 快取的大小。</span><span class="sxs-lookup"><span data-stu-id="3a665-168">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="3a665-169">有效值為：</span><span class="sxs-lookup"><span data-stu-id="3a665-169">Valid values are:</span></span> 

- <span data-ttu-id="3a665-170">P1</span><span class="sxs-lookup"><span data-stu-id="3a665-170">P1</span></span>
- <span data-ttu-id="3a665-171">又</span><span class="sxs-lookup"><span data-stu-id="3a665-171">P2</span></span>
- <span data-ttu-id="3a665-172">P3</span><span class="sxs-lookup"><span data-stu-id="3a665-172">P3</span></span>
- <span data-ttu-id="3a665-173">P4</span><span class="sxs-lookup"><span data-stu-id="3a665-173">P4</span></span>
- <span data-ttu-id="3a665-174">C0</span><span class="sxs-lookup"><span data-stu-id="3a665-174">C0</span></span>
- <span data-ttu-id="3a665-175">C1</span><span class="sxs-lookup"><span data-stu-id="3a665-175">C1</span></span>
- <span data-ttu-id="3a665-176">C3</span><span class="sxs-lookup"><span data-stu-id="3a665-176">C2</span></span>
- <span data-ttu-id="3a665-177">C3</span><span class="sxs-lookup"><span data-stu-id="3a665-177">C3</span></span>
- <span data-ttu-id="3a665-178">C4</span><span class="sxs-lookup"><span data-stu-id="3a665-178">C4</span></span>
- <span data-ttu-id="3a665-179">C5</span><span class="sxs-lookup"><span data-stu-id="3a665-179">C5</span></span>
- <span data-ttu-id="3a665-180">C6</span><span class="sxs-lookup"><span data-stu-id="3a665-180">C6</span></span>
- <span data-ttu-id="3a665-181">250MB</span><span class="sxs-lookup"><span data-stu-id="3a665-181">250MB</span></span>
- <span data-ttu-id="3a665-182">1GB</span><span class="sxs-lookup"><span data-stu-id="3a665-182">1GB</span></span>
- <span data-ttu-id="3a665-183">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="3a665-183">2.5GB</span></span>
- <span data-ttu-id="3a665-184">6GB</span><span class="sxs-lookup"><span data-stu-id="3a665-184">6GB</span></span>
- <span data-ttu-id="3a665-185">13GB</span><span class="sxs-lookup"><span data-stu-id="3a665-185">13GB</span></span>
- <span data-ttu-id="3a665-186">26GB</span><span class="sxs-lookup"><span data-stu-id="3a665-186">26GB</span></span>
- <span data-ttu-id="3a665-187">53GB</span><span class="sxs-lookup"><span data-stu-id="3a665-187">53GB</span></span>

<span data-ttu-id="3a665-188">預設值為1GB 或 C1。</span><span class="sxs-lookup"><span data-stu-id="3a665-188">The default value is 1GB or C1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a665-189">-Sku</span><span class="sxs-lookup"><span data-stu-id="3a665-189">-Sku</span></span>
<span data-ttu-id="3a665-190">指定要建立之 Redis 快取的 SKU。</span><span class="sxs-lookup"><span data-stu-id="3a665-190">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="3a665-191">有效值為：</span><span class="sxs-lookup"><span data-stu-id="3a665-191">Valid values are:</span></span> 

- <span data-ttu-id="3a665-192">空白</span><span class="sxs-lookup"><span data-stu-id="3a665-192">Basic</span></span>
- <span data-ttu-id="3a665-193">標準</span><span class="sxs-lookup"><span data-stu-id="3a665-193">Standard</span></span>
- <span data-ttu-id="3a665-194">佳</span><span class="sxs-lookup"><span data-stu-id="3a665-194">Premium</span></span>

<span data-ttu-id="3a665-195">預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="3a665-195">The default value is Standard.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a665-196">-Tag</span><span class="sxs-lookup"><span data-stu-id="3a665-196">-Tag</span></span>
<span data-ttu-id="3a665-197">代表標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3a665-197">A hash table which represents tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a665-198">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="3a665-198">-TenantSettings</span></span>
<span data-ttu-id="3a665-199">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="3a665-199">This parameter has been deprecated.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a665-200">-確認</span><span class="sxs-lookup"><span data-stu-id="3a665-200">-Confirm</span></span>
<span data-ttu-id="3a665-201">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a665-201">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a665-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a665-202">-WhatIf</span></span>
<span data-ttu-id="3a665-203">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a665-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a665-204">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a665-204">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a665-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a665-205">CommonParameters</span></span>
<span data-ttu-id="3a665-206">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a665-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a665-207">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a665-207">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a665-208">輸入</span><span class="sxs-lookup"><span data-stu-id="3a665-208">INPUTS</span></span>

### <span data-ttu-id="3a665-209">所有</span><span class="sxs-lookup"><span data-stu-id="3a665-209">None</span></span>
<span data-ttu-id="3a665-210">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a665-210">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="3a665-211">輸出</span><span class="sxs-lookup"><span data-stu-id="3a665-211">OUTPUTS</span></span>

### <span data-ttu-id="3a665-212">RedisCacheAttributesWithAccessKeys 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="3a665-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="3a665-213">傳回 Redis 快取的所有屬性，包括主要和次要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="3a665-213">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="3a665-214">筆記</span><span class="sxs-lookup"><span data-stu-id="3a665-214">NOTES</span></span>

## <span data-ttu-id="3a665-215">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a665-215">RELATED LINKS</span></span>

[<span data-ttu-id="3a665-216">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a665-216">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="3a665-217">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a665-217">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="3a665-218">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="3a665-218">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


