---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 637a1e634b0f8b6f890519bf4865378f50774e39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620971"
---
# <span data-ttu-id="7e3ca-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7e3ca-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="7e3ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e3ca-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3ca-103">修改 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="7e3ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e3ca-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e3ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="7e3ca-105">DESCRIPTION</span></span>
<span data-ttu-id="7e3ca-106">**AzRedisCache** Cmdlet 會修改 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="7e3ca-107">示例</span><span class="sxs-lookup"><span data-stu-id="7e3ca-107">EXAMPLES</span></span>

### <span data-ttu-id="7e3ca-108">範例1：修改 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="7e3ca-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="7e3ca-109">這個命令會更新名為 MyCache 的 Redis 快取 maxmemory 原則。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="7e3ca-110">參數</span><span class="sxs-lookup"><span data-stu-id="7e3ca-110">PARAMETERS</span></span>

### <span data-ttu-id="7e3ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3ca-111">-DefaultProfile</span></span>
<span data-ttu-id="7e3ca-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e3ca-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="7e3ca-113">-EnableNonSslPort</span></span>
<span data-ttu-id="7e3ca-114">指出是否已啟用非 SSL 埠。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="7e3ca-115">預設值為 $False (停用非 SSL 埠) 。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="7e3ca-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e3ca-116">-Name</span></span>
<span data-ttu-id="7e3ca-117">指定要更新之 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="7e3ca-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e3ca-118">-RedisConfiguration</span></span>
<span data-ttu-id="7e3ca-119">指定 Redis 設定。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="7e3ca-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7e3ca-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7e3ca-121">rdb-備份-啟用。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="7e3ca-122">指定已啟用 Redis 資料暫留。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="7e3ca-123">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-123">Premium tier only.</span></span>
- <span data-ttu-id="7e3ca-124">rdb-儲存體-連接字串。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="7e3ca-125">指定 Redis 資料暫留的儲存空間帳戶連接字串。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="7e3ca-126">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-126">Premium tier only.</span></span>
- <span data-ttu-id="7e3ca-127">rdb-備份頻率。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="7e3ca-128">指定 Redis 資料暫留的備份頻率。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="7e3ca-129">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-129">Premium tier only.</span></span> 
- <span data-ttu-id="7e3ca-130">maxmemory-保留。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-130">maxmemory-reserved.</span></span>
<span data-ttu-id="7e3ca-131">針對非快取程式配置保留的記憶體。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="7e3ca-132">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="7e3ca-133">maxmemory-原則。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-133">maxmemory-policy.</span></span>
<span data-ttu-id="7e3ca-134">設定快取的快取原則。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="7e3ca-135">所有定價層。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-135">All pricing tiers.</span></span> 
- <span data-ttu-id="7e3ca-136">notify-keyspace-事件。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-136">notify-keyspace-events.</span></span>
<span data-ttu-id="7e3ca-137">配置 keyspace 通知。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="7e3ca-138">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="7e3ca-139">散列-最大值-ziplist-專案。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="7e3ca-140">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="7e3ca-141">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="7e3ca-142">散列-最大值-ziplist。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="7e3ca-143">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="7e3ca-144">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="7e3ca-145">intset-專案（最大值）。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-145">set-max-intset-entries.</span></span>
<span data-ttu-id="7e3ca-146">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="7e3ca-147">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="7e3ca-148">zset-最大 ziplist 專案。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="7e3ca-149">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="7e3ca-150">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="7e3ca-151">zset-最大 ziplist 值。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="7e3ca-152">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="7e3ca-153">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="7e3ca-154">資料庫.</span><span class="sxs-lookup"><span data-stu-id="7e3ca-154">databases.</span></span>
<span data-ttu-id="7e3ca-155">設定資料庫的數目。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-155">Configures the number of databases.</span></span>
<span data-ttu-id="7e3ca-156">這個屬性只能在建立快取記憶體時設定。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="7e3ca-157">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="7e3ca-158">如需詳細資訊，請參閱使用 Azure PowerShell (管理 Azure Redis Cache https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) 。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="7e3ca-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e3ca-159">-ResourceGroupName</span></span>
<span data-ttu-id="7e3ca-160">指定包含 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="7e3ca-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="7e3ca-161">-ShardCount</span></span>
<span data-ttu-id="7e3ca-162">指定要在 Premium 群集快取上建立的 shards 數目。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="7e3ca-163">-大小</span><span class="sxs-lookup"><span data-stu-id="7e3ca-163">-Size</span></span>
<span data-ttu-id="7e3ca-164">指定 Redis 快取的大小。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="7e3ca-165">有效值為：</span><span class="sxs-lookup"><span data-stu-id="7e3ca-165">Valid values are:</span></span> 
- <span data-ttu-id="7e3ca-166">P1</span><span class="sxs-lookup"><span data-stu-id="7e3ca-166">P1</span></span>
- <span data-ttu-id="7e3ca-167">又</span><span class="sxs-lookup"><span data-stu-id="7e3ca-167">P2</span></span>
- <span data-ttu-id="7e3ca-168">P3</span><span class="sxs-lookup"><span data-stu-id="7e3ca-168">P3</span></span>
- <span data-ttu-id="7e3ca-169">P4</span><span class="sxs-lookup"><span data-stu-id="7e3ca-169">P4</span></span>
- <span data-ttu-id="7e3ca-170">C0</span><span class="sxs-lookup"><span data-stu-id="7e3ca-170">C0</span></span>
- <span data-ttu-id="7e3ca-171">C1</span><span class="sxs-lookup"><span data-stu-id="7e3ca-171">C1</span></span>
- <span data-ttu-id="7e3ca-172">C3</span><span class="sxs-lookup"><span data-stu-id="7e3ca-172">C2</span></span>
- <span data-ttu-id="7e3ca-173">C3</span><span class="sxs-lookup"><span data-stu-id="7e3ca-173">C3</span></span>
- <span data-ttu-id="7e3ca-174">C4</span><span class="sxs-lookup"><span data-stu-id="7e3ca-174">C4</span></span>
- <span data-ttu-id="7e3ca-175">C5</span><span class="sxs-lookup"><span data-stu-id="7e3ca-175">C5</span></span>
- <span data-ttu-id="7e3ca-176">C6</span><span class="sxs-lookup"><span data-stu-id="7e3ca-176">C6</span></span>
- <span data-ttu-id="7e3ca-177">250MB</span><span class="sxs-lookup"><span data-stu-id="7e3ca-177">250MB</span></span>
- <span data-ttu-id="7e3ca-178">1GB</span><span class="sxs-lookup"><span data-stu-id="7e3ca-178">1GB</span></span>
- <span data-ttu-id="7e3ca-179">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="7e3ca-179">2.5GB</span></span>
- <span data-ttu-id="7e3ca-180">6GB</span><span class="sxs-lookup"><span data-stu-id="7e3ca-180">6GB</span></span>
- <span data-ttu-id="7e3ca-181">13GB</span><span class="sxs-lookup"><span data-stu-id="7e3ca-181">13GB</span></span>
- <span data-ttu-id="7e3ca-182">26GB</span><span class="sxs-lookup"><span data-stu-id="7e3ca-182">26GB</span></span>
- <span data-ttu-id="7e3ca-183">53GB 預設值為1GB 或 C1。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="7e3ca-184">-Sku</span><span class="sxs-lookup"><span data-stu-id="7e3ca-184">-Sku</span></span>
<span data-ttu-id="7e3ca-185">指定要建立之 Redis 快取的 SKU。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="7e3ca-186">有效值為：</span><span class="sxs-lookup"><span data-stu-id="7e3ca-186">Valid values are:</span></span> 
- <span data-ttu-id="7e3ca-187">空白</span><span class="sxs-lookup"><span data-stu-id="7e3ca-187">Basic</span></span>
- <span data-ttu-id="7e3ca-188">標準</span><span class="sxs-lookup"><span data-stu-id="7e3ca-188">Standard</span></span>
- <span data-ttu-id="7e3ca-189">[特優] 預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="7e3ca-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e3ca-190">-Tag</span></span>
<span data-ttu-id="7e3ca-191">代表標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="7e3ca-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="7e3ca-192">-TenantSettings</span></span>
<span data-ttu-id="7e3ca-193">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="7e3ca-194">-確認</span><span class="sxs-lookup"><span data-stu-id="7e3ca-194">-Confirm</span></span>
<span data-ttu-id="7e3ca-195">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e3ca-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e3ca-196">-WhatIf</span></span>
<span data-ttu-id="7e3ca-197">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e3ca-198">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e3ca-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3ca-199">CommonParameters</span></span>
<span data-ttu-id="7e3ca-200">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3ca-201">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3ca-202">輸入</span><span class="sxs-lookup"><span data-stu-id="7e3ca-202">INPUTS</span></span>

### <span data-ttu-id="7e3ca-203">System.object</span><span class="sxs-lookup"><span data-stu-id="7e3ca-203">System.String</span></span>

### <span data-ttu-id="7e3ca-204">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e3ca-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7e3ca-205">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7e3ca-205">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7e3ca-206">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7e3ca-206">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7e3ca-207">輸出</span><span class="sxs-lookup"><span data-stu-id="7e3ca-207">OUTPUTS</span></span>

### <span data-ttu-id="7e3ca-208">RedisCacheAttributesWithAccessKeys 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="7e3ca-209">筆記</span><span class="sxs-lookup"><span data-stu-id="7e3ca-209">NOTES</span></span>

## <span data-ttu-id="7e3ca-210">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e3ca-210">RELATED LINKS</span></span>

[<span data-ttu-id="7e3ca-211">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7e3ca-211">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="7e3ca-212">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7e3ca-212">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="7e3ca-213">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7e3ca-213">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


