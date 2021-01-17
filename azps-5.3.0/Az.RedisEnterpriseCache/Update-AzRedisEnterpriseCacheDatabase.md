---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286628"
---
# <span data-ttu-id="9aa2b-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="9aa2b-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="9aa2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9aa2b-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa2b-103">更新資料庫</span><span class="sxs-lookup"><span data-stu-id="9aa2b-103">Updates a database</span></span>

## <span data-ttu-id="9aa2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9aa2b-104">SYNTAX</span></span>

### <span data-ttu-id="9aa2b-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="9aa2b-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9aa2b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9aa2b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9aa2b-107">說明</span><span class="sxs-lookup"><span data-stu-id="9aa2b-107">DESCRIPTION</span></span>
<span data-ttu-id="9aa2b-108">更新資料庫</span><span class="sxs-lookup"><span data-stu-id="9aa2b-108">Updates a database</span></span>

## <span data-ttu-id="9aa2b-109">示例</span><span class="sxs-lookup"><span data-stu-id="9aa2b-109">EXAMPLES</span></span>

### <span data-ttu-id="9aa2b-110">範例1：更新用戶端通訊協定</span><span class="sxs-lookup"><span data-stu-id="9aa2b-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="9aa2b-111">這個命令會針對名為 MyCache 的 Redis Enterprise Cache，更新資料庫的用戶端通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="9aa2b-112">範例2：更新用戶端通訊協定和逐出原則</span><span class="sxs-lookup"><span data-stu-id="9aa2b-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="9aa2b-113">這個命令會針對名為 MyCache 的 Redis Enterprise Cache，更新資料庫的用戶端協定和逐出原則。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="9aa2b-114">參數</span><span class="sxs-lookup"><span data-stu-id="9aa2b-114">PARAMETERS</span></span>

### <span data-ttu-id="9aa2b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9aa2b-115">-AsJob</span></span>
<span data-ttu-id="9aa2b-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="9aa2b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9aa2b-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="9aa2b-117">-ClientProtocol</span></span>
<span data-ttu-id="9aa2b-118">指定 redis 用戶端是否可使用 TLS 加密或純文字 redis 通訊協定連線。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="9aa2b-119">預設值為 TLS 加密。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-119">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="9aa2b-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="9aa2b-120">-ClusteringPolicy</span></span>
<span data-ttu-id="9aa2b-121">[群集原則]-預設值為 [OSSCluster]。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="9aa2b-122">在建立時間指定。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-122">Specified at create time.</span></span>

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

### <span data-ttu-id="9aa2b-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9aa2b-123">-ClusterName</span></span>
<span data-ttu-id="9aa2b-124">RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-124">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa2b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa2b-125">-DefaultProfile</span></span>
<span data-ttu-id="9aa2b-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aa2b-127">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="9aa2b-127">-EvictionPolicy</span></span>
<span data-ttu-id="9aa2b-128">Redis 逐出原則-預設為 VolatileLRU</span><span class="sxs-lookup"><span data-stu-id="9aa2b-128">Redis eviction policy - default is VolatileLRU</span></span>

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

### <span data-ttu-id="9aa2b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9aa2b-129">-InputObject</span></span>
<span data-ttu-id="9aa2b-130">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa2b-131">-模組</span><span class="sxs-lookup"><span data-stu-id="9aa2b-131">-Module</span></span>
<span data-ttu-id="9aa2b-132">要在此資料庫中啟用的 redis 模組的選擇性集合-只有在建立期間才能新增模組。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="9aa2b-133">若要建立，請參閱模組屬性的 [記事] 區段，並建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="9aa2b-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9aa2b-134">-NoWait</span></span>
<span data-ttu-id="9aa2b-135">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="9aa2b-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9aa2b-136">-埠</span><span class="sxs-lookup"><span data-stu-id="9aa2b-136">-Port</span></span>
<span data-ttu-id="9aa2b-137">資料庫端點的 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="9aa2b-138">在建立時間指定。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-138">Specified at create time.</span></span>
<span data-ttu-id="9aa2b-139">預設為可用的埠。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="9aa2b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aa2b-140">-ResourceGroupName</span></span>
<span data-ttu-id="9aa2b-141">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-141">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa2b-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9aa2b-142">-SubscriptionId</span></span>
<span data-ttu-id="9aa2b-143">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9aa2b-144">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa2b-145">-確認</span><span class="sxs-lookup"><span data-stu-id="9aa2b-145">-Confirm</span></span>
<span data-ttu-id="9aa2b-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aa2b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aa2b-147">-WhatIf</span></span>
<span data-ttu-id="9aa2b-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9aa2b-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aa2b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa2b-150">CommonParameters</span></span>
<span data-ttu-id="9aa2b-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa2b-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa2b-153">輸入</span><span class="sxs-lookup"><span data-stu-id="9aa2b-153">INPUTS</span></span>

### <span data-ttu-id="9aa2b-154">IRedisEnterpriseCacheIdentity （RedisEnterpriseCache）的</span><span class="sxs-lookup"><span data-stu-id="9aa2b-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="9aa2b-155">輸出</span><span class="sxs-lookup"><span data-stu-id="9aa2b-155">OUTPUTS</span></span>

### <span data-ttu-id="9aa2b-156">IDatabase （RedisEnterpriseCache）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="9aa2b-157">筆記</span><span class="sxs-lookup"><span data-stu-id="9aa2b-157">NOTES</span></span>

<span data-ttu-id="9aa2b-158">別名</span><span class="sxs-lookup"><span data-stu-id="9aa2b-158">ALIASES</span></span>

<span data-ttu-id="9aa2b-159">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9aa2b-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9aa2b-160">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9aa2b-161">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9aa2b-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9aa2b-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9aa2b-163">`[ClusterName <String>]`： RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="9aa2b-164">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9aa2b-165">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="9aa2b-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9aa2b-166">`[Location <String>]`：操作所在的地區。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="9aa2b-167">`[OperationId <String>]`：操作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="9aa2b-168">`[PrivateEndpointConnectionName <String>]`：與 Azure 資源相關聯的專用端點連接的名稱</span><span class="sxs-lookup"><span data-stu-id="9aa2b-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="9aa2b-169">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9aa2b-170">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="9aa2b-171">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="9aa2b-172">MODULE <IModule [] >：選用的一組要在此資料庫中啟用的 redis 模組-只有在建立時才能新增模組。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="9aa2b-173">`Name <String>`：模組的名稱，例如 "RedisBloom"、"RediSearch"、"RedisTimeSeries"</span><span class="sxs-lookup"><span data-stu-id="9aa2b-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="9aa2b-174">`[Arg <String>]`：模組的設定選項，例如 "ERROR_RATE 0.00 INITIAL_SIZE 400"。</span><span class="sxs-lookup"><span data-stu-id="9aa2b-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="9aa2b-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="9aa2b-175">RELATED LINKS</span></span>

