---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139923"
---
# <span data-ttu-id="4cf8f-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4cf8f-101">New-AzRedisCache</span></span>

## <span data-ttu-id="4cf8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cf8f-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf8f-103">建立 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="4cf8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cf8f-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4cf8f-105">說明</span><span class="sxs-lookup"><span data-stu-id="4cf8f-105">DESCRIPTION</span></span>
<span data-ttu-id="4cf8f-106">**新的-AzRedisCache** Cmdlet 會建立 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="4cf8f-107">示例</span><span class="sxs-lookup"><span data-stu-id="4cf8f-107">EXAMPLES</span></span>

### <span data-ttu-id="4cf8f-108">範例1：建立 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="4cf8f-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="4cf8f-109">這個命令會建立 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="4cf8f-110">範例2：建立標準 SKU Redis 快取</span><span class="sxs-lookup"><span data-stu-id="4cf8f-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="4cf8f-111">這個命令會建立 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="4cf8f-112">參數</span><span class="sxs-lookup"><span data-stu-id="4cf8f-112">PARAMETERS</span></span>

### <span data-ttu-id="4cf8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf8f-113">-DefaultProfile</span></span>
<span data-ttu-id="4cf8f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cf8f-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="4cf8f-115">-EnableNonSslPort</span></span>
<span data-ttu-id="4cf8f-116">指出是否已啟用非 SSL 埠。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="4cf8f-117">預設值為 $False (停用非 SSL 埠) 。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="4cf8f-118">-位置</span><span class="sxs-lookup"><span data-stu-id="4cf8f-118">-Location</span></span>
<span data-ttu-id="4cf8f-119">指定要建立 Redis 快取的位置。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="4cf8f-120">有效值為：</span><span class="sxs-lookup"><span data-stu-id="4cf8f-120">Valid values are:</span></span> 
- <span data-ttu-id="4cf8f-121">美國中北部</span><span class="sxs-lookup"><span data-stu-id="4cf8f-121">North Central US</span></span>
- <span data-ttu-id="4cf8f-122">美國中南部</span><span class="sxs-lookup"><span data-stu-id="4cf8f-122">South Central US</span></span>
- <span data-ttu-id="4cf8f-123">美國中部</span><span class="sxs-lookup"><span data-stu-id="4cf8f-123">Central US</span></span>
- <span data-ttu-id="4cf8f-124">西歐</span><span class="sxs-lookup"><span data-stu-id="4cf8f-124">West Europe</span></span>
- <span data-ttu-id="4cf8f-125">北歐</span><span class="sxs-lookup"><span data-stu-id="4cf8f-125">North Europe</span></span>
- <span data-ttu-id="4cf8f-126">美國西部</span><span class="sxs-lookup"><span data-stu-id="4cf8f-126">West US</span></span>
- <span data-ttu-id="4cf8f-127">東美國</span><span class="sxs-lookup"><span data-stu-id="4cf8f-127">East US</span></span>
- <span data-ttu-id="4cf8f-128">東美國2</span><span class="sxs-lookup"><span data-stu-id="4cf8f-128">East US 2</span></span>
- <span data-ttu-id="4cf8f-129">日本東</span><span class="sxs-lookup"><span data-stu-id="4cf8f-129">Japan East</span></span>
- <span data-ttu-id="4cf8f-130">日本西部</span><span class="sxs-lookup"><span data-stu-id="4cf8f-130">Japan West</span></span>
- <span data-ttu-id="4cf8f-131">巴西南部</span><span class="sxs-lookup"><span data-stu-id="4cf8f-131">Brazil South</span></span>
- <span data-ttu-id="4cf8f-132">東南亞</span><span class="sxs-lookup"><span data-stu-id="4cf8f-132">Southeast Asia</span></span>
- <span data-ttu-id="4cf8f-133">東亞</span><span class="sxs-lookup"><span data-stu-id="4cf8f-133">East Asia</span></span>
- <span data-ttu-id="4cf8f-134">澳大利亞東</span><span class="sxs-lookup"><span data-stu-id="4cf8f-134">Australia East</span></span>
- <span data-ttu-id="4cf8f-135">澳大利亞東南部</span><span class="sxs-lookup"><span data-stu-id="4cf8f-135">Australia Southeast</span></span>

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

