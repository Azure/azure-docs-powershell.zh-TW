---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 25469aa93f673d6a49bbbaa54fcaf22a91019d9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913729"
---
# <span data-ttu-id="5982a-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5982a-101">New-AzRedisCache</span></span>

## <span data-ttu-id="5982a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5982a-102">SYNOPSIS</span></span>
<span data-ttu-id="5982a-103">建立 Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="5982a-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="5982a-104">語法</span><span class="sxs-lookup"><span data-stu-id="5982a-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5982a-105">描述</span><span class="sxs-lookup"><span data-stu-id="5982a-105">DESCRIPTION</span></span>
<span data-ttu-id="5982a-106">**New-AzRedisCache** Cmdlet 會建立 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="5982a-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="5982a-107">例子</span><span class="sxs-lookup"><span data-stu-id="5982a-107">EXAMPLES</span></span>

### <span data-ttu-id="5982a-108">範例 1：建立 Redis Cache</span><span class="sxs-lookup"><span data-stu-id="5982a-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="5982a-109">此命令會建立 Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="5982a-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="5982a-110">範例 2：建立標準 SKU Redis Cache</span><span class="sxs-lookup"><span data-stu-id="5982a-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="5982a-111">此命令會建立 Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="5982a-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="5982a-112">參數</span><span class="sxs-lookup"><span data-stu-id="5982a-112">PARAMETERS</span></span>

### <span data-ttu-id="5982a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5982a-113">-DefaultProfile</span></span>
<span data-ttu-id="5982a-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5982a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5982a-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="5982a-115">-EnableNonSslPort</span></span>
<span data-ttu-id="5982a-116">指出是否已啟用非 SSL 埠。</span><span class="sxs-lookup"><span data-stu-id="5982a-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="5982a-117">預設值是$False (SSL 埠已停用) 。</span><span class="sxs-lookup"><span data-stu-id="5982a-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="5982a-118">-位置</span><span class="sxs-lookup"><span data-stu-id="5982a-118">-Location</span></span>
<span data-ttu-id="5982a-119">指定要建立 Redis Cache 的位置。</span><span class="sxs-lookup"><span data-stu-id="5982a-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="5982a-120">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="5982a-120">Valid values are:</span></span> 
- <span data-ttu-id="5982a-121">美國中北部</span><span class="sxs-lookup"><span data-stu-id="5982a-121">North Central US</span></span>
- <span data-ttu-id="5982a-122">美國中南部</span><span class="sxs-lookup"><span data-stu-id="5982a-122">South Central US</span></span>
- <span data-ttu-id="5982a-123">美國中</span><span class="sxs-lookup"><span data-stu-id="5982a-123">Central US</span></span>
- <span data-ttu-id="5982a-124">西歐</span><span class="sxs-lookup"><span data-stu-id="5982a-124">West Europe</span></span>
- <span data-ttu-id="5982a-125">北歐洲</span><span class="sxs-lookup"><span data-stu-id="5982a-125">North Europe</span></span>
- <span data-ttu-id="5982a-126">美國西部</span><span class="sxs-lookup"><span data-stu-id="5982a-126">West US</span></span>
- <span data-ttu-id="5982a-127">美國東部</span><span class="sxs-lookup"><span data-stu-id="5982a-127">East US</span></span>
- <span data-ttu-id="5982a-128">美國東部 2</span><span class="sxs-lookup"><span data-stu-id="5982a-128">East US 2</span></span>
- <span data-ttu-id="5982a-129">日本東部</span><span class="sxs-lookup"><span data-stu-id="5982a-129">Japan East</span></span>
- <span data-ttu-id="5982a-130">日本西部</span><span class="sxs-lookup"><span data-stu-id="5982a-130">Japan West</span></span>
- <span data-ttu-id="5982a-131">巴西南部</span><span class="sxs-lookup"><span data-stu-id="5982a-131">Brazil South</span></span>
- <span data-ttu-id="5982a-132">東南亞</span><span class="sxs-lookup"><span data-stu-id="5982a-132">Southeast Asia</span></span>
- <span data-ttu-id="5982a-133">東亞</span><span class="sxs-lookup"><span data-stu-id="5982a-133">East Asia</span></span>
- <span data-ttu-id="5982a-134">澳大利亞東部</span><span class="sxs-lookup"><span data-stu-id="5982a-134">Australia East</span></span>
- <span data-ttu-id="5982a-135">澳洲東南亞</span><span class="sxs-lookup"><span data-stu-id="5982a-135">Australia Southeast</span></span>

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

