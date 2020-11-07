---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
ms.openlocfilehash: ca54e2cc86daca89a9872366dea32b375080c63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624380"
---
# <span data-ttu-id="29b2d-101">Get-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="29b2d-101">Get-AzureRmFrontDoor</span></span>

## <span data-ttu-id="29b2d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="29b2d-103">取得前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="29b2d-103">Get Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29b2d-104">句法</span><span class="sxs-lookup"><span data-stu-id="29b2d-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29b2d-105">說明</span><span class="sxs-lookup"><span data-stu-id="29b2d-105">DESCRIPTION</span></span>
<span data-ttu-id="29b2d-106">**AzureRmFrontDoor** CmdletGet 會取得目前訂閱中符合所提供資訊的所有現有前門。</span><span class="sxs-lookup"><span data-stu-id="29b2d-106">The **Get-AzureRmFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="29b2d-107">示例</span><span class="sxs-lookup"><span data-stu-id="29b2d-107">EXAMPLES</span></span>

### <span data-ttu-id="29b2d-108">範例1：取得目前訂閱中的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="29b2d-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="29b2d-109">取得目前訂閱中的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="29b2d-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="29b2d-110">範例2：在目前的訂閱中取得資源群組 "rg1" 中的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="29b2d-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="29b2d-111">取得目前訂閱中資源群組 "rg1" 中的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="29b2d-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="29b2d-112">範例3：在目前訂閱中取得名為 "frontDoor1" 的資源群組 "rg1" 中的 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="29b2d-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="29b2d-113">在目前訂閱中取得名為 "frontDoor1" 的資源群組 "rg1" 中的 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="29b2d-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="29b2d-114">參數</span><span class="sxs-lookup"><span data-stu-id="29b2d-114">PARAMETERS</span></span>

### <span data-ttu-id="29b2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b2d-115">-DefaultProfile</span></span>
<span data-ttu-id="29b2d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29b2d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b2d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="29b2d-117">-Name</span></span>
<span data-ttu-id="29b2d-118">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="29b2d-118">Front Door name.</span></span>

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

### <span data-ttu-id="29b2d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29b2d-119">-ResourceGroupName</span></span>
<span data-ttu-id="29b2d-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="29b2d-120">The resource group name.</span></span>

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

### <span data-ttu-id="29b2d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b2d-121">CommonParameters</span></span>
<span data-ttu-id="29b2d-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29b2d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b2d-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29b2d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b2d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="29b2d-124">INPUTS</span></span>

### <span data-ttu-id="29b2d-125">System.object</span><span class="sxs-lookup"><span data-stu-id="29b2d-125">System.String</span></span>

## <span data-ttu-id="29b2d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="29b2d-126">OUTPUTS</span></span>

### <span data-ttu-id="29b2d-127">PSFrontDoor 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="29b2d-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="29b2d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="29b2d-128">NOTES</span></span>

## <span data-ttu-id="29b2d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="29b2d-129">RELATED LINKS</span></span>

<span data-ttu-id="29b2d-130">[新-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
[移除-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="29b2d-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span></span>
