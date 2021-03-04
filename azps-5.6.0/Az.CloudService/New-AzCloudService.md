---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 607ac4e9854f3871c4a9a0f2859c6f1fe555f392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909773"
---
# <span data-ttu-id="9f733-101">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="9f733-101">New-AzCloudService</span></span>

## <span data-ttu-id="9f733-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9f733-102">SYNOPSIS</span></span>
<span data-ttu-id="9f733-103">建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="9f733-103">Create or update a cloud service.</span></span>
<span data-ttu-id="9f733-104">請注意，某些屬性只能在建立雲端服務期間設定。</span><span class="sxs-lookup"><span data-stu-id="9f733-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="9f733-105">語法</span><span class="sxs-lookup"><span data-stu-id="9f733-105">SYNTAX</span></span>

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9f733-106">描述</span><span class="sxs-lookup"><span data-stu-id="9f733-106">DESCRIPTION</span></span>
<span data-ttu-id="9f733-107">建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="9f733-107">Create or update a cloud service.</span></span>
<span data-ttu-id="9f733-108">請注意，某些屬性只能在建立雲端服務期間設定。</span><span class="sxs-lookup"><span data-stu-id="9f733-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="9f733-109">例子</span><span class="sxs-lookup"><span data-stu-id="9f733-109">EXAMPLES</span></span>

### <span data-ttu-id="9f733-110">範例 1：使用單一角色建立新雲端服務</span><span class="sxs-lookup"><span data-stu-id="9f733-110">Example 1: Create new cloud service with single role</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile
```

<span data-ttu-id="9f733-111">上述一組命令會建立單一角色的雲端服務</span><span class="sxs-lookup"><span data-stu-id="9f733-111">Above set of commands creates a cloud service with single role</span></span>

### <span data-ttu-id="9f733-112">範例 2：使用單一角色和 RDP 擴充功能建立新雲端服務</span><span class="sxs-lookup"><span data-stu-id="9f733-112">Example 2: Create new cloud service with single role and RDP extension</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosoOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
PS C:\> $extensionProfile = @{extension = @($extension)}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile
```

<span data-ttu-id="9f733-113">上述一組命令會建立具有單一角色和 RDP 擴充功能之雲端服務</span><span class="sxs-lookup"><span data-stu-id="9f733-113">Above set of commands creates a cloud service with single role and RDP extension</span></span>

### <span data-ttu-id="9f733-114">範例 3：使用單一角色和金鑰庫的憑證建立新雲端服務</span><span class="sxs-lookup"><span data-stu-id="9f733-114">Example 3: Create new cloud service with single role and certificate from key vault</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create OS profile object
$keyVault = Get-AzKeyVault -ResourceGroupName ContosOrg -VaultName ContosKeyVault
$certificate=Get-AzKeyVaultCertificate -VaultName ContosKeyVault -Name ContosCert
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
$osProfile = @{secret = @($secretGroup)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -OSProfile $osProfile
```

<span data-ttu-id="9f733-115">上述一組命令會建立一個雲端服務，其中只提供單一角色，以及金鑰庫的憑證。</span><span class="sxs-lookup"><span data-stu-id="9f733-115">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

### <span data-ttu-id="9f733-116">範例 4：建立具有多個角色和擴充功能的新雲端服務</span><span class="sxs-lookup"><span data-stu-id="9f733-116">Example 4: Create new cloud service with multiple roles and extensions</span></span>
```powershell
# Create role profile object
PS C:\> $role1 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $role2 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoBackend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role1, $role2)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'

# Create Geneva extension object
PS C:\> $genevaExtension = New-AzCloudServiceExtensionObject -Name GenevaExtension -Publisher Microsoft.Azure.Geneva -Type GenevaMonitoringPaaS -TypeHandlerVersion "2.14.0.2"
PS C:\> $extensionProfile = @{extension = @($rdpExtension, $genevaExtension)}

# Add tags
$tag=@{"Owner" = "Contoso"}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile                           `
                  -Tag $tag
```

<span data-ttu-id="9f733-117">上述一組命令會建立一個雲端服務，其中只提供單一角色，以及金鑰庫的憑證。</span><span class="sxs-lookup"><span data-stu-id="9f733-117">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

