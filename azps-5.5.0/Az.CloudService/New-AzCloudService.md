---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 24e90ebae59c9d9a4449c57270b7ca69f9b05b88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138734"
---
# <span data-ttu-id="e5e58-101">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="e5e58-101">New-AzCloudService</span></span>

## <span data-ttu-id="e5e58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5e58-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e58-103">建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="e5e58-103">Create or update a cloud service.</span></span>
<span data-ttu-id="e5e58-104">請注意，有些屬性只能在建立雲端服務期間設定。</span><span class="sxs-lookup"><span data-stu-id="e5e58-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="e5e58-105">句法</span><span class="sxs-lookup"><span data-stu-id="e5e58-105">SYNTAX</span></span>

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e5e58-106">說明</span><span class="sxs-lookup"><span data-stu-id="e5e58-106">DESCRIPTION</span></span>
<span data-ttu-id="e5e58-107">建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="e5e58-107">Create or update a cloud service.</span></span>
<span data-ttu-id="e5e58-108">請注意，有些屬性只能在建立雲端服務期間設定。</span><span class="sxs-lookup"><span data-stu-id="e5e58-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="e5e58-109">示例</span><span class="sxs-lookup"><span data-stu-id="e5e58-109">EXAMPLES</span></span>

### <span data-ttu-id="e5e58-110">範例1：使用單一角色建立新的雲端服務</span><span class="sxs-lookup"><span data-stu-id="e5e58-110">Example 1: Create new cloud service with single role</span></span>
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

<span data-ttu-id="e5e58-111">上方的命令集建立含單一角色的雲端服務</span><span class="sxs-lookup"><span data-stu-id="e5e58-111">Above set of commands creates a cloud service with single role</span></span>

### <span data-ttu-id="e5e58-112">範例2：使用單一角色和 RDP 延伸建立新的雲端服務</span><span class="sxs-lookup"><span data-stu-id="e5e58-112">Example 2: Create new cloud service with single role and RDP extension</span></span>
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

<span data-ttu-id="e5e58-113">上方的命令集會建立含單一角色和 RDP 延伸的雲端服務</span><span class="sxs-lookup"><span data-stu-id="e5e58-113">Above set of commands creates a cloud service with single role and RDP extension</span></span>

### <span data-ttu-id="e5e58-114">範例3：使用單一角色和金鑰保存庫的憑證來建立新的雲端服務</span><span class="sxs-lookup"><span data-stu-id="e5e58-114">Example 3: Create new cloud service with single role and certificate from key vault</span></span>
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

<span data-ttu-id="e5e58-115">上方的命令集會從主要電子倉庫的單一角色和憑證建立雲端服務。</span><span class="sxs-lookup"><span data-stu-id="e5e58-115">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

### <span data-ttu-id="e5e58-116">範例4：使用多個角色和延長線建立新的雲端服務</span><span class="sxs-lookup"><span data-stu-id="e5e58-116">Example 4: Create new cloud service with multiple roles and extensions</span></span>
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

<span data-ttu-id="e5e58-117">上方的命令集會從主要電子倉庫的單一角色和憑證建立雲端服務。</span><span class="sxs-lookup"><span data-stu-id="e5e58-117">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

## <span data-ttu-id="e5e58-118">參數</span><span class="sxs-lookup"><span data-stu-id="e5e58-118">PARAMETERS</span></span>

### <span data-ttu-id="e5e58-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5e58-119">-AsJob</span></span>
<span data-ttu-id="e5e58-120">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="e5e58-120">Run the command as a job</span></span>

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

### <span data-ttu-id="e5e58-121">-配置</span><span class="sxs-lookup"><span data-stu-id="e5e58-121">-Configuration</span></span>
<span data-ttu-id="e5e58-122">指定雲端服務的 XML 服務配置 ( .cscfg) 。</span><span class="sxs-lookup"><span data-stu-id="e5e58-122">Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>

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

