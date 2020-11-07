---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: ab0b84578339568e48458de8a89daccd83092e65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791821"
---
# <span data-ttu-id="04c00-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04c00-101">New-AzRedisCache</span></span>

## <span data-ttu-id="04c00-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04c00-102">SYNOPSIS</span></span>
<span data-ttu-id="04c00-103">建立 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="04c00-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="04c00-104">句法</span><span class="sxs-lookup"><span data-stu-id="04c00-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04c00-105">說明</span><span class="sxs-lookup"><span data-stu-id="04c00-105">DESCRIPTION</span></span>
<span data-ttu-id="04c00-106">**新的-AzRedisCache** Cmdlet 會建立 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="04c00-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="04c00-107">示例</span><span class="sxs-lookup"><span data-stu-id="04c00-107">EXAMPLES</span></span>

### <span data-ttu-id="04c00-108">範例1：建立 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="04c00-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="04c00-109">這個命令會建立 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="04c00-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="04c00-110">範例2：建立標準 SKU Redis 快取</span><span class="sxs-lookup"><span data-stu-id="04c00-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="04c00-111">這個命令會建立 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="04c00-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="04c00-112">參數</span><span class="sxs-lookup"><span data-stu-id="04c00-112">PARAMETERS</span></span>

### <span data-ttu-id="04c00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c00-113">-DefaultProfile</span></span>
<span data-ttu-id="04c00-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04c00-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04c00-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="04c00-115">-EnableNonSslPort</span></span>
<span data-ttu-id="04c00-116">指出是否已啟用非 SSL 埠。</span><span class="sxs-lookup"><span data-stu-id="04c00-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="04c00-117">預設值為 $False (停用非 SSL 埠) 。</span><span class="sxs-lookup"><span data-stu-id="04c00-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="04c00-118">-位置</span><span class="sxs-lookup"><span data-stu-id="04c00-118">-Location</span></span>
<span data-ttu-id="04c00-119">指定要建立 Redis 快取的位置。</span><span class="sxs-lookup"><span data-stu-id="04c00-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="04c00-120">有效值為：</span><span class="sxs-lookup"><span data-stu-id="04c00-120">Valid values are:</span></span> 
- <span data-ttu-id="04c00-121">美國中北部</span><span class="sxs-lookup"><span data-stu-id="04c00-121">North Central US</span></span>
- <span data-ttu-id="04c00-122">美國中南部</span><span class="sxs-lookup"><span data-stu-id="04c00-122">South Central US</span></span>
- <span data-ttu-id="04c00-123">美國中部</span><span class="sxs-lookup"><span data-stu-id="04c00-123">Central US</span></span>
- <span data-ttu-id="04c00-124">西歐</span><span class="sxs-lookup"><span data-stu-id="04c00-124">West Europe</span></span>
- <span data-ttu-id="04c00-125">北歐</span><span class="sxs-lookup"><span data-stu-id="04c00-125">North Europe</span></span>
- <span data-ttu-id="04c00-126">美國西部</span><span class="sxs-lookup"><span data-stu-id="04c00-126">West US</span></span>
- <span data-ttu-id="04c00-127">東美國</span><span class="sxs-lookup"><span data-stu-id="04c00-127">East US</span></span>
- <span data-ttu-id="04c00-128">東美國2</span><span class="sxs-lookup"><span data-stu-id="04c00-128">East US 2</span></span>
- <span data-ttu-id="04c00-129">日本東</span><span class="sxs-lookup"><span data-stu-id="04c00-129">Japan East</span></span>
- <span data-ttu-id="04c00-130">日本西部</span><span class="sxs-lookup"><span data-stu-id="04c00-130">Japan West</span></span>
- <span data-ttu-id="04c00-131">巴西南部</span><span class="sxs-lookup"><span data-stu-id="04c00-131">Brazil South</span></span>
- <span data-ttu-id="04c00-132">東南亞</span><span class="sxs-lookup"><span data-stu-id="04c00-132">Southeast Asia</span></span>
- <span data-ttu-id="04c00-133">東亞</span><span class="sxs-lookup"><span data-stu-id="04c00-133">East Asia</span></span>
- <span data-ttu-id="04c00-134">澳大利亞東</span><span class="sxs-lookup"><span data-stu-id="04c00-134">Australia East</span></span>
- <span data-ttu-id="04c00-135">澳大利亞東南部</span><span class="sxs-lookup"><span data-stu-id="04c00-135">Australia Southeast</span></span>

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

