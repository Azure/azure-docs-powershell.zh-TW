---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: 55d2436d70061fb9fc70013a4d8a7ef7e99fa434
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912870"
---
# <span data-ttu-id="8c3b8-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="8c3b8-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="8c3b8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8c3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="8c3b8-103">更新應用程式組。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="8c3b8-104">語法</span><span class="sxs-lookup"><span data-stu-id="8c3b8-104">SYNTAX</span></span>

### <span data-ttu-id="8c3b8-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="8c3b8-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c3b8-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8c3b8-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8c3b8-107">描述</span><span class="sxs-lookup"><span data-stu-id="8c3b8-107">DESCRIPTION</span></span>
<span data-ttu-id="8c3b8-108">更新應用程式組。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="8c3b8-109">例子</span><span class="sxs-lookup"><span data-stu-id="8c3b8-109">EXAMPLES</span></span>

### <span data-ttu-id="8c3b8-110">範例 1：根據名稱建立 Windows 虛擬桌面應用程式組</span><span class="sxs-lookup"><span data-stu-id="8c3b8-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="8c3b8-111">此命令在資源群組中建立 Windows 虛擬桌面應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="8c3b8-112">參數</span><span class="sxs-lookup"><span data-stu-id="8c3b8-112">PARAMETERS</span></span>

### <span data-ttu-id="8c3b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c3b8-113">-DefaultProfile</span></span>
<span data-ttu-id="8c3b8-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c3b8-115">-描述</span><span class="sxs-lookup"><span data-stu-id="8c3b8-115">-Description</span></span>
<span data-ttu-id="8c3b8-116">ApplicationGroup 的描述。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="8c3b8-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8c3b8-117">-FriendlyName</span></span>
<span data-ttu-id="8c3b8-118">ApplicationGroup 的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="8c3b8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c3b8-119">-InputObject</span></span>
<span data-ttu-id="8c3b8-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8c3b8-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c3b8-121">-Name</span></span>
<span data-ttu-id="8c3b8-122">應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="8c3b8-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c3b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c3b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="8c3b8-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-124">The name of the resource group.</span></span>
<span data-ttu-id="8c3b8-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8c3b8-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c3b8-126">-SubscriptionId</span></span>
<span data-ttu-id="8c3b8-127">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8c3b8-128">-標記</span><span class="sxs-lookup"><span data-stu-id="8c3b8-128">-Tag</span></span>
<span data-ttu-id="8c3b8-129">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="8c3b8-129">tags to be updated</span></span>

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

### <span data-ttu-id="8c3b8-130">-確認</span><span class="sxs-lookup"><span data-stu-id="8c3b8-130">-Confirm</span></span>
<span data-ttu-id="8c3b8-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c3b8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c3b8-132">-WhatIf</span></span>
<span data-ttu-id="8c3b8-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c3b8-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c3b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c3b8-135">CommonParameters</span></span>
<span data-ttu-id="8c3b8-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c3b8-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c3b8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c3b8-138">輸入</span><span class="sxs-lookup"><span data-stu-id="8c3b8-138">INPUTS</span></span>

### <span data-ttu-id="8c3b8-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8c3b8-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8c3b8-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8c3b8-140">OUTPUTS</span></span>

### <span data-ttu-id="8c3b8-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="8c3b8-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="8c3b8-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8c3b8-142">NOTES</span></span>

<span data-ttu-id="8c3b8-143">別名</span><span class="sxs-lookup"><span data-stu-id="8c3b8-143">ALIASES</span></span>

<span data-ttu-id="8c3b8-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8c3b8-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8c3b8-145">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c3b8-146">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8c3b8-147">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8c3b8-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8c3b8-148">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="8c3b8-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8c3b8-149">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="8c3b8-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8c3b8-150">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="8c3b8-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8c3b8-151">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="8c3b8-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8c3b8-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="8c3b8-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8c3b8-153">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="8c3b8-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="8c3b8-154">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8c3b8-155">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="8c3b8-156">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="8c3b8-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8c3b8-157">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c3b8-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8c3b8-158">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="8c3b8-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8c3b8-159">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="8c3b8-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8c3b8-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c3b8-160">RELATED LINKS</span></span>

