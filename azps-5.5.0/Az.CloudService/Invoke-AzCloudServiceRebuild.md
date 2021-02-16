---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudservicerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
ms.openlocfilehash: 1efeb45704898588c7ba8f08148f88d0eaf3e5c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138735"
---
# <span data-ttu-id="9cb48-101">Invoke-AzCloudServiceRebuild</span><span class="sxs-lookup"><span data-stu-id="9cb48-101">Invoke-AzCloudServiceRebuild</span></span>

## <span data-ttu-id="9cb48-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9cb48-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb48-103">重建角色實例會在網頁角色或 worker 角色的實例上重新安裝作業系統，並初始化它們所使用的儲存空間資源。</span><span class="sxs-lookup"><span data-stu-id="9cb48-103">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="9cb48-104">如果您不想要初始化儲存空間資源，您可以使用重新鏡像角色實例。</span><span class="sxs-lookup"><span data-stu-id="9cb48-104">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="9cb48-105">句法</span><span class="sxs-lookup"><span data-stu-id="9cb48-105">SYNTAX</span></span>

### <span data-ttu-id="9cb48-106">RebuildExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="9cb48-106">RebuildExpanded (Default)</span></span>
```
Invoke-AzCloudServiceRebuild -CloudServiceName <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9cb48-107">RebuildViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9cb48-107">RebuildViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceRebuild -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9cb48-108">說明</span><span class="sxs-lookup"><span data-stu-id="9cb48-108">DESCRIPTION</span></span>
<span data-ttu-id="9cb48-109">重建角色實例會在網頁角色或 worker 角色的實例上重新安裝作業系統，並初始化它們所使用的儲存空間資源。</span><span class="sxs-lookup"><span data-stu-id="9cb48-109">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="9cb48-110">如果您不想要初始化儲存空間資源，您可以使用重新鏡像角色實例。</span><span class="sxs-lookup"><span data-stu-id="9cb48-110">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="9cb48-111">示例</span><span class="sxs-lookup"><span data-stu-id="9cb48-111">EXAMPLES</span></span>

### <span data-ttu-id="9cb48-112">範例1：重建雲端服務的角色實例</span><span class="sxs-lookup"><span data-stu-id="9cb48-112">Example 1: Rebuild role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="9cb48-113">這個命令會從屬於名為 ContosOrg 之資源群組的名為 ContosoCS 的雲端服務 ContosoFrontEnd_IN_0 和 ContosoBackEnd_IN_1，重新構建2個角色實例。</span><span class="sxs-lookup"><span data-stu-id="9cb48-113">This command rebuilds 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="9cb48-114">範例2：重建雲端服務的所有角色</span><span class="sxs-lookup"><span data-stu-id="9cb48-114">Example 2: Rebuild all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="9cb48-115">這個命令會重建屬於名為 ContosOrg 之資源群組的所有名為 ContosoCS 的雲端服務角色實例。</span><span class="sxs-lookup"><span data-stu-id="9cb48-115">This command rebuilds all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="9cb48-116">參數</span><span class="sxs-lookup"><span data-stu-id="9cb48-116">PARAMETERS</span></span>

### <span data-ttu-id="9cb48-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cb48-117">-AsJob</span></span>
<span data-ttu-id="9cb48-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="9cb48-118">Run the command as a job</span></span>

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

### <span data-ttu-id="9cb48-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="9cb48-119">-CloudServiceName</span></span>
<span data-ttu-id="9cb48-120">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cb48-120">Name of the cloud service.</span></span>

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

### <span data-ttu-id="9cb48-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb48-121">-DefaultProfile</span></span>
<span data-ttu-id="9cb48-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9cb48-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb48-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cb48-123">-InputObject</span></span>
<span data-ttu-id="9cb48-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9cb48-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9cb48-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9cb48-125">-NoWait</span></span>
<span data-ttu-id="9cb48-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="9cb48-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9cb48-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cb48-127">-PassThru</span></span>
<span data-ttu-id="9cb48-128">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="9cb48-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9cb48-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb48-129">-ResourceGroupName</span></span>
<span data-ttu-id="9cb48-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cb48-130">Name of the resource group.</span></span>

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

### <span data-ttu-id="9cb48-131">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="9cb48-131">-RoleInstance</span></span>
<span data-ttu-id="9cb48-132">雲端服務角色實例名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="9cb48-132">List of cloud service role instance names.</span></span>
<span data-ttu-id="9cb48-133">"\*" 的值會代表雲端服務的所有角色實例。</span><span class="sxs-lookup"><span data-stu-id="9cb48-133">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="9cb48-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9cb48-134">-SubscriptionId</span></span>
<span data-ttu-id="9cb48-135">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9cb48-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9cb48-136">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9cb48-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9cb48-137">-確認</span><span class="sxs-lookup"><span data-stu-id="9cb48-137">-Confirm</span></span>
<span data-ttu-id="9cb48-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9cb48-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb48-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb48-139">-WhatIf</span></span>
<span data-ttu-id="9cb48-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9cb48-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cb48-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9cb48-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb48-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb48-142">CommonParameters</span></span>
<span data-ttu-id="9cb48-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9cb48-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb48-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9cb48-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb48-145">輸入</span><span class="sxs-lookup"><span data-stu-id="9cb48-145">INPUTS</span></span>

### <span data-ttu-id="9cb48-146">ICloudServiceIdentity （CloudService）的</span><span class="sxs-lookup"><span data-stu-id="9cb48-146">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="9cb48-147">輸出</span><span class="sxs-lookup"><span data-stu-id="9cb48-147">OUTPUTS</span></span>

### <span data-ttu-id="9cb48-148">System.object</span><span class="sxs-lookup"><span data-stu-id="9cb48-148">System.Boolean</span></span>

## <span data-ttu-id="9cb48-149">筆記</span><span class="sxs-lookup"><span data-stu-id="9cb48-149">NOTES</span></span>

<span data-ttu-id="9cb48-150">別名</span><span class="sxs-lookup"><span data-stu-id="9cb48-150">ALIASES</span></span>

<span data-ttu-id="9cb48-151">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9cb48-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9cb48-152">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9cb48-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9cb48-153">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9cb48-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9cb48-154">INPUTOBJECT <ICloudServiceIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9cb48-154">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9cb48-155">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="9cb48-155">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="9cb48-156">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="9cb48-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9cb48-157">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="9cb48-157">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="9cb48-158">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cb48-158">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="9cb48-159">`[RoleName <String>]`：角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cb48-159">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="9cb48-160">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9cb48-160">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9cb48-161">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9cb48-161">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9cb48-162">`[UpdateDomain <Int32?>]`：指定識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="9cb48-162">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="9cb48-163">更新網域是以零為基礎的索引來標識：第一個更新網域的識別碼為0，第二個是 ID 為1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="9cb48-163">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="9cb48-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cb48-164">RELATED LINKS</span></span>

