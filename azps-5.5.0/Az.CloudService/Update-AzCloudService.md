---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: e0f9ad794f1631c5c8615480c6074f040f7fe749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127919"
---
# <span data-ttu-id="13c38-101">Update-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="13c38-101">Update-AzCloudService</span></span>

## <span data-ttu-id="13c38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13c38-102">SYNOPSIS</span></span>
<span data-ttu-id="13c38-103">建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="13c38-103">Create or update a cloud service.</span></span>
<span data-ttu-id="13c38-104">請注意，有些屬性只能在建立雲端服務期間設定。</span><span class="sxs-lookup"><span data-stu-id="13c38-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="13c38-105">句法</span><span class="sxs-lookup"><span data-stu-id="13c38-105">SYNTAX</span></span>

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13c38-106">說明</span><span class="sxs-lookup"><span data-stu-id="13c38-106">DESCRIPTION</span></span>
<span data-ttu-id="13c38-107">建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="13c38-107">Create or update a cloud service.</span></span>
<span data-ttu-id="13c38-108">請注意，有些屬性只能在建立雲端服務期間設定。</span><span class="sxs-lookup"><span data-stu-id="13c38-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="13c38-109">示例</span><span class="sxs-lookup"><span data-stu-id="13c38-109">EXAMPLES</span></span>

### <span data-ttu-id="13c38-110">範例1：將 RDP 延伸新增至現有的雲端服務</span><span class="sxs-lookup"><span data-stu-id="13c38-110">Example 1: Add RDP extension to existing cloud service</span></span>
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

<span data-ttu-id="13c38-111">上方的命令集會將 RDP 延伸新增至現有的名為 ContosoCS 的雲端服務，該名稱屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="13c38-111">Above set of commands adds a RDP extension to already existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="13c38-112">範例2：從雲端服務移除所有延伸</span><span class="sxs-lookup"><span data-stu-id="13c38-112">Example 2: Remove all extensions from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="13c38-113">上方的一組命令會從屬於名為 ContosOrg 之資源群組的現有雲端服務中移除所有延伸。</span><span class="sxs-lookup"><span data-stu-id="13c38-113">Above set of commands removes all extensions from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="13c38-114">範例3：從雲端服務移除 RDP 延伸</span><span class="sxs-lookup"><span data-stu-id="13c38-114">Example 3: Remove RDP extension from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="13c38-115">上方的一組命令會從屬於名為 ContosOrg 之資源群組的現有雲端服務，移除 RDP 延伸。</span><span class="sxs-lookup"><span data-stu-id="13c38-115">Above set of commands removes RDP extension from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="13c38-116">範例4： Scale-Out/Scale-In 角色實例</span><span class="sxs-lookup"><span data-stu-id="13c38-116">Example 4: Scale-Out / Scale-In role instances</span></span>
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

<span data-ttu-id="13c38-117">上方的命令集說明如何將屬於名為 ContosOrg 之資源群組之名為 ContosoCS 的雲端服務的「橫向」和「擴展」角色實例計數。</span><span class="sxs-lookup"><span data-stu-id="13c38-117">Above set of commands shows how to scale-out and scale-in role instance count for cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="13c38-118">參數</span><span class="sxs-lookup"><span data-stu-id="13c38-118">PARAMETERS</span></span>

### <span data-ttu-id="13c38-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13c38-119">-AsJob</span></span>
<span data-ttu-id="13c38-120">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="13c38-120">Run the command as a job</span></span>

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

### <span data-ttu-id="13c38-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c38-121">-DefaultProfile</span></span>
<span data-ttu-id="13c38-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13c38-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13c38-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13c38-123">-InputObject</span></span>
<span data-ttu-id="13c38-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="13c38-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="13c38-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="13c38-125">-NoWait</span></span>
<span data-ttu-id="13c38-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="13c38-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="13c38-127">-參數</span><span class="sxs-lookup"><span data-stu-id="13c38-127">-Parameter</span></span>
<span data-ttu-id="13c38-128">描述雲端服務。</span><span class="sxs-lookup"><span data-stu-id="13c38-128">Describes the cloud service.</span></span>
<span data-ttu-id="13c38-129">若要建立，請參閱參數屬性的 [記事] 區段，然後建立雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="13c38-129">To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="13c38-130">-確認</span><span class="sxs-lookup"><span data-stu-id="13c38-130">-Confirm</span></span>
<span data-ttu-id="13c38-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13c38-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13c38-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13c38-132">-WhatIf</span></span>
<span data-ttu-id="13c38-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13c38-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13c38-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13c38-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13c38-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c38-135">CommonParameters</span></span>
<span data-ttu-id="13c38-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13c38-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c38-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="13c38-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c38-138">輸入</span><span class="sxs-lookup"><span data-stu-id="13c38-138">INPUTS</span></span>