## <span data-ttu-id="9f733-118">參數</span><span class="sxs-lookup"><span data-stu-id="9f733-118">PARAMETERS</span></span>

### <span data-ttu-id="9f733-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f733-119">-AsJob</span></span>
<span data-ttu-id="9f733-120">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="9f733-120">Run the command as a job</span></span>

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

### <span data-ttu-id="9f733-121">-組式</span><span class="sxs-lookup"><span data-stu-id="9f733-121">-Configuration</span></span>
<span data-ttu-id="9f733-122">指定雲端服務的 XML 服務 (.csc) xml 服務組配置。</span><span class="sxs-lookup"><span data-stu-id="9f733-122">Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>

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

### <span data-ttu-id="9f733-123">-ConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="9f733-123">-ConfigurationUrl</span></span>
<span data-ttu-id="9f733-124">指定一個 URL，該 URL 參照到 Blob 服務中的服務群組原則位置。</span><span class="sxs-lookup"><span data-stu-id="9f733-124">Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span>
<span data-ttu-id="9f733-125">服務套件 URL 可以是來自任何儲存帳戶 (SAS) URI 的共用存取簽名。這是只寫入的屬性，不會在 GET 通話中返回。</span><span class="sxs-lookup"><span data-stu-id="9f733-125">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="9f733-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f733-126">-DefaultProfile</span></span>
<span data-ttu-id="9f733-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f733-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f733-128">-ExtensionProfile</span><span class="sxs-lookup"><span data-stu-id="9f733-128">-ExtensionProfile</span></span>
<span data-ttu-id="9f733-129">說明雲端服務擴充功能設定檔。</span><span class="sxs-lookup"><span data-stu-id="9f733-129">Describes a cloud service extension profile.</span></span>
<span data-ttu-id="9f733-130">若要建構，請參閱 EXTENSIONPROFILE 屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9f733-130">To construct, see NOTES section for EXTENSIONPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceExtensionProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f733-131">-位置</span><span class="sxs-lookup"><span data-stu-id="9f733-131">-Location</span></span>
<span data-ttu-id="9f733-132">資源位置。</span><span class="sxs-lookup"><span data-stu-id="9f733-132">Resource location.</span></span>

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

### <span data-ttu-id="9f733-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="9f733-133">-Name</span></span>
<span data-ttu-id="9f733-134">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f733-134">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f733-135">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9f733-135">-NetworkProfile</span></span>
<span data-ttu-id="9f733-136">雲端服務的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="9f733-136">Network Profile for the cloud service.</span></span>
<span data-ttu-id="9f733-137">若要建構，請參閱 NETWORKPROFILE 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9f733-137">To construct, see NOTES section for NETWORKPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceNetworkProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f733-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9f733-138">-NoWait</span></span>
<span data-ttu-id="9f733-139">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="9f733-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9f733-140">-OSProfile</span><span class="sxs-lookup"><span data-stu-id="9f733-140">-OSProfile</span></span>
<span data-ttu-id="9f733-141">說明雲端服務的作業系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="9f733-141">Describes the OS profile for the cloud service.</span></span>
<span data-ttu-id="9f733-142">若要建構，請參閱 OSPROFILE 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9f733-142">To construct, see NOTES section for OSPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f733-143">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="9f733-143">-PackageUrl</span></span>
<span data-ttu-id="9f733-144">指定參照 Blob 服務中服務套件位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="9f733-144">Specifies a URL that refers to the location of the service package in the Blob service.</span></span>
<span data-ttu-id="9f733-145">服務套件 URL 可以是來自任何儲存帳戶 (SAS) URI 的共用存取簽名。這是只寫入的屬性，不會在 GET 通話中返回。</span><span class="sxs-lookup"><span data-stu-id="9f733-145">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="9f733-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f733-146">-ResourceGroupName</span></span>
<span data-ttu-id="9f733-147">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f733-147">Name of the resource group.</span></span>

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

