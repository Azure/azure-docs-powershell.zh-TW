---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
ms.openlocfilehash: e61eea1d00468937a46f90fdd6a995f5f53ff468
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903033"
---
# <span data-ttu-id="1ede7-101">Restart-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="1ede7-101">Restart-AzCloudService</span></span>

## <span data-ttu-id="1ede7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1ede7-102">SYNOPSIS</span></span>
<span data-ttu-id="1ede7-103">重新開機雲端服務中的一或多個角色實例。</span><span class="sxs-lookup"><span data-stu-id="1ede7-103">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="1ede7-104">語法</span><span class="sxs-lookup"><span data-stu-id="1ede7-104">SYNTAX</span></span>

### <span data-ttu-id="1ede7-105">RestartExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="1ede7-105">RestartExpanded (Default)</span></span>
```
Restart-AzCloudService -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1ede7-106">RestartViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1ede7-106">RestartViaIdentityExpanded</span></span>
```
Restart-AzCloudService -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ede7-107">描述</span><span class="sxs-lookup"><span data-stu-id="1ede7-107">DESCRIPTION</span></span>
<span data-ttu-id="1ede7-108">重新開機雲端服務中的一或多個角色實例。</span><span class="sxs-lookup"><span data-stu-id="1ede7-108">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="1ede7-109">例子</span><span class="sxs-lookup"><span data-stu-id="1ede7-109">EXAMPLES</span></span>

### <span data-ttu-id="1ede7-110">範例 1：重新開機雲端服務的角色實例</span><span class="sxs-lookup"><span data-stu-id="1ede7-110">Example 1: Restart role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="1ede7-111">此命令會重新開機屬於 ContosOrg ContosoFrontEnd_IN_0 ContosoBackEnd_IN_1 ContosoCS 雲端服務的 2 個角色實例和一個角色實例。</span><span class="sxs-lookup"><span data-stu-id="1ede7-111">This command restarts 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="1ede7-112">範例 2：重新開機雲端服務的所有角色</span><span class="sxs-lookup"><span data-stu-id="1ede7-112">Example 2: Restart all roles of cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="1ede7-113">此命令會重新開機名為 ContosoCS 的所有雲端服務角色實例，這些角色實例屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1ede7-113">This command restarts all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="1ede7-114">參數</span><span class="sxs-lookup"><span data-stu-id="1ede7-114">PARAMETERS</span></span>

### <span data-ttu-id="1ede7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ede7-115">-AsJob</span></span>
<span data-ttu-id="1ede7-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="1ede7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1ede7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ede7-117">-DefaultProfile</span></span>
<span data-ttu-id="1ede7-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ede7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ede7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ede7-119">-InputObject</span></span>
<span data-ttu-id="1ede7-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1ede7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ede7-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ede7-121">-Name</span></span>
<span data-ttu-id="1ede7-122">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ede7-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ede7-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1ede7-123">-NoWait</span></span>
<span data-ttu-id="1ede7-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="1ede7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1ede7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ede7-125">-PassThru</span></span>
<span data-ttu-id="1ede7-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="1ede7-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1ede7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ede7-127">-ResourceGroupName</span></span>
<span data-ttu-id="1ede7-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ede7-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ede7-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="1ede7-129">-RoleInstance</span></span>
<span data-ttu-id="1ede7-130">雲端服務角色實例名稱清單。</span><span class="sxs-lookup"><span data-stu-id="1ede7-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="1ede7-131">'\*' 的值表示雲端服務的所有角色實例。</span><span class="sxs-lookup"><span data-stu-id="1ede7-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="1ede7-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ede7-132">-SubscriptionId</span></span>
<span data-ttu-id="1ede7-133">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="1ede7-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1ede7-134">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1ede7-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ede7-135">-確認</span><span class="sxs-lookup"><span data-stu-id="1ede7-135">-Confirm</span></span>
<span data-ttu-id="1ede7-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1ede7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ede7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ede7-137">-WhatIf</span></span>
<span data-ttu-id="1ede7-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ede7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ede7-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ede7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ede7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ede7-140">CommonParameters</span></span>
<span data-ttu-id="1ede7-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1ede7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ede7-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ede7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ede7-143">輸入</span><span class="sxs-lookup"><span data-stu-id="1ede7-143">INPUTS</span></span>

### <span data-ttu-id="1ede7-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="1ede7-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="1ede7-145">輸出</span><span class="sxs-lookup"><span data-stu-id="1ede7-145">OUTPUTS</span></span>

### <span data-ttu-id="1ede7-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ede7-146">System.Boolean</span></span>

## <span data-ttu-id="1ede7-147">筆記</span><span class="sxs-lookup"><span data-stu-id="1ede7-147">NOTES</span></span>

<span data-ttu-id="1ede7-148">別名</span><span class="sxs-lookup"><span data-stu-id="1ede7-148">ALIASES</span></span>

<span data-ttu-id="1ede7-149">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="1ede7-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ede7-150">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1ede7-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ede7-151">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="1ede7-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ede7-152">INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="1ede7-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ede7-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="1ede7-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="1ede7-154">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="1ede7-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ede7-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="1ede7-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="1ede7-156">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ede7-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="1ede7-157">`[RoleName <String>]`：角色名稱。</span><span class="sxs-lookup"><span data-stu-id="1ede7-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="1ede7-158">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="1ede7-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1ede7-159">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1ede7-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1ede7-160">`[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="1ede7-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="1ede7-161">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="1ede7-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="1ede7-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ede7-162">RELATED LINKS</span></span>

