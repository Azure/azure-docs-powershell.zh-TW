---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/stop-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
ms.openlocfilehash: 539106e979babd1df41ca2505a2978132e825b89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916258"
---
# <span data-ttu-id="4bc02-101">Stop-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="4bc02-101">Stop-AzCloudService</span></span>

## <span data-ttu-id="4bc02-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4bc02-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc02-103">關閉雲端服務。</span><span class="sxs-lookup"><span data-stu-id="4bc02-103">Power off the cloud service.</span></span>
<span data-ttu-id="4bc02-104">請注意，資源仍然會附加，而您正被收取資源的費用。</span><span class="sxs-lookup"><span data-stu-id="4bc02-104">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="4bc02-105">語法</span><span class="sxs-lookup"><span data-stu-id="4bc02-105">SYNTAX</span></span>

### <span data-ttu-id="4bc02-106">PowerOff (預設) </span><span class="sxs-lookup"><span data-stu-id="4bc02-106">PowerOff (Default)</span></span>
```
Stop-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4bc02-107">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4bc02-107">PowerOffViaIdentity</span></span>
```
Stop-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4bc02-108">描述</span><span class="sxs-lookup"><span data-stu-id="4bc02-108">DESCRIPTION</span></span>
<span data-ttu-id="4bc02-109">關閉雲端服務。</span><span class="sxs-lookup"><span data-stu-id="4bc02-109">Power off the cloud service.</span></span>
<span data-ttu-id="4bc02-110">請注意，資源仍然會附加，而您正被收取資源的費用。</span><span class="sxs-lookup"><span data-stu-id="4bc02-110">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="4bc02-111">例子</span><span class="sxs-lookup"><span data-stu-id="4bc02-111">EXAMPLES</span></span>

### <span data-ttu-id="4bc02-112">範例 1：停止雲端服務</span><span class="sxs-lookup"><span data-stu-id="4bc02-112">Example 1: Stop cloud service</span></span>
```powershell
PS C:\> Stop-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="4bc02-113">此命令會停止所有屬於名為 ContosoCS 之雲端服務的角色實例。</span><span class="sxs-lookup"><span data-stu-id="4bc02-113">This command stops all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="4bc02-114">參數</span><span class="sxs-lookup"><span data-stu-id="4bc02-114">PARAMETERS</span></span>

### <span data-ttu-id="4bc02-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bc02-115">-AsJob</span></span>
<span data-ttu-id="4bc02-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="4bc02-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4bc02-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc02-117">-DefaultProfile</span></span>
<span data-ttu-id="4bc02-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bc02-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bc02-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bc02-119">-InputObject</span></span>
<span data-ttu-id="4bc02-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4bc02-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc02-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4bc02-121">-Name</span></span>
<span data-ttu-id="4bc02-122">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bc02-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc02-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4bc02-123">-NoWait</span></span>
<span data-ttu-id="4bc02-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="4bc02-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4bc02-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4bc02-125">-PassThru</span></span>
<span data-ttu-id="4bc02-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="4bc02-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4bc02-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc02-127">-ResourceGroupName</span></span>
<span data-ttu-id="4bc02-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bc02-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc02-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4bc02-129">-SubscriptionId</span></span>
<span data-ttu-id="4bc02-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4bc02-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4bc02-131">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4bc02-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc02-132">-確認</span><span class="sxs-lookup"><span data-stu-id="4bc02-132">-Confirm</span></span>
<span data-ttu-id="4bc02-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4bc02-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bc02-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bc02-134">-WhatIf</span></span>
<span data-ttu-id="4bc02-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4bc02-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bc02-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bc02-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bc02-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc02-137">CommonParameters</span></span>
<span data-ttu-id="4bc02-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4bc02-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc02-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bc02-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc02-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4bc02-140">INPUTS</span></span>

### <span data-ttu-id="4bc02-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="4bc02-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="4bc02-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4bc02-142">OUTPUTS</span></span>

### <span data-ttu-id="4bc02-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4bc02-143">System.Boolean</span></span>

## <span data-ttu-id="4bc02-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4bc02-144">NOTES</span></span>

<span data-ttu-id="4bc02-145">別名</span><span class="sxs-lookup"><span data-stu-id="4bc02-145">ALIASES</span></span>

<span data-ttu-id="4bc02-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4bc02-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4bc02-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4bc02-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4bc02-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4bc02-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4bc02-149">INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4bc02-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4bc02-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="4bc02-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="4bc02-151">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="4bc02-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4bc02-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="4bc02-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="4bc02-153">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bc02-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="4bc02-154">`[RoleName <String>]`：角色名稱。</span><span class="sxs-lookup"><span data-stu-id="4bc02-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="4bc02-155">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4bc02-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4bc02-156">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4bc02-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4bc02-157">`[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="4bc02-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="4bc02-158">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="4bc02-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="4bc02-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bc02-159">RELATED LINKS</span></span>

