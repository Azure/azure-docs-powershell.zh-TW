---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: 43ad21450666fb2db9a25e1e2803651eacf511d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914645"
---
# <span data-ttu-id="7cf67-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="7cf67-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="7cf67-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7cf67-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf67-103">建立 Redis Enterpise 緩存組和相關聯的資料庫</span><span class="sxs-lookup"><span data-stu-id="7cf67-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="7cf67-104">語法</span><span class="sxs-lookup"><span data-stu-id="7cf67-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7cf67-105">描述</span><span class="sxs-lookup"><span data-stu-id="7cf67-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf67-106">建立或更新現有 (覆寫/重新建立，) 緩存組和名為"default" 的關聯資料庫有潛在的停機時間</span><span class="sxs-lookup"><span data-stu-id="7cf67-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="7cf67-107">例子</span><span class="sxs-lookup"><span data-stu-id="7cf67-107">EXAMPLES</span></span>

### <span data-ttu-id="7cf67-108">範例 1：建立 Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="7cf67-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="7cf67-109">此命令會建立名為 MyCache 的 Redis Enterprise Cache。</span><span class="sxs-lookup"><span data-stu-id="7cf67-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="7cf67-110">範例 2：使用一些選擇性參數建立 Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="7cf67-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="7cf67-111">此命令會使用一些選擇性參數建立名為 MyCache 的 Redis Enterprise Cache。</span><span class="sxs-lookup"><span data-stu-id="7cf67-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="7cf67-112">參數</span><span class="sxs-lookup"><span data-stu-id="7cf67-112">PARAMETERS</span></span>