### <span data-ttu-id="5982a-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="5982a-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="5982a-137">指定用戶端連接至緩存所需的 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="5982a-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="5982a-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="5982a-138">-Name</span></span>
<span data-ttu-id="5982a-139">指定要建立 Redis Cache 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5982a-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="5982a-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="5982a-140">-RedisConfiguration</span></span>
<span data-ttu-id="5982a-141">指定 Redis 設定設定。</span><span class="sxs-lookup"><span data-stu-id="5982a-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="5982a-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5982a-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5982a-143">已啟用 rdb 備份功能。</span><span class="sxs-lookup"><span data-stu-id="5982a-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="5982a-144">指定已啟用 Redis 資料持續性。</span><span class="sxs-lookup"><span data-stu-id="5982a-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="5982a-145">僅提供進一層。</span><span class="sxs-lookup"><span data-stu-id="5982a-145">Premium tier only.</span></span>
- <span data-ttu-id="5982a-146">rdb-storage-connection-string。</span><span class="sxs-lookup"><span data-stu-id="5982a-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="5982a-147">指定儲存空間帳戶的重新資料持續性之連接字串。</span><span class="sxs-lookup"><span data-stu-id="5982a-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="5982a-148">僅提供進一層。</span><span class="sxs-lookup"><span data-stu-id="5982a-148">Premium tier only.</span></span>
- <span data-ttu-id="5982a-149">rdb-backup-frequency。</span><span class="sxs-lookup"><span data-stu-id="5982a-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="5982a-150">指定 Redis 資料持續性的備份頻率。</span><span class="sxs-lookup"><span data-stu-id="5982a-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="5982a-151">僅提供進一層。</span><span class="sxs-lookup"><span data-stu-id="5982a-151">Premium tier only.</span></span> 
- <span data-ttu-id="5982a-152">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="5982a-152">maxmemory-reserved.</span></span>
<span data-ttu-id="5982a-153">設定非緩存程式所保留的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5982a-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="5982a-154">標準及進一層。</span><span class="sxs-lookup"><span data-stu-id="5982a-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="5982a-155">maxmemory-policy。</span><span class="sxs-lookup"><span data-stu-id="5982a-155">maxmemory-policy.</span></span>
<span data-ttu-id="5982a-156">設定緩存的清除策略。</span><span class="sxs-lookup"><span data-stu-id="5982a-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="5982a-157">所有定價層級。</span><span class="sxs-lookup"><span data-stu-id="5982a-157">All pricing tiers.</span></span> 
- <span data-ttu-id="5982a-158">notify-keyspace-events。</span><span class="sxs-lookup"><span data-stu-id="5982a-158">notify-keyspace-events.</span></span>
<span data-ttu-id="5982a-159">設定鍵格通知。</span><span class="sxs-lookup"><span data-stu-id="5982a-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="5982a-160">標準及進一層。</span><span class="sxs-lookup"><span data-stu-id="5982a-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="5982a-161">hash-max-ziplist-專案。</span><span class="sxs-lookup"><span data-stu-id="5982a-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="5982a-162">設定小型匯總資料類型的記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="5982a-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="5982a-163">標準及進一層。</span><span class="sxs-lookup"><span data-stu-id="5982a-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="5982a-164">hash-max-ziplist-value。</span><span class="sxs-lookup"><span data-stu-id="5982a-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="5982a-165">設定小型匯總資料類型的記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="5982a-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="5982a-166">標準及進一層。</span><span class="sxs-lookup"><span data-stu-id="5982a-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="5982a-167">set-max-intset-ntries。</span><span class="sxs-lookup"><span data-stu-id="5982a-167">set-max-intset-entries.</span></span>
<span data-ttu-id="5982a-168">設定小型匯總資料類型的記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="5982a-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="5982a-169">標準及進一層。</span><span class="sxs-lookup"><span data-stu-id="5982a-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="5982a-170">zset-max-ziplist-專案。</span><span class="sxs-lookup"><span data-stu-id="5982a-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="5982a-171">設定小型匯總資料類型的記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="5982a-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="5982a-172">標準及進一層。</span><span class="sxs-lookup"><span data-stu-id="5982a-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="5982a-173">zset-max-ziplist-value。</span><span class="sxs-lookup"><span data-stu-id="5982a-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="5982a-174">設定小型匯總資料類型的記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="5982a-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="5982a-175">標準及進一層。</span><span class="sxs-lookup"><span data-stu-id="5982a-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="5982a-176">資料庫。</span><span class="sxs-lookup"><span data-stu-id="5982a-176">databases.</span></span>
<span data-ttu-id="5982a-177">設定資料庫數目。</span><span class="sxs-lookup"><span data-stu-id="5982a-177">Configures the number of databases.</span></span>
<span data-ttu-id="5982a-178">此屬性只能在建立緩存時進行配置。</span><span class="sxs-lookup"><span data-stu-id="5982a-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="5982a-179">標準及進一層。</span><span class="sxs-lookup"><span data-stu-id="5982a-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="5982a-180">詳細資訊請參閱使用 Azure PowerShell 管理 Azure Redis http://go.microsoft.com/fwlink/?LinkId=800051 Cache http://go.microsoft.com/fwlink/?LinkId=800051) (。</span><span class="sxs-lookup"><span data-stu-id="5982a-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="5982a-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5982a-181">-ResourceGroupName</span></span>
<span data-ttu-id="5982a-182">指定要建立 Redis Cache 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="5982a-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="5982a-183">-Scount</span><span class="sxs-lookup"><span data-stu-id="5982a-183">-ShardCount</span></span>
<span data-ttu-id="5982a-184">指定在進一版集區緩存上要建立的資料表數目。</span><span class="sxs-lookup"><span data-stu-id="5982a-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="5982a-185">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5982a-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5982a-186">1</span><span class="sxs-lookup"><span data-stu-id="5982a-186">1</span></span>
- <span data-ttu-id="5982a-187">2</span><span class="sxs-lookup"><span data-stu-id="5982a-187">2</span></span>
- <span data-ttu-id="5982a-188">3</span><span class="sxs-lookup"><span data-stu-id="5982a-188">3</span></span>
- <span data-ttu-id="5982a-189">4</span><span class="sxs-lookup"><span data-stu-id="5982a-189">4</span></span>
- <span data-ttu-id="5982a-190">5</span><span class="sxs-lookup"><span data-stu-id="5982a-190">5</span></span>
- <span data-ttu-id="5982a-191">6</span><span class="sxs-lookup"><span data-stu-id="5982a-191">6</span></span>
- <span data-ttu-id="5982a-192">7</span><span class="sxs-lookup"><span data-stu-id="5982a-192">7</span></span>
- <span data-ttu-id="5982a-193">8</span><span class="sxs-lookup"><span data-stu-id="5982a-193">8</span></span>
- <span data-ttu-id="5982a-194">9</span><span class="sxs-lookup"><span data-stu-id="5982a-194">9</span></span> 
- <span data-ttu-id="5982a-195">10</span><span class="sxs-lookup"><span data-stu-id="5982a-195">10</span></span>

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