### <span data-ttu-id="4cf8f-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4cf8f-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="4cf8f-137">指定用戶端連接至快取所需的 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="4cf8f-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cf8f-138">-Name</span></span>
<span data-ttu-id="4cf8f-139">指定要建立之 Redis 緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="4cf8f-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cf8f-140">-RedisConfiguration</span></span>
<span data-ttu-id="4cf8f-141">指定 Redis 設定。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="4cf8f-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4cf8f-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4cf8f-143">rdb-備份-啟用。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="4cf8f-144">指定已啟用 Redis 資料暫留。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="4cf8f-145">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-145">Premium tier only.</span></span>
- <span data-ttu-id="4cf8f-146">rdb-儲存體-連接字串。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="4cf8f-147">指定 Redis 資料暫留的儲存空間帳戶連接字串。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="4cf8f-148">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-148">Premium tier only.</span></span>
- <span data-ttu-id="4cf8f-149">rdb-備份頻率。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="4cf8f-150">指定 Redis 資料暫留的備份頻率。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="4cf8f-151">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-151">Premium tier only.</span></span> 
- <span data-ttu-id="4cf8f-152">maxmemory-保留。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-152">maxmemory-reserved.</span></span>
<span data-ttu-id="4cf8f-153">針對非快取程式配置保留的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="4cf8f-154">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4cf8f-155">maxmemory-原則。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-155">maxmemory-policy.</span></span>
<span data-ttu-id="4cf8f-156">設定快取的快取原則。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="4cf8f-157">所有定價層。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-157">All pricing tiers.</span></span> 
- <span data-ttu-id="4cf8f-158">notify-keyspace-事件。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-158">notify-keyspace-events.</span></span>
<span data-ttu-id="4cf8f-159">配置 keyspace 通知。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="4cf8f-160">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="4cf8f-161">散列-最大值-ziplist-專案。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="4cf8f-162">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4cf8f-163">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4cf8f-164">散列-最大值-ziplist。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="4cf8f-165">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4cf8f-166">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4cf8f-167">intset-專案（最大值）。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-167">set-max-intset-entries.</span></span>
<span data-ttu-id="4cf8f-168">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4cf8f-169">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4cf8f-170">zset-最大 ziplist 專案。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="4cf8f-171">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4cf8f-172">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4cf8f-173">zset-最大 ziplist 值。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="4cf8f-174">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="4cf8f-175">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="4cf8f-176">資料庫.</span><span class="sxs-lookup"><span data-stu-id="4cf8f-176">databases.</span></span>
<span data-ttu-id="4cf8f-177">設定資料庫的數目。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-177">Configures the number of databases.</span></span>
<span data-ttu-id="4cf8f-178">這個屬性只能在建立快取記憶體時設定。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="4cf8f-179">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="4cf8f-180">如需詳細資訊，請參閱使用 Azure PowerShell (管理 Azure Redis Cache http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) 。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="4cf8f-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf8f-181">-ResourceGroupName</span></span>
<span data-ttu-id="4cf8f-182">指定要在其中建立 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="4cf8f-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="4cf8f-183">-ShardCount</span></span>
<span data-ttu-id="4cf8f-184">指定要在 Premium 群集快取上建立的 shards 數目。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="4cf8f-185">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4cf8f-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4cf8f-186">sr-1</span><span class="sxs-lookup"><span data-stu-id="4cf8f-186">1</span></span>
- <span data-ttu-id="4cf8f-187">pplx-2</span><span class="sxs-lookup"><span data-stu-id="4cf8f-187">2</span></span>
- <span data-ttu-id="4cf8f-188">3</span><span class="sxs-lookup"><span data-stu-id="4cf8f-188">3</span></span>
- <span data-ttu-id="4cf8f-189">4</span><span class="sxs-lookup"><span data-stu-id="4cf8f-189">4</span></span>
- <span data-ttu-id="4cf8f-190">500</span><span class="sxs-lookup"><span data-stu-id="4cf8f-190">5</span></span>
- <span data-ttu-id="4cf8f-191">6</span><span class="sxs-lookup"><span data-stu-id="4cf8f-191">6</span></span>
- <span data-ttu-id="4cf8f-192">utf-7</span><span class="sxs-lookup"><span data-stu-id="4cf8f-192">7</span></span>
- <span data-ttu-id="4cf8f-193">型</span><span class="sxs-lookup"><span data-stu-id="4cf8f-193">8</span></span>
- <span data-ttu-id="4cf8f-194">9</span><span class="sxs-lookup"><span data-stu-id="4cf8f-194">9</span></span> 
- <span data-ttu-id="4cf8f-195">第</span><span class="sxs-lookup"><span data-stu-id="4cf8f-195">10</span></span>

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

