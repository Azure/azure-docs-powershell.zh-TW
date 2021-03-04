---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareCluster.md
ms.openlocfilehash: 878691dcc0cdc2a94dd5cc8509d9d74231aaee35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910805"
---
# <span data-ttu-id="2fe9e-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="2fe9e-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="2fe9e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2fe9e-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe9e-103">刪除私人雲端中的集區</span><span class="sxs-lookup"><span data-stu-id="2fe9e-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="2fe9e-104">語法</span><span class="sxs-lookup"><span data-stu-id="2fe9e-104">SYNTAX</span></span>

### <span data-ttu-id="2fe9e-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="2fe9e-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2fe9e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2fe9e-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2fe9e-107">描述</span><span class="sxs-lookup"><span data-stu-id="2fe9e-107">DESCRIPTION</span></span>
<span data-ttu-id="2fe9e-108">刪除私人雲端中的集區</span><span class="sxs-lookup"><span data-stu-id="2fe9e-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="2fe9e-109">例子</span><span class="sxs-lookup"><span data-stu-id="2fe9e-109">EXAMPLES</span></span>

### <span data-ttu-id="2fe9e-110">範例 1：刪除私人雲端中的集區</span><span class="sxs-lookup"><span data-stu-id="2fe9e-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="2fe9e-111">刪除私人雲端中的集區</span><span class="sxs-lookup"><span data-stu-id="2fe9e-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="2fe9e-112">參數</span><span class="sxs-lookup"><span data-stu-id="2fe9e-112">PARAMETERS</span></span>

### <span data-ttu-id="2fe9e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fe9e-113">-AsJob</span></span>
<span data-ttu-id="2fe9e-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="2fe9e-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2fe9e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe9e-115">-DefaultProfile</span></span>
<span data-ttu-id="2fe9e-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fe9e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fe9e-117">-InputObject</span></span>
<span data-ttu-id="2fe9e-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2fe9e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2fe9e-119">-Name</span></span>
<span data-ttu-id="2fe9e-120">專用雲端中的組名</span><span class="sxs-lookup"><span data-stu-id="2fe9e-120">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe9e-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2fe9e-121">-NoWait</span></span>
<span data-ttu-id="2fe9e-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="2fe9e-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2fe9e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fe9e-123">-PassThru</span></span>
<span data-ttu-id="2fe9e-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="2fe9e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2fe9e-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="2fe9e-125">-PrivateCloudName</span></span>
<span data-ttu-id="2fe9e-126">私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="2fe9e-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="2fe9e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fe9e-127">-ResourceGroupName</span></span>
<span data-ttu-id="2fe9e-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-128">The name of the resource group.</span></span>
<span data-ttu-id="2fe9e-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2fe9e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2fe9e-130">-SubscriptionId</span></span>
<span data-ttu-id="2fe9e-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2fe9e-132">-確認</span><span class="sxs-lookup"><span data-stu-id="2fe9e-132">-Confirm</span></span>
<span data-ttu-id="2fe9e-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fe9e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fe9e-134">-WhatIf</span></span>
<span data-ttu-id="2fe9e-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fe9e-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fe9e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe9e-137">CommonParameters</span></span>
<span data-ttu-id="2fe9e-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe9e-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fe9e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe9e-140">輸入</span><span class="sxs-lookup"><span data-stu-id="2fe9e-140">INPUTS</span></span>

### <span data-ttu-id="2fe9e-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.models.I VMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="2fe9e-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="2fe9e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="2fe9e-142">OUTPUTS</span></span>

### <span data-ttu-id="2fe9e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2fe9e-143">System.Boolean</span></span>

## <span data-ttu-id="2fe9e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="2fe9e-144">NOTES</span></span>

<span data-ttu-id="2fe9e-145">別名</span><span class="sxs-lookup"><span data-stu-id="2fe9e-145">ALIASES</span></span>

<span data-ttu-id="2fe9e-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2fe9e-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2fe9e-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2fe9e-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2fe9e-149">INPUTOBJECT： <IVMWareIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2fe9e-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2fe9e-150">`[AuthorizationName <String>]`：專用雲端中的 ExpressRoute 回路授權名稱</span><span class="sxs-lookup"><span data-stu-id="2fe9e-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="2fe9e-151">`[ClusterName <String>]`：專用雲端中的組名</span><span class="sxs-lookup"><span data-stu-id="2fe9e-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="2fe9e-152">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="2fe9e-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="2fe9e-153">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="2fe9e-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2fe9e-154">`[Location <String>]`：Azure 區域</span><span class="sxs-lookup"><span data-stu-id="2fe9e-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="2fe9e-155">`[PrivateCloudName <String>]`：專用雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="2fe9e-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="2fe9e-156">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2fe9e-157">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="2fe9e-158">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="2fe9e-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fe9e-159">RELATED LINKS</span></span>

