---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: f552c8e21703d64efa2ac65f47461daa963fc1f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909817"
---
# <span data-ttu-id="a530c-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="a530c-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="a530c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a530c-102">SYNOPSIS</span></span>
<span data-ttu-id="a530c-103">更新 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="a530c-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="a530c-104">語法</span><span class="sxs-lookup"><span data-stu-id="a530c-104">SYNTAX</span></span>

### <span data-ttu-id="a530c-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="a530c-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a530c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a530c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a530c-107">描述</span><span class="sxs-lookup"><span data-stu-id="a530c-107">DESCRIPTION</span></span>
<span data-ttu-id="a530c-108">更新 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="a530c-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="a530c-109">例子</span><span class="sxs-lookup"><span data-stu-id="a530c-109">EXAMPLES</span></span>

### <span data-ttu-id="a530c-110">範例 1：更新 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="a530c-110">Example 1: Update a MSIX Package</span></span> 
```powershell
PS C:\> Update-AzWvdMsixPackage -HostPoolName HostPoolName `
                -ResourceGroupName ResourceGroupName `
                -SubscriptionId SubscriptionId `
                -displayName 'Updated-display-Name' `
                    -IsRegularRegistration:$False `
                -IsActive:$True

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="a530c-111">此命令會更新 HostPool 中的 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="a530c-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="a530c-112">參數</span><span class="sxs-lookup"><span data-stu-id="a530c-112">PARAMETERS</span></span>

### <span data-ttu-id="a530c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a530c-113">-DefaultProfile</span></span>
<span data-ttu-id="a530c-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a530c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a530c-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a530c-115">-DisplayName</span></span>
<span data-ttu-id="a530c-116">MSIX 套件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a530c-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="a530c-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="a530c-117">-FullName</span></span>
<span data-ttu-id="a530c-118">指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="a530c-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a530c-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a530c-119">-HostPoolName</span></span>
<span data-ttu-id="a530c-120">指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="a530c-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a530c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a530c-121">-InputObject</span></span>
<span data-ttu-id="a530c-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a530c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a530c-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="a530c-123">-IsActive</span></span>
<span data-ttu-id="a530c-124">將套件版本設定為跨主機多工緩衝處理程式有效。</span><span class="sxs-lookup"><span data-stu-id="a530c-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="a530c-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="a530c-125">-IsRegularRegistration</span></span>
<span data-ttu-id="a530c-126">設定註冊模式。</span><span class="sxs-lookup"><span data-stu-id="a530c-126">Set Registration mode.</span></span>
<span data-ttu-id="a530c-127">一般或延遲。</span><span class="sxs-lookup"><span data-stu-id="a530c-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="a530c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a530c-128">-ResourceGroupName</span></span>
<span data-ttu-id="a530c-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a530c-129">The name of the resource group.</span></span>
<span data-ttu-id="a530c-130">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a530c-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a530c-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a530c-131">-SubscriptionId</span></span>
<span data-ttu-id="a530c-132">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a530c-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a530c-133">-確認</span><span class="sxs-lookup"><span data-stu-id="a530c-133">-Confirm</span></span>
<span data-ttu-id="a530c-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a530c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a530c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a530c-135">-WhatIf</span></span>
<span data-ttu-id="a530c-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a530c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a530c-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a530c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a530c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a530c-138">CommonParameters</span></span>
<span data-ttu-id="a530c-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a530c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a530c-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a530c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a530c-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a530c-141">INPUTS</span></span>

### <span data-ttu-id="a530c-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a530c-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a530c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a530c-143">OUTPUTS</span></span>

### <span data-ttu-id="a530c-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="a530c-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="a530c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a530c-145">NOTES</span></span>

<span data-ttu-id="a530c-146">別名</span><span class="sxs-lookup"><span data-stu-id="a530c-146">ALIASES</span></span>

<span data-ttu-id="a530c-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a530c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a530c-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a530c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a530c-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a530c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a530c-150">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a530c-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a530c-151">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="a530c-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a530c-152">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="a530c-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a530c-153">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="a530c-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a530c-154">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="a530c-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a530c-155">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="a530c-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a530c-156">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="a530c-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a530c-157">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a530c-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a530c-158">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a530c-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="a530c-159">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="a530c-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a530c-160">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a530c-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a530c-161">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="a530c-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a530c-162">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="a530c-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a530c-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="a530c-163">RELATED LINKS</span></span>

