---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: 9335bb4c3177fa405d65038255f43dbba5fb88fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905442"
---
# <span data-ttu-id="9bc5d-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="9bc5d-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="9bc5d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9bc5d-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc5d-103">建立或更新工作區。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-103">Create or update a workspace.</span></span>

## <span data-ttu-id="9bc5d-104">語法</span><span class="sxs-lookup"><span data-stu-id="9bc5d-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9bc5d-105">描述</span><span class="sxs-lookup"><span data-stu-id="9bc5d-105">DESCRIPTION</span></span>
<span data-ttu-id="9bc5d-106">建立或更新工作區。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-106">Create or update a workspace.</span></span>

## <span data-ttu-id="9bc5d-107">例子</span><span class="sxs-lookup"><span data-stu-id="9bc5d-107">EXAMPLES</span></span>

### <span data-ttu-id="9bc5d-108">範例 1：根據名稱建立 Windows 虛擬桌面工作區</span><span class="sxs-lookup"><span data-stu-id="9bc5d-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference $null `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="9bc5d-109">此命令在資源群組中建立 Windows 虛擬桌面工作區。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="9bc5d-110">範例 2：根據名稱建立 Windows 虛擬桌面工作區</span><span class="sxs-lookup"><span data-stu-id="9bc5d-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="9bc5d-111">此命令在資源群組中建立 Windows 虛擬桌面工作區。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="9bc5d-112">參數</span><span class="sxs-lookup"><span data-stu-id="9bc5d-112">PARAMETERS</span></span>

### <span data-ttu-id="9bc5d-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="9bc5d-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="9bc5d-114">應用程式Group 資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-114">List of applicationGroup resource Ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc5d-115">-DefaultProfile</span></span>
<span data-ttu-id="9bc5d-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bc5d-117">-描述</span><span class="sxs-lookup"><span data-stu-id="9bc5d-117">-Description</span></span>
<span data-ttu-id="9bc5d-118">工作區的描述。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="9bc5d-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9bc5d-119">-FriendlyName</span></span>
<span data-ttu-id="9bc5d-120">工作區的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="9bc5d-121">-位置</span><span class="sxs-lookup"><span data-stu-id="9bc5d-121">-Location</span></span>
<span data-ttu-id="9bc5d-122">資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="9bc5d-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="9bc5d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="9bc5d-123">-Name</span></span>
<span data-ttu-id="9bc5d-124">工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="9bc5d-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc5d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bc5d-125">-ResourceGroupName</span></span>
<span data-ttu-id="9bc5d-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-126">The name of the resource group.</span></span>
<span data-ttu-id="9bc5d-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9bc5d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9bc5d-128">-SubscriptionId</span></span>
<span data-ttu-id="9bc5d-129">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9bc5d-130">-標記</span><span class="sxs-lookup"><span data-stu-id="9bc5d-130">-Tag</span></span>
<span data-ttu-id="9bc5d-131">資源標記。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-131">Resource tags.</span></span>

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

### <span data-ttu-id="9bc5d-132">-確認</span><span class="sxs-lookup"><span data-stu-id="9bc5d-132">-Confirm</span></span>
<span data-ttu-id="9bc5d-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bc5d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bc5d-134">-WhatIf</span></span>
<span data-ttu-id="9bc5d-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bc5d-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bc5d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc5d-137">CommonParameters</span></span>
<span data-ttu-id="9bc5d-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9bc5d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc5d-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bc5d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc5d-140">輸入</span><span class="sxs-lookup"><span data-stu-id="9bc5d-140">INPUTS</span></span>

## <span data-ttu-id="9bc5d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="9bc5d-141">OUTPUTS</span></span>

### <span data-ttu-id="9bc5d-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="9bc5d-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="9bc5d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="9bc5d-143">NOTES</span></span>

<span data-ttu-id="9bc5d-144">別名</span><span class="sxs-lookup"><span data-stu-id="9bc5d-144">ALIASES</span></span>

## <span data-ttu-id="9bc5d-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9bc5d-145">RELATED LINKS</span></span>

