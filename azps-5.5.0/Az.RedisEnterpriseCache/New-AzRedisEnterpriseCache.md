---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: f2f996bc212772b3b44202796e270ec345898a11
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139998"
---
# <span data-ttu-id="84f38-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="84f38-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="84f38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84f38-102">SYNOPSIS</span></span>
<span data-ttu-id="84f38-103">建立 Redis 企業快取叢集及相關聯的資料庫</span><span class="sxs-lookup"><span data-stu-id="84f38-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="84f38-104">句法</span><span class="sxs-lookup"><span data-stu-id="84f38-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84f38-105">說明</span><span class="sxs-lookup"><span data-stu-id="84f38-105">DESCRIPTION</span></span>
<span data-ttu-id="84f38-106">建立或更新現有的 (覆寫/重新建立，有可能的停機時間) 快取群集，以及名為「預設」的關聯資料庫</span><span class="sxs-lookup"><span data-stu-id="84f38-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="84f38-107">示例</span><span class="sxs-lookup"><span data-stu-id="84f38-107">EXAMPLES</span></span>

### <span data-ttu-id="84f38-108">範例1：建立 Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="84f38-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="84f38-109">這個命令會建立名為 MyCache 的 Redis 企業版快取。</span><span class="sxs-lookup"><span data-stu-id="84f38-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="84f38-110">範例2：使用一些選用的參數建立 Redis 企業版快取</span><span class="sxs-lookup"><span data-stu-id="84f38-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="84f38-111">這個命令會使用一些選用的參數，建立名為 MyCache 的 Redis 企業版快取。</span><span class="sxs-lookup"><span data-stu-id="84f38-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="84f38-112">參數</span><span class="sxs-lookup"><span data-stu-id="84f38-112">PARAMETERS</span></span>

### <span data-ttu-id="84f38-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84f38-113">-AsJob</span></span>
<span data-ttu-id="84f38-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="84f38-114">Run the command as a job</span></span>

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

### <span data-ttu-id="84f38-115">-容量</span><span class="sxs-lookup"><span data-stu-id="84f38-115">-Capacity</span></span>
<span data-ttu-id="84f38-116">RedisEnterprise 群集的大小。</span><span class="sxs-lookup"><span data-stu-id="84f38-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="84f38-117">根據 SKU 的預設值為2或3。</span><span class="sxs-lookup"><span data-stu-id="84f38-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="84f38-118">有效值為 (2、4、6、... ) （適用于企業版 Sku），以及 (3、9、15、... ) 的 Flash Sku。</span><span class="sxs-lookup"><span data-stu-id="84f38-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="84f38-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="84f38-119">-ClientProtocol</span></span>
<span data-ttu-id="84f38-120">指定 redis 用戶端是否可使用 TLS 加密或純文字 redis 通訊協定連線。</span><span class="sxs-lookup"><span data-stu-id="84f38-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="84f38-121">預設值為 TLS 加密。</span><span class="sxs-lookup"><span data-stu-id="84f38-121">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="84f38-122">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="84f38-122">-ClusteringPolicy</span></span>
<span data-ttu-id="84f38-123">[群集原則]-預設值為 [OSSCluster]。</span><span class="sxs-lookup"><span data-stu-id="84f38-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="84f38-124">在建立時間指定。</span><span class="sxs-lookup"><span data-stu-id="84f38-124">Specified at create time.</span></span>

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

### <span data-ttu-id="84f38-125">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="84f38-125">-ClusterName</span></span>
<span data-ttu-id="84f38-126">RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="84f38-126">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="84f38-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84f38-127">-DefaultProfile</span></span>
<span data-ttu-id="84f38-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84f38-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84f38-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="84f38-129">-EvictionPolicy</span></span>
<span data-ttu-id="84f38-130">Redis 逐出原則-預設值是 VolatileLRU。</span><span class="sxs-lookup"><span data-stu-id="84f38-130">Redis eviction policy - default is VolatileLRU.</span></span>

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

### <span data-ttu-id="84f38-131">-位置</span><span class="sxs-lookup"><span data-stu-id="84f38-131">-Location</span></span>
<span data-ttu-id="84f38-132">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="84f38-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="84f38-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="84f38-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="84f38-134">支援的群集最低 TLS 版本，例如1。2</span><span class="sxs-lookup"><span data-stu-id="84f38-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

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

