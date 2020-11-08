---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: b91332fe8867283b5fff9cbbf1f5df96209fa2f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969237"
---
# <span data-ttu-id="eaf3a-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="eaf3a-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="eaf3a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eaf3a-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf3a-103">建立或更新主機池。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-103">Create or update a host pool.</span></span>

## <span data-ttu-id="eaf3a-104">句法</span><span class="sxs-lookup"><span data-stu-id="eaf3a-104">SYNTAX</span></span>

### <span data-ttu-id="eaf3a-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="eaf3a-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoContext <String>]
 [-Tag <Hashtable>] [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eaf3a-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="eaf3a-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eaf3a-107">說明</span><span class="sxs-lookup"><span data-stu-id="eaf3a-107">DESCRIPTION</span></span>
<span data-ttu-id="eaf3a-108">建立或更新主機池。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-108">Create or update a host pool.</span></span>

## <span data-ttu-id="eaf3a-109">示例</span><span class="sxs-lookup"><span data-stu-id="eaf3a-109">EXAMPLES</span></span>

### <span data-ttu-id="eaf3a-110">範例1：依名稱建立 Windows 虛擬桌面 HostPool</span><span class="sxs-lookup"><span data-stu-id="eaf3a-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Pooled' `
                            -LoadBalancerType 'DepthFirst' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="eaf3a-111">這個命令會在資源群組中建立 Windows 虛擬桌面 HostPool。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="eaf3a-112">範例1：依名稱建立 Windows 虛擬桌面 HostPool</span><span class="sxs-lookup"><span data-stu-id="eaf3a-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Personal' `
                            -LoadBalancerType 'Persistent' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="eaf3a-113">這個命令會在資源群組中建立 Windows 虛擬桌面 HostPool。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="eaf3a-114">參數</span><span class="sxs-lookup"><span data-stu-id="eaf3a-114">PARAMETERS</span></span>

### <span data-ttu-id="eaf3a-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="eaf3a-115">-CustomRdpProperty</span></span>
<span data-ttu-id="eaf3a-116">HostPool 的自訂 rdp 屬性。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="eaf3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf3a-117">-DefaultProfile</span></span>
<span data-ttu-id="eaf3a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaf3a-119">-描述</span><span class="sxs-lookup"><span data-stu-id="eaf3a-119">-Description</span></span>
<span data-ttu-id="eaf3a-120">HostPool 的描述。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="eaf3a-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf3a-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="eaf3a-122">桌面應用程式群組名稱</span><span class="sxs-lookup"><span data-stu-id="eaf3a-122">Desktop App Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf3a-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="eaf3a-123">-ExpirationTime</span></span>
<span data-ttu-id="eaf3a-124">註冊權杖的到期時間。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-124">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf3a-125">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="eaf3a-125">-FriendlyName</span></span>
<span data-ttu-id="eaf3a-126">HostPool 的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="eaf3a-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="eaf3a-127">-HostPoolType</span></span>
<span data-ttu-id="eaf3a-128">桌面的 HostPool 類型。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-128">HostPool type for desktop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.HostPoolType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf3a-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="eaf3a-129">-LoadBalancerType</span></span>
<span data-ttu-id="eaf3a-130">負載平衡器的類型。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-130">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf3a-131">-位置</span><span class="sxs-lookup"><span data-stu-id="eaf3a-131">-Location</span></span>
<span data-ttu-id="eaf3a-132">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="eaf3a-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="eaf3a-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="eaf3a-133">-MaxSessionLimit</span></span>
<span data-ttu-id="eaf3a-134">HostPool 的最大會話限制。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="eaf3a-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="eaf3a-135">-Name</span></span>
<span data-ttu-id="eaf3a-136">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="eaf3a-136">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf3a-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="eaf3a-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="eaf3a-138">HostPool 的 PersonalDesktopAssignment 類型。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-138">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf3a-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="eaf3a-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="eaf3a-140">[優先] 應用程式群組類型的類型，預設為 [桌面應用程式] 群組</span><span class="sxs-lookup"><span data-stu-id="eaf3a-140">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf3a-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="eaf3a-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="eaf3a-142">註冊權杖 base64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="eaf3a-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="eaf3a-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="eaf3a-144">重設權杖的類型。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-144">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf3a-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf3a-145">-ResourceGroupName</span></span>
<span data-ttu-id="eaf3a-146">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-146">The name of the resource group.</span></span>
<span data-ttu-id="eaf3a-147">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="eaf3a-148">-振鈴</span><span class="sxs-lookup"><span data-stu-id="eaf3a-148">-Ring</span></span>
<span data-ttu-id="eaf3a-149">HostPool 的響數。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="eaf3a-150">-SsoCoNtext</span><span class="sxs-lookup"><span data-stu-id="eaf3a-150">-SsoContext</span></span>
<span data-ttu-id="eaf3a-151">包含 ssoCoNtext 秘密之 keyvault 的路徑。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-151">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="eaf3a-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eaf3a-152">-SubscriptionId</span></span>
<span data-ttu-id="eaf3a-153">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-153">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="eaf3a-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="eaf3a-154">-Tag</span></span>
<span data-ttu-id="eaf3a-155">資源標記。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-155">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf3a-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="eaf3a-156">-ValidationEnvironment</span></span>
<span data-ttu-id="eaf3a-157">驗證環境。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-157">Is validation environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf3a-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="eaf3a-158">-VMTemplate</span></span>
<span data-ttu-id="eaf3a-159">在 hostpool 中 sessionhosts 設定的 VM 範本。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-159">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="eaf3a-160">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eaf3a-160">-WorkspaceName</span></span>
<span data-ttu-id="eaf3a-161">工作區名稱</span><span class="sxs-lookup"><span data-stu-id="eaf3a-161">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf3a-162">-確認</span><span class="sxs-lookup"><span data-stu-id="eaf3a-162">-Confirm</span></span>
<span data-ttu-id="eaf3a-163">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf3a-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf3a-164">-WhatIf</span></span>
<span data-ttu-id="eaf3a-165">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaf3a-166">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf3a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf3a-167">CommonParameters</span></span>
<span data-ttu-id="eaf3a-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf3a-169">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf3a-170">輸入</span><span class="sxs-lookup"><span data-stu-id="eaf3a-170">INPUTS</span></span>

## <span data-ttu-id="eaf3a-171">輸出</span><span class="sxs-lookup"><span data-stu-id="eaf3a-171">OUTPUTS</span></span>

### <span data-ttu-id="eaf3a-172">IHostPool （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="eaf3a-172">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="eaf3a-173">筆記</span><span class="sxs-lookup"><span data-stu-id="eaf3a-173">NOTES</span></span>

<span data-ttu-id="eaf3a-174">別名</span><span class="sxs-lookup"><span data-stu-id="eaf3a-174">ALIASES</span></span>

## <span data-ttu-id="eaf3a-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="eaf3a-175">RELATED LINKS</span></span>