### <span data-ttu-id="9f733-148">-RoleProfile</span><span class="sxs-lookup"><span data-stu-id="9f733-148">-RoleProfile</span></span>
<span data-ttu-id="9f733-149">說明雲端服務的角色設定檔。</span><span class="sxs-lookup"><span data-stu-id="9f733-149">Describes the role profile for the cloud service.</span></span>
<span data-ttu-id="9f733-150">若要建構，請參閱 ROLEPROFILE 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9f733-150">To construct, see NOTES section for ROLEPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceRoleProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f733-151">-StartCloudService</span><span class="sxs-lookup"><span data-stu-id="9f733-151">-StartCloudService</span></span>
<span data-ttu-id="9f733-152"> (選擇性) 指出是否要在建立雲端服務後立即啟動。</span><span class="sxs-lookup"><span data-stu-id="9f733-152">(Optional) Indicates whether to start the cloud service immediately after it is created.</span></span>
<span data-ttu-id="9f733-153">預設值為 `true` 。如果為 False，服務模型仍然會部署，但程式碼不會立即執行。</span><span class="sxs-lookup"><span data-stu-id="9f733-153">The default value is `true`.If false, the service model is still deployed, but the code is not run immediately.</span></span>
<span data-ttu-id="9f733-154">服務會改為 PoweredOff，直到您打電話給 Start，此時服務就會啟動。</span><span class="sxs-lookup"><span data-stu-id="9f733-154">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span>
<span data-ttu-id="9f733-155">即使已部署的服務為關閉電源，仍會產生費用。</span><span class="sxs-lookup"><span data-stu-id="9f733-155">A deployed service still incurs charges, even if it is poweredoff.</span></span>

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

### <span data-ttu-id="9f733-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f733-156">-SubscriptionId</span></span>
<span data-ttu-id="9f733-157">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9f733-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9f733-158">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9f733-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9f733-159">-標記</span><span class="sxs-lookup"><span data-stu-id="9f733-159">-Tag</span></span>
<span data-ttu-id="9f733-160">資源標記。</span><span class="sxs-lookup"><span data-stu-id="9f733-160">Resource tags.</span></span>

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

### <span data-ttu-id="9f733-161">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="9f733-161">-UpgradeMode</span></span>
<span data-ttu-id="9f733-162">雲端服務的更新模式。</span><span class="sxs-lookup"><span data-stu-id="9f733-162">Update mode for the cloud service.</span></span>
<span data-ttu-id="9f733-163">角色實例會配置在部署服務時更新網域。</span><span class="sxs-lookup"><span data-stu-id="9f733-163">Role instances are allocated to update domains when the service is deployed.</span></span>
<span data-ttu-id="9f733-164">更新可以在每個更新網域中手動啟動，或在所有更新網域中自動啟動。可能的值為 \<br /\> \<br /\> **自動** \<br /\> \<br /\> **手動** \<br /\> \<br /\> **同時** \<br /\> \<br /\> 發生 ，如果沒有指定，預設值為自動。如果設定為手動，則必須要求 PUT UpdateDomain 以套用更新。</span><span class="sxs-lookup"><span data-stu-id="9f733-164">Updates can be initiated manually in each update domain or initiated automatically in all update domains.Possible Values are \<br /\>\<br /\>**Auto**\<br /\>\<br /\>**Manual** \<br /\>\<br /\>**Simultaneous**\<br /\>\<br /\>If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span>
<span data-ttu-id="9f733-165">如果設定為自動，系統會自動將更新順序套用至每個更新網域。</span><span class="sxs-lookup"><span data-stu-id="9f733-165">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.CloudServiceUpgradeMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f733-166">-確認</span><span class="sxs-lookup"><span data-stu-id="9f733-166">-Confirm</span></span>
<span data-ttu-id="9f733-167">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9f733-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f733-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f733-168">-WhatIf</span></span>
<span data-ttu-id="9f733-169">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9f733-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f733-170">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9f733-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f733-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f733-171">CommonParameters</span></span>
<span data-ttu-id="9f733-172">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9f733-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f733-173">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f733-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f733-174">輸入</span><span class="sxs-lookup"><span data-stu-id="9f733-174">INPUTS</span></span>

## <span data-ttu-id="9f733-175">輸出</span><span class="sxs-lookup"><span data-stu-id="9f733-175">OUTPUTS</span></span>

### <span data-ttu-id="9f733-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="9f733-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="9f733-177">筆記</span><span class="sxs-lookup"><span data-stu-id="9f733-177">NOTES</span></span>

<span data-ttu-id="9f733-178">別名</span><span class="sxs-lookup"><span data-stu-id="9f733-178">ALIASES</span></span>