### <span data-ttu-id="5982a-196">-大小</span><span class="sxs-lookup"><span data-stu-id="5982a-196">-Size</span></span>
<span data-ttu-id="5982a-197">指定 Redis Cache 的大小。</span><span class="sxs-lookup"><span data-stu-id="5982a-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="5982a-198">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="5982a-198">Valid values are:</span></span> 
- <span data-ttu-id="5982a-199">P1</span><span class="sxs-lookup"><span data-stu-id="5982a-199">P1</span></span>
- <span data-ttu-id="5982a-200">P2</span><span class="sxs-lookup"><span data-stu-id="5982a-200">P2</span></span>
- <span data-ttu-id="5982a-201">P3</span><span class="sxs-lookup"><span data-stu-id="5982a-201">P3</span></span>
- <span data-ttu-id="5982a-202">P4</span><span class="sxs-lookup"><span data-stu-id="5982a-202">P4</span></span>
- <span data-ttu-id="5982a-203">P5</span><span class="sxs-lookup"><span data-stu-id="5982a-203">P5</span></span>
- <span data-ttu-id="5982a-204">C0</span><span class="sxs-lookup"><span data-stu-id="5982a-204">C0</span></span>
- <span data-ttu-id="5982a-205">C1</span><span class="sxs-lookup"><span data-stu-id="5982a-205">C1</span></span>
- <span data-ttu-id="5982a-206">C2</span><span class="sxs-lookup"><span data-stu-id="5982a-206">C2</span></span>
- <span data-ttu-id="5982a-207">C3</span><span class="sxs-lookup"><span data-stu-id="5982a-207">C3</span></span>
- <span data-ttu-id="5982a-208">C4</span><span class="sxs-lookup"><span data-stu-id="5982a-208">C4</span></span>
- <span data-ttu-id="5982a-209">C5</span><span class="sxs-lookup"><span data-stu-id="5982a-209">C5</span></span>
- <span data-ttu-id="5982a-210">C6</span><span class="sxs-lookup"><span data-stu-id="5982a-210">C6</span></span>
- <span data-ttu-id="5982a-211">250MB</span><span class="sxs-lookup"><span data-stu-id="5982a-211">250MB</span></span>
- <span data-ttu-id="5982a-212">1GB</span><span class="sxs-lookup"><span data-stu-id="5982a-212">1GB</span></span>
- <span data-ttu-id="5982a-213">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="5982a-213">2.5GB</span></span>
- <span data-ttu-id="5982a-214">6GB</span><span class="sxs-lookup"><span data-stu-id="5982a-214">6GB</span></span>
- <span data-ttu-id="5982a-215">13 GB</span><span class="sxs-lookup"><span data-stu-id="5982a-215">13GB</span></span>
- <span data-ttu-id="5982a-216">26 GB</span><span class="sxs-lookup"><span data-stu-id="5982a-216">26GB</span></span>
- <span data-ttu-id="5982a-217">53 GB 預設值為 1GB 或 C1。</span><span class="sxs-lookup"><span data-stu-id="5982a-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="5982a-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="5982a-218">-Sku</span></span>
<span data-ttu-id="5982a-219">指定要建立 Redis Cache 的 SKU。</span><span class="sxs-lookup"><span data-stu-id="5982a-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="5982a-220">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="5982a-220">Valid values are:</span></span> 
- <span data-ttu-id="5982a-221">基本</span><span class="sxs-lookup"><span data-stu-id="5982a-221">Basic</span></span>
- <span data-ttu-id="5982a-222">標準</span><span class="sxs-lookup"><span data-stu-id="5982a-222">Standard</span></span>
- <span data-ttu-id="5982a-223">Premium 預設值為 Standard。</span><span class="sxs-lookup"><span data-stu-id="5982a-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="5982a-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="5982a-224">-StaticIP</span></span>
<span data-ttu-id="5982a-225">指定子網中 Redis Cache 的唯一 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5982a-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="5982a-226">如果您沒有為此參數指定值，此 Cmdlet 會從子網選擇 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5982a-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="5982a-227">-子網Id</span><span class="sxs-lookup"><span data-stu-id="5982a-227">-SubnetId</span></span>
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

