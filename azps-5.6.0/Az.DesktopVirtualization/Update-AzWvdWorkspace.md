---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 1da28d0003de88d9e8c10da1692ca4f61079f488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916630"
---
# <span data-ttu-id="784ad-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="784ad-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="784ad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="784ad-102">SYNOPSIS</span></span>
<span data-ttu-id="784ad-103">更新工作區。</span><span class="sxs-lookup"><span data-stu-id="784ad-103">Update a workspace.</span></span>

## <span data-ttu-id="784ad-104">語法</span><span class="sxs-lookup"><span data-stu-id="784ad-104">SYNTAX</span></span>

### <span data-ttu-id="784ad-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="784ad-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="784ad-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="784ad-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="784ad-107">描述</span><span class="sxs-lookup"><span data-stu-id="784ad-107">DESCRIPTION</span></span>
<span data-ttu-id="784ad-108">更新工作區。</span><span class="sxs-lookup"><span data-stu-id="784ad-108">Update a workspace.</span></span>

## <span data-ttu-id="784ad-109">例子</span><span class="sxs-lookup"><span data-stu-id="784ad-109">EXAMPLES</span></span>

### <span data-ttu-id="784ad-110">範例 1：根據名稱更新 Windows 虛擬桌面工作區</span><span class="sxs-lookup"><span data-stu-id="784ad-110">Example 1: Update a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="784ad-111">此命令會更新資源群組中的 Windows 虛擬桌面工作區。</span><span class="sxs-lookup"><span data-stu-id="784ad-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="784ad-112">參數</span><span class="sxs-lookup"><span data-stu-id="784ad-112">PARAMETERS</span></span>

### <span data-ttu-id="784ad-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="784ad-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="784ad-114">應用程式Group 連結清單。</span><span class="sxs-lookup"><span data-stu-id="784ad-114">List of applicationGroup links.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="784ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="784ad-115">-DefaultProfile</span></span>
<span data-ttu-id="784ad-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="784ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="784ad-117">-描述</span><span class="sxs-lookup"><span data-stu-id="784ad-117">-Description</span></span>
<span data-ttu-id="784ad-118">工作區的描述。</span><span class="sxs-lookup"><span data-stu-id="784ad-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="784ad-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="784ad-119">-FriendlyName</span></span>
<span data-ttu-id="784ad-120">工作區的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="784ad-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="784ad-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="784ad-121">-InputObject</span></span>
<span data-ttu-id="784ad-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="784ad-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="784ad-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="784ad-123">-Name</span></span>
<span data-ttu-id="784ad-124">工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="784ad-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="784ad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="784ad-125">-ResourceGroupName</span></span>
<span data-ttu-id="784ad-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="784ad-126">The name of the resource group.</span></span>
<span data-ttu-id="784ad-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="784ad-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="784ad-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="784ad-128">-SubscriptionId</span></span>
<span data-ttu-id="784ad-129">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="784ad-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="784ad-130">-標記</span><span class="sxs-lookup"><span data-stu-id="784ad-130">-Tag</span></span>
<span data-ttu-id="784ad-131">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="784ad-131">tags to be updated</span></span>

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

### <span data-ttu-id="784ad-132">-確認</span><span class="sxs-lookup"><span data-stu-id="784ad-132">-Confirm</span></span>
<span data-ttu-id="784ad-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="784ad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="784ad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="784ad-134">-WhatIf</span></span>
<span data-ttu-id="784ad-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="784ad-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="784ad-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="784ad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="784ad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="784ad-137">CommonParameters</span></span>
<span data-ttu-id="784ad-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="784ad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="784ad-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="784ad-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="784ad-140">輸入</span><span class="sxs-lookup"><span data-stu-id="784ad-140">INPUTS</span></span>

### <span data-ttu-id="784ad-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="784ad-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="784ad-142">輸出</span><span class="sxs-lookup"><span data-stu-id="784ad-142">OUTPUTS</span></span>

### <span data-ttu-id="784ad-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="784ad-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="784ad-144">筆記</span><span class="sxs-lookup"><span data-stu-id="784ad-144">NOTES</span></span>

<span data-ttu-id="784ad-145">別名</span><span class="sxs-lookup"><span data-stu-id="784ad-145">ALIASES</span></span>

<span data-ttu-id="784ad-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="784ad-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="784ad-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="784ad-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="784ad-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="784ad-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="784ad-149">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="784ad-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="784ad-150">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="784ad-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="784ad-151">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="784ad-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="784ad-152">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="784ad-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="784ad-153">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="784ad-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="784ad-154">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="784ad-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="784ad-155">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="784ad-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="784ad-156">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="784ad-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="784ad-157">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="784ad-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="784ad-158">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="784ad-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="784ad-159">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="784ad-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="784ad-160">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="784ad-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="784ad-161">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="784ad-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="784ad-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="784ad-162">RELATED LINKS</span></span>