<span data-ttu-id="9f733-179">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9f733-179">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9f733-180">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9f733-180">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f733-181">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9f733-181">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9f733-182"><ICloudServiceExtensionProfile>EXTENSIONPROFILE：說明雲端服務擴充功能設定檔。</span><span class="sxs-lookup"><span data-stu-id="9f733-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile>: Describes a cloud service extension profile.</span></span>
  - <span data-ttu-id="9f733-183">`[Extension <IExtension[]>]`：雲端服務的擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="9f733-183">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
    - <span data-ttu-id="9f733-184">`[AutoUpgradeMinorVersion <Boolean?>]`：明確指定平臺是否可以在提供類型HandlerVersion時自動升級至較高的次要版本。</span><span class="sxs-lookup"><span data-stu-id="9f733-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
    - <span data-ttu-id="9f733-185">`[ForceUpdateTag <String>]`：標記以強制使用提供的公用和受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="9f733-185">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="9f733-186">變更標記值可讓您重新經營擴充功能，而不需要變更任何公用或受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="9f733-186">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="9f733-187">如果未變更 forceUpdateTag，處理常式仍然會使用公用或受保護的設定更新。</span><span class="sxs-lookup"><span data-stu-id="9f733-187">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="9f733-188">如果 forceUpdateTag 或任何公用或受保護的設定都沒有變更，延伸模組會流向具有相同序號的角色實例，而是否要重新執行，則由處理常式的執行方式決定</span><span class="sxs-lookup"><span data-stu-id="9f733-188">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
    - <span data-ttu-id="9f733-189">`[Name <String>]`：副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f733-189">`[Name <String>]`: The name of the extension.</span></span>
    - <span data-ttu-id="9f733-190">`[ProtectedSetting <String>]`：已加密的擴充功能之受保護的設定，在送往角色實例之前。</span><span class="sxs-lookup"><span data-stu-id="9f733-190">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
    - <span data-ttu-id="9f733-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="9f733-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
    - <span data-ttu-id="9f733-192">`[Publisher <String>]`：副檔名處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f733-192">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
    - <span data-ttu-id="9f733-193">`[RolesAppliedTo <String[]>]`：可申請此擴充功能的角色清單。</span><span class="sxs-lookup"><span data-stu-id="9f733-193">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="9f733-194">如果未指定屬性或指定 '\*'，延伸模組會適用于雲端服務中的所有角色。</span><span class="sxs-lookup"><span data-stu-id="9f733-194">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
    - <span data-ttu-id="9f733-195">`[Setting <String>]`：擴充功能公用設定。</span><span class="sxs-lookup"><span data-stu-id="9f733-195">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="9f733-196">對於 JSON 擴充功能，這是該擴充功能 JSON 設定。</span><span class="sxs-lookup"><span data-stu-id="9f733-196">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="9f733-197">對於 XML 擴充 (如 RDP) ，這是該副檔名的 XML 設定。</span><span class="sxs-lookup"><span data-stu-id="9f733-197">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
    - <span data-ttu-id="9f733-198">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9f733-198">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="9f733-199">`[Type <String>]`：指定擴充功能的類型。</span><span class="sxs-lookup"><span data-stu-id="9f733-199">`[Type <String>]`: Specifies the type of the extension.</span></span>
    - <span data-ttu-id="9f733-200">`[TypeHandlerVersion <String>]`：指定擴充功能的版本。</span><span class="sxs-lookup"><span data-stu-id="9f733-200">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="9f733-201">指定擴充功能的版本。</span><span class="sxs-lookup"><span data-stu-id="9f733-201">Specifies the version of the extension.</span></span> <span data-ttu-id="9f733-202">如果未指定此元素，或是使用星號 (\*) 做為值，則使用最新版本的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="9f733-202">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="9f733-203">如果以主要版本號碼和星號指定值做為次要版本號碼 (X.) ，會選取指定主要版本的最新次要版本。</span><span class="sxs-lookup"><span data-stu-id="9f733-203">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="9f733-204">如果在 X.Y (指定主要版本號碼和次要版本號碼) ，會選取特定的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="9f733-204">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="9f733-205">如果指定版本，系統即會對角色實例執行自動升級。</span><span class="sxs-lookup"><span data-stu-id="9f733-205">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>

