---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-AzCloudServiceNetworkInterfaces
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceNetworkInterfaces.md
ms.openlocfilehash: 7f8a51c518bd034e51d8c25d5029bb57b3e38caf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137510"
---
# <span data-ttu-id="70f2e-101">Get-AzCloudServiceNetworkInterfaces</span><span class="sxs-lookup"><span data-stu-id="70f2e-101">Get-AzCloudServiceNetworkInterfaces</span></span>

## <span data-ttu-id="70f2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="70f2e-103">取得雲端服務的網路介面。</span><span class="sxs-lookup"><span data-stu-id="70f2e-103">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="70f2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="70f2e-104">SYNTAX</span></span>

### <span data-ttu-id="70f2e-105">CloudServiceName (預設) </span><span class="sxs-lookup"><span data-stu-id="70f2e-105">CloudServiceName (Default)</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-RoleInstanceName <String>] [<CommonParameters>]
```

### <span data-ttu-id="70f2e-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="70f2e-106">CloudService</span></span>
```
Get-AzCloudServiceNetworkInterfaces -CloudService <CloudService> [-SubscriptionId <String>]
 [-RoleInstanceName <String>] [<CommonParameters>]
```

## <span data-ttu-id="70f2e-107">說明</span><span class="sxs-lookup"><span data-stu-id="70f2e-107">DESCRIPTION</span></span>
<span data-ttu-id="70f2e-108">取得雲端服務的網路介面。</span><span class="sxs-lookup"><span data-stu-id="70f2e-108">Get the network interfaces of a cloud service.</span></span>

## <span data-ttu-id="70f2e-109">示例</span><span class="sxs-lookup"><span data-stu-id="70f2e-109">EXAMPLES</span></span>

### <span data-ttu-id="70f2e-110">範例1：透過雲端服務名稱取得網路介面</span><span class="sxs-lookup"><span data-stu-id="70f2e-110">Example 1: Get network interfaces by a cloud service name</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="70f2e-111">取得指定雲端服務名稱的所有網路介面。</span><span class="sxs-lookup"><span data-stu-id="70f2e-111">Gets all the network interfaces for a given cloud service name.</span></span>

### <span data-ttu-id="70f2e-112">範例2：透過雲端服務物件取得網路介面</span><span class="sxs-lookup"><span data-stu-id="70f2e-112">Example 2: Get network interfaces by a cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs

```

<span data-ttu-id="70f2e-113">取得指定雲端服務物件的所有網路介面。</span><span class="sxs-lookup"><span data-stu-id="70f2e-113">Gets all the network interfaces for a given cloud service object.</span></span>

### <span data-ttu-id="70f2e-114">範例3：透過雲端服務物件和角色實例名稱來取得網路介面。</span><span class="sxs-lookup"><span data-stu-id="70f2e-114">Example 3: Get network interfaces by a cloud service object and role instance name.</span></span>
```powershell
PS C:\> Get-AzCloudServiceNetworkInterfaces -CloudService $cs -RoleInstanceName WebRole1_IN_0

```

<span data-ttu-id="70f2e-115">取得指定雲端服務物件與角色實例名稱的所有網路介面。</span><span class="sxs-lookup"><span data-stu-id="70f2e-115">Gets all the network interfaces for a given cloud service object and role instance name.</span></span>

## <span data-ttu-id="70f2e-116">參數</span><span class="sxs-lookup"><span data-stu-id="70f2e-116">PARAMETERS</span></span>

### <span data-ttu-id="70f2e-117">-CloudService</span><span class="sxs-lookup"><span data-stu-id="70f2e-117">-CloudService</span></span>
<span data-ttu-id="70f2e-118">CloudService 實例。</span><span class="sxs-lookup"><span data-stu-id="70f2e-118">CloudService instance.</span></span>
<span data-ttu-id="70f2e-119">若要建立，請參閱 CLOUDSERVICE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="70f2e-119">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

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

### <span data-ttu-id="70f2e-120">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="70f2e-120">-CloudServiceName</span></span>
<span data-ttu-id="70f2e-121">CloudServiceName.</span><span class="sxs-lookup"><span data-stu-id="70f2e-121">CloudServiceName.</span></span>

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

