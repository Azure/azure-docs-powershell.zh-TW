---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: f708d1b752c0d8106d7a8f9f7613fa74b6b19937
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911221"
---
# <span data-ttu-id="957c9-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="957c9-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="957c9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="957c9-102">SYNOPSIS</span></span>
<span data-ttu-id="957c9-103">更新私人雲端中的組群</span><span class="sxs-lookup"><span data-stu-id="957c9-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="957c9-104">語法</span><span class="sxs-lookup"><span data-stu-id="957c9-104">SYNTAX</span></span>

### <span data-ttu-id="957c9-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="957c9-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="957c9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="957c9-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="957c9-107">描述</span><span class="sxs-lookup"><span data-stu-id="957c9-107">DESCRIPTION</span></span>
<span data-ttu-id="957c9-108">更新私人雲端中的組群</span><span class="sxs-lookup"><span data-stu-id="957c9-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="957c9-109">例子</span><span class="sxs-lookup"><span data-stu-id="957c9-109">EXAMPLES</span></span>

### <span data-ttu-id="957c9-110">範例 1：根據名稱更新組大小</span><span class="sxs-lookup"><span data-stu-id="957c9-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="957c9-111">根據名稱更新組大小</span><span class="sxs-lookup"><span data-stu-id="957c9-111">Update cluster size by name</span></span>

### <span data-ttu-id="957c9-112">範例 2：根據輸入物件更新集區大小</span><span class="sxs-lookup"><span data-stu-id="957c9-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="957c9-113">根據輸入物件更新組大小</span><span class="sxs-lookup"><span data-stu-id="957c9-113">Update cluster size by input object</span></span>

## <span data-ttu-id="957c9-114">參數</span><span class="sxs-lookup"><span data-stu-id="957c9-114">PARAMETERS</span></span>

### <span data-ttu-id="957c9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="957c9-115">-AsJob</span></span>
<span data-ttu-id="957c9-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="957c9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="957c9-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="957c9-117">-ClusterSize</span></span>
<span data-ttu-id="957c9-118">組大小</span><span class="sxs-lookup"><span data-stu-id="957c9-118">The cluster size</span></span>

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

### <span data-ttu-id="957c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957c9-119">-DefaultProfile</span></span>
<span data-ttu-id="957c9-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="957c9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="957c9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="957c9-121">-InputObject</span></span>
<span data-ttu-id="957c9-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="957c9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="957c9-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="957c9-123">-Name</span></span>
<span data-ttu-id="957c9-124">專用雲端中的組名</span><span class="sxs-lookup"><span data-stu-id="957c9-124">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="957c9-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="957c9-125">-NoWait</span></span>
<span data-ttu-id="957c9-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="957c9-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="957c9-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="957c9-127">-PrivateCloudName</span></span>
<span data-ttu-id="957c9-128">私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="957c9-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="957c9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="957c9-129">-ResourceGroupName</span></span>
<span data-ttu-id="957c9-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="957c9-130">The name of the resource group.</span></span>
<span data-ttu-id="957c9-131">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="957c9-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="957c9-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="957c9-132">-SubscriptionId</span></span>
<span data-ttu-id="957c9-133">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="957c9-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="957c9-134">-確認</span><span class="sxs-lookup"><span data-stu-id="957c9-134">-Confirm</span></span>
<span data-ttu-id="957c9-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="957c9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="957c9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="957c9-136">-WhatIf</span></span>
<span data-ttu-id="957c9-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="957c9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="957c9-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="957c9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="957c9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957c9-139">CommonParameters</span></span>
<span data-ttu-id="957c9-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="957c9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957c9-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="957c9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957c9-142">輸入</span><span class="sxs-lookup"><span data-stu-id="957c9-142">INPUTS</span></span>

### <span data-ttu-id="957c9-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.models.I VMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="957c9-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="957c9-144">輸出</span><span class="sxs-lookup"><span data-stu-id="957c9-144">OUTPUTS</span></span>

### <span data-ttu-id="957c9-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="957c9-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="957c9-146">筆記</span><span class="sxs-lookup"><span data-stu-id="957c9-146">NOTES</span></span>

<span data-ttu-id="957c9-147">別名</span><span class="sxs-lookup"><span data-stu-id="957c9-147">ALIASES</span></span>

<span data-ttu-id="957c9-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="957c9-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="957c9-149">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="957c9-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="957c9-150">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="957c9-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="957c9-151">INPUTOBJECT： <IVMWareIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="957c9-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="957c9-152">`[AuthorizationName <String>]`：專用雲端中的 ExpressRoute 回路授權名稱</span><span class="sxs-lookup"><span data-stu-id="957c9-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="957c9-153">`[ClusterName <String>]`：專用雲端中的組名</span><span class="sxs-lookup"><span data-stu-id="957c9-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="957c9-154">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="957c9-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="957c9-155">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="957c9-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="957c9-156">`[Location <String>]`：Azure 區域</span><span class="sxs-lookup"><span data-stu-id="957c9-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="957c9-157">`[PrivateCloudName <String>]`：專用雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="957c9-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="957c9-158">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="957c9-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="957c9-159">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="957c9-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="957c9-160">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="957c9-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="957c9-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="957c9-161">RELATED LINKS</span></span>

