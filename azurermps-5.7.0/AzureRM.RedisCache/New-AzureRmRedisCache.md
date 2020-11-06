---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447697"
---
# <span data-ttu-id="c70b9-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c70b9-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="c70b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c70b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c70b9-103">建立 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="c70b9-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c70b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c70b9-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c70b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="c70b9-105">DESCRIPTION</span></span>
<span data-ttu-id="c70b9-106">**新的-AzureRmRedisCache** Cmdlet 會建立 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="c70b9-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="c70b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="c70b9-107">EXAMPLES</span></span>

### <span data-ttu-id="c70b9-108">範例1：建立 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="c70b9-108">Example 1: Create a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="c70b9-109">這個命令會建立 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="c70b9-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="c70b9-110">範例2：建立標準 SKU Redis 快取</span><span class="sxs-lookup"><span data-stu-id="c70b9-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="c70b9-111">這個命令會建立 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="c70b9-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="c70b9-112">參數</span><span class="sxs-lookup"><span data-stu-id="c70b9-112">PARAMETERS</span></span>

### <span data-ttu-id="c70b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c70b9-113">-DefaultProfile</span></span>
<span data-ttu-id="c70b9-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c70b9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c70b9-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="c70b9-115">-EnableNonSslPort</span></span>
<span data-ttu-id="c70b9-116">指出是否已啟用非 SSL 埠。</span><span class="sxs-lookup"><span data-stu-id="c70b9-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="c70b9-117">預設值為 $False (停用非 SSL 埠) 。</span><span class="sxs-lookup"><span data-stu-id="c70b9-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="c70b9-118">-位置</span><span class="sxs-lookup"><span data-stu-id="c70b9-118">-Location</span></span>
<span data-ttu-id="c70b9-119">指定要建立 Redis 快取的位置。</span><span class="sxs-lookup"><span data-stu-id="c70b9-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="c70b9-120">有效值為：</span><span class="sxs-lookup"><span data-stu-id="c70b9-120">Valid values are:</span></span> 

- <span data-ttu-id="c70b9-121">美國中北部</span><span class="sxs-lookup"><span data-stu-id="c70b9-121">North Central US</span></span>
- <span data-ttu-id="c70b9-122">美國中南部</span><span class="sxs-lookup"><span data-stu-id="c70b9-122">South Central US</span></span>
- <span data-ttu-id="c70b9-123">美國中部</span><span class="sxs-lookup"><span data-stu-id="c70b9-123">Central US</span></span>
- <span data-ttu-id="c70b9-124">西歐</span><span class="sxs-lookup"><span data-stu-id="c70b9-124">West Europe</span></span>
- <span data-ttu-id="c70b9-125">北歐</span><span class="sxs-lookup"><span data-stu-id="c70b9-125">North Europe</span></span>
- <span data-ttu-id="c70b9-126">美國西部</span><span class="sxs-lookup"><span data-stu-id="c70b9-126">West US</span></span>
- <span data-ttu-id="c70b9-127">東美國</span><span class="sxs-lookup"><span data-stu-id="c70b9-127">East US</span></span>
- <span data-ttu-id="c70b9-128">東美國2</span><span class="sxs-lookup"><span data-stu-id="c70b9-128">East US 2</span></span>
- <span data-ttu-id="c70b9-129">日本東</span><span class="sxs-lookup"><span data-stu-id="c70b9-129">Japan East</span></span>
- <span data-ttu-id="c70b9-130">日本西部</span><span class="sxs-lookup"><span data-stu-id="c70b9-130">Japan West</span></span>
- <span data-ttu-id="c70b9-131">巴西南部</span><span class="sxs-lookup"><span data-stu-id="c70b9-131">Brazil South</span></span>
- <span data-ttu-id="c70b9-132">東南亞</span><span class="sxs-lookup"><span data-stu-id="c70b9-132">Southeast Asia</span></span>
- <span data-ttu-id="c70b9-133">東亞</span><span class="sxs-lookup"><span data-stu-id="c70b9-133">East Asia</span></span>
- <span data-ttu-id="c70b9-134">澳大利亞東</span><span class="sxs-lookup"><span data-stu-id="c70b9-134">Australia East</span></span>
- <span data-ttu-id="c70b9-135">澳大利亞東南部</span><span class="sxs-lookup"><span data-stu-id="c70b9-135">Australia Southeast</span></span>

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