### <span data-ttu-id="70f2e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70f2e-122">-ResourceGroupName</span></span>
<span data-ttu-id="70f2e-123">ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="70f2e-123">ResourceGroupName.</span></span>

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

### <span data-ttu-id="70f2e-124">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="70f2e-124">-RoleInstanceName</span></span>
<span data-ttu-id="70f2e-125">RoleInstanceName.</span><span class="sxs-lookup"><span data-stu-id="70f2e-125">RoleInstanceName.</span></span>

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

### <span data-ttu-id="70f2e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70f2e-126">-SubscriptionId</span></span>
<span data-ttu-id="70f2e-127">訂閱.</span><span class="sxs-lookup"><span data-stu-id="70f2e-127">Subscription.</span></span>

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

### <span data-ttu-id="70f2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f2e-128">CommonParameters</span></span>
<span data-ttu-id="70f2e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70f2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f2e-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="70f2e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f2e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="70f2e-131">INPUTS</span></span>

## <span data-ttu-id="70f2e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="70f2e-132">OUTPUTS</span></span>

## <span data-ttu-id="70f2e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="70f2e-133">NOTES</span></span>

<span data-ttu-id="70f2e-134">別名</span><span class="sxs-lookup"><span data-stu-id="70f2e-134">ALIASES</span></span>

