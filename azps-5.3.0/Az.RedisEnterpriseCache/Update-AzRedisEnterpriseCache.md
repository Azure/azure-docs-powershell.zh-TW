---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: ef1ef3d45594b0e290a014fb3aa98d670e5681a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286632"
---
# <span data-ttu-id="dd45a-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="dd45a-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="dd45a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd45a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd45a-103">更新現有的 RedisEnterprise 群集</span><span class="sxs-lookup"><span data-stu-id="dd45a-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="dd45a-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd45a-104">SYNTAX</span></span>

### <span data-ttu-id="dd45a-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="dd45a-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd45a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dd45a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dd45a-107">說明</span><span class="sxs-lookup"><span data-stu-id="dd45a-107">DESCRIPTION</span></span>
<span data-ttu-id="dd45a-108">更新現有的 RedisEnterprise 群集</span><span class="sxs-lookup"><span data-stu-id="dd45a-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="dd45a-109">示例</span><span class="sxs-lookup"><span data-stu-id="dd45a-109">EXAMPLES</span></span>

### <span data-ttu-id="dd45a-110">範例1：更新 Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="dd45a-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="dd45a-111">這個命令會更新最小的 TLS 版本，並將標籤新增到名為 MyCache 的 Redis Enterprise 快取。</span><span class="sxs-lookup"><span data-stu-id="dd45a-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="dd45a-112">參數</span><span class="sxs-lookup"><span data-stu-id="dd45a-112">PARAMETERS</span></span>

### <span data-ttu-id="dd45a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd45a-113">-AsJob</span></span>
<span data-ttu-id="dd45a-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="dd45a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="dd45a-115">-容量</span><span class="sxs-lookup"><span data-stu-id="dd45a-115">-Capacity</span></span>
<span data-ttu-id="dd45a-116">RedisEnterprise 群集的大小。</span><span class="sxs-lookup"><span data-stu-id="dd45a-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="dd45a-117">根據 SKU 的預設值為2或3。</span><span class="sxs-lookup"><span data-stu-id="dd45a-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="dd45a-118">有效值為 (2、4、6、... ) （適用于企業版 Sku），以及 (3、9、15、... ) 的 Flash Sku。</span><span class="sxs-lookup"><span data-stu-id="dd45a-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="dd45a-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dd45a-119">-ClusterName</span></span>
<span data-ttu-id="dd45a-120">RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd45a-120">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="dd45a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd45a-121">-DefaultProfile</span></span>
<span data-ttu-id="dd45a-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd45a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd45a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd45a-123">-InputObject</span></span>
<span data-ttu-id="dd45a-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dd45a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dd45a-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="dd45a-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="dd45a-126">要支援之群集的最低 TLS 版本，例如 "1.2"</span><span class="sxs-lookup"><span data-stu-id="dd45a-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="dd45a-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dd45a-127">-NoWait</span></span>
<span data-ttu-id="dd45a-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="dd45a-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dd45a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd45a-129">-ResourceGroupName</span></span>
<span data-ttu-id="dd45a-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd45a-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="dd45a-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="dd45a-131">-Sku</span></span>
<span data-ttu-id="dd45a-132">要部署的 RedisEnterprise 群集類型。</span><span class="sxs-lookup"><span data-stu-id="dd45a-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="dd45a-133">可能的值： (Enterprise_E10、EnterpriseFlash_F300 等。 ) </span><span class="sxs-lookup"><span data-stu-id="dd45a-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd45a-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd45a-134">-SubscriptionId</span></span>
<span data-ttu-id="dd45a-135">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="dd45a-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="dd45a-136">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="dd45a-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dd45a-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="dd45a-137">-Tag</span></span>
<span data-ttu-id="dd45a-138">資源標記。</span><span class="sxs-lookup"><span data-stu-id="dd45a-138">Resource tags.</span></span>

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

### <span data-ttu-id="dd45a-139">-確認</span><span class="sxs-lookup"><span data-stu-id="dd45a-139">-Confirm</span></span>
<span data-ttu-id="dd45a-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dd45a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd45a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd45a-141">-WhatIf</span></span>
<span data-ttu-id="dd45a-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd45a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd45a-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd45a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd45a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd45a-144">CommonParameters</span></span>
<span data-ttu-id="dd45a-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd45a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd45a-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dd45a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd45a-147">輸入</span><span class="sxs-lookup"><span data-stu-id="dd45a-147">INPUTS</span></span>

### <span data-ttu-id="dd45a-148">IRedisEnterpriseCacheIdentity （RedisEnterpriseCache）的</span><span class="sxs-lookup"><span data-stu-id="dd45a-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="dd45a-149">輸出</span><span class="sxs-lookup"><span data-stu-id="dd45a-149">OUTPUTS</span></span>

### <span data-ttu-id="dd45a-150">ICluster （RedisEnterpriseCache）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="dd45a-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="dd45a-151">筆記</span><span class="sxs-lookup"><span data-stu-id="dd45a-151">NOTES</span></span>

<span data-ttu-id="dd45a-152">別名</span><span class="sxs-lookup"><span data-stu-id="dd45a-152">ALIASES</span></span>

<span data-ttu-id="dd45a-153">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="dd45a-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd45a-154">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="dd45a-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd45a-155">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="dd45a-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd45a-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="dd45a-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd45a-157">`[ClusterName <String>]`： RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd45a-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="dd45a-158">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd45a-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dd45a-159">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="dd45a-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd45a-160">`[Location <String>]`：操作所在的地區。</span><span class="sxs-lookup"><span data-stu-id="dd45a-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="dd45a-161">`[OperationId <String>]`：操作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd45a-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="dd45a-162">`[PrivateEndpointConnectionName <String>]`：與 Azure 資源相關聯的專用端點連接的名稱</span><span class="sxs-lookup"><span data-stu-id="dd45a-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="dd45a-163">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd45a-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="dd45a-164">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="dd45a-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="dd45a-165">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="dd45a-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dd45a-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd45a-166">RELATED LINKS</span></span>

