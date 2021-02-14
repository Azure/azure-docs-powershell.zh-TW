---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/restart-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
ms.openlocfilehash: c31aed5422e9b142690875de242462af64acf799
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129903"
---
# <span data-ttu-id="008f7-101">Restart-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="008f7-101">Restart-AzCloudService</span></span>

## <span data-ttu-id="008f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="008f7-102">SYNOPSIS</span></span>
<span data-ttu-id="008f7-103">重新開機雲端服務中的一個或多個角色實例。</span><span class="sxs-lookup"><span data-stu-id="008f7-103">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="008f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="008f7-104">SYNTAX</span></span>

### <span data-ttu-id="008f7-105">RestartExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="008f7-105">RestartExpanded (Default)</span></span>
```
Restart-AzCloudService -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="008f7-106">RestartViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="008f7-106">RestartViaIdentityExpanded</span></span>
```
Restart-AzCloudService -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="008f7-107">說明</span><span class="sxs-lookup"><span data-stu-id="008f7-107">DESCRIPTION</span></span>
<span data-ttu-id="008f7-108">重新開機雲端服務中的一個或多個角色實例。</span><span class="sxs-lookup"><span data-stu-id="008f7-108">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="008f7-109">示例</span><span class="sxs-lookup"><span data-stu-id="008f7-109">EXAMPLES</span></span>

### <span data-ttu-id="008f7-110">範例1：重新開機雲端服務的角色實例</span><span class="sxs-lookup"><span data-stu-id="008f7-110">Example 1: Restart role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="008f7-111">這個命令會重新開機2個角色實例 ContosoFrontEnd_IN_0 並 ContosoBackEnd_IN_1 屬於名為 ContosOrg 的資源群組的雲端服務。</span><span class="sxs-lookup"><span data-stu-id="008f7-111">This command restarts 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="008f7-112">範例2：重新開機雲端服務的所有角色</span><span class="sxs-lookup"><span data-stu-id="008f7-112">Example 2: Restart all roles of cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="008f7-113">這個命令會重新開機屬於名為 ContosOrg 之資源群組的所有名為 ContosoCS 的雲端服務角色實例。</span><span class="sxs-lookup"><span data-stu-id="008f7-113">This command restarts all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="008f7-114">參數</span><span class="sxs-lookup"><span data-stu-id="008f7-114">PARAMETERS</span></span>

### <span data-ttu-id="008f7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="008f7-115">-AsJob</span></span>
<span data-ttu-id="008f7-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="008f7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="008f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008f7-117">-DefaultProfile</span></span>
<span data-ttu-id="008f7-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="008f7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="008f7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="008f7-119">-InputObject</span></span>
<span data-ttu-id="008f7-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="008f7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="008f7-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="008f7-121">-Name</span></span>
<span data-ttu-id="008f7-122">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="008f7-122">Name of the cloud service.</span></span>

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

### <span data-ttu-id="008f7-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="008f7-123">-NoWait</span></span>
<span data-ttu-id="008f7-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="008f7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="008f7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="008f7-125">-PassThru</span></span>
<span data-ttu-id="008f7-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="008f7-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="008f7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="008f7-127">-ResourceGroupName</span></span>
<span data-ttu-id="008f7-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="008f7-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="008f7-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="008f7-129">-RoleInstance</span></span>
<span data-ttu-id="008f7-130">雲端服務角色實例名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="008f7-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="008f7-131">"\*" 的值會代表雲端服務的所有角色實例。</span><span class="sxs-lookup"><span data-stu-id="008f7-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="008f7-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="008f7-132">-SubscriptionId</span></span>
<span data-ttu-id="008f7-133">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="008f7-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="008f7-134">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="008f7-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="008f7-135">-確認</span><span class="sxs-lookup"><span data-stu-id="008f7-135">-Confirm</span></span>
<span data-ttu-id="008f7-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="008f7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="008f7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="008f7-137">-WhatIf</span></span>
<span data-ttu-id="008f7-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="008f7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="008f7-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="008f7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="008f7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008f7-140">CommonParameters</span></span>
<span data-ttu-id="008f7-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="008f7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008f7-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="008f7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008f7-143">輸入</span><span class="sxs-lookup"><span data-stu-id="008f7-143">INPUTS</span></span>

### <span data-ttu-id="008f7-144">ICloudServiceIdentity （CloudService）的</span><span class="sxs-lookup"><span data-stu-id="008f7-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="008f7-145">輸出</span><span class="sxs-lookup"><span data-stu-id="008f7-145">OUTPUTS</span></span>

### <span data-ttu-id="008f7-146">System.object</span><span class="sxs-lookup"><span data-stu-id="008f7-146">System.Boolean</span></span>

## <span data-ttu-id="008f7-147">筆記</span><span class="sxs-lookup"><span data-stu-id="008f7-147">NOTES</span></span>

<span data-ttu-id="008f7-148">別名</span><span class="sxs-lookup"><span data-stu-id="008f7-148">ALIASES</span></span>

<span data-ttu-id="008f7-149">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="008f7-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="008f7-150">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="008f7-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="008f7-151">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="008f7-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="008f7-152">INPUTOBJECT <ICloudServiceIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="008f7-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="008f7-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="008f7-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="008f7-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="008f7-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="008f7-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="008f7-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="008f7-156">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="008f7-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="008f7-157">`[RoleName <String>]`：角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="008f7-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="008f7-158">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="008f7-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="008f7-159">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="008f7-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="008f7-160">`[UpdateDomain <Int32?>]`：指定識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="008f7-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="008f7-161">更新網域是以零為基礎的索引來標識：第一個更新網域的識別碼為0，第二個是 ID 為1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="008f7-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="008f7-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="008f7-162">RELATED LINKS</span></span>

