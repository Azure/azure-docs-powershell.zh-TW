---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: 9e8599edaa1a1c19d5b0629d290402c792cf2563
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909814"
---
# <span data-ttu-id="b4bb6-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="b4bb6-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="b4bb6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b4bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bb6-103">更新工作階段主機。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-103">Update a session host.</span></span>

## <span data-ttu-id="b4bb6-104">語法</span><span class="sxs-lookup"><span data-stu-id="b4bb6-104">SYNTAX</span></span>

### <span data-ttu-id="b4bb6-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="b4bb6-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b4bb6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b4bb6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b4bb6-107">描述</span><span class="sxs-lookup"><span data-stu-id="b4bb6-107">DESCRIPTION</span></span>
<span data-ttu-id="b4bb6-108">更新工作階段主機。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-108">Update a session host.</span></span>

## <span data-ttu-id="b4bb6-109">例子</span><span class="sxs-lookup"><span data-stu-id="b4bb6-109">EXAMPLES</span></span>

### <span data-ttu-id="b4bb6-110">範例 1：根據名稱更新 Windows 虛擬桌面工作階段主機</span><span class="sxs-lookup"><span data-stu-id="b4bb6-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="b4bb6-111">此命令會更新主機集中的 Windows 虛擬桌面工作階段主機。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="b4bb6-112">參數</span><span class="sxs-lookup"><span data-stu-id="b4bb6-112">PARAMETERS</span></span>

### <span data-ttu-id="b4bb6-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="b4bb6-113">-AllowNewSession</span></span>
<span data-ttu-id="b4bb6-114">允許新的會話。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-114">Allow a new session.</span></span>

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

### <span data-ttu-id="b4bb6-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="b4bb6-115">-AssignedUser</span></span>
<span data-ttu-id="b4bb6-116">指派給 SessionHost 的使用者。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="b4bb6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bb6-117">-DefaultProfile</span></span>
<span data-ttu-id="b4bb6-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4bb6-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b4bb6-119">-HostPoolName</span></span>
<span data-ttu-id="b4bb6-120">指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="b4bb6-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="b4bb6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4bb6-121">-InputObject</span></span>
<span data-ttu-id="b4bb6-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b4bb6-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4bb6-123">-Name</span></span>
<span data-ttu-id="b4bb6-124">指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="b4bb6-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bb6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4bb6-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4bb6-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-126">The name of the resource group.</span></span>
<span data-ttu-id="b4bb6-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b4bb6-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4bb6-128">-SubscriptionId</span></span>
<span data-ttu-id="b4bb6-129">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b4bb6-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b4bb6-130">-Confirm</span></span>
<span data-ttu-id="b4bb6-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4bb6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4bb6-132">-WhatIf</span></span>
<span data-ttu-id="b4bb6-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4bb6-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4bb6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bb6-135">CommonParameters</span></span>
<span data-ttu-id="b4bb6-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bb6-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4bb6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bb6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b4bb6-138">INPUTS</span></span>

### <span data-ttu-id="b4bb6-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b4bb6-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b4bb6-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b4bb6-140">OUTPUTS</span></span>

### <span data-ttu-id="b4bb6-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="b4bb6-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="b4bb6-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b4bb6-142">NOTES</span></span>

<span data-ttu-id="b4bb6-143">別名</span><span class="sxs-lookup"><span data-stu-id="b4bb6-143">ALIASES</span></span>

<span data-ttu-id="b4bb6-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b4bb6-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b4bb6-145">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b4bb6-146">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b4bb6-147">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b4bb6-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b4bb6-148">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="b4bb6-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b4bb6-149">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="b4bb6-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b4bb6-150">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="b4bb6-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b4bb6-151">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="b4bb6-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b4bb6-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b4bb6-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b4bb6-153">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="b4bb6-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b4bb6-154">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b4bb6-155">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="b4bb6-156">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="b4bb6-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b4bb6-157">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4bb6-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b4bb6-158">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="b4bb6-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b4bb6-159">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="b4bb6-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b4bb6-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4bb6-160">RELATED LINKS</span></span>

