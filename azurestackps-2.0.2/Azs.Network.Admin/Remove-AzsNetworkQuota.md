---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/remove-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: fe7c391b8f15e3389a9d61070b8f55d47af6d6ec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968068"
---
# <span data-ttu-id="c88a1-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="c88a1-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="c88a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c88a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c88a1-103">依名稱刪除配額。</span><span class="sxs-lookup"><span data-stu-id="c88a1-103">Delete a quota by name.</span></span>

## <span data-ttu-id="c88a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="c88a1-104">SYNTAX</span></span>

### <span data-ttu-id="c88a1-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="c88a1-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c88a1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c88a1-106">DeleteViaIdentity</span></span>
```
Remove-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c88a1-107">說明</span><span class="sxs-lookup"><span data-stu-id="c88a1-107">DESCRIPTION</span></span>
<span data-ttu-id="c88a1-108">依名稱刪除配額。</span><span class="sxs-lookup"><span data-stu-id="c88a1-108">Delete a quota by name.</span></span>

## <span data-ttu-id="c88a1-109">示例</span><span class="sxs-lookup"><span data-stu-id="c88a1-109">EXAMPLES</span></span>

### <span data-ttu-id="c88a1-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c88a1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="c88a1-111">依名稱移除網路配額。</span><span class="sxs-lookup"><span data-stu-id="c88a1-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="c88a1-112">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c88a1-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="c88a1-113">使用管道移除網路配額。</span><span class="sxs-lookup"><span data-stu-id="c88a1-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="c88a1-114">--------------------------範例 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="c88a1-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="c88a1-115">移除網路配額。</span><span class="sxs-lookup"><span data-stu-id="c88a1-115">Remove a network quota.</span></span>

## <span data-ttu-id="c88a1-116">參數</span><span class="sxs-lookup"><span data-stu-id="c88a1-116">PARAMETERS</span></span>

### <span data-ttu-id="c88a1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c88a1-117">-AsJob</span></span>
<span data-ttu-id="c88a1-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="c88a1-118">Run the command as a job</span></span>

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

### <span data-ttu-id="c88a1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c88a1-119">-DefaultProfile</span></span>
<span data-ttu-id="c88a1-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c88a1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c88a1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c88a1-121">-InputObject</span></span>
<span data-ttu-id="c88a1-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c88a1-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c88a1-123">-位置</span><span class="sxs-lookup"><span data-stu-id="c88a1-123">-Location</span></span>
<span data-ttu-id="c88a1-124">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="c88a1-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c88a1-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c88a1-125">-Name</span></span>
<span data-ttu-id="c88a1-126">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c88a1-126">Name of the resource.</span></span>

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

### <span data-ttu-id="c88a1-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c88a1-127">-NoWait</span></span>
<span data-ttu-id="c88a1-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="c88a1-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c88a1-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c88a1-129">-PassThru</span></span>
<span data-ttu-id="c88a1-130">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="c88a1-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c88a1-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c88a1-131">-SubscriptionId</span></span>
<span data-ttu-id="c88a1-132">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c88a1-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c88a1-133">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="c88a1-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c88a1-134">-確認</span><span class="sxs-lookup"><span data-stu-id="c88a1-134">-Confirm</span></span>
<span data-ttu-id="c88a1-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c88a1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c88a1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c88a1-136">-WhatIf</span></span>
<span data-ttu-id="c88a1-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c88a1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c88a1-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c88a1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c88a1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88a1-139">CommonParameters</span></span>
<span data-ttu-id="c88a1-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c88a1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88a1-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c88a1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88a1-142">輸入</span><span class="sxs-lookup"><span data-stu-id="c88a1-142">INPUTS</span></span>

### <span data-ttu-id="c88a1-143">INetworkAdminIdentity （NetworkAdmin）的</span><span class="sxs-lookup"><span data-stu-id="c88a1-143">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="c88a1-144">輸出</span><span class="sxs-lookup"><span data-stu-id="c88a1-144">OUTPUTS</span></span>

### <span data-ttu-id="c88a1-145">System.object</span><span class="sxs-lookup"><span data-stu-id="c88a1-145">System.Boolean</span></span>



## <span data-ttu-id="c88a1-146">筆記</span><span class="sxs-lookup"><span data-stu-id="c88a1-146">NOTES</span></span>

<span data-ttu-id="c88a1-147">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c88a1-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c88a1-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c88a1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c88a1-149">INPUTOBJECT <INetworkAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c88a1-149">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c88a1-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c88a1-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c88a1-151">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="c88a1-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c88a1-152">`[ResourceName <String>]`：資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c88a1-152">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="c88a1-153">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c88a1-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c88a1-154">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="c88a1-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c88a1-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="c88a1-155">RELATED LINKS</span></span>
