---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: 2887c343c9498eb2b8bde51b51226bffc5795ff3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902598"
---
# <span data-ttu-id="161d2-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="161d2-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="161d2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="161d2-102">SYNOPSIS</span></span>
<span data-ttu-id="161d2-103">取得前門前方端點。</span><span class="sxs-lookup"><span data-stu-id="161d2-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="161d2-104">語法</span><span class="sxs-lookup"><span data-stu-id="161d2-104">SYNTAX</span></span>

### <span data-ttu-id="161d2-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="161d2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="161d2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="161d2-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="161d2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="161d2-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="161d2-108">描述</span><span class="sxs-lookup"><span data-stu-id="161d2-108">DESCRIPTION</span></span>
<span data-ttu-id="161d2-109">**Get-AzFrontDoorFrontendPoint** Cmdlet 會取得目前前端資源中符合提供的資訊的所有現有前端端點。</span><span class="sxs-lookup"><span data-stu-id="161d2-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="161d2-110">例子</span><span class="sxs-lookup"><span data-stu-id="161d2-110">EXAMPLES</span></span>

### <span data-ttu-id="161d2-111">範例 1：在 Front Door 中取得所有前端端點"frontdoor1"，這是資源群組 "rg1" 的一部分。</span><span class="sxs-lookup"><span data-stu-id="161d2-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
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

<span data-ttu-id="161d2-112">在 「前門」中取得所有前端端點，這是資源群組「rg1」的一部分。</span><span class="sxs-lookup"><span data-stu-id="161d2-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="161d2-113">範例 2：在 Front Door "frontdoor1" 中取得名稱為 "frontdoor1-azurefd-net" 的 frontend 端點，這是資源群組 "rg1" 的一部分</span><span class="sxs-lookup"><span data-stu-id="161d2-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1" -Name "frontdoor1-azurefd-net"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="161d2-114">取得 Frontdoor1-azurefd-net 在 Front Door "frontdoor1" 中名稱為 frontdoor1-azurefd-net" 的前端端點，這是資源群組 "rg1" 的一部分</span><span class="sxs-lookup"><span data-stu-id="161d2-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="161d2-115">參數</span><span class="sxs-lookup"><span data-stu-id="161d2-115">PARAMETERS</span></span>

### <span data-ttu-id="161d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="161d2-116">-DefaultProfile</span></span>
<span data-ttu-id="161d2-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="161d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="161d2-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="161d2-118">-FrontDoorName</span></span>
<span data-ttu-id="161d2-119">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="161d2-119">Front Door name.</span></span>

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

### <span data-ttu-id="161d2-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="161d2-120">-FrontDoorObject</span></span>
<span data-ttu-id="161d2-121">FrontDoor 物件。</span><span class="sxs-lookup"><span data-stu-id="161d2-121">The FrontDoor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="161d2-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="161d2-122">-Name</span></span>
<span data-ttu-id="161d2-123">前端端點名稱。</span><span class="sxs-lookup"><span data-stu-id="161d2-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="161d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="161d2-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="161d2-125">The resource group name.</span></span>

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

### <span data-ttu-id="161d2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="161d2-126">-ResourceId</span></span>
<span data-ttu-id="161d2-127">前門的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="161d2-127">Resource Id of the Front Door</span></span>

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

### <span data-ttu-id="161d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="161d2-128">CommonParameters</span></span>
<span data-ttu-id="161d2-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="161d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="161d2-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="161d2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="161d2-131">輸入</span><span class="sxs-lookup"><span data-stu-id="161d2-131">INPUTS</span></span>

### <span data-ttu-id="161d2-132">沒有</span><span class="sxs-lookup"><span data-stu-id="161d2-132">None</span></span>

## <span data-ttu-id="161d2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="161d2-133">OUTPUTS</span></span>

### <span data-ttu-id="161d2-134">Microsoft.Azure.Commands.FrontDoor.models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="161d2-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="161d2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="161d2-135">NOTES</span></span>

## <span data-ttu-id="161d2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="161d2-136">RELATED LINKS</span></span>
