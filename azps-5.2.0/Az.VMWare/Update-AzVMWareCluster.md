---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
ms.openlocfilehash: b8e1f819c01edac24ff23c629de130036442c9e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274244"
---
# <span data-ttu-id="8aa91-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="8aa91-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="8aa91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8aa91-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa91-103">在私有雲端更新群集</span><span class="sxs-lookup"><span data-stu-id="8aa91-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="8aa91-104">句法</span><span class="sxs-lookup"><span data-stu-id="8aa91-104">SYNTAX</span></span>

### <span data-ttu-id="8aa91-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="8aa91-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8aa91-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8aa91-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8aa91-107">說明</span><span class="sxs-lookup"><span data-stu-id="8aa91-107">DESCRIPTION</span></span>
<span data-ttu-id="8aa91-108">在私有雲端更新群集</span><span class="sxs-lookup"><span data-stu-id="8aa91-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="8aa91-109">示例</span><span class="sxs-lookup"><span data-stu-id="8aa91-109">EXAMPLES</span></span>

### <span data-ttu-id="8aa91-110">範例1：依名稱更新群集大小</span><span class="sxs-lookup"><span data-stu-id="8aa91-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="8aa91-111">依名稱更新群集大小</span><span class="sxs-lookup"><span data-stu-id="8aa91-111">Update cluster size by name</span></span>

### <span data-ttu-id="8aa91-112">範例2：依輸入物件更新群集大小</span><span class="sxs-lookup"><span data-stu-id="8aa91-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="8aa91-113">依輸入物件更新群集大小</span><span class="sxs-lookup"><span data-stu-id="8aa91-113">Update cluster size by input object</span></span>

## <span data-ttu-id="8aa91-114">參數</span><span class="sxs-lookup"><span data-stu-id="8aa91-114">PARAMETERS</span></span>

### <span data-ttu-id="8aa91-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8aa91-115">-AsJob</span></span>
<span data-ttu-id="8aa91-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="8aa91-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8aa91-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="8aa91-117">-ClusterSize</span></span>
<span data-ttu-id="8aa91-118">群集大小</span><span class="sxs-lookup"><span data-stu-id="8aa91-118">The cluster size</span></span>

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

### <span data-ttu-id="8aa91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa91-119">-DefaultProfile</span></span>
<span data-ttu-id="8aa91-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8aa91-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aa91-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8aa91-121">-InputObject</span></span>
<span data-ttu-id="8aa91-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8aa91-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8aa91-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="8aa91-123">-Name</span></span>
<span data-ttu-id="8aa91-124">私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="8aa91-124">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="8aa91-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8aa91-125">-NoWait</span></span>
<span data-ttu-id="8aa91-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="8aa91-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8aa91-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="8aa91-127">-PrivateCloudName</span></span>
<span data-ttu-id="8aa91-128">私有雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="8aa91-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="8aa91-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aa91-129">-ResourceGroupName</span></span>
<span data-ttu-id="8aa91-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8aa91-130">The name of the resource group.</span></span>
<span data-ttu-id="8aa91-131">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8aa91-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8aa91-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8aa91-132">-SubscriptionId</span></span>
<span data-ttu-id="8aa91-133">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="8aa91-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8aa91-134">-確認</span><span class="sxs-lookup"><span data-stu-id="8aa91-134">-Confirm</span></span>
<span data-ttu-id="8aa91-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8aa91-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aa91-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aa91-136">-WhatIf</span></span>
<span data-ttu-id="8aa91-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8aa91-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8aa91-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8aa91-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aa91-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa91-139">CommonParameters</span></span>
<span data-ttu-id="8aa91-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8aa91-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa91-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8aa91-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa91-142">輸入</span><span class="sxs-lookup"><span data-stu-id="8aa91-142">INPUTS</span></span>

### <span data-ttu-id="8aa91-143">IVMWareIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8aa91-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="8aa91-144">輸出</span><span class="sxs-lookup"><span data-stu-id="8aa91-144">OUTPUTS</span></span>

### <span data-ttu-id="8aa91-145">ICluster 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="8aa91-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="8aa91-146">筆記</span><span class="sxs-lookup"><span data-stu-id="8aa91-146">NOTES</span></span>

<span data-ttu-id="8aa91-147">別名</span><span class="sxs-lookup"><span data-stu-id="8aa91-147">ALIASES</span></span>

<span data-ttu-id="8aa91-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8aa91-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8aa91-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8aa91-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8aa91-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8aa91-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8aa91-151">INPUTOBJECT <IVMWareIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8aa91-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8aa91-152">`[AuthorizationName <String>]`：私人雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="8aa91-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="8aa91-153">`[ClusterName <String>]`：私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="8aa91-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="8aa91-154">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="8aa91-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="8aa91-155">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="8aa91-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8aa91-156">`[Location <String>]`： Azure region</span><span class="sxs-lookup"><span data-stu-id="8aa91-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="8aa91-157">`[PrivateCloudName <String>]`：私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="8aa91-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="8aa91-158">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8aa91-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8aa91-159">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8aa91-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="8aa91-160">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8aa91-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="8aa91-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="8aa91-161">RELATED LINKS</span></span>