### <span data-ttu-id="4cf8f-196">-大小</span><span class="sxs-lookup"><span data-stu-id="4cf8f-196">-Size</span></span>
<span data-ttu-id="4cf8f-197">指定 Redis 快取的大小。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="4cf8f-198">有效值為：</span><span class="sxs-lookup"><span data-stu-id="4cf8f-198">Valid values are:</span></span> 
- <span data-ttu-id="4cf8f-199">P1</span><span class="sxs-lookup"><span data-stu-id="4cf8f-199">P1</span></span>
- <span data-ttu-id="4cf8f-200">又</span><span class="sxs-lookup"><span data-stu-id="4cf8f-200">P2</span></span>
- <span data-ttu-id="4cf8f-201">P3</span><span class="sxs-lookup"><span data-stu-id="4cf8f-201">P3</span></span>
- <span data-ttu-id="4cf8f-202">P4</span><span class="sxs-lookup"><span data-stu-id="4cf8f-202">P4</span></span>
- <span data-ttu-id="4cf8f-203">P5</span><span class="sxs-lookup"><span data-stu-id="4cf8f-203">P5</span></span>
- <span data-ttu-id="4cf8f-204">C0</span><span class="sxs-lookup"><span data-stu-id="4cf8f-204">C0</span></span>
- <span data-ttu-id="4cf8f-205">C1</span><span class="sxs-lookup"><span data-stu-id="4cf8f-205">C1</span></span>
- <span data-ttu-id="4cf8f-206">C3</span><span class="sxs-lookup"><span data-stu-id="4cf8f-206">C2</span></span>
- <span data-ttu-id="4cf8f-207">C3</span><span class="sxs-lookup"><span data-stu-id="4cf8f-207">C3</span></span>
- <span data-ttu-id="4cf8f-208">C4</span><span class="sxs-lookup"><span data-stu-id="4cf8f-208">C4</span></span>
- <span data-ttu-id="4cf8f-209">C5</span><span class="sxs-lookup"><span data-stu-id="4cf8f-209">C5</span></span>
- <span data-ttu-id="4cf8f-210">C6</span><span class="sxs-lookup"><span data-stu-id="4cf8f-210">C6</span></span>
- <span data-ttu-id="4cf8f-211">250MB</span><span class="sxs-lookup"><span data-stu-id="4cf8f-211">250MB</span></span>
- <span data-ttu-id="4cf8f-212">1GB</span><span class="sxs-lookup"><span data-stu-id="4cf8f-212">1GB</span></span>
- <span data-ttu-id="4cf8f-213">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="4cf8f-213">2.5GB</span></span>
- <span data-ttu-id="4cf8f-214">6GB</span><span class="sxs-lookup"><span data-stu-id="4cf8f-214">6GB</span></span>
- <span data-ttu-id="4cf8f-215">13GB</span><span class="sxs-lookup"><span data-stu-id="4cf8f-215">13GB</span></span>
- <span data-ttu-id="4cf8f-216">26GB</span><span class="sxs-lookup"><span data-stu-id="4cf8f-216">26GB</span></span>
- <span data-ttu-id="4cf8f-217">53GB 預設值為1GB 或 C1。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="4cf8f-218">-Sku</span><span class="sxs-lookup"><span data-stu-id="4cf8f-218">-Sku</span></span>
<span data-ttu-id="4cf8f-219">指定要建立之 Redis 快取的 SKU。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="4cf8f-220">有效值為：</span><span class="sxs-lookup"><span data-stu-id="4cf8f-220">Valid values are:</span></span> 
- <span data-ttu-id="4cf8f-221">空白</span><span class="sxs-lookup"><span data-stu-id="4cf8f-221">Basic</span></span>
- <span data-ttu-id="4cf8f-222">標準</span><span class="sxs-lookup"><span data-stu-id="4cf8f-222">Standard</span></span>
- <span data-ttu-id="4cf8f-223">[特優] 預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="4cf8f-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="4cf8f-224">-StaticIP</span></span>
<span data-ttu-id="4cf8f-225">在 Redis 快取的子網上指定唯一的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="4cf8f-226">如果您沒有指定此參數的值，這個 Cmdlet 會從子網上選擇 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="4cf8f-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4cf8f-227">-SubnetId</span></span>
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

### <span data-ttu-id="4cf8f-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="4cf8f-228">-Tag</span></span>
<span data-ttu-id="4cf8f-229">代表標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="4cf8f-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="4cf8f-230">-TenantSettings</span></span>
<span data-ttu-id="4cf8f-231">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="4cf8f-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="4cf8f-232">-Zone</span></span>
<span data-ttu-id="4cf8f-233">區域清單。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-233">List of zones.</span></span>

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

### <span data-ttu-id="4cf8f-234">-確認</span><span class="sxs-lookup"><span data-stu-id="4cf8f-234">-Confirm</span></span>
<span data-ttu-id="4cf8f-235">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cf8f-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cf8f-236">-WhatIf</span></span>
<span data-ttu-id="4cf8f-237">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cf8f-238">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cf8f-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf8f-239">CommonParameters</span></span>
<span data-ttu-id="4cf8f-240">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf8f-241">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf8f-242">輸入</span><span class="sxs-lookup"><span data-stu-id="4cf8f-242">INPUTS</span></span>

### <span data-ttu-id="4cf8f-243">System.object</span><span class="sxs-lookup"><span data-stu-id="4cf8f-243">System.String</span></span>

### <span data-ttu-id="4cf8f-244">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4cf8f-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4cf8f-245">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4cf8f-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4cf8f-246">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4cf8f-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4cf8f-247">System.object []</span><span class="sxs-lookup"><span data-stu-id="4cf8f-247">System.String[]</span></span>

## <span data-ttu-id="4cf8f-248">輸出</span><span class="sxs-lookup"><span data-stu-id="4cf8f-248">OUTPUTS</span></span>

### <span data-ttu-id="4cf8f-249">RedisCacheAttributesWithAccessKeys 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="4cf8f-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="4cf8f-250">筆記</span><span class="sxs-lookup"><span data-stu-id="4cf8f-250">NOTES</span></span>

## <span data-ttu-id="4cf8f-251">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cf8f-251">RELATED LINKS</span></span>

[<span data-ttu-id="4cf8f-252">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4cf8f-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="4cf8f-253">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4cf8f-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="4cf8f-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4cf8f-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


