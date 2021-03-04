---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: b46ab9b8dee108f6d2126c199e5609d92452b95a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916257"
---
# <span data-ttu-id="fd8a8-101">Switch-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="fd8a8-101">Switch-AzCloudService</span></span>

## <span data-ttu-id="fd8a8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd8a8-102">SYNOPSIS</span></span>
<span data-ttu-id="fd8a8-103">在兩個雲端服務之間交換 IP (延伸支援) 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-103">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="fd8a8-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd8a8-104">SYNTAX</span></span>

### <span data-ttu-id="fd8a8-105">CloudServiceName (預設) </span><span class="sxs-lookup"><span data-stu-id="fd8a8-105">CloudServiceName (Default)</span></span>
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fd8a8-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="fd8a8-106">CloudService</span></span>
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fd8a8-107">描述</span><span class="sxs-lookup"><span data-stu-id="fd8a8-107">DESCRIPTION</span></span>
<span data-ttu-id="fd8a8-108">在兩個雲端服務之間交換 IP (延伸支援) 負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-108">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="fd8a8-109">例子</span><span class="sxs-lookup"><span data-stu-id="fd8a8-109">EXAMPLES</span></span>

### <span data-ttu-id="fd8a8-110">範例 1：使用名稱切換雲端服務</span><span class="sxs-lookup"><span data-stu-id="fd8a8-110">Example 1: Switch cloud service using name</span></span>
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="fd8a8-111">上述命令會叫用名稱為 'BService' 的雲端服務上的 vipswap 作業，且一旦使用者確認確認提示上的動作後，就會執行該作業。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-111">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="fd8a8-112">使用可交換的雲端服務來交換的 'BService'。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-112">'BService' with be swapped with its swappable cloud service.</span></span>

### <span data-ttu-id="fd8a8-113">範例 2：使用雲端服務物件切換雲端服務</span><span class="sxs-lookup"><span data-stu-id="fd8a8-113">Example 2: Switch cloud service using cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

<span data-ttu-id="fd8a8-114">上述命令會叫用名稱為 'BService' 的雲端服務上的 vipswap 作業，且一旦使用者確認確認提示上的動作後，就會執行該作業。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-114">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="fd8a8-115">使用可交換的雲端服務來交換的 'BService'。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-115">'BService' with be swapped with its swappable cloud service.</span></span>

## <span data-ttu-id="fd8a8-116">參數</span><span class="sxs-lookup"><span data-stu-id="fd8a8-116">PARAMETERS</span></span>

### <span data-ttu-id="fd8a8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd8a8-117">-AsJob</span></span>
<span data-ttu-id="fd8a8-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="fd8a8-118">Run the command as a job</span></span>

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

### <span data-ttu-id="fd8a8-119">-Async</span><span class="sxs-lookup"><span data-stu-id="fd8a8-119">-Async</span></span>


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

### <span data-ttu-id="fd8a8-120">-CloudService</span><span class="sxs-lookup"><span data-stu-id="fd8a8-120">-CloudService</span></span>
<span data-ttu-id="fd8a8-121">若要建構，請參閱 CLOUDSERVICE 屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-121">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8a8-122">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="fd8a8-122">-CloudServiceName</span></span>


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8a8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd8a8-123">-DefaultProfile</span></span>
<span data-ttu-id="fd8a8-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd8a8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd8a8-125">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8a8-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd8a8-126">-SubscriptionId</span></span>
<span data-ttu-id="fd8a8-127">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fd8a8-128">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fd8a8-129">-確認</span><span class="sxs-lookup"><span data-stu-id="fd8a8-129">-Confirm</span></span>
<span data-ttu-id="fd8a8-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd8a8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd8a8-131">-WhatIf</span></span>
<span data-ttu-id="fd8a8-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd8a8-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd8a8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd8a8-134">CommonParameters</span></span>
<span data-ttu-id="fd8a8-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd8a8-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd8a8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd8a8-137">輸入</span><span class="sxs-lookup"><span data-stu-id="fd8a8-137">INPUTS</span></span>

## <span data-ttu-id="fd8a8-138">輸出</span><span class="sxs-lookup"><span data-stu-id="fd8a8-138">OUTPUTS</span></span>

### <span data-ttu-id="fd8a8-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd8a8-139">System.Boolean</span></span>

