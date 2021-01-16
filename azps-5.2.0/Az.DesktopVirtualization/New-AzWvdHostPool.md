---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: 0eacae818861b28bfd13e0354400673b26f8e23f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278585"
---
# <span data-ttu-id="bcf5e-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="bcf5e-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="bcf5e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcf5e-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf5e-103">建立或更新主機池。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-103">Create or update a host pool.</span></span>

## <span data-ttu-id="bcf5e-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcf5e-104">SYNTAX</span></span>

### <span data-ttu-id="bcf5e-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="bcf5e-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoadfsAuthority <String>]
 [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>] [-SsoContext <String>]
 [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment] [-VMTemplate <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bcf5e-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="bcf5e-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bcf5e-107">說明</span><span class="sxs-lookup"><span data-stu-id="bcf5e-107">DESCRIPTION</span></span>
<span data-ttu-id="bcf5e-108">建立或更新主機池。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-108">Create or update a host pool.</span></span>

## <span data-ttu-id="bcf5e-109">示例</span><span class="sxs-lookup"><span data-stu-id="bcf5e-109">EXAMPLES</span></span>

### <span data-ttu-id="bcf5e-110">範例1：依名稱建立 Windows 虛擬桌面 HostPool</span><span class="sxs-lookup"><span data-stu-id="bcf5e-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="bcf5e-111">這個命令會在資源群組中建立 Windows 虛擬桌面 HostPool。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="bcf5e-112">範例1：依名稱建立 Windows 虛擬桌面 HostPool</span><span class="sxs-lookup"><span data-stu-id="bcf5e-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="bcf5e-113">這個命令會在資源群組中建立 Windows 虛擬桌面 HostPool。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="bcf5e-114">參數</span><span class="sxs-lookup"><span data-stu-id="bcf5e-114">PARAMETERS</span></span>

### <span data-ttu-id="bcf5e-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="bcf5e-115">-CustomRdpProperty</span></span>
<span data-ttu-id="bcf5e-116">HostPool 的自訂 rdp 屬性。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="bcf5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf5e-117">-DefaultProfile</span></span>
<span data-ttu-id="bcf5e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcf5e-119">-描述</span><span class="sxs-lookup"><span data-stu-id="bcf5e-119">-Description</span></span>
<span data-ttu-id="bcf5e-120">HostPool 的描述。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="bcf5e-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf5e-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="bcf5e-122">桌面應用程式群組名稱</span><span class="sxs-lookup"><span data-stu-id="bcf5e-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="bcf5e-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="bcf5e-123">-ExpirationTime</span></span>
<span data-ttu-id="bcf5e-124">註冊權杖的到期時間。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="bcf5e-125">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bcf5e-125">-FriendlyName</span></span>
<span data-ttu-id="bcf5e-126">HostPool 的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="bcf5e-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="bcf5e-127">-HostPoolType</span></span>
<span data-ttu-id="bcf5e-128">桌面的 HostPool 類型。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="bcf5e-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="bcf5e-129">-LoadBalancerType</span></span>
<span data-ttu-id="bcf5e-130">負載平衡器的類型。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="bcf5e-131">-位置</span><span class="sxs-lookup"><span data-stu-id="bcf5e-131">-Location</span></span>
<span data-ttu-id="bcf5e-132">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="bcf5e-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="bcf5e-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="bcf5e-133">-MaxSessionLimit</span></span>
<span data-ttu-id="bcf5e-134">HostPool 的最大會話限制。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="bcf5e-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcf5e-135">-Name</span></span>
<span data-ttu-id="bcf5e-136">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="bcf5e-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="bcf5e-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="bcf5e-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="bcf5e-138">HostPool 的 PersonalDesktopAssignment 類型。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="bcf5e-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="bcf5e-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="bcf5e-140">[優先] 應用程式群組類型的類型，預設為 [桌面應用程式] 群組</span><span class="sxs-lookup"><span data-stu-id="bcf5e-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="bcf5e-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="bcf5e-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="bcf5e-142">註冊權杖 base64 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="bcf5e-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="bcf5e-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="bcf5e-144">重設權杖的類型。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="bcf5e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf5e-145">-ResourceGroupName</span></span>
<span data-ttu-id="bcf5e-146">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-146">The name of the resource group.</span></span>
<span data-ttu-id="bcf5e-147">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bcf5e-148">-振鈴</span><span class="sxs-lookup"><span data-stu-id="bcf5e-148">-Ring</span></span>
<span data-ttu-id="bcf5e-149">HostPool 的響數。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="bcf5e-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="bcf5e-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="bcf5e-151">用於簽署 WVD SSO 憑證之客戶 ADFS 伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="bcf5e-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="bcf5e-152">-SsoClientId</span></span>
<span data-ttu-id="bcf5e-153">使用已登錄的信賴方來頒發 WVD SSO 憑證的 ClientId。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="bcf5e-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="bcf5e-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="bcf5e-155">Azure KeyVault 的路徑，儲存用於與 ADFS 通訊的秘密。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="bcf5e-156">-SsoCoNtext</span><span class="sxs-lookup"><span data-stu-id="bcf5e-156">-SsoContext</span></span>
<span data-ttu-id="bcf5e-157">包含 ssoCoNtext 秘密之 keyvault 的路徑。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-157">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="bcf5e-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="bcf5e-158">-SsoSecretType</span></span>
<span data-ttu-id="bcf5e-159">單一登入機密類型的類型。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-159">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="bcf5e-160">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bcf5e-160">-SubscriptionId</span></span>
<span data-ttu-id="bcf5e-161">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-161">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bcf5e-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="bcf5e-162">-Tag</span></span>
<span data-ttu-id="bcf5e-163">資源標記。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-163">Resource tags.</span></span>

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

### <span data-ttu-id="bcf5e-164">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="bcf5e-164">-ValidationEnvironment</span></span>
<span data-ttu-id="bcf5e-165">驗證環境。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-165">Is validation environment.</span></span>

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

### <span data-ttu-id="bcf5e-166">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="bcf5e-166">-VMTemplate</span></span>
<span data-ttu-id="bcf5e-167">在 hostpool 中 sessionhosts 設定的 VM 範本。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-167">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="bcf5e-168">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bcf5e-168">-WorkspaceName</span></span>
<span data-ttu-id="bcf5e-169">工作區名稱</span><span class="sxs-lookup"><span data-stu-id="bcf5e-169">Workspace Name</span></span>

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

### <span data-ttu-id="bcf5e-170">-確認</span><span class="sxs-lookup"><span data-stu-id="bcf5e-170">-Confirm</span></span>
<span data-ttu-id="bcf5e-171">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcf5e-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf5e-172">-WhatIf</span></span>
<span data-ttu-id="bcf5e-173">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcf5e-174">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcf5e-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf5e-175">CommonParameters</span></span>
<span data-ttu-id="bcf5e-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf5e-177">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf5e-178">輸入</span><span class="sxs-lookup"><span data-stu-id="bcf5e-178">INPUTS</span></span>

## <span data-ttu-id="bcf5e-179">輸出</span><span class="sxs-lookup"><span data-stu-id="bcf5e-179">OUTPUTS</span></span>

### <span data-ttu-id="bcf5e-180">IHostPool （DesktopVirtualization）。 Api20201019Preview。</span><span class="sxs-lookup"><span data-stu-id="bcf5e-180">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span></span>

## <span data-ttu-id="bcf5e-181">筆記</span><span class="sxs-lookup"><span data-stu-id="bcf5e-181">NOTES</span></span>

<span data-ttu-id="bcf5e-182">別名</span><span class="sxs-lookup"><span data-stu-id="bcf5e-182">ALIASES</span></span>

## <span data-ttu-id="bcf5e-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcf5e-183">RELATED LINKS</span></span>

