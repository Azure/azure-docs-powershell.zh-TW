---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 88c56275bc2687d9693411159551684a9c76f943
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137235"
---
# <span data-ttu-id="8b476-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="8b476-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="8b476-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b476-102">SYNOPSIS</span></span>
<span data-ttu-id="8b476-103">建立或更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="8b476-103">Create or update an application.</span></span>

## <span data-ttu-id="8b476-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b476-104">SYNTAX</span></span>

### <span data-ttu-id="8b476-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="8b476-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8b476-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="8b476-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8b476-107">說明</span><span class="sxs-lookup"><span data-stu-id="8b476-107">DESCRIPTION</span></span>
<span data-ttu-id="8b476-108">建立或更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="8b476-108">Create or update an application.</span></span>

## <span data-ttu-id="8b476-109">示例</span><span class="sxs-lookup"><span data-stu-id="8b476-109">EXAMPLES</span></span>

### <span data-ttu-id="8b476-110">範例1：建立 Windows 虛擬桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="8b476-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> New-AzWvdApplication -ResourceGroupName ResourceGroupName `
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

<span data-ttu-id="8b476-111">這個命令會在 applicaton 群組中建立 Windows 虛擬桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="8b476-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="8b476-112">參數</span><span class="sxs-lookup"><span data-stu-id="8b476-112">PARAMETERS</span></span>

### <span data-ttu-id="8b476-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="8b476-113">-AppAlias</span></span>
<span data-ttu-id="8b476-114">[開始] 功能表項目目的 [應用程式別名]</span><span class="sxs-lookup"><span data-stu-id="8b476-114">App Alias from start menu item</span></span>

```yaml
Type: System.String
Parameter Sets: AppAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="8b476-115">-ApplicationType</span></span>
<span data-ttu-id="8b476-116">應用程式的資源類型。</span><span class="sxs-lookup"><span data-stu-id="8b476-116">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="8b476-117">-CommandLineArgument</span></span>
<span data-ttu-id="8b476-118">應用程式的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="8b476-118">Command Line Arguments for Application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="8b476-119">-CommandLineSetting</span></span>
<span data-ttu-id="8b476-120">指定此發佈的應用程式是否可以使用用戶端提供的命令列引數、在發佈時間指定的命令列引數，或是根本沒有命令列引數來啟動。</span><span class="sxs-lookup"><span data-stu-id="8b476-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b476-121">-DefaultProfile</span></span>
<span data-ttu-id="8b476-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b476-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b476-123">-描述</span><span class="sxs-lookup"><span data-stu-id="8b476-123">-Description</span></span>
<span data-ttu-id="8b476-124">應用程式的描述。</span><span class="sxs-lookup"><span data-stu-id="8b476-124">Description of Application.</span></span>

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

### <span data-ttu-id="8b476-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="8b476-125">-FilePath</span></span>
<span data-ttu-id="8b476-126">指定應用程式的可執行檔路徑。</span><span class="sxs-lookup"><span data-stu-id="8b476-126">Specifies a path for the executable file for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-127">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8b476-127">-FriendlyName</span></span>
<span data-ttu-id="8b476-128">應用程式的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="8b476-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="8b476-129">-[名]</span><span class="sxs-lookup"><span data-stu-id="8b476-129">-GroupName</span></span>
<span data-ttu-id="8b476-130">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="8b476-130">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="8b476-131">-IconIndex</span></span>
<span data-ttu-id="8b476-132">圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="8b476-132">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="8b476-133">-IconPath</span></span>
<span data-ttu-id="8b476-134">圖示的路徑。</span><span class="sxs-lookup"><span data-stu-id="8b476-134">Path to icon.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="8b476-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="8b476-136">指定 MSIX 應用程式的套件應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="8b476-136">Specifies the package application Id for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="8b476-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="8b476-138">指定 MSIX 應用程式的套件系列名稱</span><span class="sxs-lookup"><span data-stu-id="8b476-138">Specifies the package family name for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="8b476-139">-Name</span></span>
<span data-ttu-id="8b476-140">指定應用程式群組內的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="8b476-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b476-141">-ResourceGroupName</span></span>
<span data-ttu-id="8b476-142">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b476-142">The name of the resource group.</span></span>
<span data-ttu-id="8b476-143">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8b476-143">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="8b476-144">-ShowInPortal</span></span>
<span data-ttu-id="8b476-145">指定是否要在 RD Web Access 伺服器中顯示 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="8b476-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="8b476-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b476-146">-SubscriptionId</span></span>
<span data-ttu-id="8b476-147">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="8b476-147">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b476-148">-確認</span><span class="sxs-lookup"><span data-stu-id="8b476-148">-Confirm</span></span>
<span data-ttu-id="8b476-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8b476-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b476-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b476-150">-WhatIf</span></span>
<span data-ttu-id="8b476-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8b476-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b476-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8b476-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b476-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b476-153">CommonParameters</span></span>
<span data-ttu-id="8b476-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b476-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b476-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8b476-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b476-156">輸入</span><span class="sxs-lookup"><span data-stu-id="8b476-156">INPUTS</span></span>

## <span data-ttu-id="8b476-157">輸出</span><span class="sxs-lookup"><span data-stu-id="8b476-157">OUTPUTS</span></span>

### <span data-ttu-id="8b476-158">IApplication （DesktopVirtualization）。 Api20201102Preview。</span><span class="sxs-lookup"><span data-stu-id="8b476-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="8b476-159">筆記</span><span class="sxs-lookup"><span data-stu-id="8b476-159">NOTES</span></span>

<span data-ttu-id="8b476-160">別名</span><span class="sxs-lookup"><span data-stu-id="8b476-160">ALIASES</span></span>

## <span data-ttu-id="8b476-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b476-161">RELATED LINKS</span></span>