## <span data-ttu-id="fd8a8-140">筆記</span><span class="sxs-lookup"><span data-stu-id="fd8a8-140">NOTES</span></span>

<span data-ttu-id="fd8a8-141">別名</span><span class="sxs-lookup"><span data-stu-id="fd8a8-141">ALIASES</span></span>

<span data-ttu-id="fd8a8-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="fd8a8-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fd8a8-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fd8a8-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fd8a8-145"><CloudService>CLOUDSERVICE：</span><span class="sxs-lookup"><span data-stu-id="fd8a8-145">CLOUDSERVICE <CloudService>:</span></span> 
  - <span data-ttu-id="fd8a8-146">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-146">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="fd8a8-147">`[Configuration <String>]`：指定雲端 (.csc) XML 服務組配置。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-147">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="fd8a8-148">`[ConfigurationUrl <String>]`：指定一個 URL，該 URL 參照到 Blob 服務中的服務群組原則位置。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-148">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="fd8a8-149">服務套件 URL 可以是來自任何儲存帳戶 (SAS) URI 的共用存取簽名。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-149">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="fd8a8-150">這是只寫入的屬性，不會在 GET 通話中返回。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-150">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="fd8a8-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`：說明雲端服務擴充功能設定檔。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="fd8a8-152">`[Extension <IExtension[]>]`：雲端服務的擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-152">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="fd8a8-153">`[AutoUpgradeMinorVersion <Boolean?>]`：明確指定平臺是否可以在提供類型HandlerVersion時自動升級至較高的次要版本。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="fd8a8-154">`[ForceUpdateTag <String>]`：標記以強制使用提供的公用和受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-154">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="fd8a8-155">變更標記值可讓您重新經營擴充功能，而不需要變更任何公用或受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-155">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="fd8a8-156">如果未變更 forceUpdateTag，處理常式仍然會使用公用或受保護的設定更新。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-156">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="fd8a8-157">如果 forceUpdateTag 或任何公用或受保護的設定都沒有變更，延伸模組會流向具有相同序號的角色實例，而是否要重新執行，則由處理常式的執行方式決定</span><span class="sxs-lookup"><span data-stu-id="fd8a8-157">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="fd8a8-158">`[Name <String>]`：副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-158">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="fd8a8-159">`[ProtectedSetting <String>]`：已加密的擴充功能之受保護的設定，在送往角色實例之前。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-159">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="fd8a8-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="fd8a8-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="fd8a8-161">`[Publisher <String>]`：副檔名處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-161">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="fd8a8-162">`[RolesAppliedTo <String[]>]`：可申請此擴充功能的角色清單。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-162">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="fd8a8-163">如果未指定屬性或指定 '\*'，延伸模組會適用于雲端服務中的所有角色。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-163">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="fd8a8-164">`[Setting <String>]`：擴充功能公用設定。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-164">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="fd8a8-165">對於 JSON 擴充功能，這是該擴充功能 JSON 設定。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-165">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="fd8a8-166">對於 XML 擴充 (如 RDP) ，這是該副檔名的 XML 設定。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-166">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="fd8a8-167">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fd8a8-167">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="fd8a8-168">`[Type <String>]`：指定擴充功能的類型。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-168">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="fd8a8-169">`[TypeHandlerVersion <String>]`：指定擴充功能的版本。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-169">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="fd8a8-170">指定擴充功能的版本。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-170">Specifies the version of the extension.</span></span> <span data-ttu-id="fd8a8-171">如果未指定此元素，或是使用星號 (\*) 做為值，則使用最新版本的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-171">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="fd8a8-172">如果以主要版本號碼和星號指定值做為次要版本號碼 (X.) ，會選取指定主要版本的最新次要版本。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-172">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="fd8a8-173">如果在 X.Y (指定主要版本號碼和次要版本號碼) ，會選取特定的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-173">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="fd8a8-174">如果指定版本，系統即會對角色實例執行自動升級。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-174">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="fd8a8-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`：雲端服務的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="fd8a8-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`：雲端服務的負載平衡器組組清單。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="fd8a8-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`：IP 清單</span><span class="sxs-lookup"><span data-stu-id="fd8a8-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="fd8a8-178">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="fd8a8-178">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="fd8a8-179">`[PrivateIPAddress <String>]`：雲端服務所參照的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-179">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="fd8a8-180">`[PublicIPAddressId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fd8a8-180">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="fd8a8-181">`[SubnetId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fd8a8-181">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="fd8a8-182">`[Name <String>]`：資源名稱</span><span class="sxs-lookup"><span data-stu-id="fd8a8-182">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="fd8a8-183">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="fd8a8-183">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="fd8a8-184">`[Id <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fd8a8-184">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="fd8a8-185">`[OSProfile <ICloudServiceOSProfile>]`：說明雲端服務的 OS 設定檔。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-185">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="fd8a8-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`：指定應該要安裝在角色實例上的一組憑證。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="fd8a8-187">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fd8a8-187">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="fd8a8-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`：SourceVault 中包含憑證的重要庫參照清單。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="fd8a8-189">`[CertificateUrl <String>]`：這是憑證的 URL，已上傳至金鑰庫作為機密。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-189">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="fd8a8-190">`[PackageUrl <String>]`：指定參照 Blob 服務中服務套件位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-190">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="fd8a8-191">服務套件 URL 可以是來自任何儲存帳戶 (SAS) URI 的共用存取簽名。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-191">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="fd8a8-192">這是只寫入的屬性，不會在 GET 通話中返回。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-192">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="fd8a8-193">`[RoleProfile <ICloudServiceRoleProfile>]`：說明雲端服務的角色設定檔。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="fd8a8-194">`[Role <ICloudServiceRoleProfileProperties[]>]`：雲端服務的角色清單。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="fd8a8-195">`[Name <String>]`：資源名稱。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-195">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="fd8a8-196">`[SkuCapacity <Int64?>]`：指定雲端服務中的角色實例數目。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-196">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="fd8a8-197">`[SkuName <String>]`：SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-197">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="fd8a8-198">注意：如果雲端服務目前使用的硬體不支援新的 SKU，您必須刪除並重建雲端服務，或移回舊的 SKU。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-198">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="fd8a8-199">`[SkuTier <String>]`：指定雲端服務層級。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-199">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="fd8a8-200">可能的值為</span><span class="sxs-lookup"><span data-stu-id="fd8a8-200">Possible Values are</span></span> <br /><br /> <span data-ttu-id="fd8a8-201">**標準**</span><span class="sxs-lookup"><span data-stu-id="fd8a8-201">**Standard**</span></span> <br /><br /> <span data-ttu-id="fd8a8-202">**基本**</span><span class="sxs-lookup"><span data-stu-id="fd8a8-202">**Basic**</span></span>
  - <span data-ttu-id="fd8a8-203">`[StartCloudService <Boolean?>]`： (選擇性) 指出是否要在建立雲端服務後立即啟動。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-203">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="fd8a8-204">預設值為 `true` 。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-204">The default value is `true`.</span></span>         <span data-ttu-id="fd8a8-205">如果為 False，服務模型仍然會部署，但程式碼不會立即執行。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-205">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="fd8a8-206">服務會改為 PoweredOff，直到您打電話給 Start，此時服務就會啟動。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-206">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="fd8a8-207">即使已部署的服務為關閉電源，仍會產生費用。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-207">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="fd8a8-208">`[Tag <ICloudServiceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-208">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="fd8a8-209">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-209">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="fd8a8-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`：雲端服務的更新模式。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="fd8a8-211">角色實例會配置在部署服務時更新網域。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-211">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="fd8a8-212">更新可以在每個更新網域中手動啟動，或在所有更新網域中自動啟動。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-212">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="fd8a8-213">可能的值為</span><span class="sxs-lookup"><span data-stu-id="fd8a8-213">Possible Values are</span></span> <br /><br /><span data-ttu-id="fd8a8-214">**自動**</span><span class="sxs-lookup"><span data-stu-id="fd8a8-214">**Auto**</span></span><br /><br /><span data-ttu-id="fd8a8-215">**手動**</span><span class="sxs-lookup"><span data-stu-id="fd8a8-215">**Manual**</span></span> <br /><br /><span data-ttu-id="fd8a8-216">**同時**</span><span class="sxs-lookup"><span data-stu-id="fd8a8-216">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="fd8a8-217">如果未指定，預設值為自動。如果設定為手動，則必須要求 PUT UpdateDomain 以套用更新。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-217">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="fd8a8-218">如果設定為自動，系統會自動將更新順序套用至每個更新網域。</span><span class="sxs-lookup"><span data-stu-id="fd8a8-218">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="fd8a8-219">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd8a8-219">RELATED LINKS</span></span>