### <span data-ttu-id="04c00-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="04c00-136">-Name</span></span>
<span data-ttu-id="04c00-137">指定要建立之 Redis 緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c00-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="04c00-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="04c00-138">-RedisConfiguration</span></span>
<span data-ttu-id="04c00-139">指定 Redis 設定。</span><span class="sxs-lookup"><span data-stu-id="04c00-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="04c00-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="04c00-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="04c00-141">rdb-備份-啟用。</span><span class="sxs-lookup"><span data-stu-id="04c00-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="04c00-142">指定已啟用 Redis 資料暫留。</span><span class="sxs-lookup"><span data-stu-id="04c00-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="04c00-143">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="04c00-143">Premium tier only.</span></span>
- <span data-ttu-id="04c00-144">rdb-儲存體-連接字串。</span><span class="sxs-lookup"><span data-stu-id="04c00-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="04c00-145">指定 Redis 資料暫留的儲存空間帳戶連接字串。</span><span class="sxs-lookup"><span data-stu-id="04c00-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="04c00-146">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="04c00-146">Premium tier only.</span></span>
- <span data-ttu-id="04c00-147">rdb-備份頻率。</span><span class="sxs-lookup"><span data-stu-id="04c00-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="04c00-148">指定 Redis 資料暫留的備份頻率。</span><span class="sxs-lookup"><span data-stu-id="04c00-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="04c00-149">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="04c00-149">Premium tier only.</span></span> 
- <span data-ttu-id="04c00-150">maxmemory-保留。</span><span class="sxs-lookup"><span data-stu-id="04c00-150">maxmemory-reserved.</span></span>
<span data-ttu-id="04c00-151">針對非快取程式配置保留的記憶體。</span><span class="sxs-lookup"><span data-stu-id="04c00-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="04c00-152">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="04c00-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04c00-153">maxmemory-原則。</span><span class="sxs-lookup"><span data-stu-id="04c00-153">maxmemory-policy.</span></span>
<span data-ttu-id="04c00-154">設定快取的快取原則。</span><span class="sxs-lookup"><span data-stu-id="04c00-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="04c00-155">所有定價層。</span><span class="sxs-lookup"><span data-stu-id="04c00-155">All pricing tiers.</span></span> 
- <span data-ttu-id="04c00-156">notify-keyspace-事件。</span><span class="sxs-lookup"><span data-stu-id="04c00-156">notify-keyspace-events.</span></span>
<span data-ttu-id="04c00-157">配置 keyspace 通知。</span><span class="sxs-lookup"><span data-stu-id="04c00-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="04c00-158">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="04c00-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="04c00-159">散列-最大值-ziplist-專案。</span><span class="sxs-lookup"><span data-stu-id="04c00-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="04c00-160">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="04c00-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04c00-161">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="04c00-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04c00-162">散列-最大值-ziplist。</span><span class="sxs-lookup"><span data-stu-id="04c00-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="04c00-163">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="04c00-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04c00-164">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="04c00-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04c00-165">intset-專案（最大值）。</span><span class="sxs-lookup"><span data-stu-id="04c00-165">set-max-intset-entries.</span></span>
<span data-ttu-id="04c00-166">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="04c00-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04c00-167">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="04c00-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04c00-168">zset-最大 ziplist 專案。</span><span class="sxs-lookup"><span data-stu-id="04c00-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="04c00-169">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="04c00-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04c00-170">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="04c00-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04c00-171">zset-最大 ziplist 值。</span><span class="sxs-lookup"><span data-stu-id="04c00-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="04c00-172">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="04c00-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04c00-173">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="04c00-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04c00-174">資料庫.</span><span class="sxs-lookup"><span data-stu-id="04c00-174">databases.</span></span>
<span data-ttu-id="04c00-175">設定資料庫的數目。</span><span class="sxs-lookup"><span data-stu-id="04c00-175">Configures the number of databases.</span></span>
<span data-ttu-id="04c00-176">這個屬性只能在建立快取記憶體時設定。</span><span class="sxs-lookup"><span data-stu-id="04c00-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="04c00-177">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="04c00-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="04c00-178">如需詳細資訊，請參閱使用 Azure PowerShell (管理 Azure Redis Cache https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) 。</span><span class="sxs-lookup"><span data-stu-id="04c00-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="04c00-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04c00-179">-ResourceGroupName</span></span>
<span data-ttu-id="04c00-180">指定要在其中建立 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c00-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="04c00-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="04c00-181">-ShardCount</span></span>
<span data-ttu-id="04c00-182">指定要在 Premium 群集快取上建立的 shards 數目。</span><span class="sxs-lookup"><span data-stu-id="04c00-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="04c00-183">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="04c00-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="04c00-184">sr-1</span><span class="sxs-lookup"><span data-stu-id="04c00-184">1</span></span>
- <span data-ttu-id="04c00-185">pplx-2</span><span class="sxs-lookup"><span data-stu-id="04c00-185">2</span></span>
- <span data-ttu-id="04c00-186">3</span><span class="sxs-lookup"><span data-stu-id="04c00-186">3</span></span>
- <span data-ttu-id="04c00-187">4</span><span class="sxs-lookup"><span data-stu-id="04c00-187">4</span></span>
- <span data-ttu-id="04c00-188">500</span><span class="sxs-lookup"><span data-stu-id="04c00-188">5</span></span>
- <span data-ttu-id="04c00-189">6</span><span class="sxs-lookup"><span data-stu-id="04c00-189">6</span></span>
- <span data-ttu-id="04c00-190">utf-7</span><span class="sxs-lookup"><span data-stu-id="04c00-190">7</span></span>
- <span data-ttu-id="04c00-191">型</span><span class="sxs-lookup"><span data-stu-id="04c00-191">8</span></span>
- <span data-ttu-id="04c00-192">9</span><span class="sxs-lookup"><span data-stu-id="04c00-192">9</span></span> 
- <span data-ttu-id="04c00-193">第</span><span class="sxs-lookup"><span data-stu-id="04c00-193">10</span></span>

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

