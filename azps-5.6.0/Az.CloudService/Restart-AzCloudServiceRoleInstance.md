---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
ms.openlocfilehash: f184696dbcfce35bf6e52f889d2c787214330e70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910282"
---
# <span data-ttu-id="ca202-101">Restart-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="ca202-101">Restart-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="ca202-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ca202-102">SYNOPSIS</span></span>
<span data-ttu-id="ca202-103">重新開機角色實例非同步作業會要求重新開機雲端服務中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="ca202-103">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="ca202-104">語法</span><span class="sxs-lookup"><span data-stu-id="ca202-104">SYNTAX</span></span>

### <span data-ttu-id="ca202-105">重新開機 (預設) </span><span class="sxs-lookup"><span data-stu-id="ca202-105">Restart (Default)</span></span>
```
Restart-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca202-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ca202-106">RestartViaIdentity</span></span>
```
Restart-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca202-107">描述</span><span class="sxs-lookup"><span data-stu-id="ca202-107">DESCRIPTION</span></span>
<span data-ttu-id="ca202-108">重新開機角色實例非同步作業會要求重新開機雲端服務中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="ca202-108">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="ca202-109">例子</span><span class="sxs-lookup"><span data-stu-id="ca202-109">EXAMPLES</span></span>

### <span data-ttu-id="ca202-110">範例 1：重新開機雲端服務的角色實例</span><span class="sxs-lookup"><span data-stu-id="ca202-110">Example 1: Restart role instance of a cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="ca202-111">此命令會重新開機名為 contosoCS 的ContosoFrontEnd_IN_0名稱為 ContosoCS 之資源群組的名稱為 ContosOrg 的角色實例。</span><span class="sxs-lookup"><span data-stu-id="ca202-111">This command restarts role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="ca202-112">參數</span><span class="sxs-lookup"><span data-stu-id="ca202-112">PARAMETERS</span></span>

### <span data-ttu-id="ca202-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca202-113">-AsJob</span></span>
<span data-ttu-id="ca202-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="ca202-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ca202-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="ca202-115">-CloudServiceName</span></span>
<span data-ttu-id="ca202-116">.</span><span class="sxs-lookup"><span data-stu-id="ca202-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca202-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca202-117">-DefaultProfile</span></span>
<span data-ttu-id="ca202-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca202-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca202-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca202-119">-InputObject</span></span>
<span data-ttu-id="ca202-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ca202-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca202-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ca202-121">-NoWait</span></span>
<span data-ttu-id="ca202-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="ca202-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ca202-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca202-123">-PassThru</span></span>
<span data-ttu-id="ca202-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="ca202-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ca202-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca202-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca202-126">.</span><span class="sxs-lookup"><span data-stu-id="ca202-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca202-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="ca202-127">-RoleInstanceName</span></span>
<span data-ttu-id="ca202-128">角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca202-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca202-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca202-129">-SubscriptionId</span></span>
<span data-ttu-id="ca202-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ca202-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ca202-131">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ca202-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca202-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ca202-132">-Confirm</span></span>
<span data-ttu-id="ca202-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ca202-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca202-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca202-134">-WhatIf</span></span>
<span data-ttu-id="ca202-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca202-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca202-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca202-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca202-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca202-137">CommonParameters</span></span>
<span data-ttu-id="ca202-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ca202-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca202-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca202-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca202-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ca202-140">INPUTS</span></span>

### <span data-ttu-id="ca202-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="ca202-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="ca202-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ca202-142">OUTPUTS</span></span>

### <span data-ttu-id="ca202-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca202-143">System.Boolean</span></span>

## <span data-ttu-id="ca202-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ca202-144">NOTES</span></span>

<span data-ttu-id="ca202-145">別名</span><span class="sxs-lookup"><span data-stu-id="ca202-145">ALIASES</span></span>

<span data-ttu-id="ca202-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ca202-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca202-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ca202-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca202-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ca202-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca202-149">INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ca202-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ca202-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ca202-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="ca202-151">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="ca202-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca202-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ca202-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="ca202-153">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca202-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="ca202-154">`[RoleName <String>]`：角色名稱。</span><span class="sxs-lookup"><span data-stu-id="ca202-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="ca202-155">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ca202-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ca202-156">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ca202-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ca202-157">`[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="ca202-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="ca202-158">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="ca202-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="ca202-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca202-159">RELATED LINKS</span></span>

