---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 0dfbcabcb1869457e29d6c16c861c0743f50dc5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284753"
---
# <span data-ttu-id="2d099-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="2d099-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="2d099-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d099-102">SYNOPSIS</span></span>
<span data-ttu-id="2d099-103">建立或更新 applicationGroup。</span><span class="sxs-lookup"><span data-stu-id="2d099-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="2d099-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d099-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2d099-105">說明</span><span class="sxs-lookup"><span data-stu-id="2d099-105">DESCRIPTION</span></span>
<span data-ttu-id="2d099-106">建立或更新 applicationGroup。</span><span class="sxs-lookup"><span data-stu-id="2d099-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="2d099-107">示例</span><span class="sxs-lookup"><span data-stu-id="2d099-107">EXAMPLES</span></span>

### <span data-ttu-id="2d099-108">範例1：依名稱建立 Windows 虛擬桌面 ApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="2d099-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'RemoteApp'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="2d099-109">這個命令會在資源群組中建立 Windows 虛擬桌面 ApplicationGroup。</span><span class="sxs-lookup"><span data-stu-id="2d099-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="2d099-110">範例2：依名稱建立 Windows 虛擬桌面 ApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="2d099-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'Desktop'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="2d099-111">這個命令會在資源群組中建立 Windows 虛擬桌面 ApplicationGroup。</span><span class="sxs-lookup"><span data-stu-id="2d099-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="2d099-112">參數</span><span class="sxs-lookup"><span data-stu-id="2d099-112">PARAMETERS</span></span>

### <span data-ttu-id="2d099-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="2d099-113">-ApplicationGroupType</span></span>
<span data-ttu-id="2d099-114">ApplicationGroup 的資源類型。</span><span class="sxs-lookup"><span data-stu-id="2d099-114">Resource Type of ApplicationGroup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.ApplicationGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d099-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d099-115">-DefaultProfile</span></span>
<span data-ttu-id="2d099-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d099-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d099-117">-描述</span><span class="sxs-lookup"><span data-stu-id="2d099-117">-Description</span></span>
<span data-ttu-id="2d099-118">ApplicationGroup 的描述。</span><span class="sxs-lookup"><span data-stu-id="2d099-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="2d099-119">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2d099-119">-FriendlyName</span></span>
<span data-ttu-id="2d099-120">ApplicationGroup 的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="2d099-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="2d099-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="2d099-121">-HostPoolArmPath</span></span>
<span data-ttu-id="2d099-122">ApplicationGroup 的 HostPool 臂路徑。</span><span class="sxs-lookup"><span data-stu-id="2d099-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="2d099-123">-位置</span><span class="sxs-lookup"><span data-stu-id="2d099-123">-Location</span></span>
<span data-ttu-id="2d099-124">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="2d099-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="2d099-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="2d099-125">-Name</span></span>
<span data-ttu-id="2d099-126">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="2d099-126">The name of the application group</span></span>

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

### <span data-ttu-id="2d099-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d099-127">-ResourceGroupName</span></span>
<span data-ttu-id="2d099-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d099-128">The name of the resource group.</span></span>
<span data-ttu-id="2d099-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2d099-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2d099-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d099-130">-SubscriptionId</span></span>
<span data-ttu-id="2d099-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="2d099-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2d099-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d099-132">-Tag</span></span>
<span data-ttu-id="2d099-133">資源標記。</span><span class="sxs-lookup"><span data-stu-id="2d099-133">Resource tags.</span></span>

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

### <span data-ttu-id="2d099-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2d099-134">-Confirm</span></span>
<span data-ttu-id="2d099-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2d099-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d099-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d099-136">-WhatIf</span></span>
<span data-ttu-id="2d099-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d099-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d099-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d099-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d099-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d099-139">CommonParameters</span></span>
<span data-ttu-id="2d099-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d099-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d099-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2d099-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d099-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2d099-142">INPUTS</span></span>

## <span data-ttu-id="2d099-143">輸出</span><span class="sxs-lookup"><span data-stu-id="2d099-143">OUTPUTS</span></span>

### <span data-ttu-id="2d099-144">IApplicationGroup （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="2d099-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="2d099-145">筆記</span><span class="sxs-lookup"><span data-stu-id="2d099-145">NOTES</span></span>

<span data-ttu-id="2d099-146">別名</span><span class="sxs-lookup"><span data-stu-id="2d099-146">ALIASES</span></span>

## <span data-ttu-id="2d099-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d099-147">RELATED LINKS</span></span>

