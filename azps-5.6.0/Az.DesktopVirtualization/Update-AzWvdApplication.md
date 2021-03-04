---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8770b9e3b07b677f0f4bd4f59a6c38928421523e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914858"
---
# <span data-ttu-id="a0fbb-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="a0fbb-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="a0fbb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a0fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="a0fbb-103">更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-103">Update an application.</span></span>

## <span data-ttu-id="a0fbb-104">語法</span><span class="sxs-lookup"><span data-stu-id="a0fbb-104">SYNTAX</span></span>

### <span data-ttu-id="a0fbb-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="a0fbb-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a0fbb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a0fbb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0fbb-107">描述</span><span class="sxs-lookup"><span data-stu-id="a0fbb-107">DESCRIPTION</span></span>
<span data-ttu-id="a0fbb-108">更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-108">Update an application.</span></span>

## <span data-ttu-id="a0fbb-109">例子</span><span class="sxs-lookup"><span data-stu-id="a0fbb-109">EXAMPLES</span></span>

### <span data-ttu-id="a0fbb-110">範例 1：更新 Windows 虛擬桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="a0fbb-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> Update-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="a0fbb-111">此命令會更新應用程式群組中的 Windows 虛擬桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="a0fbb-112">參數</span><span class="sxs-lookup"><span data-stu-id="a0fbb-112">PARAMETERS</span></span>

### <span data-ttu-id="a0fbb-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="a0fbb-113">-ApplicationType</span></span>
<span data-ttu-id="a0fbb-114">應用程式的資源類型。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-114">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0fbb-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="a0fbb-115">-CommandLineArgument</span></span>
<span data-ttu-id="a0fbb-116">應用程式的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="a0fbb-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="a0fbb-117">-CommandLineSetting</span></span>
<span data-ttu-id="a0fbb-118">指定是否可以使用用戶端提供的命令列引數、在發佈時指定的命令列引數啟動此已發佈的應用程式，或是否可啟動命令列引數。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0fbb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0fbb-119">-DefaultProfile</span></span>
<span data-ttu-id="a0fbb-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0fbb-121">-描述</span><span class="sxs-lookup"><span data-stu-id="a0fbb-121">-Description</span></span>
<span data-ttu-id="a0fbb-122">應用程式描述。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-122">Description of Application.</span></span>

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

### <span data-ttu-id="a0fbb-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="a0fbb-123">-FilePath</span></span>
<span data-ttu-id="a0fbb-124">指定應用程式可執行檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="a0fbb-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a0fbb-125">-FriendlyName</span></span>
<span data-ttu-id="a0fbb-126">應用程式好用的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="a0fbb-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="a0fbb-127">-GroupName</span></span>
<span data-ttu-id="a0fbb-128">應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="a0fbb-128">The name of the application group</span></span>

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

### <span data-ttu-id="a0fbb-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="a0fbb-129">-IconIndex</span></span>
<span data-ttu-id="a0fbb-130">圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-130">Index of the icon.</span></span>

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

### <span data-ttu-id="a0fbb-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="a0fbb-131">-IconPath</span></span>
<span data-ttu-id="a0fbb-132">圖示的路徑。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-132">Path to icon.</span></span>

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

### <span data-ttu-id="a0fbb-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0fbb-133">-InputObject</span></span>
<span data-ttu-id="a0fbb-134">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a0fbb-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="a0fbb-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="a0fbb-136">指定 MSIX 應用程式的套件應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="a0fbb-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="a0fbb-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="a0fbb-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="a0fbb-138">指定 MSIX 應用程式的套件系列名稱</span><span class="sxs-lookup"><span data-stu-id="a0fbb-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="a0fbb-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0fbb-139">-Name</span></span>
<span data-ttu-id="a0fbb-140">指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="a0fbb-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0fbb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0fbb-141">-ResourceGroupName</span></span>
<span data-ttu-id="a0fbb-142">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-142">The name of the resource group.</span></span>
<span data-ttu-id="a0fbb-143">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a0fbb-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="a0fbb-144">-ShowInPortal</span></span>
<span data-ttu-id="a0fbb-145">指定是否要在 RD Web Access 伺服器中顯示 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="a0fbb-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0fbb-146">-SubscriptionId</span></span>
<span data-ttu-id="a0fbb-147">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a0fbb-148">-標記</span><span class="sxs-lookup"><span data-stu-id="a0fbb-148">-Tag</span></span>
<span data-ttu-id="a0fbb-149">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="a0fbb-149">tags to be updated</span></span>

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

### <span data-ttu-id="a0fbb-150">-確認</span><span class="sxs-lookup"><span data-stu-id="a0fbb-150">-Confirm</span></span>
<span data-ttu-id="a0fbb-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0fbb-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0fbb-152">-WhatIf</span></span>
<span data-ttu-id="a0fbb-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0fbb-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0fbb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0fbb-155">CommonParameters</span></span>
<span data-ttu-id="a0fbb-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0fbb-157">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0fbb-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0fbb-158">輸入</span><span class="sxs-lookup"><span data-stu-id="a0fbb-158">INPUTS</span></span>

### <span data-ttu-id="a0fbb-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a0fbb-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a0fbb-160">輸出</span><span class="sxs-lookup"><span data-stu-id="a0fbb-160">OUTPUTS</span></span>

### <span data-ttu-id="a0fbb-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="a0fbb-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="a0fbb-162">筆記</span><span class="sxs-lookup"><span data-stu-id="a0fbb-162">NOTES</span></span>

<span data-ttu-id="a0fbb-163">別名</span><span class="sxs-lookup"><span data-stu-id="a0fbb-163">ALIASES</span></span>

<span data-ttu-id="a0fbb-164">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a0fbb-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a0fbb-165">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0fbb-166">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a0fbb-167">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a0fbb-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a0fbb-168">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="a0fbb-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a0fbb-169">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="a0fbb-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a0fbb-170">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="a0fbb-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a0fbb-171">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="a0fbb-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a0fbb-172">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="a0fbb-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a0fbb-173">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="a0fbb-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a0fbb-174">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a0fbb-175">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="a0fbb-176">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="a0fbb-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a0fbb-177">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0fbb-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a0fbb-178">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="a0fbb-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a0fbb-179">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="a0fbb-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a0fbb-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0fbb-180">RELATED LINKS</span></span>

