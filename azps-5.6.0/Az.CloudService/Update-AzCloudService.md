---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: bb67420e3fbb4479a79c7a837aad3b9a65635d88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916249"
---
# <span data-ttu-id="5b0e9-101">Update-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="5b0e9-101">Update-AzCloudService</span></span>

## <span data-ttu-id="5b0e9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5b0e9-102">SYNOPSIS</span></span>
<span data-ttu-id="5b0e9-103">建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-103">Create or update a cloud service.</span></span>
<span data-ttu-id="5b0e9-104">請注意，某些屬性只能在建立雲端服務期間設定。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="5b0e9-105">語法</span><span class="sxs-lookup"><span data-stu-id="5b0e9-105">SYNTAX</span></span>

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5b0e9-106">描述</span><span class="sxs-lookup"><span data-stu-id="5b0e9-106">DESCRIPTION</span></span>
<span data-ttu-id="5b0e9-107">建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-107">Create or update a cloud service.</span></span>
<span data-ttu-id="5b0e9-108">請注意，某些屬性只能在建立雲端服務期間設定。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="5b0e9-109">例子</span><span class="sxs-lookup"><span data-stu-id="5b0e9-109">EXAMPLES</span></span>

### <span data-ttu-id="5b0e9-110">範例 1：新增 RDP 擴充功能至現有的雲端服務</span><span class="sxs-lookup"><span data-stu-id="5b0e9-110">Example 1: Add RDP extension to existing cloud service</span></span>
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="5b0e9-111">上述一組命令會將 RDP 擴充功能新增到現有的名為 ContosoCS 的雲端服務，該服務屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-111">Above set of commands adds a RDP extension to already existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="5b0e9-112">範例 2：從雲端服務移除所有延伸模組</span><span class="sxs-lookup"><span data-stu-id="5b0e9-112">Example 2: Remove all extensions from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="5b0e9-113">上述一組命令會從名為 ContosoCS 的現有雲端服務移除所有屬於 ContosOrg 資源群組的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-113">Above set of commands removes all extensions from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="5b0e9-114">範例 3：從雲端服務移除 RDP 擴充功能</span><span class="sxs-lookup"><span data-stu-id="5b0e9-114">Example 3: Remove RDP extension from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="5b0e9-115">上述一組命令會從名為 ContosoCS 的現有雲端服務移除 RDP 副檔名，該服務屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-115">Above set of commands removes RDP extension from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="5b0e9-116">範例 4：Scale-Out / Scale-In角色實例</span><span class="sxs-lookup"><span data-stu-id="5b0e9-116">Example 4: Scale-Out / Scale-In role instances</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="5b0e9-117">上述命令集顯示如何針對屬於 ContosOrg 資源群組的名為 ContosoCS 的雲端服務，進行縮小和縮放角色實例計數。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-117">Above set of commands shows how to scale-out and scale-in role instance count for cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="5b0e9-118">參數</span><span class="sxs-lookup"><span data-stu-id="5b0e9-118">PARAMETERS</span></span>

### <span data-ttu-id="5b0e9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b0e9-119">-AsJob</span></span>
<span data-ttu-id="5b0e9-120">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="5b0e9-120">Run the command as a job</span></span>

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

### <span data-ttu-id="5b0e9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b0e9-121">-DefaultProfile</span></span>
<span data-ttu-id="5b0e9-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b0e9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b0e9-123">-InputObject</span></span>
<span data-ttu-id="5b0e9-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e9-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5b0e9-125">-NoWait</span></span>
<span data-ttu-id="5b0e9-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="5b0e9-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5b0e9-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="5b0e9-127">-Parameter</span></span>
<span data-ttu-id="5b0e9-128">說明雲端服務。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-128">Describes the cloud service.</span></span>
<span data-ttu-id="5b0e9-129">若要建構，請參閱 PARAMETER 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-129">To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e9-130">-確認</span><span class="sxs-lookup"><span data-stu-id="5b0e9-130">-Confirm</span></span>
<span data-ttu-id="5b0e9-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b0e9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b0e9-132">-WhatIf</span></span>
<span data-ttu-id="5b0e9-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b0e9-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b0e9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b0e9-135">CommonParameters</span></span>
<span data-ttu-id="5b0e9-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b0e9-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b0e9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b0e9-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5b0e9-138">INPUTS</span></span>

### <span data-ttu-id="5b0e9-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="5b0e9-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

### <span data-ttu-id="5b0e9-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.iCloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="5b0e9-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="5b0e9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5b0e9-141">OUTPUTS</span></span>