### <span data-ttu-id="04c00-194">-大小</span><span class="sxs-lookup"><span data-stu-id="04c00-194">-Size</span></span>
<span data-ttu-id="04c00-195">指定 Redis 快取的大小。</span><span class="sxs-lookup"><span data-stu-id="04c00-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="04c00-196">有效值為：</span><span class="sxs-lookup"><span data-stu-id="04c00-196">Valid values are:</span></span> 
- <span data-ttu-id="04c00-197">P1</span><span class="sxs-lookup"><span data-stu-id="04c00-197">P1</span></span>
- <span data-ttu-id="04c00-198">又</span><span class="sxs-lookup"><span data-stu-id="04c00-198">P2</span></span>
- <span data-ttu-id="04c00-199">P3</span><span class="sxs-lookup"><span data-stu-id="04c00-199">P3</span></span>
- <span data-ttu-id="04c00-200">P4</span><span class="sxs-lookup"><span data-stu-id="04c00-200">P4</span></span>
- <span data-ttu-id="04c00-201">C0</span><span class="sxs-lookup"><span data-stu-id="04c00-201">C0</span></span>
- <span data-ttu-id="04c00-202">C1</span><span class="sxs-lookup"><span data-stu-id="04c00-202">C1</span></span>
- <span data-ttu-id="04c00-203">C3</span><span class="sxs-lookup"><span data-stu-id="04c00-203">C2</span></span>
- <span data-ttu-id="04c00-204">C3</span><span class="sxs-lookup"><span data-stu-id="04c00-204">C3</span></span>
- <span data-ttu-id="04c00-205">C4</span><span class="sxs-lookup"><span data-stu-id="04c00-205">C4</span></span>
- <span data-ttu-id="04c00-206">C5</span><span class="sxs-lookup"><span data-stu-id="04c00-206">C5</span></span>
- <span data-ttu-id="04c00-207">C6</span><span class="sxs-lookup"><span data-stu-id="04c00-207">C6</span></span>
- <span data-ttu-id="04c00-208">250MB</span><span class="sxs-lookup"><span data-stu-id="04c00-208">250MB</span></span>
- <span data-ttu-id="04c00-209">1GB</span><span class="sxs-lookup"><span data-stu-id="04c00-209">1GB</span></span>
- <span data-ttu-id="04c00-210">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="04c00-210">2.5GB</span></span>
- <span data-ttu-id="04c00-211">6GB</span><span class="sxs-lookup"><span data-stu-id="04c00-211">6GB</span></span>
- <span data-ttu-id="04c00-212">13GB</span><span class="sxs-lookup"><span data-stu-id="04c00-212">13GB</span></span>
- <span data-ttu-id="04c00-213">26GB</span><span class="sxs-lookup"><span data-stu-id="04c00-213">26GB</span></span>
- <span data-ttu-id="04c00-214">53GB 預設值為1GB 或 C1。</span><span class="sxs-lookup"><span data-stu-id="04c00-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="04c00-215">-Sku</span><span class="sxs-lookup"><span data-stu-id="04c00-215">-Sku</span></span>
<span data-ttu-id="04c00-216">指定要建立之 Redis 快取的 SKU。</span><span class="sxs-lookup"><span data-stu-id="04c00-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="04c00-217">有效值為：</span><span class="sxs-lookup"><span data-stu-id="04c00-217">Valid values are:</span></span> 
- <span data-ttu-id="04c00-218">空白</span><span class="sxs-lookup"><span data-stu-id="04c00-218">Basic</span></span>
- <span data-ttu-id="04c00-219">標準</span><span class="sxs-lookup"><span data-stu-id="04c00-219">Standard</span></span>
- <span data-ttu-id="04c00-220">[特優] 預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="04c00-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="04c00-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="04c00-221">-StaticIP</span></span>
<span data-ttu-id="04c00-222">在 Redis 快取的子網上指定唯一的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="04c00-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="04c00-223">如果您沒有指定此參數的值，這個 Cmdlet 會從子網上選擇 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="04c00-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="04c00-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="04c00-224">-SubnetId</span></span>
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