<span data-ttu-id="9f733-206"><ICloudServiceNetworkProfile>NETWORKPROFILE：雲端服務的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="9f733-206">NETWORKPROFILE <ICloudServiceNetworkProfile>: Network Profile for the cloud service.</span></span>
  - <span data-ttu-id="9f733-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`：雲端服務的負載平衡器組組清單。</span><span class="sxs-lookup"><span data-stu-id="9f733-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
    - <span data-ttu-id="9f733-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`：IP 清單</span><span class="sxs-lookup"><span data-stu-id="9f733-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
      - <span data-ttu-id="9f733-209">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="9f733-209">`[Name <String>]`:</span></span> 
      - <span data-ttu-id="9f733-210">`[PrivateIPAddress <String>]`：雲端服務所參照的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9f733-210">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
      - <span data-ttu-id="9f733-211">`[PublicIPAddressId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9f733-211">`[PublicIPAddressId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="9f733-212">`[SubnetId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9f733-212">`[SubnetId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="9f733-213">`[Name <String>]`：資源名稱</span><span class="sxs-lookup"><span data-stu-id="9f733-213">`[Name <String>]`: Resource Name</span></span>
  - <span data-ttu-id="9f733-214">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="9f733-214">`[SwappableCloudService <ISubResource>]`:</span></span> 
    - <span data-ttu-id="9f733-215">`[Id <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9f733-215">`[Id <String>]`: Resource Id</span></span>

<span data-ttu-id="9f733-216"><ICloudServiceOSProfile>OSPROFILE：說明雲端服務的 OS 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9f733-216">OSPROFILE <ICloudServiceOSProfile>: Describes the OS profile for the cloud service.</span></span>
  - <span data-ttu-id="9f733-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`：指定應該要安裝在角色實例上的一組憑證。</span><span class="sxs-lookup"><span data-stu-id="9f733-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
    - <span data-ttu-id="9f733-218">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9f733-218">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="9f733-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`：SourceVault 中包含憑證的重要庫參照清單。</span><span class="sxs-lookup"><span data-stu-id="9f733-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
      - <span data-ttu-id="9f733-220">`[CertificateUrl <String>]`：這是憑證的 URL，已上傳至金鑰庫作為機密。</span><span class="sxs-lookup"><span data-stu-id="9f733-220">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

<span data-ttu-id="9f733-221"><ICloudServiceRoleProfile>ROLEPROFILE：說明雲端服務的角色設定檔。</span><span class="sxs-lookup"><span data-stu-id="9f733-221">ROLEPROFILE <ICloudServiceRoleProfile>: Describes the role profile for the cloud service.</span></span>
  - <span data-ttu-id="9f733-222">`[Role <ICloudServiceRoleProfileProperties[]>]`：雲端服務的角色清單。</span><span class="sxs-lookup"><span data-stu-id="9f733-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
    - <span data-ttu-id="9f733-223">`[Name <String>]`：資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9f733-223">`[Name <String>]`: Resource name.</span></span>
    - <span data-ttu-id="9f733-224">`[SkuCapacity <Int64?>]`：指定雲端服務中的角色實例數目。</span><span class="sxs-lookup"><span data-stu-id="9f733-224">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
    - <span data-ttu-id="9f733-225">`[SkuName <String>]`：SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="9f733-225">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="9f733-226">注意：如果雲端服務目前使用的硬體不支援新的 SKU，您必須刪除並重建雲端服務，或移回舊的 SKU。</span><span class="sxs-lookup"><span data-stu-id="9f733-226">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
    - <span data-ttu-id="9f733-227">`[SkuTier <String>]`：指定雲端服務層級。</span><span class="sxs-lookup"><span data-stu-id="9f733-227">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="9f733-228">可能的值為</span><span class="sxs-lookup"><span data-stu-id="9f733-228">Possible Values are</span></span> <br /><br /> <span data-ttu-id="9f733-229">**標準**</span><span class="sxs-lookup"><span data-stu-id="9f733-229">**Standard**</span></span> <br /><br /> <span data-ttu-id="9f733-230">**基本**</span><span class="sxs-lookup"><span data-stu-id="9f733-230">**Basic**</span></span>

## <span data-ttu-id="9f733-231">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f733-231">RELATED LINKS</span></span>

