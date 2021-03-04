---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: af0073a94401ce8c260027fcf905fd763d89326e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909057"
---
# <span data-ttu-id="7b4c2-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="7b4c2-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="7b4c2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7b4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="7b4c2-103">建立或更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-103">Create or update an application.</span></span>

## <span data-ttu-id="7b4c2-104">語法</span><span class="sxs-lookup"><span data-stu-id="7b4c2-104">SYNTAX</span></span>

### <span data-ttu-id="7b4c2-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="7b4c2-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7b4c2-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="7b4c2-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7b4c2-107">描述</span><span class="sxs-lookup"><span data-stu-id="7b4c2-107">DESCRIPTION</span></span>
<span data-ttu-id="7b4c2-108">建立或更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-108">Create or update an application.</span></span>

## <span data-ttu-id="7b4c2-109">例子</span><span class="sxs-lookup"><span data-stu-id="7b4c2-109">EXAMPLES</span></span>

### <span data-ttu-id="7b4c2-110">範例 1：建立 Windows 虛擬桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="7b4c2-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="7b4c2-111">此命令在應用程式群組中建立 Windows 虛擬桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="7b4c2-112">參數</span><span class="sxs-lookup"><span data-stu-id="7b4c2-112">PARAMETERS</span></span>

### <span data-ttu-id="7b4c2-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="7b4c2-113">-AppAlias</span></span>
<span data-ttu-id="7b4c2-114">從開始功能表項目的應用程式別名</span><span class="sxs-lookup"><span data-stu-id="7b4c2-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="7b4c2-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="7b4c2-115">-ApplicationType</span></span>
<span data-ttu-id="7b4c2-116">應用程式的資源類型。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-116">Resource Type of Application.</span></span>

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

### <span data-ttu-id="7b4c2-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="7b4c2-117">-CommandLineArgument</span></span>
<span data-ttu-id="7b4c2-118">應用程式的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-118">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="7b4c2-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="7b4c2-119">-CommandLineSetting</span></span>
<span data-ttu-id="7b4c2-120">指定是否可以使用用戶端提供的命令列引數、在發佈時指定的命令列引數啟動此已發佈的應用程式，或是否可啟動命令列引數。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="7b4c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b4c2-121">-DefaultProfile</span></span>
<span data-ttu-id="7b4c2-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b4c2-123">-描述</span><span class="sxs-lookup"><span data-stu-id="7b4c2-123">-Description</span></span>
<span data-ttu-id="7b4c2-124">應用程式描述。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-124">Description of Application.</span></span>

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

### <span data-ttu-id="7b4c2-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="7b4c2-125">-FilePath</span></span>
<span data-ttu-id="7b4c2-126">指定應用程式可執行檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-126">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="7b4c2-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7b4c2-127">-FriendlyName</span></span>
<span data-ttu-id="7b4c2-128">應用程式好用的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="7b4c2-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="7b4c2-129">-GroupName</span></span>
<span data-ttu-id="7b4c2-130">應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="7b4c2-130">The name of the application group</span></span>

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

### <span data-ttu-id="7b4c2-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="7b4c2-131">-IconIndex</span></span>
<span data-ttu-id="7b4c2-132">圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-132">Index of the icon.</span></span>

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

### <span data-ttu-id="7b4c2-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="7b4c2-133">-IconPath</span></span>
<span data-ttu-id="7b4c2-134">圖示的路徑。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-134">Path to icon.</span></span>

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

### <span data-ttu-id="7b4c2-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="7b4c2-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="7b4c2-136">指定 MSIX 應用程式的套件應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="7b4c2-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="7b4c2-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="7b4c2-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="7b4c2-138">指定 MSIX 應用程式的套件系列名稱</span><span class="sxs-lookup"><span data-stu-id="7b4c2-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="7b4c2-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b4c2-139">-Name</span></span>
<span data-ttu-id="7b4c2-140">指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="7b4c2-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="7b4c2-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b4c2-141">-ResourceGroupName</span></span>
<span data-ttu-id="7b4c2-142">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-142">The name of the resource group.</span></span>
<span data-ttu-id="7b4c2-143">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7b4c2-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="7b4c2-144">-ShowInPortal</span></span>
<span data-ttu-id="7b4c2-145">指定是否要在 RD Web Access 伺服器中顯示 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="7b4c2-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b4c2-146">-SubscriptionId</span></span>
<span data-ttu-id="7b4c2-147">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7b4c2-148">-確認</span><span class="sxs-lookup"><span data-stu-id="7b4c2-148">-Confirm</span></span>
<span data-ttu-id="7b4c2-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b4c2-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b4c2-150">-WhatIf</span></span>
<span data-ttu-id="7b4c2-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b4c2-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b4c2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b4c2-153">CommonParameters</span></span>
<span data-ttu-id="7b4c2-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7b4c2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b4c2-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b4c2-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b4c2-156">輸入</span><span class="sxs-lookup"><span data-stu-id="7b4c2-156">INPUTS</span></span>

## <span data-ttu-id="7b4c2-157">輸出</span><span class="sxs-lookup"><span data-stu-id="7b4c2-157">OUTPUTS</span></span>

### <span data-ttu-id="7b4c2-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="7b4c2-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="7b4c2-159">筆記</span><span class="sxs-lookup"><span data-stu-id="7b4c2-159">NOTES</span></span>

<span data-ttu-id="7b4c2-160">別名</span><span class="sxs-lookup"><span data-stu-id="7b4c2-160">ALIASES</span></span>

## <span data-ttu-id="7b4c2-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b4c2-161">RELATED LINKS</span></span>