### <span data-ttu-id="04c00-225">-Tag</span><span class="sxs-lookup"><span data-stu-id="04c00-225">-Tag</span></span>
<span data-ttu-id="04c00-226">代表標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="04c00-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="04c00-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="04c00-227">-TenantSettings</span></span>
<span data-ttu-id="04c00-228">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="04c00-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="04c00-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="04c00-229">-Zone</span></span>
<span data-ttu-id="04c00-230">區域清單。</span><span class="sxs-lookup"><span data-stu-id="04c00-230">List of zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04c00-231">-確認</span><span class="sxs-lookup"><span data-stu-id="04c00-231">-Confirm</span></span>
<span data-ttu-id="04c00-232">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04c00-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04c00-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04c00-233">-WhatIf</span></span>
<span data-ttu-id="04c00-234">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04c00-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04c00-235">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04c00-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04c00-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c00-236">CommonParameters</span></span>
<span data-ttu-id="04c00-237">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04c00-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c00-238">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="04c00-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c00-239">輸入</span><span class="sxs-lookup"><span data-stu-id="04c00-239">INPUTS</span></span>

### <span data-ttu-id="04c00-240">System.object</span><span class="sxs-lookup"><span data-stu-id="04c00-240">System.String</span></span>

### <span data-ttu-id="04c00-241">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="04c00-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="04c00-242">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04c00-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="04c00-243">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04c00-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="04c00-244">System.object []</span><span class="sxs-lookup"><span data-stu-id="04c00-244">System.String[]</span></span>

## <span data-ttu-id="04c00-245">輸出</span><span class="sxs-lookup"><span data-stu-id="04c00-245">OUTPUTS</span></span>

### <span data-ttu-id="04c00-246">RedisCacheAttributesWithAccessKeys 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="04c00-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="04c00-247">筆記</span><span class="sxs-lookup"><span data-stu-id="04c00-247">NOTES</span></span>

## <span data-ttu-id="04c00-248">相關連結</span><span class="sxs-lookup"><span data-stu-id="04c00-248">RELATED LINKS</span></span>

[<span data-ttu-id="04c00-249">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04c00-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="04c00-250">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04c00-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="04c00-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04c00-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