### <span data-ttu-id="e5e58-123">-ConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="e5e58-123">-ConfigurationUrl</span></span>
<span data-ttu-id="e5e58-124">指定在 Blob 服務中參照服務配置位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="e5e58-124">Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span>
<span data-ttu-id="e5e58-125">您可以從任何儲存空間帳戶 (SAS) URI，以共用存取簽章的服務套件 URL。這是只寫屬性，不會在 [取得呼叫] 中傳回。</span><span class="sxs-lookup"><span data-stu-id="e5e58-125">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="e5e58-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e58-126">-DefaultProfile</span></span>
<span data-ttu-id="e5e58-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5e58-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5e58-128">-ExtensionProfile</span><span class="sxs-lookup"><span data-stu-id="e5e58-128">-ExtensionProfile</span></span>
<span data-ttu-id="e5e58-129">描述雲端服務延伸設定檔。</span><span class="sxs-lookup"><span data-stu-id="e5e58-129">Describes a cloud service extension profile.</span></span>
<span data-ttu-id="e5e58-130">若要建立，請參閱 EXTENSIONPROFILE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="e5e58-130">To construct, see NOTES section for EXTENSIONPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e5e58-131">-位置</span><span class="sxs-lookup"><span data-stu-id="e5e58-131">-Location</span></span>
<span data-ttu-id="e5e58-132">資源位置。</span><span class="sxs-lookup"><span data-stu-id="e5e58-132">Resource location.</span></span>

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

### <span data-ttu-id="e5e58-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5e58-133">-Name</span></span>
<span data-ttu-id="e5e58-134">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5e58-134">Name of the cloud service.</span></span>

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

### <span data-ttu-id="e5e58-135">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e5e58-135">-NetworkProfile</span></span>
<span data-ttu-id="e5e58-136">雲端服務的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="e5e58-136">Network Profile for the cloud service.</span></span>
<span data-ttu-id="e5e58-137">若要建立，請參閱 NETWORKPROFILE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="e5e58-137">To construct, see NOTES section for NETWORKPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e5e58-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e5e58-138">-NoWait</span></span>
<span data-ttu-id="e5e58-139">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="e5e58-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e5e58-140">-OSProfile</span><span class="sxs-lookup"><span data-stu-id="e5e58-140">-OSProfile</span></span>
<span data-ttu-id="e5e58-141">描述雲端服務的 OS 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e5e58-141">Describes the OS profile for the cloud service.</span></span>
<span data-ttu-id="e5e58-142">若要建立，請參閱 OSPROFILE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="e5e58-142">To construct, see NOTES section for OSPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e5e58-143">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="e5e58-143">-PackageUrl</span></span>
<span data-ttu-id="e5e58-144">指定參照 Blob 服務中服務套件位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="e5e58-144">Specifies a URL that refers to the location of the service package in the Blob service.</span></span>
<span data-ttu-id="e5e58-145">您可以從任何儲存空間帳戶 (SAS) URI，以共用存取簽章的服務套件 URL。這是只寫屬性，不會在 [取得呼叫] 中傳回。</span><span class="sxs-lookup"><span data-stu-id="e5e58-145">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="e5e58-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e58-146">-ResourceGroupName</span></span>
<span data-ttu-id="e5e58-147">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5e58-147">Name of the resource group.</span></span>

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

### <span data-ttu-id="e5e58-148">-RoleProfile</span><span class="sxs-lookup"><span data-stu-id="e5e58-148">-RoleProfile</span></span>
<span data-ttu-id="e5e58-149">描述雲端服務的角色設定檔。</span><span class="sxs-lookup"><span data-stu-id="e5e58-149">Describes the role profile for the cloud service.</span></span>
<span data-ttu-id="e5e58-150">若要建立，請參閱 ROLEPROFILE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="e5e58-150">To construct, see NOTES section for ROLEPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e5e58-151">-StartCloudService</span><span class="sxs-lookup"><span data-stu-id="e5e58-151">-StartCloudService</span></span>
<span data-ttu-id="e5e58-152"> (選用) 指出是否要在建立雲端服務後立即啟動。</span><span class="sxs-lookup"><span data-stu-id="e5e58-152">(Optional) Indicates whether to start the cloud service immediately after it is created.</span></span>
<span data-ttu-id="e5e58-153">預設值為 `true` 。如果是 false，則表示服務模型仍在部署，但程式碼不會立即執行。</span><span class="sxs-lookup"><span data-stu-id="e5e58-153">The default value is `true`.If false, the service model is still deployed, but the code is not run immediately.</span></span>
<span data-ttu-id="e5e58-154">相反地，服務會在您呼叫 Start 之前 PoweredOff，直到該服務開始時才會啟動。</span><span class="sxs-lookup"><span data-stu-id="e5e58-154">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span>
<span data-ttu-id="e5e58-155">即使是 poweredoff，部署的服務仍會產生費用。</span><span class="sxs-lookup"><span data-stu-id="e5e58-155">A deployed service still incurs charges, even if it is poweredoff.</span></span>

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

