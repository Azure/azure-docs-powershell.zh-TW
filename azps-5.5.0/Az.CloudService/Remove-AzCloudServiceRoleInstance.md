---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/remove-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 8d44cc541cf44e03e2946ce428eb96c2f902bf84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136574"
---
# <span data-ttu-id="7b49a-101">Remove-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="7b49a-101">Remove-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="7b49a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b49a-102">SYNOPSIS</span></span>
<span data-ttu-id="7b49a-103">刪除雲端服務中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="7b49a-103">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="7b49a-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b49a-104">SYNTAX</span></span>

### <span data-ttu-id="7b49a-105">DeleteExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="7b49a-105">DeleteExpanded (Default)</span></span>
```
Remove-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstance <String[]> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7b49a-106">DeleteViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7b49a-106">DeleteViaIdentityExpanded</span></span>
```
Remove-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7b49a-107">說明</span><span class="sxs-lookup"><span data-stu-id="7b49a-107">DESCRIPTION</span></span>
<span data-ttu-id="7b49a-108">刪除雲端服務中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="7b49a-108">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="7b49a-109">示例</span><span class="sxs-lookup"><span data-stu-id="7b49a-109">EXAMPLES</span></span>

### <span data-ttu-id="7b49a-110">範例1：移除雲端服務角色實例</span><span class="sxs-lookup"><span data-stu-id="7b49a-110">Example 1: Remove a cloud service role instance</span></span>
```powershell
PS C:\> Remove-AzCloudServiceInstance -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="7b49a-111">這個命令會從屬於名為 ContosOrg 之資源群組的名為 ContosoCS 的雲端服務，移除名為 ContosoFrontEnd_IN_0 的角色實例。</span><span class="sxs-lookup"><span data-stu-id="7b49a-111">This command removes the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="7b49a-112">參數</span><span class="sxs-lookup"><span data-stu-id="7b49a-112">PARAMETERS</span></span>

### <span data-ttu-id="7b49a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b49a-113">-AsJob</span></span>
<span data-ttu-id="7b49a-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="7b49a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7b49a-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="7b49a-115">-CloudServiceName</span></span>
<span data-ttu-id="7b49a-116">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b49a-116">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b49a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b49a-117">-DefaultProfile</span></span>
<span data-ttu-id="7b49a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b49a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b49a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b49a-119">-InputObject</span></span>
<span data-ttu-id="7b49a-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7b49a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: DeleteViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b49a-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7b49a-121">-NoWait</span></span>
<span data-ttu-id="7b49a-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="7b49a-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7b49a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b49a-123">-PassThru</span></span>
<span data-ttu-id="7b49a-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="7b49a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7b49a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b49a-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b49a-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b49a-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b49a-127">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="7b49a-127">-RoleInstance</span></span>
<span data-ttu-id="7b49a-128">雲端服務角色實例名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="7b49a-128">List of cloud service role instance names.</span></span>
<span data-ttu-id="7b49a-129">"\*" 的值會代表雲端服務的所有角色實例。</span><span class="sxs-lookup"><span data-stu-id="7b49a-129">Value of '\*' will signify all role instances of the cloud service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b49a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b49a-130">-SubscriptionId</span></span>
<span data-ttu-id="7b49a-131">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="7b49a-131">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7b49a-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7b49a-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b49a-133">-確認</span><span class="sxs-lookup"><span data-stu-id="7b49a-133">-Confirm</span></span>
<span data-ttu-id="7b49a-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7b49a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b49a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b49a-135">-WhatIf</span></span>
<span data-ttu-id="7b49a-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7b49a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b49a-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7b49a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b49a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b49a-138">CommonParameters</span></span>
<span data-ttu-id="7b49a-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b49a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b49a-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7b49a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b49a-141">輸入</span><span class="sxs-lookup"><span data-stu-id="7b49a-141">INPUTS</span></span>

### <span data-ttu-id="7b49a-142">ICloudServiceIdentity （CloudService）的</span><span class="sxs-lookup"><span data-stu-id="7b49a-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="7b49a-143">輸出</span><span class="sxs-lookup"><span data-stu-id="7b49a-143">OUTPUTS</span></span>

### <span data-ttu-id="7b49a-144">System.object</span><span class="sxs-lookup"><span data-stu-id="7b49a-144">System.Boolean</span></span>

## <span data-ttu-id="7b49a-145">筆記</span><span class="sxs-lookup"><span data-stu-id="7b49a-145">NOTES</span></span>

<span data-ttu-id="7b49a-146">別名</span><span class="sxs-lookup"><span data-stu-id="7b49a-146">ALIASES</span></span>

<span data-ttu-id="7b49a-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="7b49a-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7b49a-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="7b49a-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b49a-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7b49a-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7b49a-150">INPUTOBJECT <ICloudServiceIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="7b49a-150">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7b49a-151">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="7b49a-151">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="7b49a-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="7b49a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7b49a-153">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="7b49a-153">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="7b49a-154">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b49a-154">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="7b49a-155">`[RoleName <String>]`：角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b49a-155">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="7b49a-156">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="7b49a-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7b49a-157">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7b49a-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7b49a-158">`[UpdateDomain <Int32?>]`：指定識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="7b49a-158">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="7b49a-159">更新網域是以零為基礎的索引來標識：第一個更新網域的識別碼為0，第二個是 ID 為1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="7b49a-159">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="7b49a-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b49a-160">RELATED LINKS</span></span>