### <span data-ttu-id="84f38-135">-模組</span><span class="sxs-lookup"><span data-stu-id="84f38-135">-Module</span></span>
<span data-ttu-id="84f38-136">要在此資料庫中啟用的 redis 模組的選擇性集合-只有在建立期間才能新增模組。</span><span class="sxs-lookup"><span data-stu-id="84f38-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="84f38-137">若要建立，請參閱模組屬性的 [記事] 區段，並建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="84f38-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="84f38-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="84f38-138">-NoWait</span></span>
<span data-ttu-id="84f38-139">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="84f38-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="84f38-140">-埠</span><span class="sxs-lookup"><span data-stu-id="84f38-140">-Port</span></span>
<span data-ttu-id="84f38-141">資料庫端點的 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="84f38-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="84f38-142">在建立時間指定。</span><span class="sxs-lookup"><span data-stu-id="84f38-142">Specified at create time.</span></span>
<span data-ttu-id="84f38-143">預設為可用的埠。</span><span class="sxs-lookup"><span data-stu-id="84f38-143">Defaults to an available port.</span></span>

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

### <span data-ttu-id="84f38-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84f38-144">-ResourceGroupName</span></span>
<span data-ttu-id="84f38-145">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="84f38-145">The name of the resource group.</span></span>

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

### <span data-ttu-id="84f38-146">-Sku</span><span class="sxs-lookup"><span data-stu-id="84f38-146">-Sku</span></span>
<span data-ttu-id="84f38-147">要部署的 RedisEnterprise 群集類型。</span><span class="sxs-lookup"><span data-stu-id="84f38-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="84f38-148">可能的值： (Enterprise_E10、EnterpriseFlash_F300 等。 ) </span><span class="sxs-lookup"><span data-stu-id="84f38-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

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

### <span data-ttu-id="84f38-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84f38-149">-SubscriptionId</span></span>
<span data-ttu-id="84f38-150">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="84f38-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="84f38-151">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="84f38-151">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="84f38-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="84f38-152">-Tag</span></span>
<span data-ttu-id="84f38-153">資源標記。</span><span class="sxs-lookup"><span data-stu-id="84f38-153">Resource tags.</span></span>

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

### <span data-ttu-id="84f38-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="84f38-154">-Zone</span></span>
<span data-ttu-id="84f38-155">將部署此群集的區域。</span><span class="sxs-lookup"><span data-stu-id="84f38-155">The zones where this cluster will be deployed.</span></span>

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

### <span data-ttu-id="84f38-156">-確認</span><span class="sxs-lookup"><span data-stu-id="84f38-156">-Confirm</span></span>
<span data-ttu-id="84f38-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="84f38-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84f38-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84f38-158">-WhatIf</span></span>
<span data-ttu-id="84f38-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84f38-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84f38-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84f38-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84f38-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84f38-161">CommonParameters</span></span>
<span data-ttu-id="84f38-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84f38-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84f38-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="84f38-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84f38-164">輸入</span><span class="sxs-lookup"><span data-stu-id="84f38-164">INPUTS</span></span>

## <span data-ttu-id="84f38-165">輸出</span><span class="sxs-lookup"><span data-stu-id="84f38-165">OUTPUTS</span></span>

### <span data-ttu-id="84f38-166">ICluster （RedisEnterpriseCache）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="84f38-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="84f38-167">筆記</span><span class="sxs-lookup"><span data-stu-id="84f38-167">NOTES</span></span>

<span data-ttu-id="84f38-168">別名</span><span class="sxs-lookup"><span data-stu-id="84f38-168">ALIASES</span></span>

<span data-ttu-id="84f38-169">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="84f38-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="84f38-170">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="84f38-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="84f38-171">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="84f38-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="84f38-172">MODULE <IModule [] >：選用的一組要在此資料庫中啟用的 redis 模組-只有在建立時才能新增模組。</span><span class="sxs-lookup"><span data-stu-id="84f38-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="84f38-173">`Name <String>`：模組的名稱，例如 "RedisBloom"、"RediSearch"、"RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="84f38-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="84f38-174">`[Arg <String>]`：模組的設定選項，例如 "ERROR_RATE 0.00 INITIAL_SIZE 400"。</span><span class="sxs-lookup"><span data-stu-id="84f38-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="84f38-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="84f38-175">RELATED LINKS</span></span>

