---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: 22d0fed7c72aa5754b7393cdf06fb58a4bfc0db3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286636"
---
# <span data-ttu-id="47ee2-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="47ee2-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="47ee2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="47ee2-103">刪除 RedisEnterprise 的快取群集。</span><span class="sxs-lookup"><span data-stu-id="47ee2-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="47ee2-104">句法</span><span class="sxs-lookup"><span data-stu-id="47ee2-104">SYNTAX</span></span>

### <span data-ttu-id="47ee2-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="47ee2-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="47ee2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47ee2-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47ee2-107">說明</span><span class="sxs-lookup"><span data-stu-id="47ee2-107">DESCRIPTION</span></span>
<span data-ttu-id="47ee2-108">刪除 RedisEnterprise 的快取群集。</span><span class="sxs-lookup"><span data-stu-id="47ee2-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="47ee2-109">示例</span><span class="sxs-lookup"><span data-stu-id="47ee2-109">EXAMPLES</span></span>

### <span data-ttu-id="47ee2-110">範例1：移除 Redis Enterprise Cache 並傳回結果</span><span class="sxs-lookup"><span data-stu-id="47ee2-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="47ee2-111">這個命令會移除 Redis 的企業快取，並顯示操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="47ee2-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="47ee2-112">範例2：移除 Redis Enterprise Cache，但不顯示結果</span><span class="sxs-lookup"><span data-stu-id="47ee2-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="47ee2-113">這個命令會移除 Redis 的企業快取。</span><span class="sxs-lookup"><span data-stu-id="47ee2-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="47ee2-114">因為未指定 PassThru 參數，所以不會顯示運算的結果。</span><span class="sxs-lookup"><span data-stu-id="47ee2-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="47ee2-115">參數</span><span class="sxs-lookup"><span data-stu-id="47ee2-115">PARAMETERS</span></span>

### <span data-ttu-id="47ee2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47ee2-116">-AsJob</span></span>
<span data-ttu-id="47ee2-117">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="47ee2-117">Run the command as a job</span></span>

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

### <span data-ttu-id="47ee2-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="47ee2-118">-ClusterName</span></span>
<span data-ttu-id="47ee2-119">RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="47ee2-119">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="47ee2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ee2-120">-DefaultProfile</span></span>
<span data-ttu-id="47ee2-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47ee2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47ee2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47ee2-122">-InputObject</span></span>
<span data-ttu-id="47ee2-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="47ee2-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="47ee2-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="47ee2-124">-NoWait</span></span>
<span data-ttu-id="47ee2-125">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="47ee2-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="47ee2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47ee2-126">-PassThru</span></span>
<span data-ttu-id="47ee2-127">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="47ee2-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="47ee2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47ee2-128">-ResourceGroupName</span></span>
<span data-ttu-id="47ee2-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="47ee2-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="47ee2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47ee2-130">-SubscriptionId</span></span>
<span data-ttu-id="47ee2-131">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="47ee2-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="47ee2-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="47ee2-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="47ee2-133">-確認</span><span class="sxs-lookup"><span data-stu-id="47ee2-133">-Confirm</span></span>
<span data-ttu-id="47ee2-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47ee2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ee2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ee2-135">-WhatIf</span></span>
<span data-ttu-id="47ee2-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47ee2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47ee2-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47ee2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ee2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ee2-138">CommonParameters</span></span>
<span data-ttu-id="47ee2-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47ee2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ee2-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="47ee2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ee2-141">輸入</span><span class="sxs-lookup"><span data-stu-id="47ee2-141">INPUTS</span></span>

### <span data-ttu-id="47ee2-142">IRedisEnterpriseCacheIdentity （RedisEnterpriseCache）的</span><span class="sxs-lookup"><span data-stu-id="47ee2-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="47ee2-143">輸出</span><span class="sxs-lookup"><span data-stu-id="47ee2-143">OUTPUTS</span></span>

### <span data-ttu-id="47ee2-144">System.object</span><span class="sxs-lookup"><span data-stu-id="47ee2-144">System.Boolean</span></span>

## <span data-ttu-id="47ee2-145">筆記</span><span class="sxs-lookup"><span data-stu-id="47ee2-145">NOTES</span></span>

<span data-ttu-id="47ee2-146">別名</span><span class="sxs-lookup"><span data-stu-id="47ee2-146">ALIASES</span></span>

<span data-ttu-id="47ee2-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="47ee2-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47ee2-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="47ee2-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47ee2-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="47ee2-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47ee2-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="47ee2-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47ee2-151">`[ClusterName <String>]`： RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="47ee2-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="47ee2-152">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="47ee2-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="47ee2-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="47ee2-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47ee2-154">`[Location <String>]`：操作所在的地區。</span><span class="sxs-lookup"><span data-stu-id="47ee2-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="47ee2-155">`[OperationId <String>]`：操作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="47ee2-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="47ee2-156">`[PrivateEndpointConnectionName <String>]`：與 Azure 資源相關聯的專用端點連接的名稱</span><span class="sxs-lookup"><span data-stu-id="47ee2-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="47ee2-157">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="47ee2-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="47ee2-158">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="47ee2-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="47ee2-159">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="47ee2-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="47ee2-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="47ee2-160">RELATED LINKS</span></span>

