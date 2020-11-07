---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/remove-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: fe7c391b8f15e3389a9d61070b8f55d47af6d6ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794863"
---
# <span data-ttu-id="e4682-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="e4682-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="e4682-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4682-102">SYNOPSIS</span></span>
<span data-ttu-id="e4682-103">依名稱刪除配額。</span><span class="sxs-lookup"><span data-stu-id="e4682-103">Delete a quota by name.</span></span>

## <span data-ttu-id="e4682-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4682-104">SYNTAX</span></span>

### <span data-ttu-id="e4682-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="e4682-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e4682-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e4682-106">DeleteViaIdentity</span></span>
```
Remove-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4682-107">說明</span><span class="sxs-lookup"><span data-stu-id="e4682-107">DESCRIPTION</span></span>
<span data-ttu-id="e4682-108">依名稱刪除配額。</span><span class="sxs-lookup"><span data-stu-id="e4682-108">Delete a quota by name.</span></span>

## <span data-ttu-id="e4682-109">示例</span><span class="sxs-lookup"><span data-stu-id="e4682-109">EXAMPLES</span></span>

### <span data-ttu-id="e4682-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4682-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="e4682-111">依名稱移除網路配額。</span><span class="sxs-lookup"><span data-stu-id="e4682-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="e4682-112">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4682-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="e4682-113">使用管道移除網路配額。</span><span class="sxs-lookup"><span data-stu-id="e4682-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="e4682-114">--------------------------範例 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4682-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="e4682-115">移除網路配額。</span><span class="sxs-lookup"><span data-stu-id="e4682-115">Remove a network quota.</span></span>

## <span data-ttu-id="e4682-116">參數</span><span class="sxs-lookup"><span data-stu-id="e4682-116">PARAMETERS</span></span>

### <span data-ttu-id="e4682-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4682-117">-AsJob</span></span>
<span data-ttu-id="e4682-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="e4682-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e4682-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4682-119">-DefaultProfile</span></span>
<span data-ttu-id="e4682-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4682-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4682-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4682-121">-InputObject</span></span>
<span data-ttu-id="e4682-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e4682-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4682-123">-位置</span><span class="sxs-lookup"><span data-stu-id="e4682-123">-Location</span></span>
<span data-ttu-id="e4682-124">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="e4682-124">Location of the resource.</span></span>

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

### <span data-ttu-id="e4682-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4682-125">-Name</span></span>
<span data-ttu-id="e4682-126">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4682-126">Name of the resource.</span></span>

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

### <span data-ttu-id="e4682-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e4682-127">-NoWait</span></span>
<span data-ttu-id="e4682-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="e4682-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e4682-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4682-129">-PassThru</span></span>
<span data-ttu-id="e4682-130">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="e4682-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e4682-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4682-131">-SubscriptionId</span></span>
<span data-ttu-id="e4682-132">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e4682-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e4682-133">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e4682-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e4682-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e4682-134">-Confirm</span></span>
<span data-ttu-id="e4682-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e4682-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4682-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4682-136">-WhatIf</span></span>
<span data-ttu-id="e4682-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e4682-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4682-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4682-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4682-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4682-139">CommonParameters</span></span>
<span data-ttu-id="e4682-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4682-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4682-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e4682-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4682-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e4682-142">INPUTS</span></span>

### <span data-ttu-id="e4682-143">INetworkAdminIdentity （NetworkAdmin）的</span><span class="sxs-lookup"><span data-stu-id="e4682-143">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="e4682-144">輸出</span><span class="sxs-lookup"><span data-stu-id="e4682-144">OUTPUTS</span></span>

### <span data-ttu-id="e4682-145">System.object</span><span class="sxs-lookup"><span data-stu-id="e4682-145">System.Boolean</span></span>



## <span data-ttu-id="e4682-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e4682-146">NOTES</span></span>

<span data-ttu-id="e4682-147">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e4682-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4682-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e4682-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e4682-149">INPUTOBJECT <INetworkAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e4682-149">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4682-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="e4682-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4682-151">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="e4682-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e4682-152">`[ResourceName <String>]`：資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4682-152">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="e4682-153">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e4682-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e4682-154">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e4682-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e4682-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4682-155">RELATED LINKS</span></span>