### <span data-ttu-id="13c38-139">ICloudService （CloudService）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="13c38-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

### <span data-ttu-id="13c38-140">ICloudServiceIdentity （CloudService）的</span><span class="sxs-lookup"><span data-stu-id="13c38-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="13c38-141">輸出</span><span class="sxs-lookup"><span data-stu-id="13c38-141">OUTPUTS</span></span>

### <span data-ttu-id="13c38-142">ICloudService （CloudService）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="13c38-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="13c38-143">筆記</span><span class="sxs-lookup"><span data-stu-id="13c38-143">NOTES</span></span>

<span data-ttu-id="13c38-144">別名</span><span class="sxs-lookup"><span data-stu-id="13c38-144">ALIASES</span></span>

<span data-ttu-id="13c38-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="13c38-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="13c38-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="13c38-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13c38-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="13c38-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="13c38-148">INPUTOBJECT <ICloudServiceIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="13c38-148">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13c38-149">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="13c38-149">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="13c38-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="13c38-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13c38-151">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="13c38-151">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="13c38-152">`[RoleInstanceName <String>]`：角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="13c38-152">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="13c38-153">`[RoleName <String>]`：角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="13c38-153">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="13c38-154">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="13c38-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="13c38-155">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="13c38-155">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="13c38-156">`[UpdateDomain <Int32?>]`：指定識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="13c38-156">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="13c38-157">更新網域是以零為基礎的索引來標識：第一個更新網域的識別碼為0，第二個是 ID 為1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="13c38-157">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

