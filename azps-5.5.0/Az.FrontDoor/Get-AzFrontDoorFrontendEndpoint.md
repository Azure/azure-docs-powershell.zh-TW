---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: cc07dd366d5c82705a23e3b9276ee9d681c6ae2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143126"
---
# <span data-ttu-id="68ab3-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="68ab3-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="68ab3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="68ab3-103">取得前蓋前端端點。</span><span class="sxs-lookup"><span data-stu-id="68ab3-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="68ab3-104">句法</span><span class="sxs-lookup"><span data-stu-id="68ab3-104">SYNTAX</span></span>

### <span data-ttu-id="68ab3-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="68ab3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68ab3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ab3-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68ab3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ab3-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68ab3-108">說明</span><span class="sxs-lookup"><span data-stu-id="68ab3-108">DESCRIPTION</span></span>
<span data-ttu-id="68ab3-109">**AzFrontDoorFrontendEndpoint** Cmdlet 會取得目前的前門資源中符合所提供資訊的所有現有前端端點。</span><span class="sxs-lookup"><span data-stu-id="68ab3-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="68ab3-110">示例</span><span class="sxs-lookup"><span data-stu-id="68ab3-110">EXAMPLES</span></span>

### <span data-ttu-id="68ab3-111">範例1：取得前門 "frontdoor1" 中的所有前端端點，這是資源群組 "rg1" 的一部分。</span><span class="sxs-lookup"><span data-stu-id="68ab3-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
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

<span data-ttu-id="68ab3-112">取得前門 "frontdoor1" 中的所有前端端點，這是資源群組 "rg1" 的一部分。</span><span class="sxs-lookup"><span data-stu-id="68ab3-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="68ab3-113">範例2：取得名為 "frontdoor1-azurefd-net" 的前端端點，該名稱是 [frontdoor1] 資源群組 "rg1" 的一部分。</span><span class="sxs-lookup"><span data-stu-id="68ab3-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
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

<span data-ttu-id="68ab3-114">在名為 "frontdoor1-azurefd-net" 的前端端點中取得「frontdoor1」（資源群組 "rg1" 的一部分）</span><span class="sxs-lookup"><span data-stu-id="68ab3-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="68ab3-115">參數</span><span class="sxs-lookup"><span data-stu-id="68ab3-115">PARAMETERS</span></span>

### <span data-ttu-id="68ab3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ab3-116">-DefaultProfile</span></span>
<span data-ttu-id="68ab3-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68ab3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68ab3-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="68ab3-118">-FrontDoorName</span></span>
<span data-ttu-id="68ab3-119">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="68ab3-119">Front Door name.</span></span>

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

### <span data-ttu-id="68ab3-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="68ab3-120">-FrontDoorObject</span></span>
<span data-ttu-id="68ab3-121">FrontDoor 物件。</span><span class="sxs-lookup"><span data-stu-id="68ab3-121">The FrontDoor object.</span></span>

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

### <span data-ttu-id="68ab3-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="68ab3-122">-Name</span></span>
<span data-ttu-id="68ab3-123">前端端點名稱。</span><span class="sxs-lookup"><span data-stu-id="68ab3-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="68ab3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ab3-124">-ResourceGroupName</span></span>
<span data-ttu-id="68ab3-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68ab3-125">The resource group name.</span></span>

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

### <span data-ttu-id="68ab3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68ab3-126">-ResourceId</span></span>
<span data-ttu-id="68ab3-127">前門的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="68ab3-127">Resource Id of the Front Door</span></span>

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

### <span data-ttu-id="68ab3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ab3-128">CommonParameters</span></span>
<span data-ttu-id="68ab3-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68ab3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ab3-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="68ab3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ab3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="68ab3-131">INPUTS</span></span>

### <span data-ttu-id="68ab3-132">所有</span><span class="sxs-lookup"><span data-stu-id="68ab3-132">None</span></span>

## <span data-ttu-id="68ab3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="68ab3-133">OUTPUTS</span></span>

### <span data-ttu-id="68ab3-134">PSFrontendEndpoint 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="68ab3-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="68ab3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="68ab3-135">NOTES</span></span>

## <span data-ttu-id="68ab3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="68ab3-136">RELATED LINKS</span></span>
