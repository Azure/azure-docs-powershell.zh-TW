---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudservicereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceReimage.md
ms.openlocfilehash: d82b3038ad797354f000de379964b3da3a7f135b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912106"
---
# <span data-ttu-id="b0ca2-101">Invoke-AzCloudServiceReimage</span><span class="sxs-lookup"><span data-stu-id="b0ca2-101">Invoke-AzCloudServiceReimage</span></span>

## <span data-ttu-id="b0ca2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b0ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="b0ca2-103">重新映射非同步作業會以 Web 角色或員工角色實例重新安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-103">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="b0ca2-104">語法</span><span class="sxs-lookup"><span data-stu-id="b0ca2-104">SYNTAX</span></span>

### <span data-ttu-id="b0ca2-105">重新映射Expanded (預設) </span><span class="sxs-lookup"><span data-stu-id="b0ca2-105">ReimageExpanded (Default)</span></span>
```
Invoke-AzCloudServiceReimage -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b0ca2-106">ReimageViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b0ca2-106">ReimageViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceReimage -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b0ca2-107">描述</span><span class="sxs-lookup"><span data-stu-id="b0ca2-107">DESCRIPTION</span></span>
<span data-ttu-id="b0ca2-108">重新映射非同步作業會以 Web 角色或員工角色實例重新安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-108">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="b0ca2-109">例子</span><span class="sxs-lookup"><span data-stu-id="b0ca2-109">EXAMPLES</span></span>

### <span data-ttu-id="b0ca2-110">範例 1：雲端服務的重新映射角色實例</span><span class="sxs-lookup"><span data-stu-id="b0ca2-110">Example 1: Reimage role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="b0ca2-111">此命令會重新映射 2 個角色實例ContosoFrontEnd_IN_0和 ContosoBackEnd_IN_1名為 ContosoCS 的雲端服務，這些角色實例屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-111">This command reimages 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="b0ca2-112">範例 2：重新映射雲端服務的所有角色</span><span class="sxs-lookup"><span data-stu-id="b0ca2-112">Example 2: Reimage all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="b0ca2-113">此命令會重新映射所有名為 ContosoCS 的雲端服務角色實例，這些角色實例屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-113">This command reimages all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="b0ca2-114">參數</span><span class="sxs-lookup"><span data-stu-id="b0ca2-114">PARAMETERS</span></span>

### <span data-ttu-id="b0ca2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0ca2-115">-AsJob</span></span>
<span data-ttu-id="b0ca2-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="b0ca2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b0ca2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0ca2-117">-DefaultProfile</span></span>
<span data-ttu-id="b0ca2-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0ca2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0ca2-119">-InputObject</span></span>
<span data-ttu-id="b0ca2-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0ca2-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0ca2-121">-Name</span></span>
<span data-ttu-id="b0ca2-122">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ca2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b0ca2-123">-NoWait</span></span>
<span data-ttu-id="b0ca2-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="b0ca2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b0ca2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0ca2-125">-PassThru</span></span>
<span data-ttu-id="b0ca2-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="b0ca2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b0ca2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0ca2-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0ca2-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ca2-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="b0ca2-129">-RoleInstance</span></span>
<span data-ttu-id="b0ca2-130">雲端服務角色實例名稱清單。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="b0ca2-131">'\*' 的值表示雲端服務的所有角色實例。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="b0ca2-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0ca2-132">-SubscriptionId</span></span>
<span data-ttu-id="b0ca2-133">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b0ca2-134">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ca2-135">-確認</span><span class="sxs-lookup"><span data-stu-id="b0ca2-135">-Confirm</span></span>
<span data-ttu-id="b0ca2-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0ca2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0ca2-137">-WhatIf</span></span>
<span data-ttu-id="b0ca2-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0ca2-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0ca2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0ca2-140">CommonParameters</span></span>
<span data-ttu-id="b0ca2-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0ca2-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0ca2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0ca2-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b0ca2-143">INPUTS</span></span>

### <span data-ttu-id="b0ca2-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b0ca2-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="b0ca2-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b0ca2-145">OUTPUTS</span></span>

### <span data-ttu-id="b0ca2-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b0ca2-146">System.Boolean</span></span>

## <span data-ttu-id="b0ca2-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b0ca2-147">NOTES</span></span>

<span data-ttu-id="b0ca2-148">別名</span><span class="sxs-lookup"><span data-stu-id="b0ca2-148">ALIASES</span></span>

<span data-ttu-id="b0ca2-149">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b0ca2-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b0ca2-150">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0ca2-151">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b0ca2-152">INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b0ca2-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0ca2-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b0ca2-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="b0ca2-154">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b0ca2-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0ca2-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b0ca2-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="b0ca2-156">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="b0ca2-157">`[RoleName <String>]`：角色名稱。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="b0ca2-158">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b0ca2-159">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b0ca2-160">`[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="b0ca2-161">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="b0ca2-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="b0ca2-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0ca2-162">RELATED LINKS</span></span>

