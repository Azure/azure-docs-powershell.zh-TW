---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: b97db1a21afab939e94b776b3da8d43f3d1468b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438552"
---
# <span data-ttu-id="763b6-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="763b6-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="763b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="763b6-102">SYNOPSIS</span></span>
<span data-ttu-id="763b6-103">建立或更新工作區。</span><span class="sxs-lookup"><span data-stu-id="763b6-103">Create or update a workspace.</span></span>

## <span data-ttu-id="763b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="763b6-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="763b6-105">說明</span><span class="sxs-lookup"><span data-stu-id="763b6-105">DESCRIPTION</span></span>
<span data-ttu-id="763b6-106">建立或更新工作區。</span><span class="sxs-lookup"><span data-stu-id="763b6-106">Create or update a workspace.</span></span>

## <span data-ttu-id="763b6-107">示例</span><span class="sxs-lookup"><span data-stu-id="763b6-107">EXAMPLES</span></span>

### <span data-ttu-id="763b6-108">範例1：依名稱建立 Windows 虛擬桌面工作區</span><span class="sxs-lookup"><span data-stu-id="763b6-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="763b6-109">這個命令會在資源群組中建立 Windows 虛擬桌面工作區。</span><span class="sxs-lookup"><span data-stu-id="763b6-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="763b6-110">範例2：依名稱建立 Windows 虛擬桌面工作區</span><span class="sxs-lookup"><span data-stu-id="763b6-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="763b6-111">這個命令會在資源群組中建立 Windows 虛擬桌面工作區。</span><span class="sxs-lookup"><span data-stu-id="763b6-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="763b6-112">參數</span><span class="sxs-lookup"><span data-stu-id="763b6-112">PARAMETERS</span></span>

### <span data-ttu-id="763b6-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="763b6-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="763b6-114">ApplicationGroup 資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="763b6-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="763b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="763b6-115">-DefaultProfile</span></span>
<span data-ttu-id="763b6-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="763b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="763b6-117">-描述</span><span class="sxs-lookup"><span data-stu-id="763b6-117">-Description</span></span>
<span data-ttu-id="763b6-118">工作區的描述。</span><span class="sxs-lookup"><span data-stu-id="763b6-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="763b6-119">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="763b6-119">-FriendlyName</span></span>
<span data-ttu-id="763b6-120">工作區的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="763b6-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="763b6-121">-位置</span><span class="sxs-lookup"><span data-stu-id="763b6-121">-Location</span></span>
<span data-ttu-id="763b6-122">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="763b6-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="763b6-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="763b6-123">-Name</span></span>
<span data-ttu-id="763b6-124">工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="763b6-124">The name of the workspace</span></span>

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

### <span data-ttu-id="763b6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="763b6-125">-ResourceGroupName</span></span>
<span data-ttu-id="763b6-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="763b6-126">The name of the resource group.</span></span>
<span data-ttu-id="763b6-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="763b6-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="763b6-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="763b6-128">-SubscriptionId</span></span>
<span data-ttu-id="763b6-129">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="763b6-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="763b6-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="763b6-130">-Tag</span></span>
<span data-ttu-id="763b6-131">資源標記。</span><span class="sxs-lookup"><span data-stu-id="763b6-131">Resource tags.</span></span>

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

### <span data-ttu-id="763b6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="763b6-132">-Confirm</span></span>
<span data-ttu-id="763b6-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="763b6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="763b6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="763b6-134">-WhatIf</span></span>
<span data-ttu-id="763b6-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="763b6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="763b6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="763b6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="763b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="763b6-137">CommonParameters</span></span>
<span data-ttu-id="763b6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="763b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="763b6-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="763b6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="763b6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="763b6-140">INPUTS</span></span>

## <span data-ttu-id="763b6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="763b6-141">OUTPUTS</span></span>

### <span data-ttu-id="763b6-142">IWorkspace （DesktopVirtualization）。 Api20201102Preview。</span><span class="sxs-lookup"><span data-stu-id="763b6-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="763b6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="763b6-143">NOTES</span></span>

<span data-ttu-id="763b6-144">別名</span><span class="sxs-lookup"><span data-stu-id="763b6-144">ALIASES</span></span>

## <span data-ttu-id="763b6-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="763b6-145">RELATED LINKS</span></span>

