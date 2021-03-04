---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: d6b030cfbc6233d917d252f2d271eb7d4bfe65bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914638"
---
# <span data-ttu-id="c5b18-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="c5b18-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="c5b18-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c5b18-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b18-103">刪除 RedisEnterprise 緩存組。</span><span class="sxs-lookup"><span data-stu-id="c5b18-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="c5b18-104">語法</span><span class="sxs-lookup"><span data-stu-id="c5b18-104">SYNTAX</span></span>

### <span data-ttu-id="c5b18-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="c5b18-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c5b18-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c5b18-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c5b18-107">描述</span><span class="sxs-lookup"><span data-stu-id="c5b18-107">DESCRIPTION</span></span>
<span data-ttu-id="c5b18-108">刪除 RedisEnterprise 緩存組。</span><span class="sxs-lookup"><span data-stu-id="c5b18-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="c5b18-109">例子</span><span class="sxs-lookup"><span data-stu-id="c5b18-109">EXAMPLES</span></span>

### <span data-ttu-id="c5b18-110">範例 1：移除 Redis Enterprise Cache 並返回結果</span><span class="sxs-lookup"><span data-stu-id="c5b18-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="c5b18-111">此命令會移除 Redis Enterprise Cache，並顯示作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="c5b18-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="c5b18-112">範例 2：移除 Redis Enterprise Cache 且不顯示結果</span><span class="sxs-lookup"><span data-stu-id="c5b18-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="c5b18-113">此命令會移除 Redis Enterprise Cache。</span><span class="sxs-lookup"><span data-stu-id="c5b18-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="c5b18-114">由於未指定 PassThru 參數，因此不會顯示作業的結果。</span><span class="sxs-lookup"><span data-stu-id="c5b18-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="c5b18-115">參數</span><span class="sxs-lookup"><span data-stu-id="c5b18-115">PARAMETERS</span></span>

### <span data-ttu-id="c5b18-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5b18-116">-AsJob</span></span>
<span data-ttu-id="c5b18-117">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="c5b18-117">Run the command as a job</span></span>

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

### <span data-ttu-id="c5b18-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c5b18-118">-ClusterName</span></span>
<span data-ttu-id="c5b18-119">RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="c5b18-119">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b18-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b18-120">-DefaultProfile</span></span>
<span data-ttu-id="c5b18-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5b18-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5b18-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5b18-122">-InputObject</span></span>
<span data-ttu-id="c5b18-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c5b18-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b18-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c5b18-124">-NoWait</span></span>
<span data-ttu-id="c5b18-125">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="c5b18-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c5b18-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5b18-126">-PassThru</span></span>
<span data-ttu-id="c5b18-127">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="c5b18-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c5b18-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5b18-128">-ResourceGroupName</span></span>
<span data-ttu-id="c5b18-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5b18-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b18-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5b18-130">-SubscriptionId</span></span>
<span data-ttu-id="c5b18-131">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c5b18-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c5b18-132">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c5b18-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b18-133">-確認</span><span class="sxs-lookup"><span data-stu-id="c5b18-133">-Confirm</span></span>
<span data-ttu-id="c5b18-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c5b18-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5b18-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5b18-135">-WhatIf</span></span>
<span data-ttu-id="c5b18-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c5b18-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5b18-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5b18-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5b18-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b18-138">CommonParameters</span></span>
<span data-ttu-id="c5b18-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c5b18-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b18-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5b18-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b18-141">輸入</span><span class="sxs-lookup"><span data-stu-id="c5b18-141">INPUTS</span></span>

### <span data-ttu-id="c5b18-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="c5b18-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="c5b18-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c5b18-143">OUTPUTS</span></span>

### <span data-ttu-id="c5b18-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c5b18-144">System.Boolean</span></span>

## <span data-ttu-id="c5b18-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c5b18-145">NOTES</span></span>

<span data-ttu-id="c5b18-146">別名</span><span class="sxs-lookup"><span data-stu-id="c5b18-146">ALIASES</span></span>

<span data-ttu-id="c5b18-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c5b18-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c5b18-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c5b18-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c5b18-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c5b18-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c5b18-150">INPUTOBJECT： <IRedisEnterpriseCacheIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c5b18-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c5b18-151">`[ClusterName <String>]`：RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="c5b18-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="c5b18-152">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5b18-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c5b18-153">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="c5b18-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c5b18-154">`[Location <String>]`：作業所位於的區域。</span><span class="sxs-lookup"><span data-stu-id="c5b18-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="c5b18-155">`[OperationId <String>]`：作業的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5b18-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="c5b18-156">`[PrivateEndpointConnectionName <String>]`：與 Azure 資源相關聯的私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="c5b18-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="c5b18-157">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5b18-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c5b18-158">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c5b18-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="c5b18-159">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c5b18-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c5b18-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5b18-160">RELATED LINKS</span></span>

