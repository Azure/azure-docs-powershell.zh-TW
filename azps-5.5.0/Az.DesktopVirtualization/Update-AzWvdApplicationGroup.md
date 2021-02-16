---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: b03fe0c62a446c9ed54c9330708f29737e18bd59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133290"
---
# <span data-ttu-id="5f628-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="5f628-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="5f628-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f628-102">SYNOPSIS</span></span>
<span data-ttu-id="5f628-103">更新 applicationGroup。</span><span class="sxs-lookup"><span data-stu-id="5f628-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="5f628-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f628-104">SYNTAX</span></span>

### <span data-ttu-id="5f628-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="5f628-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5f628-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5f628-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5f628-107">說明</span><span class="sxs-lookup"><span data-stu-id="5f628-107">DESCRIPTION</span></span>
<span data-ttu-id="5f628-108">更新 applicationGroup。</span><span class="sxs-lookup"><span data-stu-id="5f628-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="5f628-109">示例</span><span class="sxs-lookup"><span data-stu-id="5f628-109">EXAMPLES</span></span>

### <span data-ttu-id="5f628-110">範例1：依名稱建立 Windows 虛擬桌面 ApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="5f628-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="5f628-111">這個命令會在資源群組中建立 Windows 虛擬桌面 ApplicationGroup。</span><span class="sxs-lookup"><span data-stu-id="5f628-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="5f628-112">參數</span><span class="sxs-lookup"><span data-stu-id="5f628-112">PARAMETERS</span></span>

### <span data-ttu-id="5f628-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f628-113">-DefaultProfile</span></span>
<span data-ttu-id="5f628-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f628-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f628-115">-描述</span><span class="sxs-lookup"><span data-stu-id="5f628-115">-Description</span></span>
<span data-ttu-id="5f628-116">ApplicationGroup 的描述。</span><span class="sxs-lookup"><span data-stu-id="5f628-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="5f628-117">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5f628-117">-FriendlyName</span></span>
<span data-ttu-id="5f628-118">ApplicationGroup 的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="5f628-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="5f628-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f628-119">-InputObject</span></span>
<span data-ttu-id="5f628-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5f628-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5f628-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f628-121">-Name</span></span>
<span data-ttu-id="5f628-122">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="5f628-122">The name of the application group</span></span>

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

### <span data-ttu-id="5f628-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f628-123">-ResourceGroupName</span></span>
<span data-ttu-id="5f628-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f628-124">The name of the resource group.</span></span>
<span data-ttu-id="5f628-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5f628-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5f628-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f628-126">-SubscriptionId</span></span>
<span data-ttu-id="5f628-127">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="5f628-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5f628-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="5f628-128">-Tag</span></span>
<span data-ttu-id="5f628-129">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="5f628-129">tags to be updated</span></span>

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

### <span data-ttu-id="5f628-130">-確認</span><span class="sxs-lookup"><span data-stu-id="5f628-130">-Confirm</span></span>
<span data-ttu-id="5f628-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5f628-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f628-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f628-132">-WhatIf</span></span>
<span data-ttu-id="5f628-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f628-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f628-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f628-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f628-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f628-135">CommonParameters</span></span>
<span data-ttu-id="5f628-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f628-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f628-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5f628-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f628-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5f628-138">INPUTS</span></span>

### <span data-ttu-id="5f628-139">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="5f628-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5f628-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5f628-140">OUTPUTS</span></span>

### <span data-ttu-id="5f628-141">IApplicationGroup （DesktopVirtualization）。 Api20201102Preview。</span><span class="sxs-lookup"><span data-stu-id="5f628-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="5f628-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5f628-142">NOTES</span></span>

<span data-ttu-id="5f628-143">別名</span><span class="sxs-lookup"><span data-stu-id="5f628-143">ALIASES</span></span>

<span data-ttu-id="5f628-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5f628-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5f628-145">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5f628-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f628-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5f628-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5f628-147">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5f628-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5f628-148">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="5f628-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5f628-149">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="5f628-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5f628-150">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="5f628-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5f628-151">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="5f628-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5f628-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5f628-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5f628-153">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="5f628-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="5f628-154">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f628-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5f628-155">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5f628-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="5f628-156">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="5f628-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5f628-157">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f628-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5f628-158">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="5f628-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5f628-159">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="5f628-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5f628-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f628-160">RELATED LINKS</span></span>