### <span data-ttu-id="c70b9-136">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="c70b9-136">-MaxMemoryPolicy</span></span>
<span data-ttu-id="c70b9-137">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="c70b9-137">This parameter has been deprecated.</span></span>
<span data-ttu-id="c70b9-138">使用 *RedisConfiguration* 參數來設定 maxmemory 原則。</span><span class="sxs-lookup"><span data-stu-id="c70b9-138">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="c70b9-139">例如：</span><span class="sxs-lookup"><span data-stu-id="c70b9-139">For example:</span></span> 

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

### <span data-ttu-id="c70b9-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="c70b9-140">-Name</span></span>
<span data-ttu-id="c70b9-141">指定要建立之 Redis 緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="c70b9-141">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="c70b9-142">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="c70b9-142">-RedisConfiguration</span></span>
<span data-ttu-id="c70b9-143">指定 Redis 設定。</span><span class="sxs-lookup"><span data-stu-id="c70b9-143">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="c70b9-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c70b9-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c70b9-145">rdb-備份-啟用。</span><span class="sxs-lookup"><span data-stu-id="c70b9-145">rdb-backup-enabled.</span></span>
<span data-ttu-id="c70b9-146">指定已啟用 Redis 資料暫留。</span><span class="sxs-lookup"><span data-stu-id="c70b9-146">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="c70b9-147">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="c70b9-147">Premium tier only.</span></span>
- <span data-ttu-id="c70b9-148">rdb-儲存體-連接字串。</span><span class="sxs-lookup"><span data-stu-id="c70b9-148">rdb-storage-connection-string.</span></span>
<span data-ttu-id="c70b9-149">指定 Redis 資料暫留的儲存空間帳戶連接字串。</span><span class="sxs-lookup"><span data-stu-id="c70b9-149">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="c70b9-150">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="c70b9-150">Premium tier only.</span></span>
- <span data-ttu-id="c70b9-151">rdb-備份頻率。</span><span class="sxs-lookup"><span data-stu-id="c70b9-151">rdb-backup-frequency.</span></span>
<span data-ttu-id="c70b9-152">指定 Redis 資料暫留的備份頻率。</span><span class="sxs-lookup"><span data-stu-id="c70b9-152">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="c70b9-153">僅限 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="c70b9-153">Premium tier only.</span></span> 
- <span data-ttu-id="c70b9-154">maxmemory-保留。</span><span class="sxs-lookup"><span data-stu-id="c70b9-154">maxmemory-reserved.</span></span>
<span data-ttu-id="c70b9-155">針對非快取程式配置保留的記憶體。</span><span class="sxs-lookup"><span data-stu-id="c70b9-155">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="c70b9-156">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="c70b9-156">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c70b9-157">maxmemory-原則。</span><span class="sxs-lookup"><span data-stu-id="c70b9-157">maxmemory-policy.</span></span>
<span data-ttu-id="c70b9-158">設定快取的快取原則。</span><span class="sxs-lookup"><span data-stu-id="c70b9-158">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="c70b9-159">所有定價層。</span><span class="sxs-lookup"><span data-stu-id="c70b9-159">All pricing tiers.</span></span> 
- <span data-ttu-id="c70b9-160">notify-keyspace-事件。</span><span class="sxs-lookup"><span data-stu-id="c70b9-160">notify-keyspace-events.</span></span>
<span data-ttu-id="c70b9-161">配置 keyspace 通知。</span><span class="sxs-lookup"><span data-stu-id="c70b9-161">Configures keyspace notifications.</span></span>
<span data-ttu-id="c70b9-162">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="c70b9-162">Standard and premium tiers.</span></span> 
- <span data-ttu-id="c70b9-163">散列-最大值-ziplist-專案。</span><span class="sxs-lookup"><span data-stu-id="c70b9-163">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="c70b9-164">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="c70b9-164">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c70b9-165">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="c70b9-165">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c70b9-166">散列-最大值-ziplist。</span><span class="sxs-lookup"><span data-stu-id="c70b9-166">hash-max-ziplist-value.</span></span>
<span data-ttu-id="c70b9-167">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="c70b9-167">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c70b9-168">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="c70b9-168">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c70b9-169">intset-專案（最大值）。</span><span class="sxs-lookup"><span data-stu-id="c70b9-169">set-max-intset-entries.</span></span>
<span data-ttu-id="c70b9-170">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="c70b9-170">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c70b9-171">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="c70b9-171">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c70b9-172">zset-最大 ziplist 專案。</span><span class="sxs-lookup"><span data-stu-id="c70b9-172">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="c70b9-173">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="c70b9-173">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c70b9-174">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="c70b9-174">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c70b9-175">zset-最大 ziplist 值。</span><span class="sxs-lookup"><span data-stu-id="c70b9-175">zset-max-ziplist-value.</span></span>
<span data-ttu-id="c70b9-176">針對小型匯總資料類型配置記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="c70b9-176">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c70b9-177">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="c70b9-177">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c70b9-178">資料庫.</span><span class="sxs-lookup"><span data-stu-id="c70b9-178">databases.</span></span>
<span data-ttu-id="c70b9-179">設定資料庫的數目。</span><span class="sxs-lookup"><span data-stu-id="c70b9-179">Configures the number of databases.</span></span>
<span data-ttu-id="c70b9-180">這個屬性只能在建立快取記憶體時設定。</span><span class="sxs-lookup"><span data-stu-id="c70b9-180">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="c70b9-181">[標準] 和 [特優] 層。</span><span class="sxs-lookup"><span data-stu-id="c70b9-181">Standard and Premium tiers.</span></span>

