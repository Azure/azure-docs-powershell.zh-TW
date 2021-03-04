---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/remove-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 5a29444c5f6d05ddbf614e86cd13af6818d24d79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903037"
---
# <span data-ttu-id="4e8a4-101">Remove-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="4e8a4-101">Remove-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="4e8a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4e8a4-102">SYNOPSIS</span></span>
<span data-ttu-id="4e8a4-103">刪除雲端服務中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-103">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="4e8a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="4e8a4-104">SYNTAX</span></span>

### <span data-ttu-id="4e8a4-105">DeleteExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="4e8a4-105">DeleteExpanded (Default)</span></span>
```
Remove-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstance <String[]> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e8a4-106">DeleteViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4e8a4-106">DeleteViaIdentityExpanded</span></span>
```
Remove-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e8a4-107">描述</span><span class="sxs-lookup"><span data-stu-id="4e8a4-107">DESCRIPTION</span></span>
<span data-ttu-id="4e8a4-108">刪除雲端服務中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-108">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="4e8a4-109">例子</span><span class="sxs-lookup"><span data-stu-id="4e8a4-109">EXAMPLES</span></span>

### <span data-ttu-id="4e8a4-110">範例 1：移除雲端服務角色實例</span><span class="sxs-lookup"><span data-stu-id="4e8a4-110">Example 1: Remove a cloud service role instance</span></span>
```powershell
PS C:\> Remove-AzCloudServiceInstance -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="4e8a4-111">此命令會移除名為 contosoCS ContosoFrontEnd_IN_0名為 ContosoCS 之雲端服務的名稱角色實例，該角色實例屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-111">This command removes the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="4e8a4-112">參數</span><span class="sxs-lookup"><span data-stu-id="4e8a4-112">PARAMETERS</span></span>

### <span data-ttu-id="4e8a4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e8a4-113">-AsJob</span></span>
<span data-ttu-id="4e8a4-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="4e8a4-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4e8a4-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="4e8a4-115">-CloudServiceName</span></span>
<span data-ttu-id="4e8a4-116">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-116">Name of the cloud service.</span></span>

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

### <span data-ttu-id="4e8a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e8a4-117">-DefaultProfile</span></span>
<span data-ttu-id="4e8a4-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e8a4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e8a4-119">-InputObject</span></span>
<span data-ttu-id="4e8a4-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e8a4-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4e8a4-121">-NoWait</span></span>
<span data-ttu-id="4e8a4-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="4e8a4-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4e8a4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e8a4-123">-PassThru</span></span>
<span data-ttu-id="4e8a4-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="4e8a4-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4e8a4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e8a4-125">-ResourceGroupName</span></span>
<span data-ttu-id="4e8a4-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-126">Name of the resource group.</span></span>

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

### <span data-ttu-id="4e8a4-127">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="4e8a4-127">-RoleInstance</span></span>
<span data-ttu-id="4e8a4-128">雲端服務角色實例名稱清單。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-128">List of cloud service role instance names.</span></span>
<span data-ttu-id="4e8a4-129">'\*' 的值表示雲端服務的所有角色實例。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-129">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="4e8a4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e8a4-130">-SubscriptionId</span></span>
<span data-ttu-id="4e8a4-131">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-131">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4e8a4-132">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4e8a4-133">-確認</span><span class="sxs-lookup"><span data-stu-id="4e8a4-133">-Confirm</span></span>
<span data-ttu-id="4e8a4-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e8a4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e8a4-135">-WhatIf</span></span>
<span data-ttu-id="4e8a4-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e8a4-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e8a4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e8a4-138">CommonParameters</span></span>
<span data-ttu-id="4e8a4-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e8a4-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e8a4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e8a4-141">輸入</span><span class="sxs-lookup"><span data-stu-id="4e8a4-141">INPUTS</span></span>

### <span data-ttu-id="4e8a4-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="4e8a4-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="4e8a4-143">輸出</span><span class="sxs-lookup"><span data-stu-id="4e8a4-143">OUTPUTS</span></span>

### <span data-ttu-id="4e8a4-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4e8a4-144">System.Boolean</span></span>

## <span data-ttu-id="4e8a4-145">筆記</span><span class="sxs-lookup"><span data-stu-id="4e8a4-145">NOTES</span></span>

<span data-ttu-id="4e8a4-146">別名</span><span class="sxs-lookup"><span data-stu-id="4e8a4-146">ALIASES</span></span>

<span data-ttu-id="4e8a4-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4e8a4-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e8a4-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e8a4-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e8a4-150">INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4e8a4-150">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e8a4-151">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="4e8a4-151">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="4e8a4-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="4e8a4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e8a4-153">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="4e8a4-153">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="4e8a4-154">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-154">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="4e8a4-155">`[RoleName <String>]`：角色名稱。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-155">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="4e8a4-156">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4e8a4-157">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4e8a4-158">`[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-158">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="4e8a4-159">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="4e8a4-159">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="4e8a4-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e8a4-160">RELATED LINKS</span></span>

