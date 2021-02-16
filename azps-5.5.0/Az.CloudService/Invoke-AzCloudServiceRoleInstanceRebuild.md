---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
ms.openlocfilehash: d998e29fc254b1bf507ab7d7732bc3bdcf68f54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127922"
---
# <span data-ttu-id="21d50-101">Invoke-AzCloudServiceRoleInstanceRebuild</span><span class="sxs-lookup"><span data-stu-id="21d50-101">Invoke-AzCloudServiceRoleInstanceRebuild</span></span>

## <span data-ttu-id="21d50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21d50-102">SYNOPSIS</span></span>
<span data-ttu-id="21d50-103">[重建角色實例] 非同步作業會在網頁角色或輔助角色的實例上重新安裝作業系統，並初始化它們所使用的儲存空間資源。</span><span class="sxs-lookup"><span data-stu-id="21d50-103">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="21d50-104">如果您不想要初始化儲存空間資源，您可以使用重新鏡像角色實例。</span><span class="sxs-lookup"><span data-stu-id="21d50-104">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="21d50-105">句法</span><span class="sxs-lookup"><span data-stu-id="21d50-105">SYNTAX</span></span>

### <span data-ttu-id="21d50-106">重建 (預設) </span><span class="sxs-lookup"><span data-stu-id="21d50-106">Rebuild (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="21d50-107">RebuildViaIdentity</span><span class="sxs-lookup"><span data-stu-id="21d50-107">RebuildViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="21d50-108">說明</span><span class="sxs-lookup"><span data-stu-id="21d50-108">DESCRIPTION</span></span>
<span data-ttu-id="21d50-109">[重建角色實例] 非同步作業會在網頁角色或輔助角色的實例上重新安裝作業系統，並初始化它們所使用的儲存空間資源。</span><span class="sxs-lookup"><span data-stu-id="21d50-109">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="21d50-110">如果您不想要初始化儲存空間資源，您可以使用重新鏡像角色實例。</span><span class="sxs-lookup"><span data-stu-id="21d50-110">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="21d50-111">示例</span><span class="sxs-lookup"><span data-stu-id="21d50-111">EXAMPLES</span></span>

### <span data-ttu-id="21d50-112">範例1：重新建立雲端服務的角色實例</span><span class="sxs-lookup"><span data-stu-id="21d50-112">Example 1: Rebuild role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="21d50-113">這個命令 reimages 名為 ContosoCS 的雲端服務 ContosoFrontEnd_IN_0 角色實例，該名稱屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="21d50-113">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="21d50-114">參數</span><span class="sxs-lookup"><span data-stu-id="21d50-114">PARAMETERS</span></span>

### <span data-ttu-id="21d50-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21d50-115">-AsJob</span></span>
<span data-ttu-id="21d50-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="21d50-116">Run the command as a job</span></span>

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

### <span data-ttu-id="21d50-117">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="21d50-117">-CloudServiceName</span></span>
<span data-ttu-id="21d50-118">.</span><span class="sxs-lookup"><span data-stu-id="21d50-118">.</span></span>

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

### <span data-ttu-id="21d50-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d50-119">-DefaultProfile</span></span>
<span data-ttu-id="21d50-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21d50-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21d50-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21d50-121">-InputObject</span></span>
<span data-ttu-id="21d50-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="21d50-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="21d50-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="21d50-123">-NoWait</span></span>
<span data-ttu-id="21d50-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="21d50-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="21d50-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21d50-125">-PassThru</span></span>
<span data-ttu-id="21d50-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="21d50-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="21d50-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d50-127">-ResourceGroupName</span></span>
<span data-ttu-id="21d50-128">.</span><span class="sxs-lookup"><span data-stu-id="21d50-128">.</span></span>

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

### <span data-ttu-id="21d50-129">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="21d50-129">-RoleInstanceName</span></span>
<span data-ttu-id="21d50-130">角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="21d50-130">Name of the role instance.</span></span>

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

### <span data-ttu-id="21d50-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="21d50-131">-SubscriptionId</span></span>
<span data-ttu-id="21d50-132">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="21d50-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="21d50-133">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="21d50-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="21d50-134">-確認</span><span class="sxs-lookup"><span data-stu-id="21d50-134">-Confirm</span></span>
<span data-ttu-id="21d50-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21d50-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21d50-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21d50-136">-WhatIf</span></span>
<span data-ttu-id="21d50-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21d50-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21d50-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21d50-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21d50-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d50-139">CommonParameters</span></span>
<span data-ttu-id="21d50-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21d50-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d50-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="21d50-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d50-142">輸入</span><span class="sxs-lookup"><span data-stu-id="21d50-142">INPUTS</span></span>

### <span data-ttu-id="21d50-143">ICloudServiceIdentity （CloudService）的</span><span class="sxs-lookup"><span data-stu-id="21d50-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="21d50-144">輸出</span><span class="sxs-lookup"><span data-stu-id="21d50-144">OUTPUTS</span></span>

### <span data-ttu-id="21d50-145">System.object</span><span class="sxs-lookup"><span data-stu-id="21d50-145">System.Boolean</span></span>

## <span data-ttu-id="21d50-146">筆記</span><span class="sxs-lookup"><span data-stu-id="21d50-146">NOTES</span></span>

<span data-ttu-id="21d50-147">別名</span><span class="sxs-lookup"><span data-stu-id="21d50-147">ALIASES</span></span>

<span data-ttu-id="21d50-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="21d50-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="21d50-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="21d50-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="21d50-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="21d50-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="21d50-151">INPUTOBJECT <ICloudServiceIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="21d50-151">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="21d50-152">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="21d50-152">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="21d50-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="21d50-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="21d50-154">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="21d50-154">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="21d50-155">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="21d50-155">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="21d50-156">`[RoleName <String>]`：角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="21d50-156">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="21d50-157">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="21d50-157">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="21d50-158">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="21d50-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="21d50-159">`[UpdateDomain <Int32?>]`：指定識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="21d50-159">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="21d50-160">更新網域是以零為基礎的索引來標識：第一個更新網域的識別碼為0，第二個是 ID 為1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="21d50-160">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="21d50-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="21d50-161">RELATED LINKS</span></span>

