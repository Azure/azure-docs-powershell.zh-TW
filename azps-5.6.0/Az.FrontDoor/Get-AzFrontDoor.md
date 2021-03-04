---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: f48fadb740fdca823c2513d68a2f77e0d34c4631
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902602"
---
# <span data-ttu-id="0d5e7-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0d5e7-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="0d5e7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0d5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5e7-103">取得前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="0d5e7-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="0d5e7-104">語法</span><span class="sxs-lookup"><span data-stu-id="0d5e7-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d5e7-105">描述</span><span class="sxs-lookup"><span data-stu-id="0d5e7-105">DESCRIPTION</span></span>
<span data-ttu-id="0d5e7-106">**Get-AzFrontDoor** CmdletGet 會取得目前訂閱中所有符合所提供的資訊的現有前門。</span><span class="sxs-lookup"><span data-stu-id="0d5e7-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="0d5e7-107">例子</span><span class="sxs-lookup"><span data-stu-id="0d5e7-107">EXAMPLES</span></span>

### <span data-ttu-id="0d5e7-108">範例 1：取得目前訂閱的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="0d5e7-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
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
FrontDoorId           : {guid}
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

<span data-ttu-id="0d5e7-109">取得目前訂閱中所有的 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="0d5e7-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="0d5e7-110">範例 2：取得目前訂閱中資源群組 "rg1" 的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="0d5e7-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
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
FrontDoorId           : {guid}
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

<span data-ttu-id="0d5e7-111">取得目前訂閱中資源群組 "rg1" 的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="0d5e7-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="0d5e7-112">範例 3：取得目前訂閱中名稱為 "frontDoor1" 的資源群組 "rg1" 中的 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="0d5e7-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
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

<span data-ttu-id="0d5e7-113">取得目前訂閱中名稱為 "frontDoor1" 的資源群組 "rg1" 中的 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="0d5e7-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="0d5e7-114">參數</span><span class="sxs-lookup"><span data-stu-id="0d5e7-114">PARAMETERS</span></span>

### <span data-ttu-id="0d5e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5e7-115">-DefaultProfile</span></span>
<span data-ttu-id="0d5e7-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d5e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d5e7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d5e7-117">-Name</span></span>
<span data-ttu-id="0d5e7-118">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="0d5e7-118">Front Door name.</span></span>

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

### <span data-ttu-id="0d5e7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d5e7-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d5e7-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0d5e7-120">The resource group name.</span></span>

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

### <span data-ttu-id="0d5e7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5e7-121">CommonParameters</span></span>
<span data-ttu-id="0d5e7-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0d5e7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5e7-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d5e7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5e7-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0d5e7-124">INPUTS</span></span>

### <span data-ttu-id="0d5e7-125">沒有</span><span class="sxs-lookup"><span data-stu-id="0d5e7-125">None</span></span>

## <span data-ttu-id="0d5e7-126">輸出</span><span class="sxs-lookup"><span data-stu-id="0d5e7-126">OUTPUTS</span></span>

### <span data-ttu-id="0d5e7-127">Microsoft.Azure.Commands.FrontDoor.models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0d5e7-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="0d5e7-128">筆記</span><span class="sxs-lookup"><span data-stu-id="0d5e7-128">NOTES</span></span>

## <span data-ttu-id="0d5e7-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d5e7-129">RELATED LINKS</span></span>

<span data-ttu-id="0d5e7-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md) 
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="0d5e7-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
