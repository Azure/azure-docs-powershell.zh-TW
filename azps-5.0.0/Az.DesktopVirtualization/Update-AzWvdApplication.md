---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8c2026e7ef8ed5c0eeb1e5a4cb7f605c1a030b9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138934"
---
# <span data-ttu-id="5bcaa-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="5bcaa-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="5bcaa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5bcaa-102">SYNOPSIS</span></span>
<span data-ttu-id="5bcaa-103">更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-103">Update an application.</span></span>

## <span data-ttu-id="5bcaa-104">句法</span><span class="sxs-lookup"><span data-stu-id="5bcaa-104">SYNTAX</span></span>

### <span data-ttu-id="5bcaa-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="5bcaa-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-CommandLineSetting <CommandLineSetting>]
 [-Description <String>] [-FilePath <String>] [-FriendlyName <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5bcaa-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5bcaa-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5bcaa-107">說明</span><span class="sxs-lookup"><span data-stu-id="5bcaa-107">DESCRIPTION</span></span>
<span data-ttu-id="5bcaa-108">更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-108">Update an application.</span></span>

## <span data-ttu-id="5bcaa-109">示例</span><span class="sxs-lookup"><span data-stu-id="5bcaa-109">EXAMPLES</span></span>

### <span data-ttu-id="5bcaa-110">範例1：更新 Windows 虛擬桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="5bcaa-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="5bcaa-111">這個命令會更新 applicaton 群組中的 Windows 虛擬桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="5bcaa-112">參數</span><span class="sxs-lookup"><span data-stu-id="5bcaa-112">PARAMETERS</span></span>

### <span data-ttu-id="5bcaa-113">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="5bcaa-113">-CommandLineArgument</span></span>
<span data-ttu-id="5bcaa-114">應用程式的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-114">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="5bcaa-115">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="5bcaa-115">-CommandLineSetting</span></span>
<span data-ttu-id="5bcaa-116">指定此發佈的應用程式是否可以使用用戶端提供的命令列引數、在發佈時間指定的命令列引數，或是根本沒有命令列引數來啟動。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-116">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="5bcaa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bcaa-117">-DefaultProfile</span></span>
<span data-ttu-id="5bcaa-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bcaa-119">-描述</span><span class="sxs-lookup"><span data-stu-id="5bcaa-119">-Description</span></span>
<span data-ttu-id="5bcaa-120">應用程式的描述。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-120">Description of Application.</span></span>

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

### <span data-ttu-id="5bcaa-121">-FilePath</span><span class="sxs-lookup"><span data-stu-id="5bcaa-121">-FilePath</span></span>
<span data-ttu-id="5bcaa-122">指定應用程式的可執行檔路徑。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-122">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="5bcaa-123">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5bcaa-123">-FriendlyName</span></span>
<span data-ttu-id="5bcaa-124">應用程式的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-124">Friendly name of Application.</span></span>

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

### <span data-ttu-id="5bcaa-125">-[名]</span><span class="sxs-lookup"><span data-stu-id="5bcaa-125">-GroupName</span></span>
<span data-ttu-id="5bcaa-126">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="5bcaa-126">The name of the application group</span></span>

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

### <span data-ttu-id="5bcaa-127">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="5bcaa-127">-IconIndex</span></span>
<span data-ttu-id="5bcaa-128">圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-128">Index of the icon.</span></span>

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

### <span data-ttu-id="5bcaa-129">-IconPath</span><span class="sxs-lookup"><span data-stu-id="5bcaa-129">-IconPath</span></span>
<span data-ttu-id="5bcaa-130">圖示的路徑。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-130">Path to icon.</span></span>

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

### <span data-ttu-id="5bcaa-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bcaa-131">-InputObject</span></span>
<span data-ttu-id="5bcaa-132">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-132">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5bcaa-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="5bcaa-133">-Name</span></span>
<span data-ttu-id="5bcaa-134">指定應用程式群組內的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="5bcaa-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="5bcaa-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bcaa-135">-ResourceGroupName</span></span>
<span data-ttu-id="5bcaa-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-136">The name of the resource group.</span></span>
<span data-ttu-id="5bcaa-137">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5bcaa-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="5bcaa-138">-ShowInPortal</span></span>
<span data-ttu-id="5bcaa-139">指定是否要在 RD Web Access 伺服器中顯示 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="5bcaa-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5bcaa-140">-SubscriptionId</span></span>
<span data-ttu-id="5bcaa-141">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5bcaa-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="5bcaa-142">-Tag</span></span>
<span data-ttu-id="5bcaa-143">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="5bcaa-143">tags to be updated</span></span>

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

### <span data-ttu-id="5bcaa-144">-確認</span><span class="sxs-lookup"><span data-stu-id="5bcaa-144">-Confirm</span></span>
<span data-ttu-id="5bcaa-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bcaa-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bcaa-146">-WhatIf</span></span>
<span data-ttu-id="5bcaa-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bcaa-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bcaa-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bcaa-149">CommonParameters</span></span>
<span data-ttu-id="5bcaa-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bcaa-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bcaa-152">輸入</span><span class="sxs-lookup"><span data-stu-id="5bcaa-152">INPUTS</span></span>

### <span data-ttu-id="5bcaa-153">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="5bcaa-153">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5bcaa-154">輸出</span><span class="sxs-lookup"><span data-stu-id="5bcaa-154">OUTPUTS</span></span>

### <span data-ttu-id="5bcaa-155">IApplication （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-155">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="5bcaa-156">筆記</span><span class="sxs-lookup"><span data-stu-id="5bcaa-156">NOTES</span></span>

<span data-ttu-id="5bcaa-157">別名</span><span class="sxs-lookup"><span data-stu-id="5bcaa-157">ALIASES</span></span>

<span data-ttu-id="5bcaa-158">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5bcaa-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5bcaa-159">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5bcaa-160">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5bcaa-161">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5bcaa-161">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5bcaa-162">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="5bcaa-162">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5bcaa-163">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="5bcaa-163">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5bcaa-164">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="5bcaa-164">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5bcaa-165">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="5bcaa-165">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5bcaa-166">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5bcaa-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5bcaa-167">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5bcaa-168">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="5bcaa-169">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="5bcaa-169">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5bcaa-170">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5bcaa-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5bcaa-171">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="5bcaa-171">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5bcaa-172">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="5bcaa-172">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5bcaa-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bcaa-173">RELATED LINKS</span></span>

