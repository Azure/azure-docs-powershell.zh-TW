---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: d90c81e307d56272fb9808760ef969705decb5d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905462"
---
# <span data-ttu-id="03a89-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="03a89-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="03a89-102">簡介</span><span class="sxs-lookup"><span data-stu-id="03a89-102">SYNOPSIS</span></span>
<span data-ttu-id="03a89-103">建立或更新主機主機區。</span><span class="sxs-lookup"><span data-stu-id="03a89-103">Create or update a host pool.</span></span>

## <span data-ttu-id="03a89-104">語法</span><span class="sxs-lookup"><span data-stu-id="03a89-104">SYNTAX</span></span>

### <span data-ttu-id="03a89-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="03a89-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoadfsAuthority <String>]
 [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>] [-SsoContext <String>]
 [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="03a89-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="03a89-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="03a89-107">描述</span><span class="sxs-lookup"><span data-stu-id="03a89-107">DESCRIPTION</span></span>
<span data-ttu-id="03a89-108">建立或更新主機主機區。</span><span class="sxs-lookup"><span data-stu-id="03a89-108">Create or update a host pool.</span></span>

## <span data-ttu-id="03a89-109">例子</span><span class="sxs-lookup"><span data-stu-id="03a89-109">EXAMPLES</span></span>

### <span data-ttu-id="03a89-110">範例 1：根據名稱建立 Windows 虛擬桌面 HostPool</span><span class="sxs-lookup"><span data-stu-id="03a89-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="03a89-111">此命令在資源群組中建立 Windows 虛擬桌面主機後臺。</span><span class="sxs-lookup"><span data-stu-id="03a89-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="03a89-112">範例 1：根據名稱建立 Windows 虛擬桌面 HostPool</span><span class="sxs-lookup"><span data-stu-id="03a89-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="03a89-113">此命令在資源群組中建立 Windows 虛擬桌面主機後臺。</span><span class="sxs-lookup"><span data-stu-id="03a89-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="03a89-114">參數</span><span class="sxs-lookup"><span data-stu-id="03a89-114">PARAMETERS</span></span>

### <span data-ttu-id="03a89-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="03a89-115">-CustomRdpProperty</span></span>
<span data-ttu-id="03a89-116">HostPool 的自訂 rdp 屬性。</span><span class="sxs-lookup"><span data-stu-id="03a89-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="03a89-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a89-117">-DefaultProfile</span></span>
<span data-ttu-id="03a89-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="03a89-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03a89-119">-描述</span><span class="sxs-lookup"><span data-stu-id="03a89-119">-Description</span></span>
<span data-ttu-id="03a89-120">HostPool 的描述。</span><span class="sxs-lookup"><span data-stu-id="03a89-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="03a89-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="03a89-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="03a89-122">桌面應用程式組名</span><span class="sxs-lookup"><span data-stu-id="03a89-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="03a89-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="03a89-123">-ExpirationTime</span></span>
<span data-ttu-id="03a89-124">註冊權杖的到期日。</span><span class="sxs-lookup"><span data-stu-id="03a89-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="03a89-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="03a89-125">-FriendlyName</span></span>
<span data-ttu-id="03a89-126">HostPool 的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="03a89-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="03a89-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="03a89-127">-HostPoolType</span></span>
<span data-ttu-id="03a89-128">桌上出版 HostPool 類型。</span><span class="sxs-lookup"><span data-stu-id="03a89-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="03a89-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="03a89-129">-LoadBalancerType</span></span>
<span data-ttu-id="03a89-130">負載平衡器的類型。</span><span class="sxs-lookup"><span data-stu-id="03a89-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="03a89-131">-位置</span><span class="sxs-lookup"><span data-stu-id="03a89-131">-Location</span></span>
<span data-ttu-id="03a89-132">資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="03a89-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="03a89-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="03a89-133">-MaxSessionLimit</span></span>
<span data-ttu-id="03a89-134">HostPool 的會話上限。</span><span class="sxs-lookup"><span data-stu-id="03a89-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="03a89-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="03a89-135">-Name</span></span>
<span data-ttu-id="03a89-136">指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="03a89-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="03a89-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="03a89-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="03a89-138">HostPool 的 PersonalDesktopAssignment 類型。</span><span class="sxs-lookup"><span data-stu-id="03a89-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="03a89-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="03a89-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="03a89-140">預設為桌面應用程式群組的偏好應用程式群組類型</span><span class="sxs-lookup"><span data-stu-id="03a89-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="03a89-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="03a89-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="03a89-142">登錄權杖底數為 64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="03a89-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="03a89-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="03a89-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="03a89-144">重設權杖的類型。</span><span class="sxs-lookup"><span data-stu-id="03a89-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="03a89-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03a89-145">-ResourceGroupName</span></span>
<span data-ttu-id="03a89-146">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="03a89-146">The name of the resource group.</span></span>
<span data-ttu-id="03a89-147">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="03a89-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="03a89-148">-響鈴</span><span class="sxs-lookup"><span data-stu-id="03a89-148">-Ring</span></span>
<span data-ttu-id="03a89-149">HostPool 的響鈴號碼。</span><span class="sxs-lookup"><span data-stu-id="03a89-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="03a89-150">-SsAuthority</span><span class="sxs-lookup"><span data-stu-id="03a89-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="03a89-151">客戶 ADFS 伺服器的 URL，用於簽署 WVD SSO 憑證。</span><span class="sxs-lookup"><span data-stu-id="03a89-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="03a89-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="03a89-152">-SsoClientId</span></span>
<span data-ttu-id="03a89-153">用來發行 WVD SSO 憑證之已註冊的信賴方 ClientId。</span><span class="sxs-lookup"><span data-stu-id="03a89-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="03a89-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="03a89-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="03a89-155">儲存用於與 ADFS 通訊之機密的 Azure KeyVault 路徑。</span><span class="sxs-lookup"><span data-stu-id="03a89-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="03a89-156">-SsoCoNtext</span><span class="sxs-lookup"><span data-stu-id="03a89-156">-SsoContext</span></span>
<span data-ttu-id="03a89-157">包含 ssoCoNtext 機密的 keyvault 路徑。</span><span class="sxs-lookup"><span data-stu-id="03a89-157">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="03a89-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="03a89-158">-SsoSecretType</span></span>
<span data-ttu-id="03a89-159">密碼類型上的單一登入類型。</span><span class="sxs-lookup"><span data-stu-id="03a89-159">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a89-160">-StartCONNONConnect</span><span class="sxs-lookup"><span data-stu-id="03a89-160">-StartVMOnConnect</span></span>
<span data-ttu-id="03a89-161">要開啟/關閉 StartEVONConnect 功能的標誌。</span><span class="sxs-lookup"><span data-stu-id="03a89-161">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="03a89-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03a89-162">-SubscriptionId</span></span>
<span data-ttu-id="03a89-163">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="03a89-163">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="03a89-164">-標記</span><span class="sxs-lookup"><span data-stu-id="03a89-164">-Tag</span></span>
<span data-ttu-id="03a89-165">資源標記。</span><span class="sxs-lookup"><span data-stu-id="03a89-165">Resource tags.</span></span>

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

### <span data-ttu-id="03a89-166">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="03a89-166">-ValidationEnvironment</span></span>
<span data-ttu-id="03a89-167">是驗證環境。</span><span class="sxs-lookup"><span data-stu-id="03a89-167">Is validation environment.</span></span>

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

### <span data-ttu-id="03a89-168">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="03a89-168">-VMTemplate</span></span>
<span data-ttu-id="03a89-169">主機主機組內工作階段主機配置的 VM 範本。</span><span class="sxs-lookup"><span data-stu-id="03a89-169">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="03a89-170">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="03a89-170">-WorkspaceName</span></span>
<span data-ttu-id="03a89-171">工作區名稱</span><span class="sxs-lookup"><span data-stu-id="03a89-171">Workspace Name</span></span>

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

### <span data-ttu-id="03a89-172">-確認</span><span class="sxs-lookup"><span data-stu-id="03a89-172">-Confirm</span></span>
<span data-ttu-id="03a89-173">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="03a89-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03a89-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03a89-174">-WhatIf</span></span>
<span data-ttu-id="03a89-175">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03a89-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03a89-176">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03a89-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03a89-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a89-177">CommonParameters</span></span>
<span data-ttu-id="03a89-178">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="03a89-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a89-179">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03a89-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a89-180">輸入</span><span class="sxs-lookup"><span data-stu-id="03a89-180">INPUTS</span></span>

## <span data-ttu-id="03a89-181">輸出</span><span class="sxs-lookup"><span data-stu-id="03a89-181">OUTPUTS</span></span>

### <span data-ttu-id="03a89-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="03a89-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="03a89-183">筆記</span><span class="sxs-lookup"><span data-stu-id="03a89-183">NOTES</span></span>

<span data-ttu-id="03a89-184">別名</span><span class="sxs-lookup"><span data-stu-id="03a89-184">ALIASES</span></span>

## <span data-ttu-id="03a89-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="03a89-185">RELATED LINKS</span></span>

