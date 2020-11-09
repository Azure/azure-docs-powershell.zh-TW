---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 7a78404c8dde734f756792b85d27d712b5c5ed69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284754"
---
# <span data-ttu-id="7b755-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="7b755-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="7b755-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b755-102">SYNOPSIS</span></span>
<span data-ttu-id="7b755-103">建立或更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="7b755-103">Create or update an application.</span></span>

## <span data-ttu-id="7b755-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b755-104">SYNTAX</span></span>

### <span data-ttu-id="7b755-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="7b755-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-FilePath <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7b755-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="7b755-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7b755-107">說明</span><span class="sxs-lookup"><span data-stu-id="7b755-107">DESCRIPTION</span></span>
<span data-ttu-id="7b755-108">建立或更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="7b755-108">Create or update an application.</span></span>

## <span data-ttu-id="7b755-109">示例</span><span class="sxs-lookup"><span data-stu-id="7b755-109">EXAMPLES</span></span>

### <span data-ttu-id="7b755-110">範例1：建立 Windows 虛擬桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="7b755-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="7b755-111">這個命令會在 applicaton 群組中建立 Windows 虛擬桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="7b755-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="7b755-112">參數</span><span class="sxs-lookup"><span data-stu-id="7b755-112">PARAMETERS</span></span>

### <span data-ttu-id="7b755-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="7b755-113">-AppAlias</span></span>
<span data-ttu-id="7b755-114">[開始] 功能表項目目的 [應用程式別名]</span><span class="sxs-lookup"><span data-stu-id="7b755-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="7b755-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="7b755-115">-CommandLineArgument</span></span>
<span data-ttu-id="7b755-116">應用程式的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="7b755-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="7b755-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="7b755-117">-CommandLineSetting</span></span>
<span data-ttu-id="7b755-118">指定此發佈的應用程式是否可以使用用戶端提供的命令列引數、在發佈時間指定的命令列引數，或是根本沒有命令列引數來啟動。</span><span class="sxs-lookup"><span data-stu-id="7b755-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="7b755-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b755-119">-DefaultProfile</span></span>
<span data-ttu-id="7b755-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b755-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b755-121">-描述</span><span class="sxs-lookup"><span data-stu-id="7b755-121">-Description</span></span>
<span data-ttu-id="7b755-122">應用程式的描述。</span><span class="sxs-lookup"><span data-stu-id="7b755-122">Description of Application.</span></span>

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

### <span data-ttu-id="7b755-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="7b755-123">-FilePath</span></span>
<span data-ttu-id="7b755-124">指定應用程式的可執行檔路徑。</span><span class="sxs-lookup"><span data-stu-id="7b755-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="7b755-125">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7b755-125">-FriendlyName</span></span>
<span data-ttu-id="7b755-126">應用程式的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="7b755-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="7b755-127">-[名]</span><span class="sxs-lookup"><span data-stu-id="7b755-127">-GroupName</span></span>
<span data-ttu-id="7b755-128">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="7b755-128">The name of the application group</span></span>

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

### <span data-ttu-id="7b755-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="7b755-129">-IconIndex</span></span>
<span data-ttu-id="7b755-130">圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="7b755-130">Index of the icon.</span></span>

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

### <span data-ttu-id="7b755-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="7b755-131">-IconPath</span></span>
<span data-ttu-id="7b755-132">圖示的路徑。</span><span class="sxs-lookup"><span data-stu-id="7b755-132">Path to icon.</span></span>

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

### <span data-ttu-id="7b755-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b755-133">-Name</span></span>
<span data-ttu-id="7b755-134">指定應用程式群組內的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="7b755-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="7b755-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b755-135">-ResourceGroupName</span></span>
<span data-ttu-id="7b755-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b755-136">The name of the resource group.</span></span>
<span data-ttu-id="7b755-137">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7b755-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7b755-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="7b755-138">-ShowInPortal</span></span>
<span data-ttu-id="7b755-139">指定是否要在 RD Web Access 伺服器中顯示 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="7b755-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="7b755-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b755-140">-SubscriptionId</span></span>
<span data-ttu-id="7b755-141">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="7b755-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7b755-142">-確認</span><span class="sxs-lookup"><span data-stu-id="7b755-142">-Confirm</span></span>
<span data-ttu-id="7b755-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7b755-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b755-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b755-144">-WhatIf</span></span>
<span data-ttu-id="7b755-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7b755-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b755-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7b755-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b755-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b755-147">CommonParameters</span></span>
<span data-ttu-id="7b755-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b755-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b755-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7b755-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b755-150">輸入</span><span class="sxs-lookup"><span data-stu-id="7b755-150">INPUTS</span></span>

## <span data-ttu-id="7b755-151">輸出</span><span class="sxs-lookup"><span data-stu-id="7b755-151">OUTPUTS</span></span>

### <span data-ttu-id="7b755-152">IApplication （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="7b755-152">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="7b755-153">筆記</span><span class="sxs-lookup"><span data-stu-id="7b755-153">NOTES</span></span>

<span data-ttu-id="7b755-154">別名</span><span class="sxs-lookup"><span data-stu-id="7b755-154">ALIASES</span></span>

## <span data-ttu-id="7b755-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b755-155">RELATED LINKS</span></span>

