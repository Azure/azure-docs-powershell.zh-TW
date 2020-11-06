---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6edf891d693e0c1cb2143236d12e623fdd2b4a3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612381"
---
# <span data-ttu-id="275f6-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="275f6-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="275f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="275f6-102">SYNOPSIS</span></span>
<span data-ttu-id="275f6-103">使用前門管理的憑證或從 Azure 金鑰保存庫使用自己的憑證，為自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="275f6-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="275f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="275f6-104">SYNTAX</span></span>

### <span data-ttu-id="275f6-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="275f6-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="275f6-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="275f6-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275f6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="275f6-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275f6-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="275f6-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275f6-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="275f6-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275f6-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="275f6-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="275f6-111">說明</span><span class="sxs-lookup"><span data-stu-id="275f6-111">DESCRIPTION</span></span>
<span data-ttu-id="275f6-112">**Enable-AzFrontDoorCustomDomainHttps** 會啟用自訂網域的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="275f6-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="275f6-113">示例</span><span class="sxs-lookup"><span data-stu-id="275f6-113">EXAMPLES</span></span>

### <span data-ttu-id="275f6-114">範例1：使用 FrontDoorName 和 ResourceGroupName 的自訂網域啟用 HTTPS，並使用 [前門] 管理的憑證。</span><span class="sxs-lookup"><span data-stu-id="275f6-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="275f6-115">在資源群組 "resourcegroup1" 中，使用前門管理的憑證來啟用自訂網域「frontendpointname1-custom-xyz」的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="275f6-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="275f6-116">範例2：使用 FrontDoorName 和 ResourceGroupName 在金鑰保存庫中使用自己的憑證，為自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="275f6-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="275f6-117">在資源群組 "resourcegroup1" 中，使用前門管理的憑證來啟用自訂網域「frontendpointname1-custom-xyz」的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="275f6-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="275f6-118">範例3：針對使用前門管理憑證的 PSFrontendEndpoint 物件啟用自訂網域的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="275f6-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="275f6-119">使用由前門管理憑證的 PSFrontendEndpoint 物件，為自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="275f6-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="275f6-120">範例4：針對使用前門管理憑證的自訂網域啟用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="275f6-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="275f6-121">針對自訂網域啟用 HTTPS，使用資源識別碼 $resourceId 使用前門管理的憑證。</span><span class="sxs-lookup"><span data-stu-id="275f6-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="275f6-122">參數</span><span class="sxs-lookup"><span data-stu-id="275f6-122">PARAMETERS</span></span>

### <span data-ttu-id="275f6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275f6-123">-DefaultProfile</span></span>
<span data-ttu-id="275f6-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="275f6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="275f6-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="275f6-125">-FrontDoorName</span></span>
<span data-ttu-id="275f6-126">前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="275f6-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="275f6-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="275f6-127">-FrontendEndpointName</span></span>
<span data-ttu-id="275f6-128">前端端點名稱。</span><span class="sxs-lookup"><span data-stu-id="275f6-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="275f6-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="275f6-129">-InputObject</span></span>
<span data-ttu-id="275f6-130">要更新的前端端點物件。</span><span class="sxs-lookup"><span data-stu-id="275f6-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="275f6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275f6-131">-ResourceGroupName</span></span>
<span data-ttu-id="275f6-132">前門所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="275f6-132">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="275f6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="275f6-133">-ResourceId</span></span>
<span data-ttu-id="275f6-134">要啟用 HTTPs 的前門端點的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="275f6-134">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="275f6-135">-SecretName</span><span class="sxs-lookup"><span data-stu-id="275f6-135">-SecretName</span></span>
<span data-ttu-id="275f6-136">代表完整證書 PFX 的主要保存庫密碼名稱</span><span class="sxs-lookup"><span data-stu-id="275f6-136">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="275f6-137">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="275f6-137">-SecretVersion</span></span>
<span data-ttu-id="275f6-138">代表完整證書 PFX 的主要保存庫密碼版本</span><span class="sxs-lookup"><span data-stu-id="275f6-138">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="275f6-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="275f6-139">-VaultId</span></span>
<span data-ttu-id="275f6-140">包含 SSL 憑證的主要保存庫識別碼</span><span class="sxs-lookup"><span data-stu-id="275f6-140">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="275f6-141">-確認</span><span class="sxs-lookup"><span data-stu-id="275f6-141">-Confirm</span></span>
<span data-ttu-id="275f6-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="275f6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="275f6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275f6-143">-WhatIf</span></span>
<span data-ttu-id="275f6-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="275f6-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="275f6-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="275f6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="275f6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275f6-146">CommonParameters</span></span>
<span data-ttu-id="275f6-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="275f6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275f6-148">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="275f6-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275f6-149">輸入</span><span class="sxs-lookup"><span data-stu-id="275f6-149">INPUTS</span></span>

### <span data-ttu-id="275f6-150">System.object</span><span class="sxs-lookup"><span data-stu-id="275f6-150">System.String</span></span>

## <span data-ttu-id="275f6-151">輸出</span><span class="sxs-lookup"><span data-stu-id="275f6-151">OUTPUTS</span></span>

### <span data-ttu-id="275f6-152">PSFrontendEndpoint 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="275f6-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="275f6-153">筆記</span><span class="sxs-lookup"><span data-stu-id="275f6-153">NOTES</span></span>

## <span data-ttu-id="275f6-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="275f6-154">RELATED LINKS</span></span>
