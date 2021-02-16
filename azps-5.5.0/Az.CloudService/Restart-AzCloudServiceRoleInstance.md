---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/restart-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 12a07367835341e86ca181f2fa419e8996a434a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141391"
---
# <span data-ttu-id="7cb6d-101">Restart-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="7cb6d-101">Restart-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="7cb6d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7cb6d-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb6d-103">重新開機角色實例非同步作業會要求在雲端服務中重新開機角色實例。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-103">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="7cb6d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7cb6d-104">SYNTAX</span></span>

### <span data-ttu-id="7cb6d-105">重新開機 (預設) </span><span class="sxs-lookup"><span data-stu-id="7cb6d-105">Restart (Default)</span></span>
```
Restart-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7cb6d-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7cb6d-106">RestartViaIdentity</span></span>
```
Restart-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7cb6d-107">說明</span><span class="sxs-lookup"><span data-stu-id="7cb6d-107">DESCRIPTION</span></span>
<span data-ttu-id="7cb6d-108">重新開機角色實例非同步作業會要求在雲端服務中重新開機角色實例。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-108">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="7cb6d-109">示例</span><span class="sxs-lookup"><span data-stu-id="7cb6d-109">EXAMPLES</span></span>

### <span data-ttu-id="7cb6d-110">範例1：重新開機雲端服務的角色實例</span><span class="sxs-lookup"><span data-stu-id="7cb6d-110">Example 1: Restart role instance of a cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="7cb6d-111">這個命令會從屬於名為 ContosOrg 的資源群組的名為 ContosoCS 的雲端服務，重新開機名為 ContosoFrontEnd_IN_0 的角色實例。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-111">This command restarts role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="7cb6d-112">參數</span><span class="sxs-lookup"><span data-stu-id="7cb6d-112">PARAMETERS</span></span>

### <span data-ttu-id="7cb6d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cb6d-113">-AsJob</span></span>
<span data-ttu-id="7cb6d-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="7cb6d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7cb6d-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="7cb6d-115">-CloudServiceName</span></span>
<span data-ttu-id="7cb6d-116">.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-116">.</span></span>

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

### <span data-ttu-id="7cb6d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb6d-117">-DefaultProfile</span></span>
<span data-ttu-id="7cb6d-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cb6d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cb6d-119">-InputObject</span></span>
<span data-ttu-id="7cb6d-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7cb6d-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7cb6d-121">-NoWait</span></span>
<span data-ttu-id="7cb6d-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="7cb6d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7cb6d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cb6d-123">-PassThru</span></span>
<span data-ttu-id="7cb6d-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="7cb6d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7cb6d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb6d-125">-ResourceGroupName</span></span>
<span data-ttu-id="7cb6d-126">.</span><span class="sxs-lookup"><span data-stu-id="7cb6d-126">.</span></span>

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

### <span data-ttu-id="7cb6d-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="7cb6d-127">-RoleInstanceName</span></span>
<span data-ttu-id="7cb6d-128">角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-128">Name of the role instance.</span></span>

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

### <span data-ttu-id="7cb6d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cb6d-129">-SubscriptionId</span></span>
<span data-ttu-id="7cb6d-130">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7cb6d-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7cb6d-132">-確認</span><span class="sxs-lookup"><span data-stu-id="7cb6d-132">-Confirm</span></span>
<span data-ttu-id="7cb6d-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cb6d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cb6d-134">-WhatIf</span></span>
<span data-ttu-id="7cb6d-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cb6d-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cb6d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb6d-137">CommonParameters</span></span>
<span data-ttu-id="7cb6d-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb6d-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb6d-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7cb6d-140">INPUTS</span></span>

### <span data-ttu-id="7cb6d-141">ICloudServiceIdentity （CloudService）的</span><span class="sxs-lookup"><span data-stu-id="7cb6d-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="7cb6d-142">輸出</span><span class="sxs-lookup"><span data-stu-id="7cb6d-142">OUTPUTS</span></span>

### <span data-ttu-id="7cb6d-143">System.object</span><span class="sxs-lookup"><span data-stu-id="7cb6d-143">System.Boolean</span></span>

## <span data-ttu-id="7cb6d-144">筆記</span><span class="sxs-lookup"><span data-stu-id="7cb6d-144">NOTES</span></span>

<span data-ttu-id="7cb6d-145">別名</span><span class="sxs-lookup"><span data-stu-id="7cb6d-145">ALIASES</span></span>

<span data-ttu-id="7cb6d-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="7cb6d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7cb6d-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7cb6d-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7cb6d-149">INPUTOBJECT <ICloudServiceIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="7cb6d-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7cb6d-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="7cb6d-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="7cb6d-151">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="7cb6d-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7cb6d-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="7cb6d-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="7cb6d-153">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="7cb6d-154">`[RoleName <String>]`：角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="7cb6d-155">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7cb6d-156">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7cb6d-157">`[UpdateDomain <Int32?>]`：指定識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="7cb6d-158">更新網域是以零為基礎的索引來標識：第一個更新網域的識別碼為0，第二個是 ID 為1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="7cb6d-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="7cb6d-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cb6d-159">RELATED LINKS</span></span>

