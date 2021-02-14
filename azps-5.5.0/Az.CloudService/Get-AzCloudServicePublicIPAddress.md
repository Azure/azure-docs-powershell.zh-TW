---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServicePublicIPAddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServicePublicIPAddress.md
ms.openlocfilehash: 2a3b643a9ad9d9c588589003e5edb24ceddc4ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129918"
---
# <span data-ttu-id="2a1a4-101">Get-AzCloudServicePublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="2a1a4-101">Get-AzCloudServicePublicIPAddress</span></span>

## <span data-ttu-id="2a1a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a1a4-102">SYNOPSIS</span></span>
<span data-ttu-id="2a1a4-103">取得雲端服務的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-103">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="2a1a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a1a4-104">SYNTAX</span></span>

### <span data-ttu-id="2a1a4-105">CloudServiceName (預設) </span><span class="sxs-lookup"><span data-stu-id="2a1a4-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [<CommonParameters>]
```

### <span data-ttu-id="2a1a4-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="2a1a4-106">CloudService</span></span>
```
Get-AzCloudServicePublicIPAddress -CloudService <CloudService> [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="2a1a4-107">說明</span><span class="sxs-lookup"><span data-stu-id="2a1a4-107">DESCRIPTION</span></span>
<span data-ttu-id="2a1a4-108">取得雲端服務的公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-108">Get the public IP address of a cloud service.</span></span>

## <span data-ttu-id="2a1a4-109">示例</span><span class="sxs-lookup"><span data-stu-id="2a1a4-109">EXAMPLES</span></span>

### <span data-ttu-id="2a1a4-110">範例1：針對特定雲端服務名稱取得實例層級公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-110">Example 1: Get instance level public IP addresses for a given cloud service name.</span></span>
```powershell
PS C:\> Get-AzCloudServicePublicIPAddress -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="2a1a4-111">針對指定的雲端服務名稱取得實例層級公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-111">Gets the instance level public IP addresses for a given cloud service name.</span></span>

### <span data-ttu-id="2a1a4-112">範例2：取得特定雲端服務物件的實例層級公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-112">Example 2: Get instance level public IP addresses for a given cloud service object.</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServicePublicIPAddress -CloudService $cs

```

<span data-ttu-id="2a1a4-113">取得特定雲端服務物件的實例層級公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-113">Gets the instance level public IP addresses for a given cloud service object.</span></span>

## <span data-ttu-id="2a1a4-114">參數</span><span class="sxs-lookup"><span data-stu-id="2a1a4-114">PARAMETERS</span></span>

### <span data-ttu-id="2a1a4-115">-CloudService</span><span class="sxs-lookup"><span data-stu-id="2a1a4-115">-CloudService</span></span>
<span data-ttu-id="2a1a4-116">CloudService 實例。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-116">CloudService instance.</span></span>
<span data-ttu-id="2a1a4-117">若要建立，請參閱 CLOUDSERVICE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-117">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="2a1a4-118">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="2a1a4-118">-CloudServiceName</span></span>
<span data-ttu-id="2a1a4-119">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="2a1a4-119">CloudServiceName.</span></span>

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

### <span data-ttu-id="2a1a4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a1a4-120">-ResourceGroupName</span></span>
<span data-ttu-id="2a1a4-121">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="2a1a4-121">ResourceGroupName.</span></span>

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

### <span data-ttu-id="2a1a4-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a1a4-122">-SubscriptionId</span></span>
<span data-ttu-id="2a1a4-123">訂閱.</span><span class="sxs-lookup"><span data-stu-id="2a1a4-123">Subscription.</span></span>

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

### <span data-ttu-id="2a1a4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a1a4-124">CommonParameters</span></span>
<span data-ttu-id="2a1a4-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a1a4-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a1a4-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2a1a4-127">INPUTS</span></span>

## <span data-ttu-id="2a1a4-128">輸出</span><span class="sxs-lookup"><span data-stu-id="2a1a4-128">OUTPUTS</span></span>

## <span data-ttu-id="2a1a4-129">筆記</span><span class="sxs-lookup"><span data-stu-id="2a1a4-129">NOTES</span></span>

<span data-ttu-id="2a1a4-130">別名</span><span class="sxs-lookup"><span data-stu-id="2a1a4-130">ALIASES</span></span>

<span data-ttu-id="2a1a4-131">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2a1a4-131">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a1a4-132">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-132">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a1a4-133">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a1a4-134">CLOUDSERVICE <CloudService> ： CLOUDSERVICE 實例。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-134">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="2a1a4-135">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-135">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="2a1a4-136">`[Configuration <String>]`：指定雲端服務的 XML 服務配置 ( .cscfg) 。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-136">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="2a1a4-137">`[ConfigurationUrl <String>]`：指定在 Blob 服務中參照服務配置位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-137">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="2a1a4-138">您可以從任何儲存空間帳戶 (SAS) URI，以共用存取簽章的服務套件 URL。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-138">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="2a1a4-139">這是只寫屬性，不會在 [取得呼叫] 中傳回。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-139">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="2a1a4-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`：說明雲端服務延伸設定檔。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-140">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="2a1a4-141">`[Extension <IExtension[]>]`：雲端服務的延伸清單。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-141">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="2a1a4-142">`[AutoUpgradeMinorVersion <Boolean?>]`：明確指定平臺在可用時是否可自動將 typeHandlerVersion 升級至較高的次要版本。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-142">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="2a1a4-143">`[ForceUpdateTag <String>]`：標記以強制套用提供的公用和受保護設定。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-143">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="2a1a4-144">變更 tag 值可讓您重新執行延伸，而不需變更任何公用或受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-144">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="2a1a4-145">如果 forceUpdateTag 未變更，則處理常式仍會套用對公眾或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-145">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="2a1a4-146">如果沒有 forceUpdateTag，也不會變更任何公開或受保護的設定，延伸將會以相同的序號碼流向角色實例，而不論是否重新執行，都可以使用處理程式的實現</span><span class="sxs-lookup"><span data-stu-id="2a1a4-146">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="2a1a4-147">`[Name <String>]`：延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-147">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="2a1a4-148">`[ProtectedSetting <String>]`：已在傳送至角色實例之前加密之副檔名的受保護設定。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-148">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="2a1a4-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2a1a4-149">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="2a1a4-150">`[Publisher <String>]`：延伸處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-150">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="2a1a4-151">`[RolesAppliedTo <String[]>]`：選用的角色清單來套用此延伸。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-151">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="2a1a4-152">如果未指定屬性或指定了 ' \*」，則會將延伸套用到雲端服務中的所有角色。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-152">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="2a1a4-153">`[Setting <String>]`：延伸的公開設定。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-153">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="2a1a4-154">對於 JSON 延伸，這是延伸的 JSON 設定。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-154">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="2a1a4-155">針對 XML 延伸 (例如 RDP) ，這是延伸的 XML 設定。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-155">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="2a1a4-156">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2a1a4-156">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="2a1a4-157">`[Type <String>]`：指定延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-157">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="2a1a4-158">`[TypeHandlerVersion <String>]`：指定延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-158">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="2a1a4-159">指定副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-159">Specifies the version of the extension.</span></span> <span data-ttu-id="2a1a4-160">如果未指定此元素，或使用星號 ( \* ) 作為值，就會使用最新的延伸版本。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-160">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="2a1a4-161">如果將該值指定為主要版本號碼，並以星號做為次要版本號碼 (X. ) ，則會選取指定主要版本的最新次要版本。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-161">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="2a1a4-162">如果 (X-y) 指定主要版本號碼和次要版本號碼，則會選取特定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-162">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="2a1a4-163">如果指定版本，則會在角色實例上執行自動升級。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-163">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="2a1a4-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`：雲端服務的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-164">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="2a1a4-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`：雲端服務的負載平衡器設定清單。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-165">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="2a1a4-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`： IP 清單</span><span class="sxs-lookup"><span data-stu-id="2a1a4-166">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="2a1a4-167">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2a1a4-167">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="2a1a4-168">`[PrivateIPAddress <String>]`：雲端服務所參照的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-168">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="2a1a4-169">`[PublicIPAddressId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2a1a4-169">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="2a1a4-170">`[SubnetId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2a1a4-170">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="2a1a4-171">`[Name <String>]`：資源名稱</span><span class="sxs-lookup"><span data-stu-id="2a1a4-171">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="2a1a4-172">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="2a1a4-172">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="2a1a4-173">`[Id <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2a1a4-173">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="2a1a4-174">`[OSProfile <ICloudServiceOSProfile>]`：說明雲端服務的 OS 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-174">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="2a1a4-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`：指定應該安裝在角色實例上的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-175">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="2a1a4-176">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2a1a4-176">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="2a1a4-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`： SourceVault 中包含憑證的主要保存庫參照清單。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-177">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="2a1a4-178">`[CertificateUrl <String>]`：這是已上傳到金鑰保存庫的憑證 URL （密碼）。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-178">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="2a1a4-179">`[PackageUrl <String>]`：指定要參照 Blob 服務中服務套件位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-179">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="2a1a4-180">您可以從任何儲存空間帳戶 (SAS) URI，以共用存取簽章的服務套件 URL。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-180">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="2a1a4-181">這是只寫屬性，不會在 [取得呼叫] 中傳回。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-181">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="2a1a4-182">`[RoleProfile <ICloudServiceRoleProfile>]`：說明雲端服務的角色設定檔。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-182">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="2a1a4-183">`[Role <ICloudServiceRoleProfileProperties[]>]`：雲端服務的角色清單。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-183">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="2a1a4-184">`[Name <String>]`：資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-184">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="2a1a4-185">`[SkuCapacity <Int64?>]`：指定雲端服務中的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-185">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="2a1a4-186">`[SkuName <String>]`： Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-186">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="2a1a4-187">注意：如果雲端服務目前所在的硬體不支援新版 SKU，您必須刪除並重新建立雲端服務，或移回舊版 SKU。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-187">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="2a1a4-188">`[SkuTier <String>]`：指定雲端服務的層級。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-188">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="2a1a4-189">可能的值為</span><span class="sxs-lookup"><span data-stu-id="2a1a4-189">Possible Values are</span></span> <br /><br /> <span data-ttu-id="2a1a4-190">**標準**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-190">**Standard**</span></span> <br /><br /> <span data-ttu-id="2a1a4-191">**空白**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-191">**Basic**</span></span>
  - <span data-ttu-id="2a1a4-192">`[StartCloudService <Boolean?>]`： (選用) 指出是否要在建立雲端服務後立即啟動。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-192">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="2a1a4-193">預設值為 `true` 。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-193">The default value is `true`.</span></span>         <span data-ttu-id="2a1a4-194">如果是 false，則表示服務模型仍在部署，但程式碼不會立即執行。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-194">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="2a1a4-195">相反地，服務會在您呼叫 Start 之前 PoweredOff，直到該服務開始時才會啟動。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-195">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="2a1a4-196">即使是 poweredoff，部署的服務仍會產生費用。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-196">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="2a1a4-197">`[Tag <ICloudServiceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-197">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="2a1a4-198">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2a1a4-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`：雲端服務的更新模式。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-199">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="2a1a4-200">部署服務時，系統會將角色實例指派給更新網域。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-200">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="2a1a4-201">更新可以在每個更新網域中手動啟動，或是在所有更新網域中自動啟動。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-201">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="2a1a4-202">可能的值為</span><span class="sxs-lookup"><span data-stu-id="2a1a4-202">Possible Values are</span></span> <br /><br /><span data-ttu-id="2a1a4-203">**自動**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-203">**Auto**</span></span><br /><br /><span data-ttu-id="2a1a4-204">**手動**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-204">**Manual**</span></span> <br /><br /><span data-ttu-id="2a1a4-205">**辦公**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-205">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="2a1a4-206">如果沒有指定，則預設值為 Auto。如果設定為 [手動]，則必須呼叫 UpdateDomain，才能套用更新。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-206">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="2a1a4-207">如果設為 Auto，更新會自動套用至每個更新網域。</span><span class="sxs-lookup"><span data-stu-id="2a1a4-207">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="2a1a4-208">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a1a4-208">RELATED LINKS</span></span>