### <span data-ttu-id="5982a-228">-標記</span><span class="sxs-lookup"><span data-stu-id="5982a-228">-Tag</span></span>
<span data-ttu-id="5982a-229">代表標記的雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="5982a-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="5982a-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="5982a-230">-TenantSettings</span></span>
<span data-ttu-id="5982a-231">此參數已被使用。</span><span class="sxs-lookup"><span data-stu-id="5982a-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="5982a-232">-區域</span><span class="sxs-lookup"><span data-stu-id="5982a-232">-Zone</span></span>
<span data-ttu-id="5982a-233">區域清單。</span><span class="sxs-lookup"><span data-stu-id="5982a-233">List of zones.</span></span>

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

### <span data-ttu-id="5982a-234">-確認</span><span class="sxs-lookup"><span data-stu-id="5982a-234">-Confirm</span></span>
<span data-ttu-id="5982a-235">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5982a-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5982a-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5982a-236">-WhatIf</span></span>
<span data-ttu-id="5982a-237">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5982a-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5982a-238">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5982a-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5982a-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5982a-239">CommonParameters</span></span>
<span data-ttu-id="5982a-240">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5982a-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5982a-241">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5982a-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5982a-242">輸入</span><span class="sxs-lookup"><span data-stu-id="5982a-242">INPUTS</span></span>

### <span data-ttu-id="5982a-243">System.String</span><span class="sxs-lookup"><span data-stu-id="5982a-243">System.String</span></span>

### <span data-ttu-id="5982a-244">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5982a-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5982a-245">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5982a-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5982a-246">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5982a-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5982a-247">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5982a-247">System.String[]</span></span>

## <span data-ttu-id="5982a-248">輸出</span><span class="sxs-lookup"><span data-stu-id="5982a-248">OUTPUTS</span></span>

### <span data-ttu-id="5982a-249">Microsoft.Azure.Commands.RedisCache.models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="5982a-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="5982a-250">筆記</span><span class="sxs-lookup"><span data-stu-id="5982a-250">NOTES</span></span>

## <span data-ttu-id="5982a-251">相關連結</span><span class="sxs-lookup"><span data-stu-id="5982a-251">RELATED LINKS</span></span>

[<span data-ttu-id="5982a-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5982a-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="5982a-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5982a-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="5982a-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5982a-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