### <span data-ttu-id="5b0e9-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="5b0e9-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="5b0e9-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5b0e9-143">NOTES</span></span>

<span data-ttu-id="5b0e9-144">別名</span><span class="sxs-lookup"><span data-stu-id="5b0e9-144">ALIASES</span></span>

<span data-ttu-id="5b0e9-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5b0e9-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5b0e9-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b0e9-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5b0e9-148">INPUTOBJECT： <ICloudServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5b0e9-148">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b0e9-149">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="5b0e9-149">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="5b0e9-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="5b0e9-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b0e9-151">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="5b0e9-151">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="5b0e9-152">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-152">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="5b0e9-153">`[RoleName <String>]`：角色名稱。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-153">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="5b0e9-154">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5b0e9-155">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-155">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5b0e9-156">`[UpdateDomain <Int32?>]`：指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-156">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="5b0e9-157">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-157">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

<span data-ttu-id="5b0e9-158"><ICloudService>PARAMETER：說明雲端服務。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-158">PARAMETER <ICloudService>: Describes the cloud service.</span></span>
  - <span data-ttu-id="5b0e9-159">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-159">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="5b0e9-160">`[Configuration <String>]`：指定雲端 (.csc) XML 服務組配置。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-160">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="5b0e9-161">`[ConfigurationUrl <String>]`：指定一個 URL，該 URL 參照到 Blob 服務中的服務群組原則位置。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-161">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="5b0e9-162">服務套件 URL 可以是來自任何儲存帳戶 (SAS) URI 的共用存取簽名。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-162">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="5b0e9-163">這是只寫入的屬性，不會在 GET 通話中返回。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-163">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="5b0e9-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`：說明雲端服務擴充功能設定檔。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="5b0e9-165">`[Extension <IExtension[]>]`：雲端服務的擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-165">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="5b0e9-166">`[AutoUpgradeMinorVersion <Boolean?>]`：明確指定平臺是否可以在提供類型HandlerVersion時自動升級至較高的次要版本。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-166">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="5b0e9-167">`[ForceUpdateTag <String>]`：標記以強制使用提供的公用和受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-167">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="5b0e9-168">變更標記值可讓您重新經營擴充功能，而不需要變更任何公用或受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-168">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="5b0e9-169">如果未變更 forceUpdateTag，處理常式仍然會使用公用或受保護的設定更新。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-169">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="5b0e9-170">如果 forceUpdateTag 或任何公用或受保護的設定都沒有變更，延伸模組會流向具有相同序號的角色實例，而是否要重新執行，則由處理常式的執行方式決定</span><span class="sxs-lookup"><span data-stu-id="5b0e9-170">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="5b0e9-171">`[Name <String>]`：副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-171">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="5b0e9-172">`[ProtectedSetting <String>]`：已加密的擴充功能之受保護的設定，在送往角色實例之前。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-172">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="5b0e9-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="5b0e9-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="5b0e9-174">`[Publisher <String>]`：副檔名處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-174">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="5b0e9-175">`[RolesAppliedTo <String[]>]`：可申請此擴充功能的角色清單。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-175">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="5b0e9-176">如果未指定屬性或指定 '\*'，延伸模組會適用于雲端服務中的所有角色。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-176">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="5b0e9-177">`[Setting <String>]`：擴充功能公用設定。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-177">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="5b0e9-178">對於 JSON 擴充功能，這是該擴充功能 JSON 設定。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-178">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="5b0e9-179">對於 XML 擴充 (如 RDP) ，這是該副檔名的 XML 設定。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-179">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="5b0e9-180">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5b0e9-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="5b0e9-181">`[Type <String>]`：指定擴充功能的類型。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-181">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="5b0e9-182">`[TypeHandlerVersion <String>]`：指定擴充功能的版本。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-182">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="5b0e9-183">指定擴充功能的版本。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-183">Specifies the version of the extension.</span></span> <span data-ttu-id="5b0e9-184">如果未指定此元素，或是使用星號 (\*) 做為值，則使用最新版本的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-184">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="5b0e9-185">如果以主要版本號碼和星號指定值做為次要版本號碼 (X.) ，會選取指定主要版本的最新次要版本。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-185">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="5b0e9-186">如果在 X.Y (指定主要版本號碼和次要版本號碼) ，會選取特定的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-186">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="5b0e9-187">如果指定版本，系統即會對角色實例執行自動升級。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-187">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="5b0e9-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`：雲端服務的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="5b0e9-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`：雲端服務的負載平衡器組組清單。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="5b0e9-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`：IP 清單</span><span class="sxs-lookup"><span data-stu-id="5b0e9-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="5b0e9-191">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="5b0e9-191">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="5b0e9-192">`[PrivateIPAddress <String>]`：雲端服務所參照的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-192">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="5b0e9-193">`[PublicIPAddressId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5b0e9-193">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="5b0e9-194">`[SubnetId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5b0e9-194">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="5b0e9-195">`[Name <String>]`：資源名稱</span><span class="sxs-lookup"><span data-stu-id="5b0e9-195">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="5b0e9-196">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="5b0e9-196">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="5b0e9-197">`[Id <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5b0e9-197">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="5b0e9-198">`[OSProfile <ICloudServiceOSProfile>]`：說明雲端服務的 OS 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-198">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="5b0e9-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`：指定應該要安裝在角色實例上的一組憑證。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="5b0e9-200">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5b0e9-200">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="5b0e9-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`：SourceVault 中包含憑證的重要庫參照清單。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="5b0e9-202">`[CertificateUrl <String>]`：這是憑證的 URL，已上傳至金鑰庫作為機密。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-202">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="5b0e9-203">`[PackageUrl <String>]`：指定參照 Blob 服務中服務套件位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-203">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="5b0e9-204">服務套件 URL 可以是來自任何儲存帳戶 (SAS) URI 的共用存取簽名。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-204">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="5b0e9-205">這是只寫入的屬性，不會在 GET 通話中返回。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-205">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="5b0e9-206">`[RoleProfile <ICloudServiceRoleProfile>]`：說明雲端服務的角色設定檔。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-206">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="5b0e9-207">`[Role <ICloudServiceRoleProfileProperties[]>]`：雲端服務的角色清單。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="5b0e9-208">`[Name <String>]`：資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-208">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="5b0e9-209">`[SkuCapacity <Int64?>]`：指定雲端服務中的角色實例數目。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-209">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="5b0e9-210">`[SkuName <String>]`：SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-210">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="5b0e9-211">注意：如果雲端服務目前使用的硬體不支援新的 SKU，您必須刪除並重建雲端服務，或移回舊的 SKU。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-211">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="5b0e9-212">`[SkuTier <String>]`：指定雲端服務層級。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-212">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="5b0e9-213">可能的值為</span><span class="sxs-lookup"><span data-stu-id="5b0e9-213">Possible Values are</span></span> <br /><br /> <span data-ttu-id="5b0e9-214">**標準**</span><span class="sxs-lookup"><span data-stu-id="5b0e9-214">**Standard**</span></span> <br /><br /> <span data-ttu-id="5b0e9-215">**基本**</span><span class="sxs-lookup"><span data-stu-id="5b0e9-215">**Basic**</span></span>
  - <span data-ttu-id="5b0e9-216">`[StartCloudService <Boolean?>]`： (選擇性) 指出是否要在建立雲端服務後立即啟動。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-216">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="5b0e9-217">預設值為 `true` 。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-217">The default value is `true`.</span></span>         <span data-ttu-id="5b0e9-218">如果為 False，服務模型仍然會部署，但程式碼不會立即執行。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-218">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="5b0e9-219">服務會改為 PoweredOff，直到您打電話給 Start，此時服務就會啟動。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-219">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="5b0e9-220">即使已部署的服務為關閉電源，仍會產生費用。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-220">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="5b0e9-221">`[Tag <ICloudServiceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-221">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="5b0e9-222">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-222">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5b0e9-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`：雲端服務的更新模式。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="5b0e9-224">角色實例會配置在部署服務時更新網域。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-224">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="5b0e9-225">更新可以在每個更新網域中手動啟動，或在所有更新網域中自動啟動。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-225">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="5b0e9-226">可能的值為</span><span class="sxs-lookup"><span data-stu-id="5b0e9-226">Possible Values are</span></span> <br /><br /><span data-ttu-id="5b0e9-227">**自動**</span><span class="sxs-lookup"><span data-stu-id="5b0e9-227">**Auto**</span></span><br /><br /><span data-ttu-id="5b0e9-228">**手動**</span><span class="sxs-lookup"><span data-stu-id="5b0e9-228">**Manual**</span></span> <br /><br /><span data-ttu-id="5b0e9-229">**同時**</span><span class="sxs-lookup"><span data-stu-id="5b0e9-229">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="5b0e9-230">如果未指定，預設值為自動。如果設定為手動，則必須要求 PUT UpdateDomain 以套用更新。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-230">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="5b0e9-231">如果設定為自動，系統會自動將更新順序套用至每個更新網域。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-231">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="5b0e9-232">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b0e9-232">RELATED LINKS</span></span>

