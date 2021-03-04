---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: 5b69ff6bb04f1e8b1ae5e13fbab2c6a5f7c67927
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909818"
---
# <span data-ttu-id="92e57-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="92e57-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="92e57-102">簡介</span><span class="sxs-lookup"><span data-stu-id="92e57-102">SYNOPSIS</span></span>
<span data-ttu-id="92e57-103">更新主機區。</span><span class="sxs-lookup"><span data-stu-id="92e57-103">Update a host pool.</span></span>

## <span data-ttu-id="92e57-104">語法</span><span class="sxs-lookup"><span data-stu-id="92e57-104">SYNTAX</span></span>

### <span data-ttu-id="92e57-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="92e57-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="92e57-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="92e57-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="92e57-107">描述</span><span class="sxs-lookup"><span data-stu-id="92e57-107">DESCRIPTION</span></span>
<span data-ttu-id="92e57-108">更新主機區。</span><span class="sxs-lookup"><span data-stu-id="92e57-108">Update a host pool.</span></span>

## <span data-ttu-id="92e57-109">例子</span><span class="sxs-lookup"><span data-stu-id="92e57-109">EXAMPLES</span></span>

### <span data-ttu-id="92e57-110">範例 1：根據名稱更新 Windows 虛擬桌面主機後臺</span><span class="sxs-lookup"><span data-stu-id="92e57-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Update-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -LoadBalancerType 'BreadthFirst' `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 6 `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="92e57-111">此命令會更新資源群組中的 Windows 虛擬桌面主機後臺。</span><span class="sxs-lookup"><span data-stu-id="92e57-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="92e57-112">參數</span><span class="sxs-lookup"><span data-stu-id="92e57-112">PARAMETERS</span></span>

### <span data-ttu-id="92e57-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="92e57-113">-CustomRdpProperty</span></span>
<span data-ttu-id="92e57-114">HostPool 的自訂 rdp 屬性。</span><span class="sxs-lookup"><span data-stu-id="92e57-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="92e57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e57-115">-DefaultProfile</span></span>
<span data-ttu-id="92e57-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="92e57-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92e57-117">-描述</span><span class="sxs-lookup"><span data-stu-id="92e57-117">-Description</span></span>
<span data-ttu-id="92e57-118">HostPool 的描述。</span><span class="sxs-lookup"><span data-stu-id="92e57-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="92e57-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="92e57-119">-FriendlyName</span></span>
<span data-ttu-id="92e57-120">HostPool 的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="92e57-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="92e57-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92e57-121">-InputObject</span></span>
<span data-ttu-id="92e57-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="92e57-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92e57-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="92e57-123">-LoadBalancerType</span></span>
<span data-ttu-id="92e57-124">負載平衡器的類型。</span><span class="sxs-lookup"><span data-stu-id="92e57-124">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e57-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="92e57-125">-MaxSessionLimit</span></span>
<span data-ttu-id="92e57-126">HostPool 的會話上限。</span><span class="sxs-lookup"><span data-stu-id="92e57-126">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e57-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="92e57-127">-Name</span></span>
<span data-ttu-id="92e57-128">指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="92e57-128">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e57-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="92e57-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="92e57-130">HostPool 的 PersonalDesktopAssignment 類型。</span><span class="sxs-lookup"><span data-stu-id="92e57-130">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e57-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="92e57-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="92e57-132">預設為桌面應用程式群組的偏好應用程式群組類型</span><span class="sxs-lookup"><span data-stu-id="92e57-132">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e57-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="92e57-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="92e57-134">註冊權杖的到期日。</span><span class="sxs-lookup"><span data-stu-id="92e57-134">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e57-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="92e57-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="92e57-136">重設權杖的類型。</span><span class="sxs-lookup"><span data-stu-id="92e57-136">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e57-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e57-137">-ResourceGroupName</span></span>
<span data-ttu-id="92e57-138">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92e57-138">The name of the resource group.</span></span>
<span data-ttu-id="92e57-139">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="92e57-139">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e57-140">-響鈴</span><span class="sxs-lookup"><span data-stu-id="92e57-140">-Ring</span></span>
<span data-ttu-id="92e57-141">HostPool 的響鈴號碼。</span><span class="sxs-lookup"><span data-stu-id="92e57-141">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e57-142">-SsAuthority</span><span class="sxs-lookup"><span data-stu-id="92e57-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="92e57-143">客戶 ADFS 伺服器的 URL，用於簽署 WVD SSO 憑證。</span><span class="sxs-lookup"><span data-stu-id="92e57-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="92e57-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="92e57-144">-SsoClientId</span></span>
<span data-ttu-id="92e57-145">用來發行 WVD SSO 憑證之已註冊的信賴方 ClientId。</span><span class="sxs-lookup"><span data-stu-id="92e57-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="92e57-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="92e57-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="92e57-147">儲存用於與 ADFS 通訊之機密的 Azure KeyVault 路徑。</span><span class="sxs-lookup"><span data-stu-id="92e57-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="92e57-148">-SsoCoNtext</span><span class="sxs-lookup"><span data-stu-id="92e57-148">-SsoContext</span></span>
<span data-ttu-id="92e57-149">包含 ssoCoNtext 機密的 keyvault 路徑。</span><span class="sxs-lookup"><span data-stu-id="92e57-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="92e57-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="92e57-150">-SsoSecretType</span></span>
<span data-ttu-id="92e57-151">密碼類型上的單一登入類型。</span><span class="sxs-lookup"><span data-stu-id="92e57-151">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e57-152">-StartCONNONConnect</span><span class="sxs-lookup"><span data-stu-id="92e57-152">-StartVMOnConnect</span></span>
<span data-ttu-id="92e57-153">要開啟/關閉 StartEVONConnect 功能的標誌。</span><span class="sxs-lookup"><span data-stu-id="92e57-153">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="92e57-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92e57-154">-SubscriptionId</span></span>
<span data-ttu-id="92e57-155">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="92e57-155">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e57-156">-標記</span><span class="sxs-lookup"><span data-stu-id="92e57-156">-Tag</span></span>
<span data-ttu-id="92e57-157">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="92e57-157">tags to be updated</span></span>

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