<span data-ttu-id="70f2e-135">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="70f2e-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="70f2e-136">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="70f2e-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="70f2e-137">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="70f2e-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="70f2e-138">CLOUDSERVICE <CloudService> ： CLOUDSERVICE 實例。</span><span class="sxs-lookup"><span data-stu-id="70f2e-138">CLOUDSERVICE <CloudService>: CloudService instance.</span></span>
  - <span data-ttu-id="70f2e-139">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="70f2e-139">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="70f2e-140">`[Configuration <String>]`：指定雲端服務的 XML 服務配置 ( .cscfg) 。</span><span class="sxs-lookup"><span data-stu-id="70f2e-140">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="70f2e-141">`[ConfigurationUrl <String>]`：指定在 Blob 服務中參照服務配置位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="70f2e-141">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="70f2e-142">您可以從任何儲存空間帳戶 (SAS) URI，以共用存取簽章的服務套件 URL。</span><span class="sxs-lookup"><span data-stu-id="70f2e-142">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="70f2e-143">這是只寫屬性，不會在 [取得呼叫] 中傳回。</span><span class="sxs-lookup"><span data-stu-id="70f2e-143">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="70f2e-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`：說明雲端服務延伸設定檔。</span><span class="sxs-lookup"><span data-stu-id="70f2e-144">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="70f2e-145">`[Extension <IExtension[]>]`：雲端服務的延伸清單。</span><span class="sxs-lookup"><span data-stu-id="70f2e-145">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="70f2e-146">`[AutoUpgradeMinorVersion <Boolean?>]`：明確指定平臺在可用時是否可自動將 typeHandlerVersion 升級至較高的次要版本。</span><span class="sxs-lookup"><span data-stu-id="70f2e-146">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="70f2e-147">`[ForceUpdateTag <String>]`：標記以強制套用提供的公用和受保護設定。</span><span class="sxs-lookup"><span data-stu-id="70f2e-147">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="70f2e-148">變更 tag 值可讓您重新執行延伸，而不需變更任何公用或受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="70f2e-148">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="70f2e-149">如果 forceUpdateTag 未變更，則處理常式仍會套用對公眾或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="70f2e-149">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="70f2e-150">如果沒有 forceUpdateTag，也不會變更任何公開或受保護的設定，延伸將會以相同的序號碼流向角色實例，而不論是否重新執行，都可以使用處理程式的實現</span><span class="sxs-lookup"><span data-stu-id="70f2e-150">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="70f2e-151">`[Name <String>]`：延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="70f2e-151">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="70f2e-152">`[ProtectedSetting <String>]`：已在傳送至角色實例之前加密之副檔名的受保護設定。</span><span class="sxs-lookup"><span data-stu-id="70f2e-152">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="70f2e-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="70f2e-153">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="70f2e-154">`[Publisher <String>]`：延伸處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="70f2e-154">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="70f2e-155">`[RolesAppliedTo <String[]>]`：選用的角色清單來套用此延伸。</span><span class="sxs-lookup"><span data-stu-id="70f2e-155">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="70f2e-156">如果未指定屬性或指定了 ' \*」，則會將延伸套用到雲端服務中的所有角色。</span><span class="sxs-lookup"><span data-stu-id="70f2e-156">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="70f2e-157">`[Setting <String>]`：延伸的公開設定。</span><span class="sxs-lookup"><span data-stu-id="70f2e-157">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="70f2e-158">對於 JSON 延伸，這是延伸的 JSON 設定。</span><span class="sxs-lookup"><span data-stu-id="70f2e-158">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="70f2e-159">針對 XML 延伸 (例如 RDP) ，這是延伸的 XML 設定。</span><span class="sxs-lookup"><span data-stu-id="70f2e-159">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="70f2e-160">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="70f2e-160">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="70f2e-161">`[Type <String>]`：指定延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="70f2e-161">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="70f2e-162">`[TypeHandlerVersion <String>]`：指定延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="70f2e-162">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="70f2e-163">指定副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="70f2e-163">Specifies the version of the extension.</span></span> <span data-ttu-id="70f2e-164">如果未指定此元素，或使用星號 ( \* ) 作為值，就會使用最新的延伸版本。</span><span class="sxs-lookup"><span data-stu-id="70f2e-164">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="70f2e-165">如果將該值指定為主要版本號碼，並以星號做為次要版本號碼 (X. ) ，則會選取指定主要版本的最新次要版本。</span><span class="sxs-lookup"><span data-stu-id="70f2e-165">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="70f2e-166">如果 (X-y) 指定主要版本號碼和次要版本號碼，則會選取特定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="70f2e-166">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="70f2e-167">如果指定版本，則會在角色實例上執行自動升級。</span><span class="sxs-lookup"><span data-stu-id="70f2e-167">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="70f2e-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`：雲端服務的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="70f2e-168">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="70f2e-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`：雲端服務的負載平衡器設定清單。</span><span class="sxs-lookup"><span data-stu-id="70f2e-169">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="70f2e-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`： IP 清單</span><span class="sxs-lookup"><span data-stu-id="70f2e-170">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="70f2e-171">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="70f2e-171">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="70f2e-172">`[PrivateIPAddress <String>]`：雲端服務所參照的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="70f2e-172">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="70f2e-173">`[PublicIPAddressId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="70f2e-173">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="70f2e-174">`[SubnetId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="70f2e-174">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="70f2e-175">`[Name <String>]`：資源名稱</span><span class="sxs-lookup"><span data-stu-id="70f2e-175">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="70f2e-176">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="70f2e-176">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="70f2e-177">`[Id <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="70f2e-177">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="70f2e-178">`[OSProfile <ICloudServiceOSProfile>]`：說明雲端服務的 OS 設定檔。</span><span class="sxs-lookup"><span data-stu-id="70f2e-178">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="70f2e-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`：指定應該安裝在角色實例上的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="70f2e-179">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="70f2e-180">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="70f2e-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="70f2e-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`： SourceVault 中包含憑證的主要保存庫參照清單。</span><span class="sxs-lookup"><span data-stu-id="70f2e-181">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="70f2e-182">`[CertificateUrl <String>]`：這是已上傳到金鑰保存庫的憑證 URL （密碼）。</span><span class="sxs-lookup"><span data-stu-id="70f2e-182">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="70f2e-183">`[PackageUrl <String>]`：指定要參照 Blob 服務中服務套件位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="70f2e-183">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="70f2e-184">您可以從任何儲存空間帳戶 (SAS) URI，以共用存取簽章的服務套件 URL。</span><span class="sxs-lookup"><span data-stu-id="70f2e-184">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="70f2e-185">這是只寫屬性，不會在 [取得呼叫] 中傳回。</span><span class="sxs-lookup"><span data-stu-id="70f2e-185">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="70f2e-186">`[RoleProfile <ICloudServiceRoleProfile>]`：說明雲端服務的角色設定檔。</span><span class="sxs-lookup"><span data-stu-id="70f2e-186">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="70f2e-187">`[Role <ICloudServiceRoleProfileProperties[]>]`：雲端服務的角色清單。</span><span class="sxs-lookup"><span data-stu-id="70f2e-187">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="70f2e-188">`[Name <String>]`：資源名稱。</span><span class="sxs-lookup"><span data-stu-id="70f2e-188">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="70f2e-189">`[SkuCapacity <Int64?>]`：指定雲端服務中的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="70f2e-189">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="70f2e-190">`[SkuName <String>]`： Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="70f2e-190">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="70f2e-191">注意：如果雲端服務目前所在的硬體不支援新版 SKU，您必須刪除並重新建立雲端服務，或移回舊版 SKU。</span><span class="sxs-lookup"><span data-stu-id="70f2e-191">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="70f2e-192">`[SkuTier <String>]`：指定雲端服務的層級。</span><span class="sxs-lookup"><span data-stu-id="70f2e-192">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="70f2e-193">可能的值為</span><span class="sxs-lookup"><span data-stu-id="70f2e-193">Possible Values are</span></span> <br /><br /> <span data-ttu-id="70f2e-194">**標準**</span><span class="sxs-lookup"><span data-stu-id="70f2e-194">**Standard**</span></span> <br /><br /> <span data-ttu-id="70f2e-195">**空白**</span><span class="sxs-lookup"><span data-stu-id="70f2e-195">**Basic**</span></span>
  - <span data-ttu-id="70f2e-196">`[StartCloudService <Boolean?>]`： (選用) 指出是否要在建立雲端服務後立即啟動。</span><span class="sxs-lookup"><span data-stu-id="70f2e-196">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="70f2e-197">預設值為 `true` 。</span><span class="sxs-lookup"><span data-stu-id="70f2e-197">The default value is `true`.</span></span>         <span data-ttu-id="70f2e-198">如果是 false，則表示服務模型仍在部署，但程式碼不會立即執行。</span><span class="sxs-lookup"><span data-stu-id="70f2e-198">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="70f2e-199">相反地，服務會在您呼叫 Start 之前 PoweredOff，直到該服務開始時才會啟動。</span><span class="sxs-lookup"><span data-stu-id="70f2e-199">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="70f2e-200">即使是 poweredoff，部署的服務仍會產生費用。</span><span class="sxs-lookup"><span data-stu-id="70f2e-200">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="70f2e-201">`[Tag <ICloudServiceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="70f2e-201">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="70f2e-202">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="70f2e-202">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="70f2e-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`：雲端服務的更新模式。</span><span class="sxs-lookup"><span data-stu-id="70f2e-203">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="70f2e-204">部署服務時，系統會將角色實例指派給更新網域。</span><span class="sxs-lookup"><span data-stu-id="70f2e-204">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="70f2e-205">更新可以在每個更新網域中手動啟動，或是在所有更新網域中自動啟動。</span><span class="sxs-lookup"><span data-stu-id="70f2e-205">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="70f2e-206">可能的值為</span><span class="sxs-lookup"><span data-stu-id="70f2e-206">Possible Values are</span></span> <br /><br /><span data-ttu-id="70f2e-207">**自動**</span><span class="sxs-lookup"><span data-stu-id="70f2e-207">**Auto**</span></span><br /><br /><span data-ttu-id="70f2e-208">**手動**</span><span class="sxs-lookup"><span data-stu-id="70f2e-208">**Manual**</span></span> <br /><br /><span data-ttu-id="70f2e-209">**辦公**</span><span class="sxs-lookup"><span data-stu-id="70f2e-209">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="70f2e-210">如果沒有指定，則預設值為 Auto。如果設定為 [手動]，則必須呼叫 UpdateDomain，才能套用更新。</span><span class="sxs-lookup"><span data-stu-id="70f2e-210">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="70f2e-211">如果設為 Auto，更新會自動套用至每個更新網域。</span><span class="sxs-lookup"><span data-stu-id="70f2e-211">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="70f2e-212">相關連結</span><span class="sxs-lookup"><span data-stu-id="70f2e-212">RELATED LINKS</span></span>