<span data-ttu-id="c70b9-182">如需詳細資訊，請參閱使用 Azure PowerShell (管理 Azure Redis Cache https://go.microsoft.com/fwlink/?LinkId=800051 https://go.microsoft.com/fwlink/?LinkId=800051) 。</span><span class="sxs-lookup"><span data-stu-id="c70b9-182">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="c70b9-183">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="c70b9-183">-RedisVersion</span></span>
<span data-ttu-id="c70b9-184">此參數已棄用，將會從未來版本中移除。</span><span class="sxs-lookup"><span data-stu-id="c70b9-184">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="c70b9-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c70b9-185">-ResourceGroupName</span></span>
<span data-ttu-id="c70b9-186">指定要在其中建立 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c70b9-186">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="c70b9-187">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="c70b9-187">-ShardCount</span></span>
<span data-ttu-id="c70b9-188">指定要在 Premium 群集快取上建立的 shards 數目。</span><span class="sxs-lookup"><span data-stu-id="c70b9-188">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="c70b9-189">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c70b9-189">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c70b9-190">sr-1</span><span class="sxs-lookup"><span data-stu-id="c70b9-190">1</span></span>
- <span data-ttu-id="c70b9-191">pplx-2</span><span class="sxs-lookup"><span data-stu-id="c70b9-191">2</span></span>
- <span data-ttu-id="c70b9-192">3</span><span class="sxs-lookup"><span data-stu-id="c70b9-192">3</span></span>
- <span data-ttu-id="c70b9-193">4</span><span class="sxs-lookup"><span data-stu-id="c70b9-193">4</span></span>
- <span data-ttu-id="c70b9-194">500</span><span class="sxs-lookup"><span data-stu-id="c70b9-194">5</span></span>
- <span data-ttu-id="c70b9-195">6</span><span class="sxs-lookup"><span data-stu-id="c70b9-195">6</span></span>
- <span data-ttu-id="c70b9-196">utf-7</span><span class="sxs-lookup"><span data-stu-id="c70b9-196">7</span></span>
- <span data-ttu-id="c70b9-197">型</span><span class="sxs-lookup"><span data-stu-id="c70b9-197">8</span></span>
- <span data-ttu-id="c70b9-198">9</span><span class="sxs-lookup"><span data-stu-id="c70b9-198">9</span></span> 
- <span data-ttu-id="c70b9-199">第</span><span class="sxs-lookup"><span data-stu-id="c70b9-199">10</span></span>

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

### <span data-ttu-id="c70b9-200">-大小</span><span class="sxs-lookup"><span data-stu-id="c70b9-200">-Size</span></span>
<span data-ttu-id="c70b9-201">指定 Redis 快取的大小。</span><span class="sxs-lookup"><span data-stu-id="c70b9-201">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="c70b9-202">有效值為：</span><span class="sxs-lookup"><span data-stu-id="c70b9-202">Valid values are:</span></span> 

- <span data-ttu-id="c70b9-203">P1</span><span class="sxs-lookup"><span data-stu-id="c70b9-203">P1</span></span>
- <span data-ttu-id="c70b9-204">又</span><span class="sxs-lookup"><span data-stu-id="c70b9-204">P2</span></span>
- <span data-ttu-id="c70b9-205">P3</span><span class="sxs-lookup"><span data-stu-id="c70b9-205">P3</span></span>
- <span data-ttu-id="c70b9-206">P4</span><span class="sxs-lookup"><span data-stu-id="c70b9-206">P4</span></span>
- <span data-ttu-id="c70b9-207">C0</span><span class="sxs-lookup"><span data-stu-id="c70b9-207">C0</span></span>
- <span data-ttu-id="c70b9-208">C1</span><span class="sxs-lookup"><span data-stu-id="c70b9-208">C1</span></span>
- <span data-ttu-id="c70b9-209">C3</span><span class="sxs-lookup"><span data-stu-id="c70b9-209">C2</span></span>
- <span data-ttu-id="c70b9-210">C3</span><span class="sxs-lookup"><span data-stu-id="c70b9-210">C3</span></span>
- <span data-ttu-id="c70b9-211">C4</span><span class="sxs-lookup"><span data-stu-id="c70b9-211">C4</span></span>
- <span data-ttu-id="c70b9-212">C5</span><span class="sxs-lookup"><span data-stu-id="c70b9-212">C5</span></span>
- <span data-ttu-id="c70b9-213">C6</span><span class="sxs-lookup"><span data-stu-id="c70b9-213">C6</span></span>
- <span data-ttu-id="c70b9-214">250MB</span><span class="sxs-lookup"><span data-stu-id="c70b9-214">250MB</span></span>
- <span data-ttu-id="c70b9-215">1GB</span><span class="sxs-lookup"><span data-stu-id="c70b9-215">1GB</span></span>
- <span data-ttu-id="c70b9-216">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="c70b9-216">2.5GB</span></span>
- <span data-ttu-id="c70b9-217">6GB</span><span class="sxs-lookup"><span data-stu-id="c70b9-217">6GB</span></span>
- <span data-ttu-id="c70b9-218">13GB</span><span class="sxs-lookup"><span data-stu-id="c70b9-218">13GB</span></span>
- <span data-ttu-id="c70b9-219">26GB</span><span class="sxs-lookup"><span data-stu-id="c70b9-219">26GB</span></span>
- <span data-ttu-id="c70b9-220">53GB</span><span class="sxs-lookup"><span data-stu-id="c70b9-220">53GB</span></span>

<span data-ttu-id="c70b9-221">預設值為1GB 或 C1。</span><span class="sxs-lookup"><span data-stu-id="c70b9-221">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="c70b9-222">-Sku</span><span class="sxs-lookup"><span data-stu-id="c70b9-222">-Sku</span></span>
<span data-ttu-id="c70b9-223">指定要建立之 Redis 快取的 SKU。</span><span class="sxs-lookup"><span data-stu-id="c70b9-223">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="c70b9-224">有效值為：</span><span class="sxs-lookup"><span data-stu-id="c70b9-224">Valid values are:</span></span> 

- <span data-ttu-id="c70b9-225">空白</span><span class="sxs-lookup"><span data-stu-id="c70b9-225">Basic</span></span>
- <span data-ttu-id="c70b9-226">標準</span><span class="sxs-lookup"><span data-stu-id="c70b9-226">Standard</span></span>
- <span data-ttu-id="c70b9-227">佳</span><span class="sxs-lookup"><span data-stu-id="c70b9-227">Premium</span></span>

<span data-ttu-id="c70b9-228">預設值為 [標準]。</span><span class="sxs-lookup"><span data-stu-id="c70b9-228">The default value is Standard.</span></span>

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

### <span data-ttu-id="c70b9-229">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="c70b9-229">-StaticIP</span></span>
<span data-ttu-id="c70b9-230">在 Redis 快取的子網上指定唯一的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c70b9-230">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="c70b9-231">如果您沒有指定此參數的值，這個 Cmdlet 會從子網上選擇 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c70b9-231">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="c70b9-232">-子網</span><span class="sxs-lookup"><span data-stu-id="c70b9-232">-Subnet</span></span>
<span data-ttu-id="c70b9-233">指定要在其中部署 Redis 快取的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="c70b9-233">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="c70b9-234">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c70b9-234">-SubnetId</span></span>
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

### <span data-ttu-id="c70b9-235">-Tag</span><span class="sxs-lookup"><span data-stu-id="c70b9-235">-Tag</span></span>
<span data-ttu-id="c70b9-236">代表標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c70b9-236">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="c70b9-237">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="c70b9-237">-TenantSettings</span></span>
<span data-ttu-id="c70b9-238">已棄用此參數。</span><span class="sxs-lookup"><span data-stu-id="c70b9-238">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="c70b9-239">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c70b9-239">-VirtualNetwork</span></span>
<span data-ttu-id="c70b9-240">指定要部署 Redis 快取的虛擬網路資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c70b9-240">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="c70b9-241">-Zone</span><span class="sxs-lookup"><span data-stu-id="c70b9-241">-Zone</span></span>
<span data-ttu-id="c70b9-242">區域清單。</span><span class="sxs-lookup"><span data-stu-id="c70b9-242">List of zones.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c70b9-243">-確認</span><span class="sxs-lookup"><span data-stu-id="c70b9-243">-Confirm</span></span>
<span data-ttu-id="c70b9-244">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c70b9-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c70b9-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c70b9-245">-WhatIf</span></span>
<span data-ttu-id="c70b9-246">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c70b9-246">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c70b9-247">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c70b9-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c70b9-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c70b9-248">CommonParameters</span></span>
<span data-ttu-id="c70b9-249">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c70b9-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c70b9-250">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c70b9-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c70b9-251">輸入</span><span class="sxs-lookup"><span data-stu-id="c70b9-251">INPUTS</span></span>

### <span data-ttu-id="c70b9-252">所有</span><span class="sxs-lookup"><span data-stu-id="c70b9-252">None</span></span>
<span data-ttu-id="c70b9-253">您可以依名稱將輸入管到這個 Cmdlet，但不能依值進行。</span><span class="sxs-lookup"><span data-stu-id="c70b9-253">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="c70b9-254">輸出</span><span class="sxs-lookup"><span data-stu-id="c70b9-254">OUTPUTS</span></span>

### <span data-ttu-id="c70b9-255">RedisCacheAttributesWithAccessKeys 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="c70b9-255">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="c70b9-256">這個 Cmdlet 會傳回 Redis 快取的所有屬性，包括主要和次要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c70b9-256">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="c70b9-257">筆記</span><span class="sxs-lookup"><span data-stu-id="c70b9-257">NOTES</span></span>

## <span data-ttu-id="c70b9-258">相關連結</span><span class="sxs-lookup"><span data-stu-id="c70b9-258">RELATED LINKS</span></span>

[<span data-ttu-id="c70b9-259">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c70b9-259">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="c70b9-260">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c70b9-260">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="c70b9-261">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c70b9-261">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