### <span data-ttu-id="e5e58-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5e58-156">-SubscriptionId</span></span>
<span data-ttu-id="e5e58-157">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e5e58-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e5e58-158">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e5e58-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e5e58-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5e58-159">-Tag</span></span>
<span data-ttu-id="e5e58-160">資源標記。</span><span class="sxs-lookup"><span data-stu-id="e5e58-160">Resource tags.</span></span>

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

### <span data-ttu-id="e5e58-161">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="e5e58-161">-UpgradeMode</span></span>
<span data-ttu-id="e5e58-162">雲端服務的更新模式。</span><span class="sxs-lookup"><span data-stu-id="e5e58-162">Update mode for the cloud service.</span></span>
<span data-ttu-id="e5e58-163">部署服務時，系統會將角色實例指派給更新網域。</span><span class="sxs-lookup"><span data-stu-id="e5e58-163">Role instances are allocated to update domains when the service is deployed.</span></span>
<span data-ttu-id="e5e58-164">更新可以在每個更新網域中手動啟動，或是在所有更新網域中自動啟動。可能的值為 \<br /\> \<br /\> **自動** \<br /\> \<br /\> **手動手動** \<br /\> \<br /\>  \<br /\> \<br /\> （如果沒有指定，則預設值為 auto）。如果設定為 [手動]，則必須呼叫 UpdateDomain，才能套用更新。</span><span class="sxs-lookup"><span data-stu-id="e5e58-164">Updates can be initiated manually in each update domain or initiated automatically in all update domains.Possible Values are \<br /\>\<br /\>**Auto**\<br /\>\<br /\>**Manual** \<br /\>\<br /\>**Simultaneous**\<br /\>\<br /\>If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span>
<span data-ttu-id="e5e58-165">如果設為 Auto，更新會自動套用至每個更新網域。</span><span class="sxs-lookup"><span data-stu-id="e5e58-165">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

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

### <span data-ttu-id="e5e58-166">-確認</span><span class="sxs-lookup"><span data-stu-id="e5e58-166">-Confirm</span></span>
<span data-ttu-id="e5e58-167">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5e58-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5e58-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5e58-168">-WhatIf</span></span>
<span data-ttu-id="e5e58-169">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5e58-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5e58-170">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5e58-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5e58-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e58-171">CommonParameters</span></span>
<span data-ttu-id="e5e58-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5e58-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e58-173">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e5e58-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e58-174">輸入</span><span class="sxs-lookup"><span data-stu-id="e5e58-174">INPUTS</span></span>

## <span data-ttu-id="e5e58-175">輸出</span><span class="sxs-lookup"><span data-stu-id="e5e58-175">OUTPUTS</span></span>

### <span data-ttu-id="e5e58-176">ICloudService （CloudService）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="e5e58-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="e5e58-177">筆記</span><span class="sxs-lookup"><span data-stu-id="e5e58-177">NOTES</span></span>

<span data-ttu-id="e5e58-178">別名</span><span class="sxs-lookup"><span data-stu-id="e5e58-178">ALIASES</span></span>

