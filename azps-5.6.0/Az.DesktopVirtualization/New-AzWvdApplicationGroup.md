---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 38292351f091528ef4e153f9374dff75ccbfe941
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905461"
---
# <span data-ttu-id="b91f2-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="b91f2-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="b91f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b91f2-102">SYNOPSIS</span></span>
<span data-ttu-id="b91f2-103">建立或更新應用程式工作組。</span><span class="sxs-lookup"><span data-stu-id="b91f2-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="b91f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="b91f2-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b91f2-105">描述</span><span class="sxs-lookup"><span data-stu-id="b91f2-105">DESCRIPTION</span></span>
<span data-ttu-id="b91f2-106">建立或更新應用程式組。</span><span class="sxs-lookup"><span data-stu-id="b91f2-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="b91f2-107">例子</span><span class="sxs-lookup"><span data-stu-id="b91f2-107">EXAMPLES</span></span>

### <span data-ttu-id="b91f2-108">範例 1：根據名稱建立 Windows 虛擬桌面應用程式組</span><span class="sxs-lookup"><span data-stu-id="b91f2-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="b91f2-109">此命令在資源群組中建立 Windows 虛擬桌面應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="b91f2-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="b91f2-110">範例 2：根據名稱建立 Windows 虛擬桌面應用程式組</span><span class="sxs-lookup"><span data-stu-id="b91f2-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="b91f2-111">此命令在資源群組中建立 Windows 虛擬桌面應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="b91f2-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="b91f2-112">參數</span><span class="sxs-lookup"><span data-stu-id="b91f2-112">PARAMETERS</span></span>

### <span data-ttu-id="b91f2-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="b91f2-113">-ApplicationGroupType</span></span>
<span data-ttu-id="b91f2-114">ApplicationGroup 的資源類型。</span><span class="sxs-lookup"><span data-stu-id="b91f2-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="b91f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b91f2-115">-DefaultProfile</span></span>
<span data-ttu-id="b91f2-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b91f2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b91f2-117">-描述</span><span class="sxs-lookup"><span data-stu-id="b91f2-117">-Description</span></span>
<span data-ttu-id="b91f2-118">ApplicationGroup 的描述。</span><span class="sxs-lookup"><span data-stu-id="b91f2-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="b91f2-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b91f2-119">-FriendlyName</span></span>
<span data-ttu-id="b91f2-120">ApplicationGroup 的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="b91f2-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="b91f2-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="b91f2-121">-HostPoolArmPath</span></span>
<span data-ttu-id="b91f2-122">ApplicationGroup 的 HostPool arm 路徑。</span><span class="sxs-lookup"><span data-stu-id="b91f2-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="b91f2-123">-位置</span><span class="sxs-lookup"><span data-stu-id="b91f2-123">-Location</span></span>
<span data-ttu-id="b91f2-124">資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="b91f2-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="b91f2-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b91f2-125">-Name</span></span>
<span data-ttu-id="b91f2-126">應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="b91f2-126">The name of the application group</span></span>

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

### <span data-ttu-id="b91f2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b91f2-127">-ResourceGroupName</span></span>
<span data-ttu-id="b91f2-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b91f2-128">The name of the resource group.</span></span>
<span data-ttu-id="b91f2-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b91f2-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b91f2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b91f2-130">-SubscriptionId</span></span>
<span data-ttu-id="b91f2-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b91f2-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b91f2-132">-標記</span><span class="sxs-lookup"><span data-stu-id="b91f2-132">-Tag</span></span>
<span data-ttu-id="b91f2-133">資源標記。</span><span class="sxs-lookup"><span data-stu-id="b91f2-133">Resource tags.</span></span>

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

### <span data-ttu-id="b91f2-134">-確認</span><span class="sxs-lookup"><span data-stu-id="b91f2-134">-Confirm</span></span>
<span data-ttu-id="b91f2-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b91f2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b91f2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b91f2-136">-WhatIf</span></span>
<span data-ttu-id="b91f2-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b91f2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b91f2-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b91f2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b91f2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b91f2-139">CommonParameters</span></span>
<span data-ttu-id="b91f2-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b91f2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b91f2-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b91f2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b91f2-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b91f2-142">INPUTS</span></span>

## <span data-ttu-id="b91f2-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b91f2-143">OUTPUTS</span></span>

### <span data-ttu-id="b91f2-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="b91f2-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="b91f2-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b91f2-145">NOTES</span></span>

<span data-ttu-id="b91f2-146">別名</span><span class="sxs-lookup"><span data-stu-id="b91f2-146">ALIASES</span></span>

## <span data-ttu-id="b91f2-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="b91f2-147">RELATED LINKS</span></span>

