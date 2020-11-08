---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
ms.openlocfilehash: 13f5e76a7fbb101e9fa6b1247f233c0f85aba8bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128409"
---
# <span data-ttu-id="5c614-101">Remove-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="5c614-101">Remove-AzVMWareAuthorization</span></span>

## <span data-ttu-id="5c614-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c614-102">SYNOPSIS</span></span>
<span data-ttu-id="5c614-103">在私有雲端刪除 ExpressRoute 線路授權</span><span class="sxs-lookup"><span data-stu-id="5c614-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="5c614-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c614-104">SYNTAX</span></span>

### <span data-ttu-id="5c614-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="5c614-105">Delete (Default)</span></span>
```
Remove-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5c614-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5c614-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5c614-107">說明</span><span class="sxs-lookup"><span data-stu-id="5c614-107">DESCRIPTION</span></span>
<span data-ttu-id="5c614-108">在私有雲端刪除 ExpressRoute 線路授權</span><span class="sxs-lookup"><span data-stu-id="5c614-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="5c614-109">示例</span><span class="sxs-lookup"><span data-stu-id="5c614-109">EXAMPLES</span></span>

### <span data-ttu-id="5c614-110">範例1：刪除私有雲端授權</span><span class="sxs-lookup"><span data-stu-id="5c614-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="5c614-111">刪除私有雲端的授權</span><span class="sxs-lookup"><span data-stu-id="5c614-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="5c614-112">參數</span><span class="sxs-lookup"><span data-stu-id="5c614-112">PARAMETERS</span></span>

### <span data-ttu-id="5c614-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c614-113">-AsJob</span></span>
<span data-ttu-id="5c614-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="5c614-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5c614-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c614-115">-DefaultProfile</span></span>
<span data-ttu-id="5c614-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c614-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c614-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c614-117">-InputObject</span></span>
<span data-ttu-id="5c614-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5c614-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c614-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c614-119">-Name</span></span>
<span data-ttu-id="5c614-120">私有雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="5c614-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c614-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5c614-121">-NoWait</span></span>
<span data-ttu-id="5c614-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="5c614-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5c614-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c614-123">-PassThru</span></span>
<span data-ttu-id="5c614-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="5c614-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5c614-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="5c614-125">-PrivateCloudName</span></span>
<span data-ttu-id="5c614-126">私有雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="5c614-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="5c614-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c614-127">-ResourceGroupName</span></span>
<span data-ttu-id="5c614-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c614-128">The name of the resource group.</span></span>
<span data-ttu-id="5c614-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5c614-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5c614-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5c614-130">-SubscriptionId</span></span>
<span data-ttu-id="5c614-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="5c614-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5c614-132">-確認</span><span class="sxs-lookup"><span data-stu-id="5c614-132">-Confirm</span></span>
<span data-ttu-id="5c614-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5c614-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c614-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c614-134">-WhatIf</span></span>
<span data-ttu-id="5c614-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c614-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c614-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c614-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c614-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c614-137">CommonParameters</span></span>
<span data-ttu-id="5c614-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c614-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c614-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5c614-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c614-140">輸入</span><span class="sxs-lookup"><span data-stu-id="5c614-140">INPUTS</span></span>

### <span data-ttu-id="5c614-141">IVMWareIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5c614-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="5c614-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5c614-142">OUTPUTS</span></span>

### <span data-ttu-id="5c614-143">System.object</span><span class="sxs-lookup"><span data-stu-id="5c614-143">System.Boolean</span></span>

## <span data-ttu-id="5c614-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5c614-144">NOTES</span></span>

<span data-ttu-id="5c614-145">別名</span><span class="sxs-lookup"><span data-stu-id="5c614-145">ALIASES</span></span>

<span data-ttu-id="5c614-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5c614-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5c614-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5c614-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5c614-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5c614-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5c614-149">INPUTOBJECT <IVMWareIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5c614-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5c614-150">`[AuthorizationName <String>]`：私人雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="5c614-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="5c614-151">`[ClusterName <String>]`：私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="5c614-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="5c614-152">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="5c614-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="5c614-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5c614-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5c614-154">`[Location <String>]`： Azure region</span><span class="sxs-lookup"><span data-stu-id="5c614-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="5c614-155">`[PrivateCloudName <String>]`：私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="5c614-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="5c614-156">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c614-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5c614-157">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5c614-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="5c614-158">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c614-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="5c614-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c614-159">RELATED LINKS</span></span>

