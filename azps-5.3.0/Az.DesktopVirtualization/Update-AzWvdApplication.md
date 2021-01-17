---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 87932f3f703ba1ffe8ae7e367d44445166728032
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436594"
---
# <span data-ttu-id="d5f7d-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="d5f7d-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="d5f7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f7d-103">更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-103">Update an application.</span></span>

## <span data-ttu-id="d5f7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5f7d-104">SYNTAX</span></span>

### <span data-ttu-id="d5f7d-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="d5f7d-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d5f7d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d5f7d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5f7d-107">說明</span><span class="sxs-lookup"><span data-stu-id="d5f7d-107">DESCRIPTION</span></span>
<span data-ttu-id="d5f7d-108">更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-108">Update an application.</span></span>

## <span data-ttu-id="d5f7d-109">示例</span><span class="sxs-lookup"><span data-stu-id="d5f7d-109">EXAMPLES</span></span>

### <span data-ttu-id="d5f7d-110">範例1：更新 Windows 虛擬桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="d5f7d-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="d5f7d-111">這個命令會更新 applicaton 群組中的 Windows 虛擬桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="d5f7d-112">參數</span><span class="sxs-lookup"><span data-stu-id="d5f7d-112">PARAMETERS</span></span>

### <span data-ttu-id="d5f7d-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="d5f7d-113">-ApplicationType</span></span>
<span data-ttu-id="d5f7d-114">應用程式的資源類型。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-114">Resource Type of Application.</span></span>

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

### <span data-ttu-id="d5f7d-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="d5f7d-115">-CommandLineArgument</span></span>
<span data-ttu-id="d5f7d-116">應用程式的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="d5f7d-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="d5f7d-117">-CommandLineSetting</span></span>
<span data-ttu-id="d5f7d-118">指定此發佈的應用程式是否可以使用用戶端提供的命令列引數、在發佈時間指定的命令列引數，或是根本沒有命令列引數來啟動。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="d5f7d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f7d-119">-DefaultProfile</span></span>
<span data-ttu-id="d5f7d-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5f7d-121">-描述</span><span class="sxs-lookup"><span data-stu-id="d5f7d-121">-Description</span></span>
<span data-ttu-id="d5f7d-122">應用程式的描述。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-122">Description of Application.</span></span>

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

### <span data-ttu-id="d5f7d-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d5f7d-123">-FilePath</span></span>
<span data-ttu-id="d5f7d-124">指定應用程式的可執行檔路徑。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="d5f7d-125">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d5f7d-125">-FriendlyName</span></span>
<span data-ttu-id="d5f7d-126">應用程式的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="d5f7d-127">-[名]</span><span class="sxs-lookup"><span data-stu-id="d5f7d-127">-GroupName</span></span>
<span data-ttu-id="d5f7d-128">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="d5f7d-128">The name of the application group</span></span>

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

### <span data-ttu-id="d5f7d-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="d5f7d-129">-IconIndex</span></span>
<span data-ttu-id="d5f7d-130">圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-130">Index of the icon.</span></span>

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

### <span data-ttu-id="d5f7d-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="d5f7d-131">-IconPath</span></span>
<span data-ttu-id="d5f7d-132">圖示的路徑。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-132">Path to icon.</span></span>

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

### <span data-ttu-id="d5f7d-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5f7d-133">-InputObject</span></span>
<span data-ttu-id="d5f7d-134">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d5f7d-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="d5f7d-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="d5f7d-136">指定 MSIX 應用程式的套件應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="d5f7d-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="d5f7d-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="d5f7d-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="d5f7d-138">指定 MSIX 應用程式的套件系列名稱</span><span class="sxs-lookup"><span data-stu-id="d5f7d-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="d5f7d-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="d5f7d-139">-Name</span></span>
<span data-ttu-id="d5f7d-140">指定應用程式群組內的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="d5f7d-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="d5f7d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5f7d-141">-ResourceGroupName</span></span>
<span data-ttu-id="d5f7d-142">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-142">The name of the resource group.</span></span>
<span data-ttu-id="d5f7d-143">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d5f7d-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="d5f7d-144">-ShowInPortal</span></span>
<span data-ttu-id="d5f7d-145">指定是否要在 RD Web Access 伺服器中顯示 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="d5f7d-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5f7d-146">-SubscriptionId</span></span>
<span data-ttu-id="d5f7d-147">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d5f7d-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5f7d-148">-Tag</span></span>
<span data-ttu-id="d5f7d-149">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="d5f7d-149">tags to be updated</span></span>

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

### <span data-ttu-id="d5f7d-150">-確認</span><span class="sxs-lookup"><span data-stu-id="d5f7d-150">-Confirm</span></span>
<span data-ttu-id="d5f7d-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5f7d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5f7d-152">-WhatIf</span></span>
<span data-ttu-id="d5f7d-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5f7d-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5f7d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f7d-155">CommonParameters</span></span>
<span data-ttu-id="d5f7d-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f7d-157">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f7d-158">輸入</span><span class="sxs-lookup"><span data-stu-id="d5f7d-158">INPUTS</span></span>

### <span data-ttu-id="d5f7d-159">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="d5f7d-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d5f7d-160">輸出</span><span class="sxs-lookup"><span data-stu-id="d5f7d-160">OUTPUTS</span></span>

### <span data-ttu-id="d5f7d-161">IApplication （DesktopVirtualization）。 Api20201102Preview。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="d5f7d-162">筆記</span><span class="sxs-lookup"><span data-stu-id="d5f7d-162">NOTES</span></span>

<span data-ttu-id="d5f7d-163">別名</span><span class="sxs-lookup"><span data-stu-id="d5f7d-163">ALIASES</span></span>

<span data-ttu-id="d5f7d-164">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d5f7d-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5f7d-165">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5f7d-166">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5f7d-167">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d5f7d-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d5f7d-168">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="d5f7d-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d5f7d-169">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="d5f7d-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d5f7d-170">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="d5f7d-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d5f7d-171">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="d5f7d-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d5f7d-172">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="d5f7d-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5f7d-173">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="d5f7d-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="d5f7d-174">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d5f7d-175">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="d5f7d-176">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="d5f7d-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d5f7d-177">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5f7d-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d5f7d-178">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="d5f7d-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d5f7d-179">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="d5f7d-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d5f7d-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5f7d-180">RELATED LINKS</span></span>