<span data-ttu-id="e5e58-179">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e5e58-179">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e5e58-180">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e5e58-180">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e5e58-181">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e5e58-181">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e5e58-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile> ：說明雲端服務延伸設定檔。</span><span class="sxs-lookup"><span data-stu-id="e5e58-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile>: Describes a cloud service extension profile.</span></span>
  - <span data-ttu-id="e5e58-183">`[Extension <IExtension[]>]`：雲端服務的延伸清單。</span><span class="sxs-lookup"><span data-stu-id="e5e58-183">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
    - <span data-ttu-id="e5e58-184">`[AutoUpgradeMinorVersion <Boolean?>]`：明確指定平臺在可用時是否可自動將 typeHandlerVersion 升級至較高的次要版本。</span><span class="sxs-lookup"><span data-stu-id="e5e58-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
    - <span data-ttu-id="e5e58-185">`[ForceUpdateTag <String>]`：標記以強制套用提供的公用和受保護設定。</span><span class="sxs-lookup"><span data-stu-id="e5e58-185">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="e5e58-186">變更 tag 值可讓您重新執行延伸，而不需變更任何公用或受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="e5e58-186">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="e5e58-187">如果 forceUpdateTag 未變更，則處理常式仍會套用對公眾或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="e5e58-187">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="e5e58-188">如果沒有 forceUpdateTag，也不會變更任何公開或受保護的設定，延伸將會以相同的序號碼流向角色實例，而不論是否重新執行，都可以使用處理程式的實現</span><span class="sxs-lookup"><span data-stu-id="e5e58-188">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
    - <span data-ttu-id="e5e58-189">`[Name <String>]`：延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5e58-189">`[Name <String>]`: The name of the extension.</span></span>
    - <span data-ttu-id="e5e58-190">`[ProtectedSetting <String>]`：已在傳送至角色實例之前加密之副檔名的受保護設定。</span><span class="sxs-lookup"><span data-stu-id="e5e58-190">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
    - <span data-ttu-id="e5e58-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e5e58-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
    - <span data-ttu-id="e5e58-192">`[Publisher <String>]`：延伸處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5e58-192">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
    - <span data-ttu-id="e5e58-193">`[RolesAppliedTo <String[]>]`：選用的角色清單來套用此延伸。</span><span class="sxs-lookup"><span data-stu-id="e5e58-193">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="e5e58-194">如果未指定屬性或指定了 ' \*」，則會將延伸套用到雲端服務中的所有角色。</span><span class="sxs-lookup"><span data-stu-id="e5e58-194">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
    - <span data-ttu-id="e5e58-195">`[Setting <String>]`：延伸的公開設定。</span><span class="sxs-lookup"><span data-stu-id="e5e58-195">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="e5e58-196">對於 JSON 延伸，這是延伸的 JSON 設定。</span><span class="sxs-lookup"><span data-stu-id="e5e58-196">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="e5e58-197">針對 XML 延伸 (例如 RDP) ，這是延伸的 XML 設定。</span><span class="sxs-lookup"><span data-stu-id="e5e58-197">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
    - <span data-ttu-id="e5e58-198">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e5e58-198">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="e5e58-199">`[Type <String>]`：指定延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="e5e58-199">`[Type <String>]`: Specifies the type of the extension.</span></span>
    - <span data-ttu-id="e5e58-200">`[TypeHandlerVersion <String>]`：指定延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="e5e58-200">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="e5e58-201">指定副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="e5e58-201">Specifies the version of the extension.</span></span> <span data-ttu-id="e5e58-202">如果未指定此元素，或使用星號 ( \* ) 作為值，就會使用最新的延伸版本。</span><span class="sxs-lookup"><span data-stu-id="e5e58-202">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="e5e58-203">如果將該值指定為主要版本號碼，並以星號做為次要版本號碼 (X. ) ，則會選取指定主要版本的最新次要版本。</span><span class="sxs-lookup"><span data-stu-id="e5e58-203">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="e5e58-204">如果 (X-y) 指定主要版本號碼和次要版本號碼，則會選取特定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="e5e58-204">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="e5e58-205">如果指定版本，則會在角色實例上執行自動升級。</span><span class="sxs-lookup"><span data-stu-id="e5e58-205">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>