<span data-ttu-id="13c38-158">參數 <ICloudService> ：說明雲端服務。</span><span class="sxs-lookup"><span data-stu-id="13c38-158">PARAMETER <ICloudService>: Describes the cloud service.</span></span>
  - <span data-ttu-id="13c38-159">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="13c38-159">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="13c38-160">`[Configuration <String>]`：指定雲端服務的 XML 服務配置 ( .cscfg) 。</span><span class="sxs-lookup"><span data-stu-id="13c38-160">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="13c38-161">`[ConfigurationUrl <String>]`：指定在 Blob 服務中參照服務配置位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="13c38-161">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="13c38-162">您可以從任何儲存空間帳戶 (SAS) URI，以共用存取簽章的服務套件 URL。</span><span class="sxs-lookup"><span data-stu-id="13c38-162">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="13c38-163">這是只寫屬性，不會在 [取得呼叫] 中傳回。</span><span class="sxs-lookup"><span data-stu-id="13c38-163">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="13c38-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`：說明雲端服務延伸設定檔。</span><span class="sxs-lookup"><span data-stu-id="13c38-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="13c38-165">`[Extension <IExtension[]>]`：雲端服務的延伸清單。</span><span class="sxs-lookup"><span data-stu-id="13c38-165">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="13c38-166">`[AutoUpgradeMinorVersion <Boolean?>]`：明確指定平臺在可用時是否可自動將 typeHandlerVersion 升級至較高的次要版本。</span><span class="sxs-lookup"><span data-stu-id="13c38-166">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="13c38-167">`[ForceUpdateTag <String>]`：標記以強制套用提供的公用和受保護設定。</span><span class="sxs-lookup"><span data-stu-id="13c38-167">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="13c38-168">變更 tag 值可讓您重新執行延伸，而不需變更任何公用或受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="13c38-168">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="13c38-169">如果 forceUpdateTag 未變更，則處理常式仍會套用對公眾或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="13c38-169">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="13c38-170">如果沒有 forceUpdateTag，也不會變更任何公開或受保護的設定，延伸將會以相同的序號碼流向角色實例，而不論是否重新執行，都可以使用處理程式的實現</span><span class="sxs-lookup"><span data-stu-id="13c38-170">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="13c38-171">`[Name <String>]`：延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="13c38-171">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="13c38-172">`[ProtectedSetting <String>]`：已在傳送至角色實例之前加密之副檔名的受保護設定。</span><span class="sxs-lookup"><span data-stu-id="13c38-172">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="13c38-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="13c38-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="13c38-174">`[Publisher <String>]`：延伸處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="13c38-174">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="13c38-175">`[RolesAppliedTo <String[]>]`：選用的角色清單來套用此延伸。</span><span class="sxs-lookup"><span data-stu-id="13c38-175">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="13c38-176">如果未指定屬性或指定了 ' \*」，則會將延伸套用到雲端服務中的所有角色。</span><span class="sxs-lookup"><span data-stu-id="13c38-176">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="13c38-177">`[Setting <String>]`：延伸的公開設定。</span><span class="sxs-lookup"><span data-stu-id="13c38-177">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="13c38-178">對於 JSON 延伸，這是延伸的 JSON 設定。</span><span class="sxs-lookup"><span data-stu-id="13c38-178">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="13c38-179">針對 XML 延伸 (例如 RDP) ，這是延伸的 XML 設定。</span><span class="sxs-lookup"><span data-stu-id="13c38-179">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="13c38-180">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="13c38-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="13c38-181">`[Type <String>]`：指定延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="13c38-181">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="13c38-182">`[TypeHandlerVersion <String>]`：指定延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="13c38-182">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="13c38-183">指定副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="13c38-183">Specifies the version of the extension.</span></span> <span data-ttu-id="13c38-184">如果未指定此元素，或使用星號 ( \* ) 作為值，就會使用最新的延伸版本。</span><span class="sxs-lookup"><span data-stu-id="13c38-184">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="13c38-185">如果將該值指定為主要版本號碼，並以星號做為次要版本號碼 (X. ) ，則會選取指定主要版本的最新次要版本。</span><span class="sxs-lookup"><span data-stu-id="13c38-185">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="13c38-186">如果 (X-y) 指定主要版本號碼和次要版本號碼，則會選取特定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="13c38-186">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="13c38-187">如果指定版本，則會在角色實例上執行自動升級。</span><span class="sxs-lookup"><span data-stu-id="13c38-187">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="13c38-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`：雲端服務的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="13c38-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="13c38-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`：雲端服務的負載平衡器設定清單。</span><span class="sxs-lookup"><span data-stu-id="13c38-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="13c38-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`： IP 清單</span><span class="sxs-lookup"><span data-stu-id="13c38-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="13c38-191">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="13c38-191">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="13c38-192">`[PrivateIPAddress <String>]`：雲端服務所參照的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="13c38-192">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="13c38-193">`[PublicIPAddressId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="13c38-193">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="13c38-194">`[SubnetId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="13c38-194">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="13c38-195">`[Name <String>]`：資源名稱</span><span class="sxs-lookup"><span data-stu-id="13c38-195">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="13c38-196">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="13c38-196">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="13c38-197">`[Id <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="13c38-197">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="13c38-198">`[OSProfile <ICloudServiceOSProfile>]`：說明雲端服務的 OS 設定檔。</span><span class="sxs-lookup"><span data-stu-id="13c38-198">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="13c38-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`：指定應該安裝在角色實例上的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="13c38-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="13c38-200">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="13c38-200">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="13c38-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`： SourceVault 中包含憑證的主要保存庫參照清單。</span><span class="sxs-lookup"><span data-stu-id="13c38-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="13c38-202">`[CertificateUrl <String>]`：這是已上傳到金鑰保存庫的憑證 URL （密碼）。</span><span class="sxs-lookup"><span data-stu-id="13c38-202">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="13c38-203">`[PackageUrl <String>]`：指定要參照 Blob 服務中服務套件位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="13c38-203">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="13c38-204">您可以從任何儲存空間帳戶 (SAS) URI，以共用存取簽章的服務套件 URL。</span><span class="sxs-lookup"><span data-stu-id="13c38-204">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="13c38-205">這是只寫屬性，不會在 [取得呼叫] 中傳回。</span><span class="sxs-lookup"><span data-stu-id="13c38-205">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="13c38-206">`[RoleProfile <ICloudServiceRoleProfile>]`：說明雲端服務的角色設定檔。</span><span class="sxs-lookup"><span data-stu-id="13c38-206">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="13c38-207">`[Role <ICloudServiceRoleProfileProperties[]>]`：雲端服務的角色清單。</span><span class="sxs-lookup"><span data-stu-id="13c38-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="13c38-208">`[Name <String>]`：資源名稱。</span><span class="sxs-lookup"><span data-stu-id="13c38-208">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="13c38-209">`[SkuCapacity <Int64?>]`：指定雲端服務中的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="13c38-209">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="13c38-210">`[SkuName <String>]`： Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="13c38-210">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="13c38-211">注意：如果雲端服務目前所在的硬體不支援新版 SKU，您必須刪除並重新建立雲端服務，或移回舊版 SKU。</span><span class="sxs-lookup"><span data-stu-id="13c38-211">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="13c38-212">`[SkuTier <String>]`：指定雲端服務的層級。</span><span class="sxs-lookup"><span data-stu-id="13c38-212">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="13c38-213">可能的值為</span><span class="sxs-lookup"><span data-stu-id="13c38-213">Possible Values are</span></span> <br /><br /> <span data-ttu-id="13c38-214">**標準**</span><span class="sxs-lookup"><span data-stu-id="13c38-214">**Standard**</span></span> <br /><br /> <span data-ttu-id="13c38-215">**空白**</span><span class="sxs-lookup"><span data-stu-id="13c38-215">**Basic**</span></span>
  - <span data-ttu-id="13c38-216">`[StartCloudService <Boolean?>]`： (選用) 指出是否要在建立雲端服務後立即啟動。</span><span class="sxs-lookup"><span data-stu-id="13c38-216">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="13c38-217">預設值為 `true` 。</span><span class="sxs-lookup"><span data-stu-id="13c38-217">The default value is `true`.</span></span>         <span data-ttu-id="13c38-218">如果是 false，則表示服務模型仍在部署，但程式碼不會立即執行。</span><span class="sxs-lookup"><span data-stu-id="13c38-218">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="13c38-219">相反地，服務會在您呼叫 Start 之前 PoweredOff，直到該服務開始時才會啟動。</span><span class="sxs-lookup"><span data-stu-id="13c38-219">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="13c38-220">即使是 poweredoff，部署的服務仍會產生費用。</span><span class="sxs-lookup"><span data-stu-id="13c38-220">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="13c38-221">`[Tag <ICloudServiceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="13c38-221">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="13c38-222">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="13c38-222">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="13c38-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`：雲端服務的更新模式。</span><span class="sxs-lookup"><span data-stu-id="13c38-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="13c38-224">部署服務時，系統會將角色實例指派給更新網域。</span><span class="sxs-lookup"><span data-stu-id="13c38-224">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="13c38-225">更新可以在每個更新網域中手動啟動，或是在所有更新網域中自動啟動。</span><span class="sxs-lookup"><span data-stu-id="13c38-225">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="13c38-226">可能的值為</span><span class="sxs-lookup"><span data-stu-id="13c38-226">Possible Values are</span></span> <br /><br /><span data-ttu-id="13c38-227">**自動**</span><span class="sxs-lookup"><span data-stu-id="13c38-227">**Auto**</span></span><br /><br /><span data-ttu-id="13c38-228">**手動**</span><span class="sxs-lookup"><span data-stu-id="13c38-228">**Manual**</span></span> <br /><br /><span data-ttu-id="13c38-229">**辦公**</span><span class="sxs-lookup"><span data-stu-id="13c38-229">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="13c38-230">如果沒有指定，則預設值為 Auto。如果設定為 [手動]，則必須呼叫 UpdateDomain，才能套用更新。</span><span class="sxs-lookup"><span data-stu-id="13c38-230">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="13c38-231">如果設為 Auto，更新會自動套用至每個更新網域。</span><span class="sxs-lookup"><span data-stu-id="13c38-231">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="13c38-232">相關連結</span><span class="sxs-lookup"><span data-stu-id="13c38-232">RELATED LINKS</span></span>

