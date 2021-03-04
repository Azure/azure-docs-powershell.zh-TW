---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: cb5986d7e8d467c76b64baddb5fd389eda1b5b8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917333"
---
# <span data-ttu-id="c8667-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="c8667-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="c8667-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c8667-102">SYNOPSIS</span></span>
<span data-ttu-id="c8667-103">使用 Front Door 受管理的憑證，或是使用 Azure 金鑰庫的憑證，為自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8667-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="c8667-104">語法</span><span class="sxs-lookup"><span data-stu-id="c8667-104">SYNTAX</span></span>

### <span data-ttu-id="c8667-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c8667-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8667-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8667-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8667-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8667-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8667-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8667-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8667-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8667-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8667-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8667-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8667-111">描述</span><span class="sxs-lookup"><span data-stu-id="c8667-111">DESCRIPTION</span></span>
<span data-ttu-id="c8667-112">**Enable-AzFrontDoorCustomDomainHttps 可** 啟用自訂網域的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8667-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="c8667-113">例子</span><span class="sxs-lookup"><span data-stu-id="c8667-113">EXAMPLES</span></span>

### <span data-ttu-id="c8667-114">範例 1：使用 FrontDoorName 和 ResourceGroupName 使用 FrontDoorName 管理的憑證，為自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8667-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -MinimumTlsVersion "1.2"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="c8667-115">針對使用 Front Door 受管理的憑證，在資源群組"resourcegroup1"中屬於「frontdoor1」一部分的自訂網域「frontendpointname1-custom-xyz」啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8667-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="c8667-116">範例 2：在 Key Vault 中使用自己的憑證，針對使用 FrontDoorName 和 ResourceGroupName 的自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8667-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion -MinimumTlsVersion "1.0"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.0
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="c8667-117">針對使用 Front Door 受管理的憑證，在資源群組"resourcegroup1"中屬於「frontdoor1」一部分的自訂網域「frontendpointname1-custom-xyz」啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8667-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="c8667-118">範例 3：針對使用 Front Door 受管理的憑證使用 PSFrontendEndpoint 物件的自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8667-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -Name "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="c8667-119">使用 Front Door 受管理的憑證，以 PSFrontendEndpoint 物件為自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8667-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="c8667-120">範例 4：使用 Front Door 受管理的憑證，為具有資源識別碼的自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8667-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="c8667-121">針對使用 Front Door 受管理的憑證使用資源識別碼的自訂網域「frontendpointname1-custom-xyz」$resourceId HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8667-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="c8667-122">參數</span><span class="sxs-lookup"><span data-stu-id="c8667-122">PARAMETERS</span></span>

### <span data-ttu-id="c8667-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8667-123">-DefaultProfile</span></span>
<span data-ttu-id="c8667-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8667-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8667-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c8667-125">-FrontDoorName</span></span>
<span data-ttu-id="c8667-126">前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8667-126">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8667-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="c8667-127">-FrontendEndpointName</span></span>
<span data-ttu-id="c8667-128">前端端點名稱。</span><span class="sxs-lookup"><span data-stu-id="c8667-128">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8667-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8667-129">-InputObject</span></span>
<span data-ttu-id="c8667-130">要更新的 Frontend 端點物件。</span><span class="sxs-lookup"><span data-stu-id="c8667-130">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8667-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c8667-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="c8667-132">用戶端建立與前門的 SSL 交握所需的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="c8667-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="c8667-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8667-133">-ResourceGroupName</span></span>
<span data-ttu-id="c8667-134">前門所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c8667-134">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8667-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8667-135">-ResourceId</span></span>
<span data-ttu-id="c8667-136">啟用 HTTPs 之前門端點的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c8667-136">Resource Id of the Front Door endpoint to enable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8667-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="c8667-137">-SecretName</span></span>
<span data-ttu-id="c8667-138">代表完整憑證 PFX 之金鑰庫密碼的名稱</span><span class="sxs-lookup"><span data-stu-id="c8667-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8667-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="c8667-139">-SecretVersion</span></span>
<span data-ttu-id="c8667-140">代表完整憑證 PFX 之金鑰庫密碼的版本</span><span class="sxs-lookup"><span data-stu-id="c8667-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8667-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c8667-141">-VaultId</span></span>
<span data-ttu-id="c8667-142">包含 SSL 憑證的金鑰庫識別碼</span><span class="sxs-lookup"><span data-stu-id="c8667-142">The Key Vault id containing the SSL certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8667-143">-確認</span><span class="sxs-lookup"><span data-stu-id="c8667-143">-Confirm</span></span>
<span data-ttu-id="c8667-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c8667-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8667-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8667-145">-WhatIf</span></span>
<span data-ttu-id="c8667-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8667-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8667-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8667-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8667-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8667-148">CommonParameters</span></span>
<span data-ttu-id="c8667-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c8667-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8667-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8667-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8667-151">輸入</span><span class="sxs-lookup"><span data-stu-id="c8667-151">INPUTS</span></span>

### <span data-ttu-id="c8667-152">System.String</span><span class="sxs-lookup"><span data-stu-id="c8667-152">System.String</span></span>
## <span data-ttu-id="c8667-153">輸出</span><span class="sxs-lookup"><span data-stu-id="c8667-153">OUTPUTS</span></span>

### <span data-ttu-id="c8667-154">Microsoft.Azure.Commands.FrontDoor.models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8667-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="c8667-155">筆記</span><span class="sxs-lookup"><span data-stu-id="c8667-155">NOTES</span></span>

## <span data-ttu-id="c8667-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8667-156">RELATED LINKS</span></span>
