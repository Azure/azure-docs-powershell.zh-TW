---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435600"
---
# <span data-ttu-id="dfd49-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dfd49-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="dfd49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dfd49-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd49-103">修改 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="dfd49-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="dfd49-104">句法</span><span class="sxs-lookup"><span data-stu-id="dfd49-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfd49-105">說明</span><span class="sxs-lookup"><span data-stu-id="dfd49-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd49-106">**AzRedisCache** Cmdlet 會修改 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="dfd49-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="dfd49-107">示例</span><span class="sxs-lookup"><span data-stu-id="dfd49-107">EXAMPLES</span></span>

### <span data-ttu-id="dfd49-108">範例1：修改 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="dfd49-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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

<span data-ttu-id="dfd49-109">這個命令會更新名為 MyCache 的 Redis 快取 maxmemory 原則。</span><span class="sxs-lookup"><span data-stu-id="dfd49-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="dfd49-110">參數</span><span class="sxs-lookup"><span data-stu-id="dfd49-110">PARAMETERS</span></span>

### <span data-ttu-id="dfd49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd49-111">-DefaultProfile</span></span>
<span data-ttu-id="dfd49-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfd49-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfd49-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="dfd49-113">-EnableNonSslPort</span></span>
<span data-ttu-id="dfd49-114">指出是否已啟用非 SSL 埠。</span><span class="sxs-lookup"><span data-stu-id="dfd49-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="dfd49-115">預設值為 $False (停用非 SSL 埠) 。</span><span class="sxs-lookup"><span data-stu-id="dfd49-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="dfd49-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="dfd49-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="dfd49-117">指定用戶端連接至快取所需的 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="dfd49-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="dfd49-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="dfd49-118">-Name</span></span>
<span data-ttu-id="dfd49-119">指定要更新之 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfd49-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="dfd49-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfd49-120">-RedisConfiguration</span></span>
<span data-ttu-id="dfd49-121">指定 Redis 設定。</span><span class="sxs-lookup"><span data-stu-id="dfd49-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="dfd49-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="dfd49-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dfd49-123">rdb-備份-啟用。</span><span class="sxs-lookup"><span data-stu-id="dfd49-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="dfd49-124">指定已啟用 Redis 資料暫留。</span><span class="sxs-lookup"><span data-stu-id="dfd49-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="dfd49-125">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="dfd49-125">Premium tier only.</span></span>
- <span data-ttu-id="dfd49-126">rdb-儲存體-連接字串。</span><span class="sxs-lookup"><span data-stu-id="dfd49-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="dfd49-127">指定 Redis 資料暫留的儲存空間帳戶連接字串。</span><span class="sxs-lookup"><span data-stu-id="dfd49-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="dfd49-128">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="dfd49-128">Premium tier only.</span></span>
- <span data-ttu-id="dfd49-129">rdb-備份頻率。</span><span class="sxs-lookup"><span data-stu-id="dfd49-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="dfd49-130">指定 Redis 資料暫留的備份頻率。</span><span class="sxs-lookup"><span data-stu-id="dfd49-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="dfd49-131">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="dfd49-131">Premium tier only.</span></span> 
- <span data-ttu-id="dfd49-132">maxmemory-保留。</span><span class="sxs-lookup"><span data-stu-id="dfd49-132">maxmemory-reserved.</span></span>
<span data-ttu-id="dfd49-133">針對非快取程式配置保留的記憶體。</span><span class="sxs-lookup"><span data-stu-id="dfd49-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="dfd49-134">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="dfd49-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfd49-135">maxmemory-原則。</span><span class="sxs-lookup"><span data-stu-id="dfd49-135">maxmemory-policy.</span></span>
<span data-ttu-id="dfd49-136">設定快取的快取原則。</span><span class="sxs-lookup"><span data-stu-id="dfd49-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="dfd49-137">所有定價層。</span><span class="sxs-lookup"><span data-stu-id="dfd49-137">All pricing tiers.</span></span> 
- <span data-ttu-id="dfd49-138">notify-keyspace-事件。</span><span class="sxs-lookup"><span data-stu-id="dfd49-138">notify-keyspace-events.</span></span>
<span data-ttu-id="dfd49-139">配置 keyspace 通知。</span><span class="sxs-lookup"><span data-stu-id="dfd49-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="dfd49-140">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="dfd49-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="dfd49-141">散列-最大值-ziplist-專案。</span><span class="sxs-lookup"><span data-stu-id="dfd49-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="dfd49-142">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="dfd49-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfd49-143">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="dfd49-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfd49-144">散列-最大值-ziplist。</span><span class="sxs-lookup"><span data-stu-id="dfd49-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="dfd49-145">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="dfd49-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfd49-146">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="dfd49-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfd49-147">intset-專案（最大值）。</span><span class="sxs-lookup"><span data-stu-id="dfd49-147">set-max-intset-entries.</span></span>
<span data-ttu-id="dfd49-148">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="dfd49-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfd49-149">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="dfd49-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfd49-150">zset-最大 ziplist 專案。</span><span class="sxs-lookup"><span data-stu-id="dfd49-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="dfd49-151">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="dfd49-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfd49-152">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="dfd49-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfd49-153">zset-最大 ziplist 值。</span><span class="sxs-lookup"><span data-stu-id="dfd49-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="dfd49-154">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="dfd49-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfd49-155">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="dfd49-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfd49-156">資料庫.</span><span class="sxs-lookup"><span data-stu-id="dfd49-156">databases.</span></span>
<span data-ttu-id="dfd49-157">設定資料庫的數目。</span><span class="sxs-lookup"><span data-stu-id="dfd49-157">Configures the number of databases.</span></span>
<span data-ttu-id="dfd49-158">這個屬性只能在建立快取記憶體時設定。</span><span class="sxs-lookup"><span data-stu-id="dfd49-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="dfd49-159">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="dfd49-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="dfd49-160">如需詳細資訊，請參閱使用 Azure PowerShell (管理 Azure Redis Cache http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) 。</span><span class="sxs-lookup"><span data-stu-id="dfd49-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="dfd49-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfd49-161">-ResourceGroupName</span></span>
<span data-ttu-id="dfd49-162">指定包含 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfd49-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="dfd49-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="dfd49-163">-ShardCount</span></span>
<span data-ttu-id="dfd49-164">指定要在 Premium 群集快取上建立的 shards 數目。</span><span class="sxs-lookup"><span data-stu-id="dfd49-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="dfd49-165">-大小</span><span class="sxs-lookup"><span data-stu-id="dfd49-165">-Size</span></span>
<span data-ttu-id="dfd49-166">指定 Redis 快取的大小。</span><span class="sxs-lookup"><span data-stu-id="dfd49-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="dfd49-167">有效值為：</span><span class="sxs-lookup"><span data-stu-id="dfd49-167">Valid values are:</span></span> 
- <span data-ttu-id="dfd49-168">P1</span><span class="sxs-lookup"><span data-stu-id="dfd49-168">P1</span></span>
- <span data-ttu-id="dfd49-169">又</span><span class="sxs-lookup"><span data-stu-id="dfd49-169">P2</span></span>
- <span data-ttu-id="dfd49-170">P3</span><span class="sxs-lookup"><span data-stu-id="dfd49-170">P3</span></span>
- <span data-ttu-id="dfd49-171">P4</span><span class="sxs-lookup"><span data-stu-id="dfd49-171">P4</span></span>
- <span data-ttu-id="dfd49-172">P5</span><span class="sxs-lookup"><span data-stu-id="dfd49-172">P5</span></span>
- <span data-ttu-id="dfd49-173">C0</span><span class="sxs-lookup"><span data-stu-id="dfd49-173">C0</span></span>
- <span data-ttu-id="dfd49-174">C1</span><span class="sxs-lookup"><span data-stu-id="dfd49-174">C1</span></span>
- <span data-ttu-id="dfd49-175">C3</span><span class="sxs-lookup"><span data-stu-id="dfd49-175">C2</span></span>
- <span data-ttu-id="dfd49-176">C3</span><span class="sxs-lookup"><span data-stu-id="dfd49-176">C3</span></span>
- <span data-ttu-id="dfd49-177">C4</span><span class="sxs-lookup"><span data-stu-id="dfd49-177">C4</span></span>
- <span data-ttu-id="dfd49-178">C5</span><span class="sxs-lookup"><span data-stu-id="dfd49-178">C5</span></span>
- <span data-ttu-id="dfd49-179">C6</span><span class="sxs-lookup"><span data-stu-id="dfd49-179">C6</span></span>
- <span data-ttu-id="dfd49-180">250MB</span><span class="sxs-lookup"><span data-stu-id="dfd49-180">250MB</span></span>
- <span data-ttu-id="dfd49-181">1GB</span><span class="sxs-lookup"><span data-stu-id="dfd49-181">1GB</span></span>
- <span data-ttu-id="dfd49-182">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="dfd49-182">2.5GB</span></span>
- <span data-ttu-id="dfd49-183">6GB</span><span class="sxs-lookup"><span data-stu-id="dfd49-183">6GB</span></span>
- <span data-ttu-id="dfd49-184">13GB</span><span class="sxs-lookup"><span data-stu-id="dfd49-184">13GB</span></span>
- <span data-ttu-id="dfd49-185">26GB</span><span class="sxs-lookup"><span data-stu-id="dfd49-185">26GB</span></span>
- <span data-ttu-id="dfd49-186">53GB</span><span class="sxs-lookup"><span data-stu-id="dfd49-186">53GB</span></span>
- <span data-ttu-id="dfd49-187">120GB 預設值為1GB 或 C1。</span><span class="sxs-lookup"><span data-stu-id="dfd49-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="dfd49-188">-Sku</span><span class="sxs-lookup"><span data-stu-id="dfd49-188">-Sku</span></span>
<span data-ttu-id="dfd49-189">指定要建立之 Redis 快取的 SKU。</span><span class="sxs-lookup"><span data-stu-id="dfd49-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="dfd49-190">有效值為：</span><span class="sxs-lookup"><span data-stu-id="dfd49-190">Valid values are:</span></span> 
- <span data-ttu-id="dfd49-191">空白</span><span class="sxs-lookup"><span data-stu-id="dfd49-191">Basic</span></span>
- <span data-ttu-id="dfd49-192">標準</span><span class="sxs-lookup"><span data-stu-id="dfd49-192">Standard</span></span>
- <span data-ttu-id="dfd49-193">[特優] 預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="dfd49-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="dfd49-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="dfd49-194">-Tag</span></span>
<span data-ttu-id="dfd49-195">代表標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="dfd49-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="dfd49-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="dfd49-196">-TenantSettings</span></span>
<span data-ttu-id="dfd49-197">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="dfd49-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="dfd49-198">-確認</span><span class="sxs-lookup"><span data-stu-id="dfd49-198">-Confirm</span></span>
<span data-ttu-id="dfd49-199">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dfd49-199">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd49-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfd49-200">-WhatIf</span></span>
<span data-ttu-id="dfd49-201">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dfd49-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfd49-202">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dfd49-202">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd49-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd49-203">CommonParameters</span></span>
<span data-ttu-id="dfd49-204">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dfd49-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd49-205">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dfd49-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd49-206">輸入</span><span class="sxs-lookup"><span data-stu-id="dfd49-206">INPUTS</span></span>

### <span data-ttu-id="dfd49-207">System.object</span><span class="sxs-lookup"><span data-stu-id="dfd49-207">System.String</span></span>

### <span data-ttu-id="dfd49-208">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dfd49-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dfd49-209">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dfd49-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dfd49-210">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dfd49-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="dfd49-211">輸出</span><span class="sxs-lookup"><span data-stu-id="dfd49-211">OUTPUTS</span></span>

### <span data-ttu-id="dfd49-212">RedisCacheAttributesWithAccessKeys 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="dfd49-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="dfd49-213">筆記</span><span class="sxs-lookup"><span data-stu-id="dfd49-213">NOTES</span></span>

## <span data-ttu-id="dfd49-214">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfd49-214">RELATED LINKS</span></span>

[<span data-ttu-id="dfd49-215">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dfd49-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="dfd49-216">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dfd49-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="dfd49-217">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dfd49-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


