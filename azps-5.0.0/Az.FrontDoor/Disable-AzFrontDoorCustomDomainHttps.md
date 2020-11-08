---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 65c9bca6eb678ff3f3cb0a61d815f8415c715e43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140511"
---
# <span data-ttu-id="8ccac-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="8ccac-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="8ccac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ccac-102">SYNOPSIS</span></span>
<span data-ttu-id="8ccac-103">停用自訂網域的 HTTPS</span><span class="sxs-lookup"><span data-stu-id="8ccac-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="8ccac-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ccac-104">SYNTAX</span></span>

### <span data-ttu-id="8ccac-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8ccac-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ccac-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ccac-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ccac-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ccac-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ccac-108">說明</span><span class="sxs-lookup"><span data-stu-id="8ccac-108">DESCRIPTION</span></span>
<span data-ttu-id="8ccac-109">**Disable-AzFrontDoorCustomDomainHttps** 會停用自訂網域的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="8ccac-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="8ccac-110">示例</span><span class="sxs-lookup"><span data-stu-id="8ccac-110">EXAMPLES</span></span>

### <span data-ttu-id="8ccac-111">範例1：停用 FrontDoorName 和 ResourceGroupName 的自訂網域的 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="8ccac-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
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

<span data-ttu-id="8ccac-112">針對自訂網域停用 HTTPS "frontendpointname1-custom-xyz"，FrontDoorName 為 "frontdoor1" 且 ResourceGroupName 為 "resourcegroup1"。</span><span class="sxs-lookup"><span data-stu-id="8ccac-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="8ccac-113">範例2：針對含 PSFrontendEndpoint 物件的自訂網域停用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="8ccac-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
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

<span data-ttu-id="8ccac-114">針對含 PSFrontendEndpoint 物件的自訂網域停用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="8ccac-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="8ccac-115">範例3：針對具有 ResourceId 的自訂網域停用 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="8ccac-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
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

<span data-ttu-id="8ccac-116">針對自訂網域停用 HTTPS "frontendpointname1-自訂-xyz" 與 ResourceId 為 $resourceId。</span><span class="sxs-lookup"><span data-stu-id="8ccac-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="8ccac-117">參數</span><span class="sxs-lookup"><span data-stu-id="8ccac-117">PARAMETERS</span></span>

### <span data-ttu-id="8ccac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ccac-118">-DefaultProfile</span></span>
<span data-ttu-id="8ccac-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ccac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ccac-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8ccac-120">-FrontDoorName</span></span>
<span data-ttu-id="8ccac-121">前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ccac-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="8ccac-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="8ccac-122">-FrontendEndpointName</span></span>
<span data-ttu-id="8ccac-123">前端端點名稱。</span><span class="sxs-lookup"><span data-stu-id="8ccac-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="8ccac-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ccac-124">-InputObject</span></span>
<span data-ttu-id="8ccac-125">要更新的前端端點物件。</span><span class="sxs-lookup"><span data-stu-id="8ccac-125">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="8ccac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ccac-126">-ResourceGroupName</span></span>
<span data-ttu-id="8ccac-127">前門所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8ccac-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="8ccac-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ccac-128">-ResourceId</span></span>
<span data-ttu-id="8ccac-129">用來停用 HTTPs 之前門端點的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8ccac-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="8ccac-130">-確認</span><span class="sxs-lookup"><span data-stu-id="8ccac-130">-Confirm</span></span>
<span data-ttu-id="8ccac-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ccac-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ccac-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ccac-132">-WhatIf</span></span>
<span data-ttu-id="8ccac-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ccac-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ccac-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ccac-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ccac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ccac-135">CommonParameters</span></span>
<span data-ttu-id="8ccac-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ccac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ccac-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8ccac-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ccac-138">輸入</span><span class="sxs-lookup"><span data-stu-id="8ccac-138">INPUTS</span></span>

### <span data-ttu-id="8ccac-139">System.object</span><span class="sxs-lookup"><span data-stu-id="8ccac-139">System.String</span></span>

## <span data-ttu-id="8ccac-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8ccac-140">OUTPUTS</span></span>

### <span data-ttu-id="8ccac-141">PSFrontendEndpoint 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="8ccac-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="8ccac-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8ccac-142">NOTES</span></span>

## <span data-ttu-id="8ccac-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ccac-143">RELATED LINKS</span></span>