---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6d3eb8d4cbeb2a8c40e3fc6fbf0f54e8973e8f79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140509"
---
# <span data-ttu-id="50b5c-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="50b5c-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="50b5c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="50b5c-103">使用前門管理的憑證或從 Azure 金鑰保存庫使用自己的憑證，為自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="50b5c-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="50b5c-104">句法</span><span class="sxs-lookup"><span data-stu-id="50b5c-104">SYNTAX</span></span>

### <span data-ttu-id="50b5c-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="50b5c-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50b5c-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="50b5c-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50b5c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50b5c-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50b5c-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="50b5c-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50b5c-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50b5c-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50b5c-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="50b5c-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50b5c-111">說明</span><span class="sxs-lookup"><span data-stu-id="50b5c-111">DESCRIPTION</span></span>
<span data-ttu-id="50b5c-112">**Enable-AzFrontDoorCustomDomainHttps** 會啟用自訂網域的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="50b5c-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="50b5c-113">示例</span><span class="sxs-lookup"><span data-stu-id="50b5c-113">EXAMPLES</span></span>

### <span data-ttu-id="50b5c-114">範例1：使用 FrontDoorName 和 ResourceGroupName 的自訂網域啟用 HTTPS，並使用 [前門] 管理的憑證。</span><span class="sxs-lookup"><span data-stu-id="50b5c-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
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

<span data-ttu-id="50b5c-115">在資源群組 "resourcegroup1" 中，使用前門管理的憑證來啟用自訂網域「frontendpointname1-custom-xyz」的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="50b5c-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="50b5c-116">範例2：使用 FrontDoorName 和 ResourceGroupName 在金鑰保存庫中使用自己的憑證，為自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="50b5c-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
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

<span data-ttu-id="50b5c-117">在資源群組 "resourcegroup1" 中，使用前門管理的憑證來啟用自訂網域「frontendpointname1-custom-xyz」的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="50b5c-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="50b5c-118">範例3：針對使用前門管理憑證的 PSFrontendEndpoint 物件啟用自訂網域的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="50b5c-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
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

<span data-ttu-id="50b5c-119">使用由前門管理憑證的 PSFrontendEndpoint 物件，為自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="50b5c-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="50b5c-120">範例4：針對使用前門管理憑證的自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="50b5c-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="50b5c-121">針對自訂網域啟用 HTTPS，使用資源識別碼 $resourceId 使用前門管理的憑證。</span><span class="sxs-lookup"><span data-stu-id="50b5c-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="50b5c-122">參數</span><span class="sxs-lookup"><span data-stu-id="50b5c-122">PARAMETERS</span></span>

### <span data-ttu-id="50b5c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b5c-123">-DefaultProfile</span></span>
<span data-ttu-id="50b5c-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50b5c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50b5c-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="50b5c-125">-FrontDoorName</span></span>
<span data-ttu-id="50b5c-126">前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="50b5c-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="50b5c-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="50b5c-127">-FrontendEndpointName</span></span>
<span data-ttu-id="50b5c-128">前端端點名稱。</span><span class="sxs-lookup"><span data-stu-id="50b5c-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="50b5c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50b5c-129">-InputObject</span></span>
<span data-ttu-id="50b5c-130">要更新的前端端點物件。</span><span class="sxs-lookup"><span data-stu-id="50b5c-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="50b5c-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="50b5c-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="50b5c-132">用戶端所需的最低 TLS 版本，以使用前門建立 SSL 握手。</span><span class="sxs-lookup"><span data-stu-id="50b5c-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="50b5c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50b5c-133">-ResourceGroupName</span></span>
<span data-ttu-id="50b5c-134">前門所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="50b5c-134">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="50b5c-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50b5c-135">-ResourceId</span></span>
<span data-ttu-id="50b5c-136">要啟用 HTTPs 的前門端點的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="50b5c-136">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="50b5c-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="50b5c-137">-SecretName</span></span>
<span data-ttu-id="50b5c-138">代表完整證書 PFX 的主要保存庫密碼名稱</span><span class="sxs-lookup"><span data-stu-id="50b5c-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="50b5c-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="50b5c-139">-SecretVersion</span></span>
<span data-ttu-id="50b5c-140">代表完整證書 PFX 的主要保存庫密碼版本</span><span class="sxs-lookup"><span data-stu-id="50b5c-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="50b5c-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="50b5c-141">-VaultId</span></span>
<span data-ttu-id="50b5c-142">包含 SSL 憑證的主要保存庫識別碼</span><span class="sxs-lookup"><span data-stu-id="50b5c-142">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="50b5c-143">-確認</span><span class="sxs-lookup"><span data-stu-id="50b5c-143">-Confirm</span></span>
<span data-ttu-id="50b5c-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50b5c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50b5c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50b5c-145">-WhatIf</span></span>
<span data-ttu-id="50b5c-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50b5c-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50b5c-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50b5c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50b5c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b5c-148">CommonParameters</span></span>
<span data-ttu-id="50b5c-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50b5c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b5c-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="50b5c-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b5c-151">輸入</span><span class="sxs-lookup"><span data-stu-id="50b5c-151">INPUTS</span></span>

### <span data-ttu-id="50b5c-152">System.object</span><span class="sxs-lookup"><span data-stu-id="50b5c-152">System.String</span></span>
## <span data-ttu-id="50b5c-153">輸出</span><span class="sxs-lookup"><span data-stu-id="50b5c-153">OUTPUTS</span></span>

### <span data-ttu-id="50b5c-154">PSFrontendEndpoint 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="50b5c-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="50b5c-155">筆記</span><span class="sxs-lookup"><span data-stu-id="50b5c-155">NOTES</span></span>

## <span data-ttu-id="50b5c-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="50b5c-156">RELATED LINKS</span></span>