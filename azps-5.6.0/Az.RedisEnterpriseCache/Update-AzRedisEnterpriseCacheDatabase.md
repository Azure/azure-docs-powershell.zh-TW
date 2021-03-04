---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 882bbb9f45720114fe3ca12e8094e1464b895881
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914625"
---
# <span data-ttu-id="1bcbc-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="1bcbc-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="1bcbc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1bcbc-102">SYNOPSIS</span></span>
<span data-ttu-id="1bcbc-103">更新資料庫</span><span class="sxs-lookup"><span data-stu-id="1bcbc-103">Updates a database</span></span>

## <span data-ttu-id="1bcbc-104">語法</span><span class="sxs-lookup"><span data-stu-id="1bcbc-104">SYNTAX</span></span>

### <span data-ttu-id="1bcbc-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="1bcbc-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1bcbc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1bcbc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1bcbc-107">描述</span><span class="sxs-lookup"><span data-stu-id="1bcbc-107">DESCRIPTION</span></span>
<span data-ttu-id="1bcbc-108">更新資料庫</span><span class="sxs-lookup"><span data-stu-id="1bcbc-108">Updates a database</span></span>

## <span data-ttu-id="1bcbc-109">例子</span><span class="sxs-lookup"><span data-stu-id="1bcbc-109">EXAMPLES</span></span>

### <span data-ttu-id="1bcbc-110">範例 1：更新用戶端通訊協定</span><span class="sxs-lookup"><span data-stu-id="1bcbc-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="1bcbc-111">此命令會更新名為 MyCache 的 Redis Enterprise Cache 資料庫的用戶端通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="1bcbc-112">範例 2：更新用戶端通訊協定和路由策略</span><span class="sxs-lookup"><span data-stu-id="1bcbc-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="1bcbc-113">此命令會更新名為 MyCache 之 Redis Enterprise Cache 之資料庫的用戶端通訊協定和修正策略。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="1bcbc-114">參數</span><span class="sxs-lookup"><span data-stu-id="1bcbc-114">PARAMETERS</span></span>

### <span data-ttu-id="1bcbc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bcbc-115">-AsJob</span></span>
<span data-ttu-id="1bcbc-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="1bcbc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1bcbc-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="1bcbc-117">-ClientProtocol</span></span>
<span data-ttu-id="1bcbc-118">指定重新發送用戶端是否可以使用 TLS 加密或純文字重新文本通訊協定進行連結。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="1bcbc-119">預設值為 TLS 加密。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-119">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="1bcbc-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="1bcbc-120">-ClusteringPolicy</span></span>
<span data-ttu-id="1bcbc-121">叢集策略 - 預設值為 OSSCluster。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="1bcbc-122">于建立時指定。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-122">Specified at create time.</span></span>

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

### <span data-ttu-id="1bcbc-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1bcbc-123">-ClusterName</span></span>
<span data-ttu-id="1bcbc-124">RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-124">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="1bcbc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bcbc-125">-DefaultProfile</span></span>
<span data-ttu-id="1bcbc-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bcbc-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="1bcbc-127">-EvictionPolicy</span></span>
<span data-ttu-id="1bcbc-128">重新發佈發佈規則 - 預設值為 VolatileLRU</span><span class="sxs-lookup"><span data-stu-id="1bcbc-128">Redis eviction policy - default is VolatileLRU</span></span>

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

### <span data-ttu-id="1bcbc-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bcbc-129">-InputObject</span></span>
<span data-ttu-id="1bcbc-130">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1bcbc-131">-模組</span><span class="sxs-lookup"><span data-stu-id="1bcbc-131">-Module</span></span>
<span data-ttu-id="1bcbc-132">在此資料庫中啟用的選擇性重新模組組 - 模組只能在建立時新增。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="1bcbc-133">若要建構，請參閱 MODULE 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="1bcbc-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1bcbc-134">-NoWait</span></span>
<span data-ttu-id="1bcbc-135">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="1bcbc-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1bcbc-136">-埠</span><span class="sxs-lookup"><span data-stu-id="1bcbc-136">-Port</span></span>
<span data-ttu-id="1bcbc-137">資料庫端點的 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="1bcbc-138">于建立時指定。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-138">Specified at create time.</span></span>
<span data-ttu-id="1bcbc-139">預設為可用的埠。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="1bcbc-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bcbc-140">-ResourceGroupName</span></span>
<span data-ttu-id="1bcbc-141">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="1bcbc-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1bcbc-142">-SubscriptionId</span></span>
<span data-ttu-id="1bcbc-143">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1bcbc-144">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-144">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1bcbc-145">-確認</span><span class="sxs-lookup"><span data-stu-id="1bcbc-145">-Confirm</span></span>
<span data-ttu-id="1bcbc-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bcbc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bcbc-147">-WhatIf</span></span>
<span data-ttu-id="1bcbc-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bcbc-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bcbc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bcbc-150">CommonParameters</span></span>
<span data-ttu-id="1bcbc-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bcbc-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bcbc-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bcbc-153">輸入</span><span class="sxs-lookup"><span data-stu-id="1bcbc-153">INPUTS</span></span>

### <span data-ttu-id="1bcbc-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="1bcbc-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="1bcbc-155">輸出</span><span class="sxs-lookup"><span data-stu-id="1bcbc-155">OUTPUTS</span></span>

### <span data-ttu-id="1bcbc-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="1bcbc-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="1bcbc-157">筆記</span><span class="sxs-lookup"><span data-stu-id="1bcbc-157">NOTES</span></span>

<span data-ttu-id="1bcbc-158">別名</span><span class="sxs-lookup"><span data-stu-id="1bcbc-158">ALIASES</span></span>

<span data-ttu-id="1bcbc-159">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="1bcbc-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1bcbc-160">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1bcbc-161">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1bcbc-162">INPUTOBJECT： <IRedisEnterpriseCacheIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="1bcbc-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1bcbc-163">`[ClusterName <String>]`：RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="1bcbc-164">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1bcbc-165">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="1bcbc-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1bcbc-166">`[Location <String>]`：作業所位於的區域。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="1bcbc-167">`[OperationId <String>]`：作業的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="1bcbc-168">`[PrivateEndpointConnectionName <String>]`：與 Azure 資源相關聯的私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="1bcbc-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="1bcbc-169">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1bcbc-170">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="1bcbc-171">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="1bcbc-172">MODULE <IModule[]>：在此資料庫中啟用的選擇性重新模組組 - 模組只能在建立時新增。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="1bcbc-173">`Name <String>`：模組的名稱，例如'RedisBloom'，'RediSearch'， 'RedisTimeSeries'</span><span class="sxs-lookup"><span data-stu-id="1bcbc-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="1bcbc-174">`[Arg <String>]`：模組的組ERROR_RATE，例如'ERROR_RATE 0.00 INITIAL_SIZE 400'。</span><span class="sxs-lookup"><span data-stu-id="1bcbc-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="1bcbc-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bcbc-175">RELATED LINKS</span></span>