### <span data-ttu-id="92e57-158">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="92e57-158">-ValidationEnvironment</span></span>
<span data-ttu-id="92e57-159">是驗證環境。</span><span class="sxs-lookup"><span data-stu-id="92e57-159">Is validation environment.</span></span>

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

### <span data-ttu-id="92e57-160">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="92e57-160">-VMTemplate</span></span>
<span data-ttu-id="92e57-161">主機主機組內工作階段主機配置的 VM 範本。</span><span class="sxs-lookup"><span data-stu-id="92e57-161">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="92e57-162">-確認</span><span class="sxs-lookup"><span data-stu-id="92e57-162">-Confirm</span></span>
<span data-ttu-id="92e57-163">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="92e57-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92e57-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92e57-164">-WhatIf</span></span>
<span data-ttu-id="92e57-165">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92e57-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92e57-166">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92e57-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92e57-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e57-167">CommonParameters</span></span>
<span data-ttu-id="92e57-168">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="92e57-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e57-169">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92e57-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e57-170">輸入</span><span class="sxs-lookup"><span data-stu-id="92e57-170">INPUTS</span></span>

### <span data-ttu-id="92e57-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="92e57-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="92e57-172">輸出</span><span class="sxs-lookup"><span data-stu-id="92e57-172">OUTPUTS</span></span>

### <span data-ttu-id="92e57-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="92e57-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="92e57-174">筆記</span><span class="sxs-lookup"><span data-stu-id="92e57-174">NOTES</span></span>

<span data-ttu-id="92e57-175">別名</span><span class="sxs-lookup"><span data-stu-id="92e57-175">ALIASES</span></span>

<span data-ttu-id="92e57-176">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="92e57-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="92e57-177">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="92e57-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92e57-178">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="92e57-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="92e57-179">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="92e57-179">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92e57-180">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="92e57-180">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="92e57-181">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="92e57-181">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="92e57-182">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="92e57-182">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="92e57-183">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="92e57-183">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="92e57-184">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="92e57-184">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92e57-185">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="92e57-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="92e57-186">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92e57-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="92e57-187">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="92e57-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="92e57-188">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="92e57-188">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="92e57-189">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="92e57-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="92e57-190">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="92e57-190">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="92e57-191">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="92e57-191">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="92e57-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="92e57-192">RELATED LINKS</span></span>

