---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
ms.openlocfilehash: 8d1918599832f5740515dc6334192bf9b4cc54ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905705"
---
# <span data-ttu-id="5a7b6-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="5a7b6-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="5a7b6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5a7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7b6-103">刪除私人雲端</span><span class="sxs-lookup"><span data-stu-id="5a7b6-103">Delete a private cloud</span></span>

## <span data-ttu-id="5a7b6-104">語法</span><span class="sxs-lookup"><span data-stu-id="5a7b6-104">SYNTAX</span></span>

### <span data-ttu-id="5a7b6-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="5a7b6-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5a7b6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5a7b6-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5a7b6-107">描述</span><span class="sxs-lookup"><span data-stu-id="5a7b6-107">DESCRIPTION</span></span>
<span data-ttu-id="5a7b6-108">刪除私人雲端</span><span class="sxs-lookup"><span data-stu-id="5a7b6-108">Delete a private cloud</span></span>

## <span data-ttu-id="5a7b6-109">例子</span><span class="sxs-lookup"><span data-stu-id="5a7b6-109">EXAMPLES</span></span>

### <span data-ttu-id="5a7b6-110">範例 1：刪除私人雲端</span><span class="sxs-lookup"><span data-stu-id="5a7b6-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="5a7b6-111">刪除私人雲端</span><span class="sxs-lookup"><span data-stu-id="5a7b6-111">Delete private cloud</span></span>

## <span data-ttu-id="5a7b6-112">參數</span><span class="sxs-lookup"><span data-stu-id="5a7b6-112">PARAMETERS</span></span>

### <span data-ttu-id="5a7b6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a7b6-113">-AsJob</span></span>
<span data-ttu-id="5a7b6-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="5a7b6-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5a7b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7b6-115">-DefaultProfile</span></span>
<span data-ttu-id="5a7b6-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a7b6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a7b6-117">-InputObject</span></span>
<span data-ttu-id="5a7b6-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5a7b6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a7b6-119">-Name</span></span>
<span data-ttu-id="5a7b6-120">私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="5a7b6-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7b6-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5a7b6-121">-NoWait</span></span>
<span data-ttu-id="5a7b6-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="5a7b6-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5a7b6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a7b6-123">-PassThru</span></span>
<span data-ttu-id="5a7b6-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="5a7b6-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5a7b6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a7b6-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a7b6-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-126">The name of the resource group.</span></span>
<span data-ttu-id="5a7b6-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5a7b6-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a7b6-128">-SubscriptionId</span></span>
<span data-ttu-id="5a7b6-129">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5a7b6-130">-確認</span><span class="sxs-lookup"><span data-stu-id="5a7b6-130">-Confirm</span></span>
<span data-ttu-id="5a7b6-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a7b6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a7b6-132">-WhatIf</span></span>
<span data-ttu-id="5a7b6-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a7b6-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a7b6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7b6-135">CommonParameters</span></span>
<span data-ttu-id="5a7b6-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7b6-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a7b6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7b6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5a7b6-138">INPUTS</span></span>

### <span data-ttu-id="5a7b6-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.models.I VMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="5a7b6-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="5a7b6-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5a7b6-140">OUTPUTS</span></span>

### <span data-ttu-id="5a7b6-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a7b6-141">System.Boolean</span></span>

## <span data-ttu-id="5a7b6-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5a7b6-142">NOTES</span></span>

<span data-ttu-id="5a7b6-143">別名</span><span class="sxs-lookup"><span data-stu-id="5a7b6-143">ALIASES</span></span>

<span data-ttu-id="5a7b6-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5a7b6-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5a7b6-145">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5a7b6-146">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5a7b6-147">INPUTOBJECT： <IVMWareIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5a7b6-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5a7b6-148">`[AuthorizationName <String>]`：專用雲端中的 ExpressRoute 回路授權名稱</span><span class="sxs-lookup"><span data-stu-id="5a7b6-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="5a7b6-149">`[ClusterName <String>]`：專用雲端中的組名</span><span class="sxs-lookup"><span data-stu-id="5a7b6-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="5a7b6-150">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="5a7b6-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="5a7b6-151">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="5a7b6-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5a7b6-152">`[Location <String>]`：Azure 區域</span><span class="sxs-lookup"><span data-stu-id="5a7b6-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="5a7b6-153">`[PrivateCloudName <String>]`：專用雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="5a7b6-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="5a7b6-154">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5a7b6-155">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="5a7b6-156">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a7b6-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="5a7b6-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a7b6-157">RELATED LINKS</span></span>