<span data-ttu-id="e5e58-206">NETWORKPROFILE <ICloudServiceNetworkProfile> ：雲端服務的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="e5e58-206">NETWORKPROFILE <ICloudServiceNetworkProfile>: Network Profile for the cloud service.</span></span>
  - <span data-ttu-id="e5e58-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`：雲端服務的負載平衡器設定清單。</span><span class="sxs-lookup"><span data-stu-id="e5e58-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
    - <span data-ttu-id="e5e58-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`： IP 清單</span><span class="sxs-lookup"><span data-stu-id="e5e58-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
      - <span data-ttu-id="e5e58-209">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e5e58-209">`[Name <String>]`:</span></span> 
      - <span data-ttu-id="e5e58-210">`[PrivateIPAddress <String>]`：雲端服務所參照的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e5e58-210">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
      - <span data-ttu-id="e5e58-211">`[PublicIPAddressId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e5e58-211">`[PublicIPAddressId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="e5e58-212">`[SubnetId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e5e58-212">`[SubnetId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="e5e58-213">`[Name <String>]`：資源名稱</span><span class="sxs-lookup"><span data-stu-id="e5e58-213">`[Name <String>]`: Resource Name</span></span>
  - <span data-ttu-id="e5e58-214">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="e5e58-214">`[SwappableCloudService <ISubResource>]`:</span></span> 
    - <span data-ttu-id="e5e58-215">`[Id <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e5e58-215">`[Id <String>]`: Resource Id</span></span>

<span data-ttu-id="e5e58-216">OSPROFILE <ICloudServiceOSProfile> ：說明雲端服務的 OS 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e5e58-216">OSPROFILE <ICloudServiceOSProfile>: Describes the OS profile for the cloud service.</span></span>
  - <span data-ttu-id="e5e58-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`：指定應該安裝在角色實例上的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="e5e58-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
    - <span data-ttu-id="e5e58-218">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e5e58-218">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="e5e58-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`： SourceVault 中包含憑證的主要保存庫參照清單。</span><span class="sxs-lookup"><span data-stu-id="e5e58-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
      - <span data-ttu-id="e5e58-220">`[CertificateUrl <String>]`：這是已上傳到金鑰保存庫的憑證 URL （密碼）。</span><span class="sxs-lookup"><span data-stu-id="e5e58-220">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

<span data-ttu-id="e5e58-221">ROLEPROFILE <ICloudServiceRoleProfile> ：說明雲端服務的角色設定檔。</span><span class="sxs-lookup"><span data-stu-id="e5e58-221">ROLEPROFILE <ICloudServiceRoleProfile>: Describes the role profile for the cloud service.</span></span>
  - <span data-ttu-id="e5e58-222">`[Role <ICloudServiceRoleProfileProperties[]>]`：雲端服務的角色清單。</span><span class="sxs-lookup"><span data-stu-id="e5e58-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
    - <span data-ttu-id="e5e58-223">`[Name <String>]`：資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e5e58-223">`[Name <String>]`: Resource name.</span></span>
    - <span data-ttu-id="e5e58-224">`[SkuCapacity <Int64?>]`：指定雲端服務中的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="e5e58-224">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
    - <span data-ttu-id="e5e58-225">`[SkuName <String>]`： Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="e5e58-225">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="e5e58-226">注意：如果雲端服務目前所在的硬體不支援新版 SKU，您必須刪除並重新建立雲端服務，或移回舊版 SKU。</span><span class="sxs-lookup"><span data-stu-id="e5e58-226">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
    - <span data-ttu-id="e5e58-227">`[SkuTier <String>]`：指定雲端服務的層級。</span><span class="sxs-lookup"><span data-stu-id="e5e58-227">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="e5e58-228">可能的值為</span><span class="sxs-lookup"><span data-stu-id="e5e58-228">Possible Values are</span></span> <br /><br /> <span data-ttu-id="e5e58-229">**標準**</span><span class="sxs-lookup"><span data-stu-id="e5e58-229">**Standard**</span></span> <br /><br /> <span data-ttu-id="e5e58-230">**空白**</span><span class="sxs-lookup"><span data-stu-id="e5e58-230">**Basic**</span></span>

## <span data-ttu-id="e5e58-231">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5e58-231">RELATED LINKS</span></span>

