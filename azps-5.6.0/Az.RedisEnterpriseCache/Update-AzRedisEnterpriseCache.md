---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: 1b16f30b068eb41bf0202c65e95f55f94769ba2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914626"
---
# <span data-ttu-id="5f81c-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="5f81c-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="5f81c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5f81c-102">SYNOPSIS</span></span>
<span data-ttu-id="5f81c-103">更新現有的 RedisEnterprise 集區</span><span class="sxs-lookup"><span data-stu-id="5f81c-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="5f81c-104">語法</span><span class="sxs-lookup"><span data-stu-id="5f81c-104">SYNTAX</span></span>

### <span data-ttu-id="5f81c-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="5f81c-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5f81c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5f81c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5f81c-107">描述</span><span class="sxs-lookup"><span data-stu-id="5f81c-107">DESCRIPTION</span></span>
<span data-ttu-id="5f81c-108">更新現有的 RedisEnterprise 集區</span><span class="sxs-lookup"><span data-stu-id="5f81c-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="5f81c-109">例子</span><span class="sxs-lookup"><span data-stu-id="5f81c-109">EXAMPLES</span></span>

### <span data-ttu-id="5f81c-110">範例 1：更新 Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="5f81c-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="5f81c-111">此命令會更新最小 TLS 版本，並將標記新增到名為 MyCache 的 Redis Enterprise Cache。</span><span class="sxs-lookup"><span data-stu-id="5f81c-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="5f81c-112">參數</span><span class="sxs-lookup"><span data-stu-id="5f81c-112">PARAMETERS</span></span>

### <span data-ttu-id="5f81c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f81c-113">-AsJob</span></span>
<span data-ttu-id="5f81c-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="5f81c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5f81c-115">-容量</span><span class="sxs-lookup"><span data-stu-id="5f81c-115">-Capacity</span></span>
<span data-ttu-id="5f81c-116">RedisEnterprise 集區的大小。</span><span class="sxs-lookup"><span data-stu-id="5f81c-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="5f81c-117">根據 SKU，預設為 2 或 3。</span><span class="sxs-lookup"><span data-stu-id="5f81c-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="5f81c-118">有效的值 (2、4、6、...) 企業 SKUS 和 (3、9、15、...) Flash SK。</span><span class="sxs-lookup"><span data-stu-id="5f81c-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="5f81c-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5f81c-119">-ClusterName</span></span>
<span data-ttu-id="5f81c-120">RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="5f81c-120">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="5f81c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f81c-121">-DefaultProfile</span></span>
<span data-ttu-id="5f81c-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f81c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f81c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f81c-123">-InputObject</span></span>
<span data-ttu-id="5f81c-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5f81c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5f81c-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="5f81c-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="5f81c-126">要支援的組組最低 TLS 版本，例如'1.2'</span><span class="sxs-lookup"><span data-stu-id="5f81c-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="5f81c-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5f81c-127">-NoWait</span></span>
<span data-ttu-id="5f81c-128">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="5f81c-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5f81c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f81c-129">-ResourceGroupName</span></span>
<span data-ttu-id="5f81c-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f81c-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="5f81c-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="5f81c-131">-Sku</span></span>
<span data-ttu-id="5f81c-132">要部署的 RedisEnterprise 集區類型。</span><span class="sxs-lookup"><span data-stu-id="5f81c-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="5f81c-133">可能的值： (Enterprise_E10、EnterpriseFlash_F300等) </span><span class="sxs-lookup"><span data-stu-id="5f81c-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

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

### <span data-ttu-id="5f81c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f81c-134">-SubscriptionId</span></span>
<span data-ttu-id="5f81c-135">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5f81c-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5f81c-136">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5f81c-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5f81c-137">-標記</span><span class="sxs-lookup"><span data-stu-id="5f81c-137">-Tag</span></span>
<span data-ttu-id="5f81c-138">資源標記。</span><span class="sxs-lookup"><span data-stu-id="5f81c-138">Resource tags.</span></span>

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

### <span data-ttu-id="5f81c-139">-確認</span><span class="sxs-lookup"><span data-stu-id="5f81c-139">-Confirm</span></span>
<span data-ttu-id="5f81c-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5f81c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f81c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f81c-141">-WhatIf</span></span>
<span data-ttu-id="5f81c-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f81c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f81c-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f81c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f81c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f81c-144">CommonParameters</span></span>
<span data-ttu-id="5f81c-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5f81c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f81c-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f81c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f81c-147">輸入</span><span class="sxs-lookup"><span data-stu-id="5f81c-147">INPUTS</span></span>

### <span data-ttu-id="5f81c-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="5f81c-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="5f81c-149">輸出</span><span class="sxs-lookup"><span data-stu-id="5f81c-149">OUTPUTS</span></span>

### <span data-ttu-id="5f81c-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="5f81c-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="5f81c-151">筆記</span><span class="sxs-lookup"><span data-stu-id="5f81c-151">NOTES</span></span>

<span data-ttu-id="5f81c-152">別名</span><span class="sxs-lookup"><span data-stu-id="5f81c-152">ALIASES</span></span>

<span data-ttu-id="5f81c-153">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5f81c-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5f81c-154">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5f81c-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f81c-155">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5f81c-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5f81c-156">INPUTOBJECT： <IRedisEnterpriseCacheIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5f81c-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5f81c-157">`[ClusterName <String>]`：RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="5f81c-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="5f81c-158">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f81c-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5f81c-159">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="5f81c-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5f81c-160">`[Location <String>]`：作業所位於的區域。</span><span class="sxs-lookup"><span data-stu-id="5f81c-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="5f81c-161">`[OperationId <String>]`：作業的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f81c-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="5f81c-162">`[PrivateEndpointConnectionName <String>]`：與 Azure 資源相關聯的私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="5f81c-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="5f81c-163">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f81c-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5f81c-164">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5f81c-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="5f81c-165">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5f81c-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5f81c-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f81c-166">RELATED LINKS</span></span>

