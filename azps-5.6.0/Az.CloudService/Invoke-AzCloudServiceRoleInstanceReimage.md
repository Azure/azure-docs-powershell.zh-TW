---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
ms.openlocfilehash: 644912b841475c660852adcda2cba320d9026618
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905186"
---
# <span data-ttu-id="c4ee4-101">Invoke-AzCloudServiceRoleInstanceReimage</span><span class="sxs-lookup"><span data-stu-id="c4ee4-101">Invoke-AzCloudServiceRoleInstanceReimage</span></span>

## <span data-ttu-id="c4ee4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c4ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ee4-103">重新映射角色實例非同步作業會以 Web 角色或員工角色實例重新安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-103">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="c4ee4-104">語法</span><span class="sxs-lookup"><span data-stu-id="c4ee4-104">SYNTAX</span></span>

### <span data-ttu-id="c4ee4-105">重新映射 (預設) </span><span class="sxs-lookup"><span data-stu-id="c4ee4-105">Reimage (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4ee4-106">ReimageViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4ee4-106">ReimageViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4ee4-107">描述</span><span class="sxs-lookup"><span data-stu-id="c4ee4-107">DESCRIPTION</span></span>
<span data-ttu-id="c4ee4-108">重新映射角色實例非同步作業會以 Web 角色或員工角色實例重新安裝作業系統。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-108">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="c4ee4-109">例子</span><span class="sxs-lookup"><span data-stu-id="c4ee4-109">EXAMPLES</span></span>

### <span data-ttu-id="c4ee4-110">範例 1：雲端服務的重新映射角色實例</span><span class="sxs-lookup"><span data-stu-id="c4ee4-110">Example 1: Reimage role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="c4ee4-111">此命令會重新製作名稱為 contosoCS ContosoFrontEnd_IN_0名為 ContosOrg 之資源群組之雲端服務的名稱角色實例。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-111">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="c4ee4-112">參數</span><span class="sxs-lookup"><span data-stu-id="c4ee4-112">PARAMETERS</span></span>

### <span data-ttu-id="c4ee4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4ee4-113">-AsJob</span></span>
<span data-ttu-id="c4ee4-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="c4ee4-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c4ee4-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="c4ee4-115">-CloudServiceName</span></span>
<span data-ttu-id="c4ee4-116">.</span><span class="sxs-lookup"><span data-stu-id="c4ee4-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ee4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ee4-117">-DefaultProfile</span></span>
<span data-ttu-id="c4ee4-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4ee4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4ee4-119">-InputObject</span></span>
<span data-ttu-id="c4ee4-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ee4-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c4ee4-121">-NoWait</span></span>
<span data-ttu-id="c4ee4-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="c4ee4-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c4ee4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4ee4-123">-PassThru</span></span>
<span data-ttu-id="c4ee4-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="c4ee4-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c4ee4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ee4-125">-ResourceGroupName</span></span>
<span data-ttu-id="c4ee4-126">.</span><span class="sxs-lookup"><span data-stu-id="c4ee4-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ee4-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="c4ee4-127">-RoleInstanceName</span></span>
<span data-ttu-id="c4ee4-128">角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ee4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4ee4-129">-SubscriptionId</span></span>
<span data-ttu-id="c4ee4-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c4ee4-131">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ee4-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c4ee4-132">-Confirm</span></span>
<span data-ttu-id="c4ee4-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4ee4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4ee4-134">-WhatIf</span></span>
<span data-ttu-id="c4ee4-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4ee4-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4ee4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ee4-137">CommonParameters</span></span>
<span data-ttu-id="c4ee4-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ee4-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4ee4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ee4-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c4ee4-140">INPUTS</span></span>

### <span data-ttu-id="c4ee4-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="c4ee4-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="c4ee4-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c4ee4-142">OUTPUTS</span></span>

### <span data-ttu-id="c4ee4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4ee4-143">System.Boolean</span></span>

## <span data-ttu-id="c4ee4-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c4ee4-144">NOTES</span></span>

<span data-ttu-id="c4ee4-145">別名</span><span class="sxs-lookup"><span data-stu-id="c4ee4-145">ALIASES</span></span>

<span data-ttu-id="c4ee4-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c4ee4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4ee4-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4ee4-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4ee4-149">INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c4ee4-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4ee4-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="c4ee4-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="c4ee4-151">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="c4ee4-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4ee4-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="c4ee4-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="c4ee4-153">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="c4ee4-154">`[RoleName <String>]`：角色名稱。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="c4ee4-155">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c4ee4-156">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c4ee4-157">`[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="c4ee4-158">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="c4ee4-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="c4ee4-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4ee4-159">RELATED LINKS</span></span>

