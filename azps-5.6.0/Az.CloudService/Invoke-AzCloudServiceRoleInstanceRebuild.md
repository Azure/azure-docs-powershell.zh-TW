---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
ms.openlocfilehash: 1f204b40bcf6cbd81449a6478d9d7d4e3f7d432d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916262"
---
# <span data-ttu-id="6a0c4-101">Invoke-AzCloudServiceRoleInstanceRebuild</span><span class="sxs-lookup"><span data-stu-id="6a0c4-101">Invoke-AzCloudServiceRoleInstanceRebuild</span></span>

## <span data-ttu-id="6a0c4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6a0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="6a0c4-103">重建角色實例非同步作業會重新安裝作業系統上的網頁角色或員工角色實例，並初始化他們所使用的儲存資源。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-103">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="6a0c4-104">如果您不想初始化儲存資源，可以使用重新映射角色實例。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-104">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="6a0c4-105">語法</span><span class="sxs-lookup"><span data-stu-id="6a0c4-105">SYNTAX</span></span>

### <span data-ttu-id="6a0c4-106">重建 (預設) </span><span class="sxs-lookup"><span data-stu-id="6a0c4-106">Rebuild (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6a0c4-107">RebuildViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6a0c4-107">RebuildViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a0c4-108">描述</span><span class="sxs-lookup"><span data-stu-id="6a0c4-108">DESCRIPTION</span></span>
<span data-ttu-id="6a0c4-109">重建角色實例非同步作業會重新安裝作業系統上的網頁角色或員工角色實例，並初始化他們所使用的儲存資源。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-109">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="6a0c4-110">如果您不想初始化儲存資源，可以使用重新映射角色實例。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-110">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="6a0c4-111">例子</span><span class="sxs-lookup"><span data-stu-id="6a0c4-111">EXAMPLES</span></span>

### <span data-ttu-id="6a0c4-112">範例 1：重建雲端服務的角色實例</span><span class="sxs-lookup"><span data-stu-id="6a0c4-112">Example 1: Rebuild role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="6a0c4-113">此命令會重新製作名稱為 contosoCS ContosoFrontEnd_IN_0名為 ContosOrg 之資源群組之雲端服務的名稱角色實例。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-113">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="6a0c4-114">參數</span><span class="sxs-lookup"><span data-stu-id="6a0c4-114">PARAMETERS</span></span>

### <span data-ttu-id="6a0c4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a0c4-115">-AsJob</span></span>
<span data-ttu-id="6a0c4-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="6a0c4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6a0c4-117">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="6a0c4-117">-CloudServiceName</span></span>
<span data-ttu-id="6a0c4-118">.</span><span class="sxs-lookup"><span data-stu-id="6a0c4-118">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a0c4-119">-DefaultProfile</span></span>
<span data-ttu-id="6a0c4-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a0c4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a0c4-121">-InputObject</span></span>
<span data-ttu-id="6a0c4-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c4-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6a0c4-123">-NoWait</span></span>
<span data-ttu-id="6a0c4-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="6a0c4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6a0c4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a0c4-125">-PassThru</span></span>
<span data-ttu-id="6a0c4-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="6a0c4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6a0c4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a0c4-127">-ResourceGroupName</span></span>
<span data-ttu-id="6a0c4-128">.</span><span class="sxs-lookup"><span data-stu-id="6a0c4-128">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c4-129">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="6a0c4-129">-RoleInstanceName</span></span>
<span data-ttu-id="6a0c4-130">角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-130">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c4-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a0c4-131">-SubscriptionId</span></span>
<span data-ttu-id="6a0c4-132">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6a0c4-133">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a0c4-134">-確認</span><span class="sxs-lookup"><span data-stu-id="6a0c4-134">-Confirm</span></span>
<span data-ttu-id="6a0c4-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a0c4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a0c4-136">-WhatIf</span></span>
<span data-ttu-id="6a0c4-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a0c4-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a0c4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a0c4-139">CommonParameters</span></span>
<span data-ttu-id="6a0c4-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a0c4-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a0c4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a0c4-142">輸入</span><span class="sxs-lookup"><span data-stu-id="6a0c4-142">INPUTS</span></span>

### <span data-ttu-id="6a0c4-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="6a0c4-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="6a0c4-144">輸出</span><span class="sxs-lookup"><span data-stu-id="6a0c4-144">OUTPUTS</span></span>

### <span data-ttu-id="6a0c4-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a0c4-145">System.Boolean</span></span>

## <span data-ttu-id="6a0c4-146">筆記</span><span class="sxs-lookup"><span data-stu-id="6a0c4-146">NOTES</span></span>

<span data-ttu-id="6a0c4-147">別名</span><span class="sxs-lookup"><span data-stu-id="6a0c4-147">ALIASES</span></span>

<span data-ttu-id="6a0c4-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6a0c4-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a0c4-149">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a0c4-150">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a0c4-151">INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6a0c4-151">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a0c4-152">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="6a0c4-152">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="6a0c4-153">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="6a0c4-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a0c4-154">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="6a0c4-154">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="6a0c4-155">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-155">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="6a0c4-156">`[RoleName <String>]`：角色名稱。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-156">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="6a0c4-157">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-157">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6a0c4-158">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6a0c4-159">`[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-159">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="6a0c4-160">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="6a0c4-160">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="6a0c4-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a0c4-161">RELATED LINKS</span></span>

