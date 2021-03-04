---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: fbc61ec485be94eacb0267a9698a861f962c61a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914853"
---
# <span data-ttu-id="61a84-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="61a84-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="61a84-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61a84-102">SYNOPSIS</span></span>
<span data-ttu-id="61a84-103">更新桌面。</span><span class="sxs-lookup"><span data-stu-id="61a84-103">Update a desktop.</span></span>

## <span data-ttu-id="61a84-104">語法</span><span class="sxs-lookup"><span data-stu-id="61a84-104">SYNTAX</span></span>

### <span data-ttu-id="61a84-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="61a84-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="61a84-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="61a84-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="61a84-107">描述</span><span class="sxs-lookup"><span data-stu-id="61a84-107">DESCRIPTION</span></span>
<span data-ttu-id="61a84-108">更新桌面。</span><span class="sxs-lookup"><span data-stu-id="61a84-108">Update a desktop.</span></span>

## <span data-ttu-id="61a84-109">例子</span><span class="sxs-lookup"><span data-stu-id="61a84-109">EXAMPLES</span></span>

### <span data-ttu-id="61a84-110">範例 1：更新 Windows 虛擬桌面</span><span class="sxs-lookup"><span data-stu-id="61a84-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="61a84-111">此命令會更新應用程式群組中的 Windows 虛擬桌面。</span><span class="sxs-lookup"><span data-stu-id="61a84-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="61a84-112">參數</span><span class="sxs-lookup"><span data-stu-id="61a84-112">PARAMETERS</span></span>

### <span data-ttu-id="61a84-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="61a84-113">-ApplicationGroupName</span></span>
<span data-ttu-id="61a84-114">應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="61a84-114">The name of the application group</span></span>

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

### <span data-ttu-id="61a84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a84-115">-DefaultProfile</span></span>
<span data-ttu-id="61a84-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="61a84-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61a84-117">-描述</span><span class="sxs-lookup"><span data-stu-id="61a84-117">-Description</span></span>
<span data-ttu-id="61a84-118">桌面的描述。</span><span class="sxs-lookup"><span data-stu-id="61a84-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="61a84-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="61a84-119">-FriendlyName</span></span>
<span data-ttu-id="61a84-120">電腦好用的名稱。</span><span class="sxs-lookup"><span data-stu-id="61a84-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="61a84-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61a84-121">-InputObject</span></span>
<span data-ttu-id="61a84-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="61a84-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="61a84-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="61a84-123">-Name</span></span>
<span data-ttu-id="61a84-124">指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="61a84-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a84-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61a84-125">-ResourceGroupName</span></span>
<span data-ttu-id="61a84-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61a84-126">The name of the resource group.</span></span>
<span data-ttu-id="61a84-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="61a84-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="61a84-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61a84-128">-SubscriptionId</span></span>
<span data-ttu-id="61a84-129">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="61a84-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="61a84-130">-標記</span><span class="sxs-lookup"><span data-stu-id="61a84-130">-Tag</span></span>
<span data-ttu-id="61a84-131">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="61a84-131">tags to be updated</span></span>

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

### <span data-ttu-id="61a84-132">-確認</span><span class="sxs-lookup"><span data-stu-id="61a84-132">-Confirm</span></span>
<span data-ttu-id="61a84-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="61a84-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61a84-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61a84-134">-WhatIf</span></span>
<span data-ttu-id="61a84-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61a84-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61a84-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61a84-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61a84-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a84-137">CommonParameters</span></span>
<span data-ttu-id="61a84-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61a84-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a84-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61a84-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a84-140">輸入</span><span class="sxs-lookup"><span data-stu-id="61a84-140">INPUTS</span></span>

### <span data-ttu-id="61a84-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="61a84-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="61a84-142">輸出</span><span class="sxs-lookup"><span data-stu-id="61a84-142">OUTPUTS</span></span>

### <span data-ttu-id="61a84-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="61a84-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

## <span data-ttu-id="61a84-144">筆記</span><span class="sxs-lookup"><span data-stu-id="61a84-144">NOTES</span></span>

<span data-ttu-id="61a84-145">別名</span><span class="sxs-lookup"><span data-stu-id="61a84-145">ALIASES</span></span>

<span data-ttu-id="61a84-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="61a84-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="61a84-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="61a84-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="61a84-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="61a84-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="61a84-149">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="61a84-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="61a84-150">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="61a84-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="61a84-151">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="61a84-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="61a84-152">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="61a84-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="61a84-153">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="61a84-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="61a84-154">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="61a84-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="61a84-155">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="61a84-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="61a84-156">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61a84-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="61a84-157">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="61a84-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="61a84-158">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="61a84-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="61a84-159">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="61a84-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="61a84-160">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="61a84-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="61a84-161">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="61a84-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="61a84-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="61a84-162">RELATED LINKS</span></span>

