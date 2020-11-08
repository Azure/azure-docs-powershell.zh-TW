---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127398"
---
# <span data-ttu-id="90b9e-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90b9e-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="90b9e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="90b9e-103">修改 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="90b9e-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="90b9e-104">句法</span><span class="sxs-lookup"><span data-stu-id="90b9e-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90b9e-105">說明</span><span class="sxs-lookup"><span data-stu-id="90b9e-105">DESCRIPTION</span></span>
<span data-ttu-id="90b9e-106">**AzRedisCache** Cmdlet 會修改 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="90b9e-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="90b9e-107">示例</span><span class="sxs-lookup"><span data-stu-id="90b9e-107">EXAMPLES</span></span>

### <span data-ttu-id="90b9e-108">範例1：修改 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="90b9e-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="90b9e-109">這個命令會更新名為 MyCache 的 Redis 快取 maxmemory 原則。</span><span class="sxs-lookup"><span data-stu-id="90b9e-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="90b9e-110">參數</span><span class="sxs-lookup"><span data-stu-id="90b9e-110">PARAMETERS</span></span>

### <span data-ttu-id="90b9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b9e-111">-DefaultProfile</span></span>
<span data-ttu-id="90b9e-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90b9e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90b9e-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="90b9e-113">-EnableNonSslPort</span></span>
<span data-ttu-id="90b9e-114">指出是否已啟用非 SSL 埠。</span><span class="sxs-lookup"><span data-stu-id="90b9e-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="90b9e-115">預設值為 $False (停用非 SSL 埠) 。</span><span class="sxs-lookup"><span data-stu-id="90b9e-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="90b9e-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="90b9e-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="90b9e-117">指定用戶端連接至快取所需的 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="90b9e-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="90b9e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="90b9e-118">-Name</span></span>
<span data-ttu-id="90b9e-119">指定要更新之 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="90b9e-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="90b9e-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="90b9e-120">-RedisConfiguration</span></span>
<span data-ttu-id="90b9e-121">指定 Redis 設定。</span><span class="sxs-lookup"><span data-stu-id="90b9e-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="90b9e-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="90b9e-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90b9e-123">rdb-備份-啟用。</span><span class="sxs-lookup"><span data-stu-id="90b9e-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="90b9e-124">指定已啟用 Redis 資料暫留。</span><span class="sxs-lookup"><span data-stu-id="90b9e-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="90b9e-125">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="90b9e-125">Premium tier only.</span></span>
- <span data-ttu-id="90b9e-126">rdb-儲存體-連接字串。</span><span class="sxs-lookup"><span data-stu-id="90b9e-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="90b9e-127">指定 Redis 資料暫留的儲存空間帳戶連接字串。</span><span class="sxs-lookup"><span data-stu-id="90b9e-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="90b9e-128">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="90b9e-128">Premium tier only.</span></span>
- <span data-ttu-id="90b9e-129">rdb-備份頻率。</span><span class="sxs-lookup"><span data-stu-id="90b9e-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="90b9e-130">指定 Redis 資料暫留的備份頻率。</span><span class="sxs-lookup"><span data-stu-id="90b9e-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="90b9e-131">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="90b9e-131">Premium tier only.</span></span> 
- <span data-ttu-id="90b9e-132">maxmemory-保留。</span><span class="sxs-lookup"><span data-stu-id="90b9e-132">maxmemory-reserved.</span></span>
<span data-ttu-id="90b9e-133">針對非快取程式配置保留的記憶體。</span><span class="sxs-lookup"><span data-stu-id="90b9e-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="90b9e-134">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="90b9e-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="90b9e-135">maxmemory-原則。</span><span class="sxs-lookup"><span data-stu-id="90b9e-135">maxmemory-policy.</span></span>
<span data-ttu-id="90b9e-136">設定快取的快取原則。</span><span class="sxs-lookup"><span data-stu-id="90b9e-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="90b9e-137">所有定價層。</span><span class="sxs-lookup"><span data-stu-id="90b9e-137">All pricing tiers.</span></span> 
- <span data-ttu-id="90b9e-138">notify-keyspace-事件。</span><span class="sxs-lookup"><span data-stu-id="90b9e-138">notify-keyspace-events.</span></span>
<span data-ttu-id="90b9e-139">配置 keyspace 通知。</span><span class="sxs-lookup"><span data-stu-id="90b9e-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="90b9e-140">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="90b9e-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="90b9e-141">散列-最大值-ziplist-專案。</span><span class="sxs-lookup"><span data-stu-id="90b9e-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="90b9e-142">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="90b9e-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="90b9e-143">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="90b9e-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="90b9e-144">散列-最大值-ziplist。</span><span class="sxs-lookup"><span data-stu-id="90b9e-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="90b9e-145">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="90b9e-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="90b9e-146">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="90b9e-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="90b9e-147">intset-專案（最大值）。</span><span class="sxs-lookup"><span data-stu-id="90b9e-147">set-max-intset-entries.</span></span>
<span data-ttu-id="90b9e-148">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="90b9e-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="90b9e-149">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="90b9e-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="90b9e-150">zset-最大 ziplist 專案。</span><span class="sxs-lookup"><span data-stu-id="90b9e-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="90b9e-151">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="90b9e-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="90b9e-152">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="90b9e-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="90b9e-153">zset-最大 ziplist 值。</span><span class="sxs-lookup"><span data-stu-id="90b9e-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="90b9e-154">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="90b9e-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="90b9e-155">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="90b9e-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="90b9e-156">資料庫.</span><span class="sxs-lookup"><span data-stu-id="90b9e-156">databases.</span></span>
<span data-ttu-id="90b9e-157">設定資料庫的數目。</span><span class="sxs-lookup"><span data-stu-id="90b9e-157">Configures the number of databases.</span></span>
<span data-ttu-id="90b9e-158">這個屬性只能在建立快取記憶體時設定。</span><span class="sxs-lookup"><span data-stu-id="90b9e-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="90b9e-159">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="90b9e-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="90b9e-160">如需詳細資訊，請參閱使用 Azure PowerShell (管理 Azure Redis Cache http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) 。</span><span class="sxs-lookup"><span data-stu-id="90b9e-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="90b9e-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90b9e-161">-ResourceGroupName</span></span>
<span data-ttu-id="90b9e-162">指定包含 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90b9e-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="90b9e-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="90b9e-163">-ShardCount</span></span>
<span data-ttu-id="90b9e-164">指定要在 Premium 群集快取上建立的 shards 數目。</span><span class="sxs-lookup"><span data-stu-id="90b9e-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="90b9e-165">-大小</span><span class="sxs-lookup"><span data-stu-id="90b9e-165">-Size</span></span>
<span data-ttu-id="90b9e-166">指定 Redis 快取的大小。</span><span class="sxs-lookup"><span data-stu-id="90b9e-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="90b9e-167">有效值為：</span><span class="sxs-lookup"><span data-stu-id="90b9e-167">Valid values are:</span></span> 
- <span data-ttu-id="90b9e-168">P1</span><span class="sxs-lookup"><span data-stu-id="90b9e-168">P1</span></span>
- <span data-ttu-id="90b9e-169">又</span><span class="sxs-lookup"><span data-stu-id="90b9e-169">P2</span></span>
- <span data-ttu-id="90b9e-170">P3</span><span class="sxs-lookup"><span data-stu-id="90b9e-170">P3</span></span>
- <span data-ttu-id="90b9e-171">P4</span><span class="sxs-lookup"><span data-stu-id="90b9e-171">P4</span></span>
- <span data-ttu-id="90b9e-172">P5</span><span class="sxs-lookup"><span data-stu-id="90b9e-172">P5</span></span>
- <span data-ttu-id="90b9e-173">C0</span><span class="sxs-lookup"><span data-stu-id="90b9e-173">C0</span></span>
- <span data-ttu-id="90b9e-174">C1</span><span class="sxs-lookup"><span data-stu-id="90b9e-174">C1</span></span>
- <span data-ttu-id="90b9e-175">C3</span><span class="sxs-lookup"><span data-stu-id="90b9e-175">C2</span></span>
- <span data-ttu-id="90b9e-176">C3</span><span class="sxs-lookup"><span data-stu-id="90b9e-176">C3</span></span>
- <span data-ttu-id="90b9e-177">C4</span><span class="sxs-lookup"><span data-stu-id="90b9e-177">C4</span></span>
- <span data-ttu-id="90b9e-178">C5</span><span class="sxs-lookup"><span data-stu-id="90b9e-178">C5</span></span>
- <span data-ttu-id="90b9e-179">C6</span><span class="sxs-lookup"><span data-stu-id="90b9e-179">C6</span></span>
- <span data-ttu-id="90b9e-180">250MB</span><span class="sxs-lookup"><span data-stu-id="90b9e-180">250MB</span></span>
- <span data-ttu-id="90b9e-181">1GB</span><span class="sxs-lookup"><span data-stu-id="90b9e-181">1GB</span></span>
- <span data-ttu-id="90b9e-182">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="90b9e-182">2.5GB</span></span>
- <span data-ttu-id="90b9e-183">6GB</span><span class="sxs-lookup"><span data-stu-id="90b9e-183">6GB</span></span>
- <span data-ttu-id="90b9e-184">13GB</span><span class="sxs-lookup"><span data-stu-id="90b9e-184">13GB</span></span>
- <span data-ttu-id="90b9e-185">26GB</span><span class="sxs-lookup"><span data-stu-id="90b9e-185">26GB</span></span>
- <span data-ttu-id="90b9e-186">53GB</span><span class="sxs-lookup"><span data-stu-id="90b9e-186">53GB</span></span>
- <span data-ttu-id="90b9e-187">120GB 預設值為1GB 或 C1。</span><span class="sxs-lookup"><span data-stu-id="90b9e-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="90b9e-188">-Sku</span><span class="sxs-lookup"><span data-stu-id="90b9e-188">-Sku</span></span>
<span data-ttu-id="90b9e-189">指定要建立之 Redis 快取的 SKU。</span><span class="sxs-lookup"><span data-stu-id="90b9e-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="90b9e-190">有效值為：</span><span class="sxs-lookup"><span data-stu-id="90b9e-190">Valid values are:</span></span> 
- <span data-ttu-id="90b9e-191">空白</span><span class="sxs-lookup"><span data-stu-id="90b9e-191">Basic</span></span>
- <span data-ttu-id="90b9e-192">標準</span><span class="sxs-lookup"><span data-stu-id="90b9e-192">Standard</span></span>
- <span data-ttu-id="90b9e-193">[特優] 預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="90b9e-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="90b9e-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="90b9e-194">-Tag</span></span>
<span data-ttu-id="90b9e-195">代表標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="90b9e-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="90b9e-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="90b9e-196">-TenantSettings</span></span>
<span data-ttu-id="90b9e-197">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="90b9e-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="90b9e-198">-確認</span><span class="sxs-lookup"><span data-stu-id="90b9e-198">-Confirm</span></span>
<span data-ttu-id="90b9e-199">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90b9e-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90b9e-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90b9e-200">-WhatIf</span></span>
<span data-ttu-id="90b9e-201">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90b9e-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90b9e-202">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90b9e-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90b9e-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b9e-203">CommonParameters</span></span>
<span data-ttu-id="90b9e-204">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90b9e-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b9e-205">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="90b9e-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b9e-206">輸入</span><span class="sxs-lookup"><span data-stu-id="90b9e-206">INPUTS</span></span>

### <span data-ttu-id="90b9e-207">System.object</span><span class="sxs-lookup"><span data-stu-id="90b9e-207">System.String</span></span>

### <span data-ttu-id="90b9e-208">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="90b9e-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="90b9e-209">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="90b9e-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="90b9e-210">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="90b9e-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="90b9e-211">輸出</span><span class="sxs-lookup"><span data-stu-id="90b9e-211">OUTPUTS</span></span>

### <span data-ttu-id="90b9e-212">RedisCacheAttributesWithAccessKeys 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="90b9e-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="90b9e-213">筆記</span><span class="sxs-lookup"><span data-stu-id="90b9e-213">NOTES</span></span>

## <span data-ttu-id="90b9e-214">相關連結</span><span class="sxs-lookup"><span data-stu-id="90b9e-214">RELATED LINKS</span></span>

[<span data-ttu-id="90b9e-215">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90b9e-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="90b9e-216">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90b9e-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="90b9e-217">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90b9e-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


