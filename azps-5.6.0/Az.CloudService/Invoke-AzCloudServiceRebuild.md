---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudservicerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
ms.openlocfilehash: aa9f128021aba1dff08f1c8757c8135676ddc003
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907905"
---
# <span data-ttu-id="5d90a-101">Invoke-AzCloudServiceRebuild</span><span class="sxs-lookup"><span data-stu-id="5d90a-101">Invoke-AzCloudServiceRebuild</span></span>

## <span data-ttu-id="5d90a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5d90a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d90a-103">重建角色實例會以 Web 角色或員工角色實例重新安裝作業系統，並初始化他們所使用的儲存資源。</span><span class="sxs-lookup"><span data-stu-id="5d90a-103">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="5d90a-104">如果您不想初始化儲存資源，可以使用重新映射角色實例。</span><span class="sxs-lookup"><span data-stu-id="5d90a-104">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="5d90a-105">語法</span><span class="sxs-lookup"><span data-stu-id="5d90a-105">SYNTAX</span></span>

### <span data-ttu-id="5d90a-106">RebuildExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="5d90a-106">RebuildExpanded (Default)</span></span>
```
Invoke-AzCloudServiceRebuild -CloudServiceName <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5d90a-107">RebuildViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5d90a-107">RebuildViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceRebuild -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5d90a-108">描述</span><span class="sxs-lookup"><span data-stu-id="5d90a-108">DESCRIPTION</span></span>
<span data-ttu-id="5d90a-109">重建角色實例會以 Web 角色或員工角色實例重新安裝作業系統，並初始化他們所使用的儲存資源。</span><span class="sxs-lookup"><span data-stu-id="5d90a-109">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="5d90a-110">如果您不想初始化儲存資源，可以使用重新映射角色實例。</span><span class="sxs-lookup"><span data-stu-id="5d90a-110">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="5d90a-111">例子</span><span class="sxs-lookup"><span data-stu-id="5d90a-111">EXAMPLES</span></span>

### <span data-ttu-id="5d90a-112">範例 1：重建雲端服務的角色實例</span><span class="sxs-lookup"><span data-stu-id="5d90a-112">Example 1: Rebuild role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="5d90a-113">此命令會重建 2 個角色實例ContosoFrontEnd_IN_0，ContosoBackEnd_IN_1名為 ContosoCS 的雲端服務，這些角色實例屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5d90a-113">This command rebuilds 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="5d90a-114">範例 2：重建雲端服務的所有角色</span><span class="sxs-lookup"><span data-stu-id="5d90a-114">Example 2: Rebuild all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="5d90a-115">此命令會重建名為 ContosoCS 的所有雲端服務角色實例，這些角色實例屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5d90a-115">This command rebuilds all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="5d90a-116">參數</span><span class="sxs-lookup"><span data-stu-id="5d90a-116">PARAMETERS</span></span>

### <span data-ttu-id="5d90a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d90a-117">-AsJob</span></span>
<span data-ttu-id="5d90a-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="5d90a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="5d90a-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="5d90a-119">-CloudServiceName</span></span>
<span data-ttu-id="5d90a-120">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d90a-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d90a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d90a-121">-DefaultProfile</span></span>
<span data-ttu-id="5d90a-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d90a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d90a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d90a-123">-InputObject</span></span>
<span data-ttu-id="5d90a-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5d90a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d90a-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5d90a-125">-NoWait</span></span>
<span data-ttu-id="5d90a-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="5d90a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5d90a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d90a-127">-PassThru</span></span>
<span data-ttu-id="5d90a-128">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="5d90a-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5d90a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d90a-129">-ResourceGroupName</span></span>
<span data-ttu-id="5d90a-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d90a-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d90a-131">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="5d90a-131">-RoleInstance</span></span>
<span data-ttu-id="5d90a-132">雲端服務角色實例名稱清單。</span><span class="sxs-lookup"><span data-stu-id="5d90a-132">List of cloud service role instance names.</span></span>
<span data-ttu-id="5d90a-133">'\*' 的值表示雲端服務的所有角色實例。</span><span class="sxs-lookup"><span data-stu-id="5d90a-133">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="5d90a-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d90a-134">-SubscriptionId</span></span>
<span data-ttu-id="5d90a-135">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5d90a-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d90a-136">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5d90a-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d90a-137">-確認</span><span class="sxs-lookup"><span data-stu-id="5d90a-137">-Confirm</span></span>
<span data-ttu-id="5d90a-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5d90a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d90a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d90a-139">-WhatIf</span></span>
<span data-ttu-id="5d90a-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5d90a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d90a-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d90a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d90a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d90a-142">CommonParameters</span></span>
<span data-ttu-id="5d90a-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5d90a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d90a-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d90a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d90a-145">輸入</span><span class="sxs-lookup"><span data-stu-id="5d90a-145">INPUTS</span></span>

### <span data-ttu-id="5d90a-146">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="5d90a-146">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="5d90a-147">輸出</span><span class="sxs-lookup"><span data-stu-id="5d90a-147">OUTPUTS</span></span>

### <span data-ttu-id="5d90a-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d90a-148">System.Boolean</span></span>

## <span data-ttu-id="5d90a-149">筆記</span><span class="sxs-lookup"><span data-stu-id="5d90a-149">NOTES</span></span>

<span data-ttu-id="5d90a-150">別名</span><span class="sxs-lookup"><span data-stu-id="5d90a-150">ALIASES</span></span>

<span data-ttu-id="5d90a-151">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5d90a-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5d90a-152">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5d90a-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d90a-153">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5d90a-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5d90a-154">INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5d90a-154">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d90a-155">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="5d90a-155">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="5d90a-156">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="5d90a-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d90a-157">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="5d90a-157">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="5d90a-158">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d90a-158">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="5d90a-159">`[RoleName <String>]`：角色名稱。</span><span class="sxs-lookup"><span data-stu-id="5d90a-159">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="5d90a-160">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5d90a-160">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5d90a-161">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5d90a-161">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5d90a-162">`[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="5d90a-162">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="5d90a-163">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="5d90a-163">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="5d90a-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d90a-164">RELATED LINKS</span></span>