### <span data-ttu-id="7cf67-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cf67-113">-AsJob</span></span>
<span data-ttu-id="7cf67-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="7cf67-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-115">-容量</span><span class="sxs-lookup"><span data-stu-id="7cf67-115">-Capacity</span></span>
<span data-ttu-id="7cf67-116">RedisEnterprise 集區的大小。</span><span class="sxs-lookup"><span data-stu-id="7cf67-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="7cf67-117">根據 SKU，預設為 2 或 3。</span><span class="sxs-lookup"><span data-stu-id="7cf67-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="7cf67-118">有效的值 (2、4、6、...) 企業 SKUS 和 (3、9、15、...) Flash SK。</span><span class="sxs-lookup"><span data-stu-id="7cf67-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: SkuCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="7cf67-119">-ClientProtocol</span></span>
<span data-ttu-id="7cf67-120">指定重新發送用戶端是否可以使用 TLS 加密或純文字重新文本通訊協定進行連結。</span><span class="sxs-lookup"><span data-stu-id="7cf67-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="7cf67-121">預設值為 TLS 加密。</span><span class="sxs-lookup"><span data-stu-id="7cf67-121">Default is TLS-encrypted.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.Protocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-122">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf67-122">-ClusteringPolicy</span></span>
<span data-ttu-id="7cf67-123">叢集策略 - 預設值為 OSSCluster。</span><span class="sxs-lookup"><span data-stu-id="7cf67-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="7cf67-124">于建立時指定。</span><span class="sxs-lookup"><span data-stu-id="7cf67-124">Specified at create time.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.ClusteringPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-125">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7cf67-125">-ClusterName</span></span>
<span data-ttu-id="7cf67-126">RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="7cf67-126">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf67-127">-DefaultProfile</span></span>
<span data-ttu-id="7cf67-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7cf67-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="7cf67-129">-EvictionPolicy</span></span>
<span data-ttu-id="7cf67-130">重新發佈發佈規則 - 預設值為 VolatileLRU。</span><span class="sxs-lookup"><span data-stu-id="7cf67-130">Redis eviction policy - default is VolatileLRU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.EvictionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-131">-位置</span><span class="sxs-lookup"><span data-stu-id="7cf67-131">-Location</span></span>
<span data-ttu-id="7cf67-132">資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="7cf67-132">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="7cf67-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="7cf67-134">支援之組群的最小 TLS 版本，例如 1.2</span><span class="sxs-lookup"><span data-stu-id="7cf67-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-135">-模組</span><span class="sxs-lookup"><span data-stu-id="7cf67-135">-Module</span></span>
<span data-ttu-id="7cf67-136">在此資料庫中啟用的選擇性重新模組組 - 模組只能在建立時新增。</span><span class="sxs-lookup"><span data-stu-id="7cf67-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="7cf67-137">若要建構，請參閱 MODULE 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7cf67-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IModule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7cf67-138">-NoWait</span></span>
<span data-ttu-id="7cf67-139">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="7cf67-139">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-140">-埠</span><span class="sxs-lookup"><span data-stu-id="7cf67-140">-Port</span></span>
<span data-ttu-id="7cf67-141">資料庫端點的 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="7cf67-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="7cf67-142">于建立時指定。</span><span class="sxs-lookup"><span data-stu-id="7cf67-142">Specified at create time.</span></span>
<span data-ttu-id="7cf67-143">預設為可用的埠。</span><span class="sxs-lookup"><span data-stu-id="7cf67-143">Defaults to an available port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf67-144">-ResourceGroupName</span></span>
<span data-ttu-id="7cf67-145">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cf67-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="7cf67-146">-Sku</span></span>
<span data-ttu-id="7cf67-147">要部署的 RedisEnterprise 集區類型。</span><span class="sxs-lookup"><span data-stu-id="7cf67-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="7cf67-148">可能的值： (Enterprise_E10、EnterpriseFlash_F300等) </span><span class="sxs-lookup"><span data-stu-id="7cf67-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cf67-149">-SubscriptionId</span></span>
<span data-ttu-id="7cf67-150">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="7cf67-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7cf67-151">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7cf67-151">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-152">-標記</span><span class="sxs-lookup"><span data-stu-id="7cf67-152">-Tag</span></span>
<span data-ttu-id="7cf67-153">資源標記。</span><span class="sxs-lookup"><span data-stu-id="7cf67-153">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-154">-區域</span><span class="sxs-lookup"><span data-stu-id="7cf67-154">-Zone</span></span>
<span data-ttu-id="7cf67-155">將會部署此組組的區域。</span><span class="sxs-lookup"><span data-stu-id="7cf67-155">The zones where this cluster will be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf67-156">-確認</span><span class="sxs-lookup"><span data-stu-id="7cf67-156">-Confirm</span></span>
<span data-ttu-id="7cf67-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7cf67-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf67-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf67-158">-WhatIf</span></span>
<span data-ttu-id="7cf67-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7cf67-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf67-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7cf67-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf67-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf67-161">CommonParameters</span></span>
<span data-ttu-id="7cf67-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7cf67-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf67-163">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cf67-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf67-164">輸入</span><span class="sxs-lookup"><span data-stu-id="7cf67-164">INPUTS</span></span>

## <span data-ttu-id="7cf67-165">輸出</span><span class="sxs-lookup"><span data-stu-id="7cf67-165">OUTPUTS</span></span>

### <span data-ttu-id="7cf67-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="7cf67-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="7cf67-167">筆記</span><span class="sxs-lookup"><span data-stu-id="7cf67-167">NOTES</span></span>

<span data-ttu-id="7cf67-168">別名</span><span class="sxs-lookup"><span data-stu-id="7cf67-168">ALIASES</span></span>

<span data-ttu-id="7cf67-169">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="7cf67-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7cf67-170">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7cf67-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7cf67-171">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7cf67-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7cf67-172">MODULE <IModule[]>：在此資料庫中啟用的選擇性重新模組組 - 模組只能在建立時新增。</span><span class="sxs-lookup"><span data-stu-id="7cf67-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="7cf67-173">`Name <String>`：模組的名稱，例如'RedisBloom'，'RediSearch'， 'RedisTimeSeries'</span><span class="sxs-lookup"><span data-stu-id="7cf67-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="7cf67-174">`[Arg <String>]`：模組的組ERROR_RATE，例如'ERROR_RATE 0.00 INITIAL_SIZE 400'。</span><span class="sxs-lookup"><span data-stu-id="7cf67-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="7cf67-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cf67-175">RELATED LINKS</span></span>

