---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: e76d4f0da95e8cc315cbbf4218a68f340b2a5e7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911957"
---
# <span data-ttu-id="c8645-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="c8645-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="c8645-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c8645-102">SYNOPSIS</span></span>
<span data-ttu-id="c8645-103">停用自訂網域的 HTTPS</span><span class="sxs-lookup"><span data-stu-id="c8645-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="c8645-104">語法</span><span class="sxs-lookup"><span data-stu-id="c8645-104">SYNTAX</span></span>

### <span data-ttu-id="c8645-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c8645-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8645-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8645-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8645-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8645-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8645-108">描述</span><span class="sxs-lookup"><span data-stu-id="c8645-108">DESCRIPTION</span></span>
<span data-ttu-id="c8645-109">**Disable-AzFrontDoorCustomDomainHttps 會** 停用自訂網域的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8645-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="c8645-110">例子</span><span class="sxs-lookup"><span data-stu-id="c8645-110">EXAMPLES</span></span>

### <span data-ttu-id="c8645-111">範例 1：停用具有 FrontDoorName 和 ResourceGroupName 之自訂網域的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8645-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
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

<span data-ttu-id="c8645-112">停用自訂網域的 HTTPS"frontendpointname1-custom-xyz"，且 FrontDoorName 為"frontdoor1"，ResourceGroupName 為 "resourcegroup1"。</span><span class="sxs-lookup"><span data-stu-id="c8645-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="c8645-113">範例 2：停用具有 PSFrontendEndpoint 物件的自訂網域 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8645-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Disable-AzFrontDoorCustomDomainHttps -InputObject $frontendEndpointObj 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
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

<span data-ttu-id="c8645-114">停用具有 PSFrontendEndpoint 物件的自訂網域 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8645-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="c8645-115">範例 3：停用具有 ResourceId 之自訂網域的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="c8645-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
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

<span data-ttu-id="c8645-116">停用具有 ResourceId 做為自訂網域 「frontendpointname1-custom-xyz」的 HTTPS $resourceId。</span><span class="sxs-lookup"><span data-stu-id="c8645-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="c8645-117">參數</span><span class="sxs-lookup"><span data-stu-id="c8645-117">PARAMETERS</span></span>

### <span data-ttu-id="c8645-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8645-118">-DefaultProfile</span></span>
<span data-ttu-id="c8645-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8645-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8645-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c8645-120">-FrontDoorName</span></span>
<span data-ttu-id="c8645-121">前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8645-121">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8645-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="c8645-122">-FrontendEndpointName</span></span>
<span data-ttu-id="c8645-123">前端端點名稱。</span><span class="sxs-lookup"><span data-stu-id="c8645-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8645-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8645-124">-InputObject</span></span>
<span data-ttu-id="c8645-125">要更新的 Frontend 端點物件。</span><span class="sxs-lookup"><span data-stu-id="c8645-125">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8645-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8645-126">-ResourceGroupName</span></span>
<span data-ttu-id="c8645-127">前門所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c8645-127">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8645-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8645-128">-ResourceId</span></span>
<span data-ttu-id="c8645-129">要停用 HTTPs 之前門端點的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c8645-129">Resource Id of the Front Door endpoint to disable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8645-130">-確認</span><span class="sxs-lookup"><span data-stu-id="c8645-130">-Confirm</span></span>
<span data-ttu-id="c8645-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c8645-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8645-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8645-132">-WhatIf</span></span>
<span data-ttu-id="c8645-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8645-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8645-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8645-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8645-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8645-135">CommonParameters</span></span>
<span data-ttu-id="c8645-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c8645-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8645-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8645-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8645-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c8645-138">INPUTS</span></span>

### <span data-ttu-id="c8645-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c8645-139">System.String</span></span>

## <span data-ttu-id="c8645-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c8645-140">OUTPUTS</span></span>

### <span data-ttu-id="c8645-141">Microsoft.Azure.Commands.FrontDoor.models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8645-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="c8645-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c8645-142">NOTES</span></span>

## <span data-ttu-id="c8645-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8645-143">RELATED LINKS</span></span>
