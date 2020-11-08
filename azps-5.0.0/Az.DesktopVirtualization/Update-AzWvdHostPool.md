---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: ffb38dd20c5bc43c3d243e5a6f320fdc5d48d008
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139067"
---
# <span data-ttu-id="dbe87-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="dbe87-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="dbe87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbe87-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe87-103">更新主機池。</span><span class="sxs-lookup"><span data-stu-id="dbe87-103">Update a host pool.</span></span>

## <span data-ttu-id="dbe87-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbe87-104">SYNTAX</span></span>

### <span data-ttu-id="dbe87-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="dbe87-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dbe87-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dbe87-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dbe87-107">說明</span><span class="sxs-lookup"><span data-stu-id="dbe87-107">DESCRIPTION</span></span>
<span data-ttu-id="dbe87-108">更新主機池。</span><span class="sxs-lookup"><span data-stu-id="dbe87-108">Update a host pool.</span></span>

## <span data-ttu-id="dbe87-109">示例</span><span class="sxs-lookup"><span data-stu-id="dbe87-109">EXAMPLES</span></span>

### <span data-ttu-id="dbe87-110">範例1：依名稱更新 Windows 虛擬桌面 HostPool</span><span class="sxs-lookup"><span data-stu-id="dbe87-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Update-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -LoadBalancerType 'BreadthFirst' `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 6 `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="dbe87-111">這個命令會更新資源群組中的 Windows 虛擬桌面 HostPool。</span><span class="sxs-lookup"><span data-stu-id="dbe87-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="dbe87-112">參數</span><span class="sxs-lookup"><span data-stu-id="dbe87-112">PARAMETERS</span></span>

### <span data-ttu-id="dbe87-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="dbe87-113">-CustomRdpProperty</span></span>
<span data-ttu-id="dbe87-114">HostPool 的自訂 rdp 屬性。</span><span class="sxs-lookup"><span data-stu-id="dbe87-114">Custom rdp property of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe87-115">-DefaultProfile</span></span>
<span data-ttu-id="dbe87-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbe87-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbe87-117">-描述</span><span class="sxs-lookup"><span data-stu-id="dbe87-117">-Description</span></span>
<span data-ttu-id="dbe87-118">HostPool 的描述。</span><span class="sxs-lookup"><span data-stu-id="dbe87-118">Description of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-119">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="dbe87-119">-FriendlyName</span></span>
<span data-ttu-id="dbe87-120">HostPool 的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="dbe87-120">Friendly name of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbe87-121">-InputObject</span></span>
<span data-ttu-id="dbe87-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dbe87-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="dbe87-123">-LoadBalancerType</span></span>
<span data-ttu-id="dbe87-124">負載平衡器的類型。</span><span class="sxs-lookup"><span data-stu-id="dbe87-124">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="dbe87-125">-MaxSessionLimit</span></span>
<span data-ttu-id="dbe87-126">HostPool 的最大會話限制。</span><span class="sxs-lookup"><span data-stu-id="dbe87-126">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="dbe87-127">-Name</span></span>
<span data-ttu-id="dbe87-128">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="dbe87-128">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="dbe87-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="dbe87-130">HostPool 的 PersonalDesktopAssignment 類型。</span><span class="sxs-lookup"><span data-stu-id="dbe87-130">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="dbe87-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="dbe87-132">[優先] 應用程式群組類型的類型，預設為 [桌面應用程式] 群組</span><span class="sxs-lookup"><span data-stu-id="dbe87-132">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="dbe87-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="dbe87-134">註冊權杖的到期時間。</span><span class="sxs-lookup"><span data-stu-id="dbe87-134">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="dbe87-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="dbe87-136">重設權杖的類型。</span><span class="sxs-lookup"><span data-stu-id="dbe87-136">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbe87-137">-ResourceGroupName</span></span>
<span data-ttu-id="dbe87-138">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbe87-138">The name of the resource group.</span></span>
<span data-ttu-id="dbe87-139">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="dbe87-139">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-140">-振鈴</span><span class="sxs-lookup"><span data-stu-id="dbe87-140">-Ring</span></span>
<span data-ttu-id="dbe87-141">HostPool 的響數。</span><span class="sxs-lookup"><span data-stu-id="dbe87-141">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-142">-SsoCoNtext</span><span class="sxs-lookup"><span data-stu-id="dbe87-142">-SsoContext</span></span>
<span data-ttu-id="dbe87-143">包含 ssoCoNtext 秘密之 keyvault 的路徑。</span><span class="sxs-lookup"><span data-stu-id="dbe87-143">Path to keyvault containing ssoContext secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dbe87-144">-SubscriptionId</span></span>
<span data-ttu-id="dbe87-145">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="dbe87-145">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="dbe87-146">-Tag</span></span>
<span data-ttu-id="dbe87-147">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="dbe87-147">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe87-148">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="dbe87-148">-ValidationEnvironment</span></span>
<span data-ttu-id="dbe87-149">驗證環境。</span><span class="sxs-lookup"><span data-stu-id="dbe87-149">Is validation environment.</span></span>

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

### <span data-ttu-id="dbe87-150">-確認</span><span class="sxs-lookup"><span data-stu-id="dbe87-150">-Confirm</span></span>
<span data-ttu-id="dbe87-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dbe87-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbe87-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbe87-152">-WhatIf</span></span>
<span data-ttu-id="dbe87-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dbe87-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbe87-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbe87-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbe87-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe87-155">CommonParameters</span></span>
<span data-ttu-id="dbe87-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbe87-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe87-157">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dbe87-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe87-158">輸入</span><span class="sxs-lookup"><span data-stu-id="dbe87-158">INPUTS</span></span>

### <span data-ttu-id="dbe87-159">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="dbe87-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="dbe87-160">輸出</span><span class="sxs-lookup"><span data-stu-id="dbe87-160">OUTPUTS</span></span>

### <span data-ttu-id="dbe87-161">IHostPool （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="dbe87-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="dbe87-162">筆記</span><span class="sxs-lookup"><span data-stu-id="dbe87-162">NOTES</span></span>

<span data-ttu-id="dbe87-163">別名</span><span class="sxs-lookup"><span data-stu-id="dbe87-163">ALIASES</span></span>

<span data-ttu-id="dbe87-164">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="dbe87-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dbe87-165">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="dbe87-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dbe87-166">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="dbe87-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dbe87-167">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="dbe87-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dbe87-168">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="dbe87-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="dbe87-169">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="dbe87-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="dbe87-170">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="dbe87-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="dbe87-171">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="dbe87-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="dbe87-172">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="dbe87-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dbe87-173">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbe87-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dbe87-174">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="dbe87-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="dbe87-175">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="dbe87-175">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="dbe87-176">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dbe87-176">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dbe87-177">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="dbe87-177">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="dbe87-178">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="dbe87-178">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="dbe87-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbe87-179">RELATED LINKS</span></span>
